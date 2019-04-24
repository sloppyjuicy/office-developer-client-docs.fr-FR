---
title: Obtenir l’ID du projet dans un composant de complément sur une page de détails du projet
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 009cd997-c7e5-4078-b495-c40caa29a5fb
description: Les composants de complément sont hébergés dans des éléments iframe entièrement isolés de la page d'hébergement. Pour obtenir des informations sur le projet actif à partir d'un composant de complément sur la page de détails du projet (PDP), vous pouvez utiliser la méthode Window. postMessage, un écouteur d'événements et un gestionnaire d'événements qui analyse l'ID de projet à partir du message.
ms.openlocfilehash: ffaf9cb7dac783a754b2d56b5ece4d5a7a0319be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322595"
---
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a><span data-ttu-id="b0422-104">Obtenir l’ID du projet dans un composant de complément sur une page de détails du projet</span><span class="sxs-lookup"><span data-stu-id="b0422-104">Get the project ID in an add-in part on a Project Details Page</span></span>

<span data-ttu-id="b0422-105">Les composants de complément sont hébergés dans des éléments **IFRAME** entièrement isolés de la page d'hébergement.</span><span class="sxs-lookup"><span data-stu-id="b0422-105">Add-in parts are hosted in **iframe** elements that are fully isolated from the hosting page.</span></span> <span data-ttu-id="b0422-106">Pour obtenir des informations sur le projet actif à partir d'un composant de complément sur la page de détails du projet (PDP), vous pouvez utiliser la méthode **Window. PostMessage** , un écouteur d'événements et un gestionnaire d'événements qui analyse l'ID de projet à partir du message.</span><span class="sxs-lookup"><span data-stu-id="b0422-106">To get information about the current project from an add-in part on Project Details Page (PDP), you can use the **window.postMessage** method, an event listener, and an event handler that parses out the project ID from the message.</span></span> 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a><span data-ttu-id="b0422-107">Conditions préalables à la création d'un composant de complément hébergé par SharePoint qui obtient l'ID de projet</span><span class="sxs-lookup"><span data-stu-id="b0422-107">Prerequisites for creating a SharePoint-hosted add-in part that gets the project ID</span></span>
<span data-ttu-id="b0422-108"><a name="Prereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="b0422-108"></span></span>

<span data-ttu-id="b0422-109">Pour utiliser l'exemple de code de cet article, vous devez disposer de l'un des éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="b0422-109">To use the code example in this article, you'll need either of the following:</span></span>
  
- <span data-ttu-id="b0422-110">SharePoint 2013 et Project Server 2013, configurés pour l'isolation des compléments.</span><span class="sxs-lookup"><span data-stu-id="b0422-110">SharePoint 2013 and Project Server 2013, configured for add-in isolation.</span></span> <span data-ttu-id="b0422-111">Si vous effectuez un développement à distance, le serveur doit prendre en charge chargement de compléments ou installer le complément sur un site du développeur.</span><span class="sxs-lookup"><span data-stu-id="b0422-111">If you're developing remotely, the server must support sideloading of add-ins or you must install the add-in on a Developer Site.</span></span>
  
- <span data-ttu-id="b0422-112">SharePoint Online et Project Online</span><span class="sxs-lookup"><span data-stu-id="b0422-112">SharePoint Online and Project Online</span></span>
    
    - <span data-ttu-id="b0422-113">Visual Studio 2013, Visual Studio 2012 avec les outils de développement Office pour Visual Studio 2013 ou Napa</span><span class="sxs-lookup"><span data-stu-id="b0422-113">Visual Studio 2013, Visual Studio 2012 with Office Developer Tools for Visual Studio 2013, or Napa</span></span>
        
    - <span data-ttu-id="b0422-114">Autorisations suffisantes pour l'utilisateur connecté :</span><span class="sxs-lookup"><span data-stu-id="b0422-114">Sufficient permissions for the logged-on user:</span></span>
        
        - <span data-ttu-id="b0422-115">Autorisations d'administrateur local sur l'ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="b0422-115">Local administrator permissions on the development computer.</span></span>
            
        - <span data-ttu-id="b0422-116">Accès en lecture à au moins un projet.</span><span class="sxs-lookup"><span data-stu-id="b0422-116">Read access to at least one project.</span></span>
            
        - <span data-ttu-id="b0422-117">Autorisation de modifier des pages sur le site Project Web App.</span><span class="sxs-lookup"><span data-stu-id="b0422-117">Permission to edit pages on the Project Web App site.</span></span>
            
        - <span data-ttu-id="b0422-118">Vous devez être connecté en tant que quelqu'un d'autre que le compte système.</span><span class="sxs-lookup"><span data-stu-id="b0422-118">You must be logged on as someone other than the system account.</span></span> <span data-ttu-id="b0422-119">Le compte système n'est pas autorisé à installer un complément.</span><span class="sxs-lookup"><span data-stu-id="b0422-119">The system account does not have permission to install an add-in.</span></span>
    
