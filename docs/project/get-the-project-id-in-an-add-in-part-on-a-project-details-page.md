---
title: Obtenir l’ID du projet dans un composant de complément sur une page de détails du projet
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 009cd997-c7e5-4078-b495-c40caa29a5fb
description: Les composants de add-in sont hébergés dans des éléments iframe totalement isolés de la page d’hébergement. Pour obtenir des informations sur le projet actuel à partir d’un partie de la page de détails du projet (PDP), vous pouvez utiliser la méthode window.postMessage, un lanceur d’événements et un responsable du traitement des événements qui analyse l’ID de projet à partir du message.
ms.openlocfilehash: ffaf9cb7dac783a754b2d56b5ece4d5a7a0319be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322595"
---
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a>Obtenir l’ID du projet dans un composant de complément sur une page de détails du projet

Les composants de add-in sont hébergés dans des **éléments iframe** totalement isolés de la page d’hébergement. Pour obtenir des informations sur le projet actuel à partir d’un partie de la page de détails du projet (PDP), vous pouvez utiliser la méthode **window.postMessage,** un lanceur d’événements et un responsable du traitement des événements qui analyse l’ID de projet à partir du message. 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a>Conditions préalables à la création d’un partie de add-in hébergé par SharePoint qui obtient l’ID de projet
<a name="Prereqs"> </a>

Pour utiliser l’exemple de code de cet article, vous aurez besoin de l’une des procédures suivantes :
  
- SharePoint 2013 et Project Server 2013, configurés pour l’isolation des add-ins. Si vous développez à distance, le serveur doit prendre en charge le chargement indépendant des modules ou vous devez installer le module sur un Site du développeur.
  
- SharePoint Online et Project Online
    
    - Visual Studio 2013, Visual Studio 2012 avec outils de développement Office pour Visual Studio 2013 ou Napa
        
    - Autorisations suffisantes pour l'utilisateur connecté :
        
        - Autorisations d'administrateur local sur l'ordinateur de développement.
            
        - Accès en lecture à au moins un projet.
            
        - Autorisation de modifier des pages sur le site Project Web App.
            
        - Vous devez être connecté en tant que quelqu'un d'autre que le compte système. Le compte système n’est pas autorisé à installer un add-in.
    
Pour plus d’informations sur les modules complémentaires pour Project, voir Conditions préalables à la création d’un module complémentaire pour [Project Server 2013.](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) Voir Configurer un environnement de développement local pour les [add-ins SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) pour obtenir des instructions sur l’installation locale (y compris la désactivation de la vérification en boucle, si nécessaire). Si vous développez à distance, voir [Développement d’applications pour SharePoint sur un système distant.](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins)
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a>Créer le module de développement hébergé par SharePoint et le partie web client
<a name="CreateApp"> </a>

1. Ouvrez Visual Studio et choisissez **Fichier**  >  **nouveau**  >  **projet.**
    
2. Dans la boîte de dialogue **Nouveau projet**, sélectionnez **.NET Framework 4.5** dans la liste déroulante située en haut de la boîte de dialogue. 
    
3. Dans la **liste Modèles,** sélectionnez **Visual C#**  >  **Office/SharePoint**  >  **Add-ins Add-ins**  >  **for SharePoint 2013**.
    
4. Nommez le add-in GetProjectIdAddinPart, puis choisissez le **bouton OK.** 
    
5. Dans la boîte de dialogue Nouveau **add-in pour SharePoint,** entrez l’URL du site PWA que vous souhaitez utiliser pour le débogage (par exemple :  _https://contoso.com/sites/pwasite/_ ).
    
6. Choisissez **l’option hébergée par SharePoint** pour héberger votre add-in, puis choisissez le **bouton** Terminer. 
    
7. Dans **l’Explorateur** de solutions, ouvrez le menu raccourci du projet GetProjectIdAddinPart, puis choisissez **Ajouter** un  >  **nouvel élément.**
    
8. Dans la **boîte de dialogue** Ajouter un nouvel élément, choisissez le client web part **(site web hôte)**, nommez le partie Web Part GetProjectId, puis choisissez **le bouton** Ajouter. 
    
9. Dans la **boîte de dialogue Créer** un client, choisissez l’option Créer une page de partie **Web** Client, puis choisissez le **bouton** Terminer. 
    
## <a name="get-the-project-id-in-the-add-in-part"></a>Obtenir l’ID de projet dans le partie de add-in
<a name="GetProjectId"> </a>

Le partie de l’application GetProjectId définit son code personnalisé dans la page GetProjectId.aspx du client. La logique qui reçoit et gère le message est définie dans l’élément **head** de la page et les contrôles de page sont définis dans l’élément **body** de la page. 
  
1. Ouvrez la page de partie Web GetProjectId.aspx (dans le **dossier Pages).** 
    
2. Dans **l’élément en-tête** de la page, remplacez le code entre les **balises de script** par le code suivant. 
    
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

3. Ajoutez le code suivant dans **l’élément body** de la page. Le code définit un contrôle span qui affiche l’ID de projet. 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. Dans le Elements.xml, modifiez éventuellement le nom, le titre, la description et la taille par défaut du fichier de recherche. Cet exemple utilise les valeurs par défaut.
    
5. Pour tester le partie de la add-in, dans la barre de menus, choisissez **Déboguer,** **Démarrer le débogage**. Si vous êtes invité à modifier le fichier web.config, cliquez sur le bouton **OK**. 
    
   Pour déboguer le partie de la mise à jour, définissez les points d’arrêt appropriés dans le script que vous avez ajouté.
    
6. Accédez à une page PDP et choisissez **Modifier dans** le menu Outils (icône d’engrenage). 
    
7. Ajoutez **le partie titre GetProjectId** à un élément Web Part sur la page. L’ID de projet s’affiche dans le contrôle **d’étendue** sur la page de partie Web. 
    
## <a name="next-steps"></a>Étapes suivantes
<a name="NextSteps"> </a>

Dans cet exemple, le module de développement n’accède pas aux données Project Server ni aux données SharePoint. Vous pouvez utiliser l’ID produit pour obtenir des informations sur le projet actuel à l’aide d’une API cliente, telle que le modèle objet JavaScript ou le service REST.
  
Dans le AppManifest.xml, spécifiez les autorisations dont votre add-in a besoin pour accéder aux données Project Server ou aux données SharePoint. 
  
Pour découvrir comment définir des propriétés personnalisées pour un composant de add-in, voir Créer des composants de add-in à installer avec votre Add-in [SharePoint.](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a>Exemple : obtention de l’ID de projet dans un partie de add-in sur une page PDP
<a name="CodeExample"> </a>

L’exemple suivant est le code complet de la page GetProjectID.aspx du client. Le code inscrit un listener d’événements et un handler d’événements qui reçoit et parse un message qui contient l’ID de projet.
  
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
    

