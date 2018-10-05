---
title: Obtenir l’ID du projet dans un composant de complément sur une page de détails du projet
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 009cd997-c7e5-4078-b495-c40caa29a5fb
description: Dans Ajouter des composants sont hébergés dans les éléments iframe qui sont entièrement isolés à partir de la page d’hébergement. Pour obtenir plus d’informations sur le projet actuel dans un complément composant sur Page de détails de projet (PDP), vous pouvez utiliser la méthode window.postMessage, un récepteur d’événements et un gestionnaire d’événements qui analyse l’ID du projet à partir du message.
ms.openlocfilehash: ffaf9cb7dac783a754b2d56b5ece4d5a7a0319be
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389882"
---
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a>Obtenir l’ID du projet dans un composant de complément sur une page de détails du projet

Dans Ajouter des composants sont hébergés dans les éléments **iframe** qui sont entièrement isolés à partir de la page d’hébergement. Pour obtenir plus d’informations sur le projet actuel dans un complément composant sur Page de détails de projet (PDP), vous pouvez utiliser la méthode **window.postMessage** , un récepteur d’événements et un gestionnaire d’événements qui analyse l’ID du projet à partir du message. 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a>Conditions requises pour la création d’un hébergée par SharePoint complément composant qui obtient l’ID du projet
<a name="Prereqs"> </a>

Pour utiliser l’exemple de code dans cet article, vous avez besoin d’une des options suivantes :
  
- SharePoint 2013 et Project Server 2013, configuré pour l’isolement du complément. Si vous développez à distance, le serveur doit prendre en charge le chargement de version test des compléments ou vous devez installer le complément sur un Site du développeur.
  
- SharePoint Online et Project Online
    
    - Visual Studio 2013, outils de Visual Studio 2012 avec des développeurs Office pour Visual Studio 2013, ou Napa
        
    - Autorisations suffisantes pour l'utilisateur connecté :
        
        - Autorisations d'administrateur local sur l'ordinateur de développement.
            
        - Accès en lecture au moins un projet.
            
        - Autorisation de modifier des pages sur le site Project Web App.
            
        - Vous devez être connecté en tant qu’utilisateur autre que le compte système. Le compte système ne dispose pas d’autorisation pour installer un complément.
    
Pour plus d’informations sur les compléments pour Project, consultez [conditions requises pour créer un complément pour Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) . Pour obtenir des conseils sur le programme d’installation locale (y compris comment désactiver la vérification en boucle, si nécessaire), consultez [configurer un environnement de développement local pour les compléments SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) . Si vous développez à distance, voir [Developing apps for SharePoint sur un système distant](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins).
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a>Créer le hébergée par SharePoint complément et client de composant WebPart
<a name="CreateApp"> </a>

1. Ouvrez Visual Studio et choisissez **fichier** > **New** > **Project**.
    
2. Dans la boîte de dialogue **Nouveau projet**, sélectionnez **.NET Framework 4.5** dans la liste déroulante située en haut de la boîte de dialogue. 
    
3. Dans la liste des **modèles** , sélectionnez **Visual c#** > **Office/SharePoint** > **Add-ins** > **complément pour SharePoint 2013**.
    
4. Nom de la macro complémentaire GetProjectIdAddinPart, puis cliquez sur le bouton **OK** . 
    
5. Dans la boîte de dialogue **nouveau complément pour SharePoint** , entrez l’URL du site PWA que vous souhaitez utiliser pour le débogage (par exemple : _https://contoso.com/sites/pwasite/_).
    
6. Choisissez l’option **hébergée par SharePoint** pour héberger votre complément, puis cliquez sur le bouton **Terminer** . 
    
7. Dans **L’Explorateur de solutions**, ouvrez le menu contextuel du projet GetProjectIdAddinPart, puis choisissez **Ajouter** > **Un nouvel élément**.
    
8. Dans la boîte de dialogue **Ajouter un nouvel élément** , choisissez **le composant WebPart Client (site Web hôte)**, nom du composant WebPart GetProjectId, puis cliquez sur le bouton **Ajouter** . 
    
9. Dans la boîte de dialogue **composant WebPart Client créer** , choisissez l’option **créer une nouvelle page de composant WebPart client** , puis cliquez sur le bouton **Terminer** . 
    
## <a name="get-the-project-id-in-the-add-in-part"></a>Obtenez l’ID de projet dans le composant du complément
<a name="GetProjectId"> </a>

Le composant du complément GetProjectId définit son code personnalisé dans la page GetProjectId.aspx du composant WebPart client. La logique qui reçoit et gère le message est définie dans l’élément **head** de la page et les contrôles de page sont définis dans l’élément **body** de la page. 
  
1. Ouvrez la page de composants WebPart GetProjectId.aspx (dans le dossier **Pages** ). 
    
2. Dans l’élément **head** de la page, remplacez le code entre les balises **script** par le code suivant. 
    
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

3. Ajoutez le code suivant dans l’élément **body** de la page. Le code définit un contrôle d’étendue qui affiche l’ID du projet. 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. Dans le fichier Elements.xml, éventuellement modifier le nom, titre, description et taille par défaut de la partie du complément. Cet exemple utilise les valeurs par défaut.
    
5. Pour tester le composant de compléments, dans la barre de menus, choisissez **débogage**, **Démarrer le débogage**. Si vous êtes invité à modifier le fichier web.config, cliquez sur le bouton **OK** . 
    
   Pour déboguer le composant du complément, définir des points d’arrêt appropriés dans le script que vous avez ajouté.
    
6. Accédez à une page PDP et choisissez **Modifier la page** dans le menu Outils (icône représentant un engrenage). 
    
7. Ajoutez le composant **GetProjectId titre** à un composant WebPart dans la page. L’ID du projet s’affiche dans le contrôle **span** sur la page de composants WebPart. 
    
## <a name="next-steps"></a>Étapes suivantes
<a name="NextSteps"> </a>

Le composant de compléments dans cet exemple n’accéder aux données Project Server ou SharePoint. Vous pouvez utiliser l’ID de produit pour obtenir des informations sur le projet en cours à l’aide d’un client API, telles que le modèle objet JavaScript ou le service REST.
  
Dans le fichier AppManifest.xml, spécifiez les autorisations que votre complément doit accéder aux données Project Server ou SharePoint. 
  
Voir [Création de compléments composants à installer avec votre complément SharePoint](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) pour découvrir comment définir les propriétés personnalisées pour une partie du complément. 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a>Exemple : Obtention de l’ID de projet dans un composant complément sur une page PDP
<a name="CodeExample"> </a>

L’exemple suivant est le code complet de la page de GetProjectID.aspx du composant WebPart client. Le code inscrit un écouteur d’événement et un gestionnaire d’événements qui reçoit et analyse un message qui contient l’ID du projet.
  
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
    