<span data-ttu-id="b0422-120">Pour plus d'informations sur les compléments pour Project, rePortez-vous à la rubrique [conditions préalables à la création d'un complément pour Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) .</span><span class="sxs-lookup"><span data-stu-id="b0422-120">See [Prerequisites for creating an add-in for Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) for more information about add-ins for Project.</span></span> <span data-ttu-id="b0422-121">Voir [configurer un environnement de développement local pour les compléments pour SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) pour obtenir des instructions sur l'installation locale (notamment comment désactiver la vérification en boucle, si nécessaire).</span><span class="sxs-lookup"><span data-stu-id="b0422-121">See [Set up an on-premises development environment for SharePoint Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) for guidance about on-premises setup (including how to disable the loopback check, if necessary).</span></span> <span data-ttu-id="b0422-122">Si vous développez à distance, voir [développement d'applications pour SharePoint sur un système distant](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins).</span><span class="sxs-lookup"><span data-stu-id="b0422-122">If you're developing remotely, see [Developing apps for SharePoint on a remote system](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins).</span></span>
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a><span data-ttu-id="b0422-123">Créer le complément hébergé par SharePoint et le composant WebPart client</span><span class="sxs-lookup"><span data-stu-id="b0422-123">Create the SharePoint-hosted add-in and client web part</span></span>
<span data-ttu-id="b0422-124"><a name="CreateApp"> </a></span><span class="sxs-lookup"><span data-stu-id="b0422-124"></span></span>

1. <span data-ttu-id="b0422-125">Ouvrez Visual Studio et choisissez **fichier** > **nouveau** > **projet**.</span><span class="sxs-lookup"><span data-stu-id="b0422-125">Open Visual Studio and choose **File** > **New** > **Project**.</span></span>
    
2. <span data-ttu-id="b0422-126">Dans la boîte de dialogue **Nouveau projet**, sélectionnez **.NET Framework 4.5** dans la liste déroulante située en haut de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b0422-126">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
    
3. <span data-ttu-id="b0422-127">dans la liste des **modèles** , choisissez complément **Visual C#** > **Office/sharepoint** > **add-ins** > **pour SharePoint 2013**.</span><span class="sxs-lookup"><span data-stu-id="b0422-127">In the **Templates** list, choose **Visual C#** > **Office/SharePoint** > **Add-ins** > **Add-in for SharePoint 2013**.</span></span>
    
4. <span data-ttu-id="b0422-128">Nommez le complément GetProjectIdAddinPart, puis cliquez sur le bouton **OK** .</span><span class="sxs-lookup"><span data-stu-id="b0422-128">Name the add-in GetProjectIdAddinPart, and then choose the **OK** button.</span></span> 
    
5. <span data-ttu-id="b0422-129">Dans la boîte de dialogue **nouveau complément pour SharePoint** , entrez l'URL du site PWA que vous souhaitez utiliser pour le débogage (par exemple: _https://contoso.com/sites/pwasite/_).</span><span class="sxs-lookup"><span data-stu-id="b0422-129">In the **New add-in for SharePoint** dialog box, enter the URL of the PWA site that you want to use for debugging (for example:  _https://contoso.com/sites/pwasite/_).</span></span>
    
6. <span data-ttu-id="b0422-130">Choisissez l'option hébergée par **SharePoint** pour héberger votre complément, puis cliquez sur le bouton **Terminer** .</span><span class="sxs-lookup"><span data-stu-id="b0422-130">Choose the **SharePoint-hosted** option to host your add-in, and then choose the **Finish** button.</span></span> 
    
7. <span data-ttu-id="b0422-131">Dans **l'Explorateur de solutions**, ouvrez le menu contextuel du projet GetProjectIdAddinPart, puis choisissez **Ajouter** > **un nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="b0422-131">In **Solution Explorer**, open the shortcut menu for the GetProjectIdAddinPart project, and then choose **Add** > **New Item**.</span></span>
    
