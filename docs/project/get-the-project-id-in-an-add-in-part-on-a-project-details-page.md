---
title: Obtenir l’ID du projet dans un composant de complément sur une page de détails du projet
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 009cd997-c7e5-4078-b495-c40caa29a5fb
description: Les composants de complément sont hébergés dans des éléments iframe entièrement isolés de la page d’hébergement. Pour obtenir des informations sur le projet actuel à partir d’un composant de complément sur Project Page de détails (PDP), vous pouvez utiliser la méthode window.postMessage, un écouteur d’événements et un gestionnaire d’événements qui analyse l’ID de projet à partir du message.
ms.openlocfilehash: 723cf5f7797aa61e37f1172fb9e309969a3855c7
ms.sourcegitcommit: a6d13fdae7eb2e503236c1b629a59b36a4fb76f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2022
ms.locfileid: "66083898"
---
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a>Obtenir l’ID du projet dans un composant de complément sur une page de détails du projet

Les composants de complément sont hébergés dans des éléments **iframe** entièrement isolés de la page d’hébergement. Pour obtenir des informations sur le projet actuel à partir d’un composant de complément sur Project Page de détails (PDP), vous pouvez utiliser la méthode **window.postMessage**, un écouteur d’événements et un gestionnaire d’événements qui analyse l’ID de projet à partir du message. 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a>Conditions préalables à la création d’un composant de complément hébergé par SharePoint qui obtient l’ID de projet
<a name="Prereqs"> </a>

Pour utiliser l’exemple de code de cet article, vous avez besoin de l’une des options suivantes :
  
- SharePoint 2013 et Project Server 2013, configurés pour l’isolation des compléments. Si vous développez à distance, le serveur doit gérer le chargement indépendant des compléments ou vous devez installer le complément sur un site de développeur.
  
- SharePoint Online et Project Online
    
    - Visual Studio 2013, Visual Studio 2012 avec Office Developer Tools for Visual Studio 2013 ou Napa
        
    - Autorisations suffisantes pour l'utilisateur connecté :
        
        - Autorisations d'administrateur local sur l'ordinateur de développement.
            
        - Accès en lecture à au moins un projet.
            
        - Autorisation de modifier des pages sur le site Project Web App.
            
        - Vous devez être connecté en tant que quelqu'un d'autre que le compte système. Le compte système n’est pas autorisé à installer un complément.
    
Pour plus [d’informations sur les compléments pour Project, consultez les conditions préalables à la création d’un complément pour Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites). Consultez [Configurer un environnement de développement local pour SharePoint compléments](/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) pour obtenir des conseils sur la configuration locale (notamment la désactivation de la vérification de bouclage, si nécessaire). Si vous développez à distance, consultez [Développer des applications pour SharePoint sur un système distant](/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins).
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a>Créer le complément hébergé par SharePoint et le composant WebPart client
<a name="CreateApp"> </a>

1. Ouvrez Visual Studio et choisissez **Fichier** > **nouveau** >  **Project**.
    
2. Dans la boîte de dialogue **Nouveau projet**, sélectionnez **.NET Framework 4.5** dans la liste déroulante située en haut. 
    
3. Dans la liste **Modèles**, choisissez **Le complément Visual C#** > **Office/SharePoint** >  **Add-ins** > **pour SharePoint 2013**.
    
4. Nommez le complément GetProjectIdAddinPart, puis choisissez le bouton **OK** . 
    
