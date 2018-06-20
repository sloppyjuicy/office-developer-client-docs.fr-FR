---
title: Obtenez l’ID de projet dans un composant sur une Page de détails de projet de complément
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 009cd997-c7e5-4078-b495-c40caa29a5fb
description: Dans Ajouter des composants sont hébergés dans les éléments iframe qui sont entièrement isolés à partir de la page d’hébergement. Pour obtenir plus d’informations sur le projet actuel dans un complément composant sur Page de détails de projet (PDP), vous pouvez utiliser la méthode window.postMessage, un récepteur d’événements et un gestionnaire d’événements qui analyse l’ID du projet à partir du message.
ms.openlocfilehash: 6704dae7ded385f86d2da47a1334ae4c81622a74
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787788"
---
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a><span data-ttu-id="dbe00-104">Obtenez l’ID de projet dans un composant sur une Page de détails de projet de complément</span><span class="sxs-lookup"><span data-stu-id="dbe00-104">Get the project ID in an add-in part on a Project Details Page</span></span>

<span data-ttu-id="dbe00-105">Dans Ajouter des composants sont hébergés dans les éléments **iframe** qui sont entièrement isolés à partir de la page d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="dbe00-105">Add-in parts are hosted in **iframe** elements that are fully isolated from the hosting page.</span></span> <span data-ttu-id="dbe00-106">Pour obtenir plus d’informations sur le projet actuel dans un complément composant sur Page de détails de projet (PDP), vous pouvez utiliser la méthode **window.postMessage** , un récepteur d’événements et un gestionnaire d’événements qui analyse l’ID du projet à partir du message.</span><span class="sxs-lookup"><span data-stu-id="dbe00-106">To get information about the current project from an add-in part on Project Details Page (PDP), you can use the **window.postMessage** method, an event listener, and an event handler that parses out the project ID from the message.</span></span> 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a><span data-ttu-id="dbe00-107">Conditions requises pour la création d’un hébergée par SharePoint complément composant qui obtient l’ID du projet</span><span class="sxs-lookup"><span data-stu-id="dbe00-107">Prerequisites for creating a SharePoint-hosted add-in part that gets the project ID</span></span>
<span data-ttu-id="dbe00-108"><a name="Prereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="dbe00-108"></span></span>

<span data-ttu-id="dbe00-109">Pour utiliser l’exemple de code dans cet article, vous avez besoin d’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="dbe00-109">To use the code example in this article, you'll need either of the following:</span></span>
  
- <span data-ttu-id="dbe00-110">SharePoint 2013 et Project Server 2013, configuré pour l’isolement du complément.</span><span class="sxs-lookup"><span data-stu-id="dbe00-110">SharePoint 2013 and Project Server 2013, configured for add-in isolation.</span></span> <span data-ttu-id="dbe00-111">Si vous développez à distance, le serveur doit prendre en charge le chargement de version test des compléments ou vous devez installer le complément sur un Site du développeur.</span><span class="sxs-lookup"><span data-stu-id="dbe00-111">If you're developing remotely, the server must support sideloading of add-ins or you must install the add-in on a Developer Site.</span></span>
  
- <span data-ttu-id="dbe00-112">SharePoint Online et Project Online</span><span class="sxs-lookup"><span data-stu-id="dbe00-112">SharePoint Online and Project Online</span></span>
    
    - <span data-ttu-id="dbe00-113">Visual Studio 2013, outils de Visual Studio 2012 avec des développeurs Office pour Visual Studio 2013, ou Napa</span><span class="sxs-lookup"><span data-stu-id="dbe00-113">Visual Studio 2013, Visual Studio 2012 with Office Developer Tools for Visual Studio 2013, or Napa</span></span>
        
    - <span data-ttu-id="dbe00-114">Autorisations suffisantes pour l'utilisateur connecté :</span><span class="sxs-lookup"><span data-stu-id="dbe00-114">Sufficient permissions for the logged-on user:</span></span>
        
        - <span data-ttu-id="dbe00-115">Autorisations d'administrateur local sur l'ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="dbe00-115">Local administrator permissions on the development computer.</span></span>
            
        - <span data-ttu-id="dbe00-116">Accès en lecture au moins un projet.</span><span class="sxs-lookup"><span data-stu-id="dbe00-116">Read access to at least one project.</span></span>
            
        - <span data-ttu-id="dbe00-117">Autorisation de modifier des pages sur le site Project Web App.</span><span class="sxs-lookup"><span data-stu-id="dbe00-117">Permission to edit pages on the Project Web App site.</span></span>
            
        - <span data-ttu-id="dbe00-118">Vous devez être connecté en tant qu’utilisateur autre que le compte système.</span><span class="sxs-lookup"><span data-stu-id="dbe00-118">You must be logged on as someone other than the system account.</span></span> <span data-ttu-id="dbe00-119">Le compte système ne dispose pas d’autorisation pour installer un complément.</span><span class="sxs-lookup"><span data-stu-id="dbe00-119">The system account does not have permission to install an add-in.</span></span>
    