8. <span data-ttu-id="b0422-132">Dans la boîte de dialogue **Ajouter un nouvel élément** , sélectionnez **composant WebPart client (site Web hôte)**, nommez le composant WebPart GetProjectId, puis cliquez sur le bouton **Ajouter** .</span><span class="sxs-lookup"><span data-stu-id="b0422-132">In the **Add New Item** dialog box, choose **Client web part (Host Web)**, name the web part GetProjectId, and then choose the **Add** button.</span></span> 
    
9. <span data-ttu-id="b0422-133">Dans la boîte de dialogue **créer un composant WebPart client** , sélectionnez l'option **créer une nouvelle page de composants WebPart client** , puis cliquez sur le bouton **Terminer** .</span><span class="sxs-lookup"><span data-stu-id="b0422-133">In the **Create Client web part** dialog box, choose the **Create a new client web part page** option, and then choose the **Finish** button.</span></span> 
    
## <a name="get-the-project-id-in-the-add-in-part"></a><span data-ttu-id="b0422-134">Obtenir l'ID de projet dans le composant de complément</span><span class="sxs-lookup"><span data-stu-id="b0422-134">Get the project ID in the add-in part</span></span>
<span data-ttu-id="b0422-135"><a name="GetProjectId"> </a></span><span class="sxs-lookup"><span data-stu-id="b0422-135"></span></span>

<span data-ttu-id="b0422-136">Le composant de complément GetProjectId définit son code personnalisé dans la page GetProjectId. aspx du composant WebPart client.</span><span class="sxs-lookup"><span data-stu-id="b0422-136">The GetProjectId add-in part defines its custom code in the GetProjectId.aspx page of the client web part.</span></span> <span data-ttu-id="b0422-137">La logique qui reçoit et gère le message est définie dans l'élément **Head** de la page et les contrôles de page sont définis dans l'élément **Body** de la page.</span><span class="sxs-lookup"><span data-stu-id="b0422-137">The logic that receives and handles the message is defined in the **head** element of the page and the page controls are defined in the **body** element of the page.</span></span> 
  
1. <span data-ttu-id="b0422-138">Ouvrez la page de composant WebPart GetProjectId. aspx (dans le dossier **pages** ).</span><span class="sxs-lookup"><span data-stu-id="b0422-138">Open the GetProjectId.aspx web part page (in the **Pages** folder).</span></span> 
    
2. <span data-ttu-id="b0422-139">Dans l'élément **Head** de la page, remplacez le code entre les balises **script** par le code suivant.</span><span class="sxs-lookup"><span data-stu-id="b0422-139">In the **head** element of the page, replace the code between the **script** tags with the following code.</span></span> 
    
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

3. <span data-ttu-id="b0422-140">Ajoutez le code suivant dans l'élément **Body** de la page.</span><span class="sxs-lookup"><span data-stu-id="b0422-140">Add the following code in the **body** element of the page.</span></span> <span data-ttu-id="b0422-141">Le code définit un contrôle span qui affiche l'ID de projet.</span><span class="sxs-lookup"><span data-stu-id="b0422-141">The code defines a span control that displays the project ID.</span></span> 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. <span data-ttu-id="b0422-142">Dans le fichier Elements. xml, modifiez éventuellement le nom, le titre, la description et la taille par défaut du composant de complément.</span><span class="sxs-lookup"><span data-stu-id="b0422-142">In the Elements.xml file, optionally change the name, title, description, and default size of the add-in part.</span></span> <span data-ttu-id="b0422-143">Cet exemple utilise les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="b0422-143">This example uses the default values.</span></span>
    
5. <span data-ttu-id="b0422-144">Pour tester le composant de complément, dans la barre de menus, choisissez \*\*\*\* déboguer, **Démarrer**le débogage.</span><span class="sxs-lookup"><span data-stu-id="b0422-144">To test the add-in part, on the menu bar, choose **Debug**, **Start Debugging**.</span></span> <span data-ttu-id="b0422-145">Si vous êtes invité à modifier le fichier web.config, cliquez sur le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="b0422-145">If you're prompted to modify the web.config file, choose the **OK** button.</span></span> 
    
   <span data-ttu-id="b0422-146">Pour déboguer le composant de complément, définissez les points d'arrêt appropriés dans le script que vous avez ajouté.</span><span class="sxs-lookup"><span data-stu-id="b0422-146">To debug the add-in part, set appropriate breakpoints in the script that you added.</span></span>
    