5. Dans la boîte **de dialogue Nouveau complément pour SharePoint**, entrez l’URL du site PWA que vous souhaitez utiliser pour le débogage (par exemple : _https://contoso.com/sites/pwasite/_).
    
6. Choisissez l’option **hébergée par SharePoint** pour héberger votre complément, puis choisissez le bouton **Terminer**. 
    
7. Dans **Explorateur de solutions**, ouvrez le menu contextuel du projet GetProjectIdAddinPart, puis choisissez **Ajouter** > **un nouvel élément**.
    
8. Dans la boîte **de dialogue Ajouter un nouvel élément** , choisissez le **composant WebPart client (Site web hôte),** nommez le composant WebPart GetProjectId, puis **choisissez** le bouton Ajouter. 
    
9. Dans la boîte de dialogue **Créer un composant WebPart client** , choisissez l’option **Créer un composant WebPart client** , puis cliquez sur le bouton **Terminer** . 
    
## <a name="get-the-project-id-in-the-add-in-part"></a>Obtenir l’ID de projet dans le composant de complément
<a name="GetProjectId"> </a>

Le composant de complément GetProjectId définit son code personnalisé dans la page GetProjectId.aspx du composant WebPart client. La logique qui reçoit et gère le message est définie dans l’élément **principal** de la page et les contrôles de page sont définis dans l’élément **corps** de la page. 
  
1. Ouvrez la page du composant WebPart GetProjectId.aspx (dans le dossier **Pages** ). 
    
2. Dans l’élément **principal** de la page, remplacez le code entre les balises de **script** par le code suivant. 
    
   ```js
        'use strict';
        // Define global variables.
        var hostUrl = '';
        var projectUid;
        // Set the style of the client web part page to be consistent with the host web.
                (function () {
                    var hostUrl = '';
                    var link = document.createElement('link');
                    link.setAttribute('rel', 'stylesheet');
                    if (document.URL.indexOf('?') != -1) {
                        var params = document.URL.split('?')[1].split('&');
                        for (var i = 0; i < params.length; i++) {
                            var p = decodeURIComponent(params[i]);
                            if (/^SPHostUrl=/i.test(p)) {
                                hostUrl = p.split('=')[1];
                                link.setAttribute('href', hostUrl + '/_layouts/15/defaultcss.ashx');
                                break;
                            }
                        }
                    }
                    if (hostUrl == '') {
                        link.setAttribute('href', '/_layouts/15/1033/styles/themable/corev15.css');
                    }
                    document.head.appendChild(link);
                })();
        // Get the message.
        function getProjectUid() {
            window.parent.postMessage('getprojectuid', hostUrl);
        }
        getProjectUid();
        // Add an event listener and register the event handler.
        // If the IE browser version is earlier than 9, use the attachEvent method.
        if (window.addEventListener) {
            window.addEventListener("message", onMessage, false);
        }
        else {
            if (window.attachEvent) {
                window.attachEvent("onmessage", onMessage);
            }
        }
        // Get the project ID from the message.
        function onMessage(event) {
            // Verify the message origin.
            if (hostUrl.indexOf(event.origin) != 0) return;
            // The expected message format is "<PDPProjectUid>00000000-0000-0000-0000-000000000000</PDPProjectUid>,"
            // so validate by using the length and the start and end tags.
            var length = event.data.length;
            if (length = 67) {
                var expectedStart = "<PDPProjectUid>";
                var expectedEnd = "</PDPProjectUid>";
                var endTagPosition = length - expectedEnd.length;
                var start = event.data.substr(0, expectedStart.length);
                var end = event.data.substr(endTagPosition, expectedEnd.length);
                // Parse out the project ID.
                if (start == expectedStart && end == expectedEnd) {
                    projectUid = event.data.substr(expectedStart.length, 36);
                    $get('projectUid').innerText = projectUid;
                }
            }
        }
   ```

3. Ajoutez le code suivant dans l’élément **de corps** de la page. Le code définit un contrôle d’étendue qui affiche l’ID de projet. 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. Dans le fichier Elements.xml, modifiez éventuellement le nom, le titre, la description et la taille par défaut du composant de complément. Cet exemple utilise les valeurs par défaut.
    
5. Pour tester le composant de complément, dans la barre de menus, choisissez **Déboguer**, Démarrer le **débogage**. Si vous êtes invité à modifier le fichier web.config, cliquez sur le bouton **OK**. 
    
   Pour déboguer le composant de complément, définissez les points d’arrêt appropriés dans le script que vous avez ajouté.
    
6. Accédez à une page PDP et choisissez **Modifier la page** dans le menu Outils (icône d’engrenage). 
    
7. Ajoutez le composant **GetProjectId Title** à un composant WebPart sur la page. L’ID de projet s’affiche dans le contrôle **d’étendue** sur la page du composant WebPart. 
    
## <a name="next-steps"></a>Étapes suivantes
<a name="NextSteps"> </a>

La partie de complément de cet exemple n’accède pas aux données Project Server ni aux données SharePoint. Vous pouvez utiliser l’ID de produit pour obtenir des informations sur le projet actuel à l’aide d’une API cliente, comme le modèle objet JavaScript ou le service REST.
  
Dans le fichier AppManifest.xml, spécifiez les autorisations dont votre complément a besoin pour accéder aux données Project Serveur ou SharePoint données. 
  
Consultez [Créer des composants de complément à installer avec votre complément SharePoint](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) pour savoir comment définir des propriétés personnalisées pour un composant de complément. 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a>Exemple : Obtention de l’ID de projet dans un composant de complément sur une page PDP
<a name="CodeExample"> </a>

L’exemple suivant est le code complet dans la page GetProjectID.aspx du composant WebPart client. Le code inscrit un écouteur d’événements et un gestionnaire d’événements qui reçoit et analyse un message qui contient l’ID de projet.
  
```HTML
<%@ Page language="C#" Inherits="Microsoft.SharePoint.WebPartPages.WebPartPage, Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="SharePoint" Namespace="Microsoft.SharePoint.WebControls" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="Utilities" Namespace="Microsoft.SharePoint.Utilities" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="WebPartPages" Namespace="Microsoft.SharePoint.WebPartPages" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<WebPartPages:AllowFraming ID="AllowFraming" runat="server" />
<html>
<head>
    <title></title>
    <script type="text/javascript" src="../Scripts/jquery-1.7.1.min.js"></script>
    <script type="text/javascript" src="/_layouts/15/MicrosoftAjax.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.runtime.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.js"></script>
    <script type="text/javascript">
        'use strict';
        // Define global variables.
        var hostUrl = '';
        var projectUid;
        // Set the style of the client web part page to be consistent with the host web.
        (function () {
            var hostUrl = '';
            var link = document.createElement('link');
            link.setAttribute('rel', 'stylesheet');
            if (document.URL.indexOf('?') != -1) {
                var params = document.URL.split('?')[1].split('&');
                for (var i = 0; i < params.length; i++) {
                    var p = decodeURIComponent(params[i]);
                    if (/^SPHostUrl=/i.test(p)) {
                        hostUrl = p.split('=')[1];
                        link.setAttribute('href', hostUrl + '/_layouts/15/defaultcss.ashx');
                        break;
                    }
                }
            }
            if (hostUrl == '') {
                link.setAttribute('href', '/_layouts/15/1033/styles/themable/corev15.css');
            }
            document.head.appendChild(link);
        })();
        // Get the message.
        function getProjectUid() {
            window.parent.postMessage('getprojectuid', hostUrl);
        }
        getProjectUid();
        // Add an event listener and register the event handler.
        // If the IE browser version is earlier than 9, use the attachEvent method.
        if (window.addEventListener) {
            window.addEventListener("message", onMessage, false);
        }
        else {
            if (window.attachEvent) {
                window.attachEvent("onmessage", onMessage);
            }
        }
        // Get the project ID from the message.
        function onMessage(event) {
            // Verify the message origin.
            if (hostUrl.indexOf(event.origin) != 0) return;
            // The expected message format is "<PDPProjectUid>00000000-0000-0000-0000-000000000000</PDPProjectUid>,"
            // so validate by using the length and the start and end tags.
            var length = event.data.length;
            if (length = 67) {
                var expectedStart = "<PDPProjectUid>";
                var expectedEnd = "</PDPProjectUid>";
                var endTagPosition = length - expectedEnd.length;
                var start = event.data.substr(0, expectedStart.length);
                var end = event.data.substr(endTagPosition, expectedEnd.length);
                // Parse out the project ID.
                if (start == expectedStart && end == expectedEnd) {
                    projectUid = event.data.substr(expectedStart.length, 36);
                    $get('projectUid').innerText = projectUid;
                }
            }
        }
    </script>
</head>
<body>
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
</body>
</html>

```

## <a name="see-also"></a>Voir aussi

- [Tâches de programmation Project](project-programming-tasks.md)
- [Créer un complément Project Server hébergé sur SharePoint](create-a-sharepoint-hosted-project-server-add-in.md)
- [Créer des composants de complément à installer avec votre complément SharePoint](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)
    