<span data-ttu-id="dbe00-120">Pour plus d’informations sur les compléments pour Project, consultez [conditions requises pour créer un complément pour Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) .</span><span class="sxs-lookup"><span data-stu-id="dbe00-120">See [Prerequisites for creating an add-in for Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) for more information about add-ins for Project.</span></span> <span data-ttu-id="dbe00-121">Pour obtenir des conseils sur le programme d’installation locale (y compris comment désactiver la vérification en boucle, si nécessaire), consultez [configurer un environnement de développement local pour les compléments SharePoint](http://msdn.microsoft.com/library/b0878c12-27c9-4eea-ae3b-7e79e5a8838d%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="dbe00-121">See [Set up an on-premises development environment for SharePoint Add-ins](http://msdn.microsoft.com/library/b0878c12-27c9-4eea-ae3b-7e79e5a8838d%28Office.15%29.aspx) for guidance about on-premises setup (including how to disable the loopback check, if necessary).</span></span> <span data-ttu-id="dbe00-122">Si vous développez à distance, voir [Developing apps for SharePoint sur un système distant](http://msdn.microsoft.com/library/bf35d59c-9b84-42e5-877e-fa6881a7b6fc%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="dbe00-122">If you're developing remotely, see [Developing apps for SharePoint on a remote system](http://msdn.microsoft.com/library/bf35d59c-9b84-42e5-877e-fa6881a7b6fc%28Office.15%29.aspx).</span></span>
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a><span data-ttu-id="dbe00-123">Créer le hébergée par SharePoint complément et client de composant WebPart</span><span class="sxs-lookup"><span data-stu-id="dbe00-123">Create the SharePoint-hosted add-in and client web part</span></span>
<span data-ttu-id="dbe00-124"><a name="CreateApp"> </a></span><span class="sxs-lookup"><span data-stu-id="dbe00-124"></span></span>

1. <span data-ttu-id="dbe00-125">Ouvrez Visual Studio et choisissez **fichier** > **New** > **Project**.</span><span class="sxs-lookup"><span data-stu-id="dbe00-125">Open Visual Studio and choose **File** > **New** > **Project**.</span></span>
    
2. <span data-ttu-id="dbe00-126">Dans la boîte de dialogue **Nouveau projet**, sélectionnez **.NET Framework 4.5** dans la liste déroulante située en haut de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="dbe00-126">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
    
3. <span data-ttu-id="dbe00-127">Dans la liste des **modèles** , sélectionnez **Visual c#** > **Office/SharePoint** > **Add-ins** > **complément pour SharePoint 2013**.</span><span class="sxs-lookup"><span data-stu-id="dbe00-127">In the **Templates** list, choose **Visual C#** > **Office/SharePoint** > **Add-ins** > **Add-in for SharePoint 2013**.</span></span>
    
4. <span data-ttu-id="dbe00-128">Nom de la macro complémentaire GetProjectIdAddinPart, puis cliquez sur le bouton **OK** .</span><span class="sxs-lookup"><span data-stu-id="dbe00-128">Name the add-in GetProjectIdAddinPart, and then choose the **OK** button.</span></span> 
    
5. <span data-ttu-id="dbe00-129">Dans la boîte de dialogue **nouveau complément pour SharePoint** , entrez l’URL du site PWA que vous souhaitez utiliser pour le débogage (par exemple : _https://contoso.com/sites/pwasite/_).</span><span class="sxs-lookup"><span data-stu-id="dbe00-129">In the **New add-in for SharePoint** dialog box, enter the URL of the PWA site that you want to use for debugging (for example:  _https://contoso.com/sites/pwasite/_).</span></span>
    
6. <span data-ttu-id="dbe00-130">Choisissez l’option **hébergée par SharePoint** pour héberger votre complément, puis cliquez sur le bouton **Terminer** .</span><span class="sxs-lookup"><span data-stu-id="dbe00-130">Choose the **SharePoint-hosted** option to host your add-in, and then choose the **Finish** button.</span></span> 
    
7. <span data-ttu-id="dbe00-131">Dans **L’Explorateur de solutions**, ouvrez le menu contextuel du projet GetProjectIdAddinPart, puis choisissez **Ajouter** > **Un nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="dbe00-131">In **Solution Explorer**, open the shortcut menu for the GetProjectIdAddinPart project, and then choose **Add** > **New Item**.</span></span>
    
8. <span data-ttu-id="dbe00-132">Dans la boîte de dialogue **Ajouter un nouvel élément** , choisissez **le composant WebPart Client (site Web hôte)**, nom du composant WebPart GetProjectId, puis cliquez sur le bouton **Ajouter** .</span><span class="sxs-lookup"><span data-stu-id="dbe00-132">In the **Add New Item** dialog box, choose **Client web part (Host Web)**, name the web part GetProjectId, and then choose the **Add** button.</span></span> 
    
9. <span data-ttu-id="dbe00-133">Dans la boîte de dialogue **composant WebPart Client créer** , choisissez l’option **créer une nouvelle page de composant WebPart client** , puis cliquez sur le bouton **Terminer** .</span><span class="sxs-lookup"><span data-stu-id="dbe00-133">In the **Create Client web part** dialog box, choose the **Create a new client web part page** option, and then choose the **Finish** button.</span></span> 
    
## <a name="get-the-project-id-in-the-add-in-part"></a><span data-ttu-id="dbe00-134">Obtenez l’ID de projet dans le composant du complément</span><span class="sxs-lookup"><span data-stu-id="dbe00-134">Get the project ID in the add-in part</span></span>
<span data-ttu-id="dbe00-135"><a name="GetProjectId"> </a></span><span class="sxs-lookup"><span data-stu-id="dbe00-135"></span></span>

<span data-ttu-id="dbe00-136">Le composant du complément GetProjectId définit son code personnalisé dans la page GetProjectId.aspx du composant WebPart client.</span><span class="sxs-lookup"><span data-stu-id="dbe00-136">The GetProjectId add-in part defines its custom code in the GetProjectId.aspx page of the client web part.</span></span> <span data-ttu-id="dbe00-137">La logique qui reçoit et gère le message est définie dans l’élément **head** de la page et les contrôles de page sont définis dans l’élément **body** de la page.</span><span class="sxs-lookup"><span data-stu-id="dbe00-137">The logic that receives and handles the message is defined in the **head** element of the page and the page controls are defined in the **body** element of the page.</span></span> 
  
1. <span data-ttu-id="dbe00-138">Ouvrez la page de composants WebPart GetProjectId.aspx (dans le dossier **Pages** ).</span><span class="sxs-lookup"><span data-stu-id="dbe00-138">Open the GetProjectId.aspx web part page (in the **Pages** folder).</span></span> 
    
2. <span data-ttu-id="dbe00-139">Dans l’élément **head** de la page, remplacez le code entre les balises **script** par le code suivant.</span><span class="sxs-lookup"><span data-stu-id="dbe00-139">In the **head** element of the page, replace the code between the **script** tags with the following code.</span></span> 
    
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

3. <span data-ttu-id="dbe00-140">Ajoutez le code suivant dans l’élément **body** de la page.</span><span class="sxs-lookup"><span data-stu-id="dbe00-140">Add the following code in the **body** element of the page.</span></span> <span data-ttu-id="dbe00-141">Le code définit un contrôle d’étendue qui affiche l’ID du projet.</span><span class="sxs-lookup"><span data-stu-id="dbe00-141">The code defines a span control that displays the project ID.</span></span> 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. <span data-ttu-id="dbe00-142">Dans le fichier Elements.xml, éventuellement modifier le nom, titre, description et taille par défaut de la partie du complément.</span><span class="sxs-lookup"><span data-stu-id="dbe00-142">In the Elements.xml file, optionally change the name, title, description, and default size of the add-in part.</span></span> <span data-ttu-id="dbe00-143">Cet exemple utilise les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="dbe00-143">This example uses the default values.</span></span>
    
5. <span data-ttu-id="dbe00-144">Pour tester le composant de compléments, dans la barre de menus, choisissez **débogage**, **Démarrer le débogage**.</span><span class="sxs-lookup"><span data-stu-id="dbe00-144">To test the add-in part, on the menu bar, choose **Debug**, **Start Debugging**.</span></span> <span data-ttu-id="dbe00-145">Si vous êtes invité à modifier le fichier web.config, cliquez sur le bouton **OK** .</span><span class="sxs-lookup"><span data-stu-id="dbe00-145">If you're prompted to modify the web.config file, choose the **OK** button.</span></span> 
    
   <span data-ttu-id="dbe00-146">Pour déboguer le composant du complément, définir des points d’arrêt appropriés dans le script que vous avez ajouté.</span><span class="sxs-lookup"><span data-stu-id="dbe00-146">To debug the add-in part, set appropriate breakpoints in the script that you added.</span></span>
    
6. <span data-ttu-id="dbe00-147">Accédez à une page PDP et choisissez **Modifier la page** dans le menu Outils (icône représentant un engrenage).</span><span class="sxs-lookup"><span data-stu-id="dbe00-147">Browse to a PDP page and choose **Edit page** from the Tools menu (gear icon).</span></span> 
    
7. <span data-ttu-id="dbe00-148">Ajoutez le composant **GetProjectId titre** à un composant WebPart dans la page.</span><span class="sxs-lookup"><span data-stu-id="dbe00-148">Add the **GetProjectId Title** part to a web part on the page.</span></span> <span data-ttu-id="dbe00-149">L’ID du projet s’affiche dans le contrôle **span** sur la page de composants WebPart.</span><span class="sxs-lookup"><span data-stu-id="dbe00-149">The project ID displays in the **span** control on the web part page.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="dbe00-150">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="dbe00-150">Next steps</span></span>
<span data-ttu-id="dbe00-151"><a name="NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="dbe00-151"></span></span>

<span data-ttu-id="dbe00-152">Le composant de compléments dans cet exemple n’accéder aux données Project Server ou SharePoint.</span><span class="sxs-lookup"><span data-stu-id="dbe00-152">The add-in part in this example doesn't access Project Server data or SharePoint data.</span></span> <span data-ttu-id="dbe00-153">Vous pouvez utiliser l’ID de produit pour obtenir des informations sur le projet en cours à l’aide d’un client API, telles que le modèle objet JavaScript ou le service REST.</span><span class="sxs-lookup"><span data-stu-id="dbe00-153">You can use the product ID to get information about the current project by using a client API, such as the JavaScript object model or the REST service.</span></span>
  
<span data-ttu-id="dbe00-154">Dans le fichier AppManifest.xml, spécifiez les autorisations que votre complément doit accéder aux données Project Server ou SharePoint.</span><span class="sxs-lookup"><span data-stu-id="dbe00-154">In the AppManifest.xml file, specify the permissions that your add-in needs to access Project Server data or SharePoint data.</span></span> 
  
<span data-ttu-id="dbe00-155">Voir [Création de compléments composants à installer avec votre complément SharePoint](http://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) pour découvrir comment définir les propriétés personnalisées pour une partie du complément.</span><span class="sxs-lookup"><span data-stu-id="dbe00-155">See [Create add-in parts to install with your SharePoint Add-in](http://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) to learn how to set custom properties for an add-in part.</span></span> 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a><span data-ttu-id="dbe00-156">Exemple : Obtention de l’ID de projet dans un composant complément sur une page PDP</span><span class="sxs-lookup"><span data-stu-id="dbe00-156">Example: Getting the project ID in an add-in part on a PDP page</span></span>
<span data-ttu-id="dbe00-157"><a name="CodeExample"> </a></span><span class="sxs-lookup"><span data-stu-id="dbe00-157"></span></span>

<span data-ttu-id="dbe00-158">L’exemple suivant est le code complet de la page de GetProjectID.aspx du composant WebPart client.</span><span class="sxs-lookup"><span data-stu-id="dbe00-158">The following example is the complete code in the client web part's GetProjectID.aspx page.</span></span> <span data-ttu-id="dbe00-159">Le code inscrit un écouteur d’événement et un gestionnaire d’événements qui reçoit et analyse un message qui contient l’ID du projet.</span><span class="sxs-lookup"><span data-stu-id="dbe00-159">The code registers an event listener and an event handler that receives and parses a message that contains the project ID.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="dbe00-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbe00-160">See also</span></span>

- [<span data-ttu-id="dbe00-161">Tâches de programmation du projet</span><span class="sxs-lookup"><span data-stu-id="dbe00-161">Project programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="dbe00-162">Créer un complément hébergée par SharePoint Project Server</span><span class="sxs-lookup"><span data-stu-id="dbe00-162">Create a SharePoint-hosted Project Server add-in</span></span>](create-a-sharepoint-hosted-project-server-add-in.md)
- [<span data-ttu-id="dbe00-163">Créer des composants de complément à installer avec votre complément SharePoint</span><span class="sxs-lookup"><span data-stu-id="dbe00-163">Create add-in parts to install with your SharePoint Add-in</span></span>](http://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)
    