6. <span data-ttu-id="b0422-147">Accédez à une page PDP et choisissez **modifier la page** dans le menu Outils (icône d'engrenage).</span><span class="sxs-lookup"><span data-stu-id="b0422-147">Browse to a PDP page and choose **Edit page** from the Tools menu (gear icon).</span></span> 
    
7. <span data-ttu-id="b0422-148">Ajoutez le composant de **titre GetProjectId** à un composant WebPart sur la page.</span><span class="sxs-lookup"><span data-stu-id="b0422-148">Add the **GetProjectId Title** part to a web part on the page.</span></span> <span data-ttu-id="b0422-149">L'ID de projet s'affiche dans le contrôle **span** sur la page de composants WebPart.</span><span class="sxs-lookup"><span data-stu-id="b0422-149">The project ID displays in the **span** control on the web part page.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="b0422-150">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="b0422-150">Next steps</span></span>
<span data-ttu-id="b0422-151"><a name="NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="b0422-151"></span></span>

<span data-ttu-id="b0422-152">Le composant de complément de cet exemple n'accède pas aux données Project Server ou aux données SharePoint.</span><span class="sxs-lookup"><span data-stu-id="b0422-152">The add-in part in this example doesn't access Project Server data or SharePoint data.</span></span> <span data-ttu-id="b0422-153">Vous pouvez utiliser l'ID de produit pour obtenir des informations sur le projet en cours à l'aide d'une API cliente, telle que le modèle objet JavaScript ou le service REST.</span><span class="sxs-lookup"><span data-stu-id="b0422-153">You can use the product ID to get information about the current project by using a client API, such as the JavaScript object model or the REST service.</span></span>
  
<span data-ttu-id="b0422-154">Dans le fichier AppManifest. xml, spécifiez les autorisations dont votre complément a besoin pour accéder aux données Project Server ou aux données SharePoint.</span><span class="sxs-lookup"><span data-stu-id="b0422-154">In the AppManifest.xml file, specify the permissions that your add-in needs to access Project Server data or SharePoint data.</span></span> 
  
<span data-ttu-id="b0422-155">Pour savoir comment définir des propriétés personnalisées pour un composant de complément, voir [créer des composants de complément à installer avec votre complément SharePoint](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b0422-155">See [Create add-in parts to install with your SharePoint Add-in](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) to learn how to set custom properties for an add-in part.</span></span> 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a><span data-ttu-id="b0422-156">Exemple: obtention de l'ID de projet dans un composant de complément sur une page PDP</span><span class="sxs-lookup"><span data-stu-id="b0422-156">Example: Getting the project ID in an add-in part on a PDP page</span></span>
<span data-ttu-id="b0422-157"><a name="CodeExample"> </a></span><span class="sxs-lookup"><span data-stu-id="b0422-157"></span></span>

<span data-ttu-id="b0422-158">L'exemple suivant est le code complet dans la page GetProjectID. aspx du composant WebPart client.</span><span class="sxs-lookup"><span data-stu-id="b0422-158">The following example is the complete code in the client web part's GetProjectID.aspx page.</span></span> <span data-ttu-id="b0422-159">Le code enregistre un écouteur d'événements et un gestionnaire d'événements qui reçoit et analyse un message qui contient l'ID de projet.</span><span class="sxs-lookup"><span data-stu-id="b0422-159">The code registers an event listener and an event handler that receives and parses a message that contains the project ID.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="b0422-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0422-160">See also</span></span>

- [<span data-ttu-id="b0422-161">Tâches de programmation Project</span><span class="sxs-lookup"><span data-stu-id="b0422-161">Project programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="b0422-162">Créer un complément Project Server hébergé sur SharePoint</span><span class="sxs-lookup"><span data-stu-id="b0422-162">Create a SharePoint-hosted Project Server add-in</span></span>](create-a-sharepoint-hosted-project-server-add-in.md)
- [<span data-ttu-id="b0422-163">Créer des composants de complément à installer avec votre complément SharePoint</span><span class="sxs-lookup"><span data-stu-id="b0422-163">Create add-in parts to install with your SharePoint Add-in</span></span>](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)
    

