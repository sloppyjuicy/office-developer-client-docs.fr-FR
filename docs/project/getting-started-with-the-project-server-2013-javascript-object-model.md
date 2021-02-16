---
title: Prise en main du modèle objet JavaScript Project Server 2013
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30dc3194-7480-4e7c-b731-4a171d652ee0
description: Dans Project Server 2013, le modèle objet JavaScript peut être utilisé dans Project Online, le développement mobile et local. Cette rubrique fournit une brève vue d’ensemble du modèle objet JavaScript, puis explique comment créer une page d’application qui récupère et itérera les projets à l’aide du modèle objet JavaScript.
ms.openlocfilehash: ec8a10e987276807dc4648bd8948b2285f76fd37
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360472"
---
# <a name="getting-started-with-the-project-server-2013-javascript-object-model"></a><span data-ttu-id="1b745-104">Prise en main du modèle objet JavaScript Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="1b745-104">Getting started with the Project Server 2013 JavaScript object model</span></span>

<span data-ttu-id="1b745-105">Dans Project Server 2013, le modèle objet JavaScript peut être utilisé dans Project Online, le développement mobile et local.</span><span class="sxs-lookup"><span data-stu-id="1b745-105">In Project Server 2013, the JavaScript object model can be used in Project Online, mobile, and on-premise development.</span></span> <span data-ttu-id="1b745-106">Cette rubrique fournit une brève vue d’ensemble du modèle objet JavaScript, puis explique comment créer une page d’application qui récupère et itérera les projets à l’aide du modèle objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1b745-106">This topic provides a brief overview of the JavaScript object model and then describes how to create an application page that retrieves and iterates through projects by using the JavaScript object model.</span></span>
  
## <a name="using-the-project-server-javascript-object-model"></a><span data-ttu-id="1b745-107">Utilisation du modèle objet JavaScript Project Server</span><span class="sxs-lookup"><span data-stu-id="1b745-107">Using the Project Server JavaScript object model</span></span>
<span data-ttu-id="1b745-108"><a name="pj15_GetStartedJSOM_UseJSOM"> </a></span><span class="sxs-lookup"><span data-stu-id="1b745-108"><a name="pj15_GetStartedJSOM_UseJSOM"> </a></span></span>

<span data-ttu-id="1b745-109">L’utilisation du modèle objet JavaScript est un excellent moyen de créer une application qui s’exécute côté client (par opposition au code client géré qui doit s’exécuter à distance).</span><span class="sxs-lookup"><span data-stu-id="1b745-109">Using the JavaScript object model is a great way to create an app that runs client-side (as opposed to managed client code which needs to run remotely).</span></span> <span data-ttu-id="1b745-110">Les applications peuvent utiliser le modèle objet JavaScript pour récupérer ou modifier des objets en envoyant des appels asynchrones au serveur.</span><span class="sxs-lookup"><span data-stu-id="1b745-110">Apps can use the JavaScript object model to retrieve or change objects by sending asynchronous calls to the server.</span></span> <span data-ttu-id="1b745-111">Les applications qui utilisent le modèle objet JavaScript sont généralement déployées en tant que Applications SharePoint personnalisées, pages d’application et WebParts.</span><span class="sxs-lookup"><span data-stu-id="1b745-111">Apps that use the JavaScript object model are typically deployed as custom SharePoint Add-ins, application pages, and Web Parts.</span></span> <span data-ttu-id="1b745-112">Pour plus d’informations, voir « Types de composants SharePoint qui peuvent se trouver dans une application pour SharePoint » dans les sites web hôtes, les sites web de add-in et les [composants SharePoint dans SharePoint 2013.](https://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b745-112">For more information, see "Types of SharePoint components that can be in an app for SharePoint" in [Host webs, add-in webs, and SharePoint components in SharePoint 2013](https://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="1b745-113">Le modèle objet JavaScript implémente la fonctionnalité principale de Project Server 2013, mais le modèle objet JavaScript et le modèle objet serveur n’ont pas de parité un-à-un.</span><span class="sxs-lookup"><span data-stu-id="1b745-113">The JavaScript object model implements the main functionality of Project Server 2013, but the JavaScript object model and the server object model do not have one-to-one parity.</span></span> <span data-ttu-id="1b745-114">Le point d’entrée du modèle objet JavaScript est l’objet **ProjectContext,** qui représente le contexte client pour Project Server 2013 et fournit l’accès au contenu et aux fonctionnalités du serveur.</span><span class="sxs-lookup"><span data-stu-id="1b745-114">The entry point to the JavaScript object model is the **ProjectContext** object, which represents the client context for Project Server 2013 and provides access to server content and functionality.</span></span> <span data-ttu-id="1b745-115">Le modèle objet JavaScript pour Project Server 2013 est défini dans le fichier PS.js, qui se trouve dans le chemin d’accès par défaut sur le serveur  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS` d’applications.</span><span class="sxs-lookup"><span data-stu-id="1b745-115">The JavaScript object model for Project Server 2013 is defined in the PS.js file, which is located in the default path  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS` on the application server.</span></span> <span data-ttu-id="1b745-116">Project Server 2013 installe également le fichier PS.Debug.js au même emplacement.</span><span class="sxs-lookup"><span data-stu-id="1b745-116">Project Server 2013 also installs the PS.Debug.js file in the same location.</span></span> <span data-ttu-id="1b745-117">Ce fichier est une version déminifiée de PS.js qui fournit des informations sur IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="1b745-117">PS.Debug.js is an unminified version of PS.js that provides IntelliSense information.</span></span> 
  
<span data-ttu-id="1b745-118">Le modèle objet JavaScript permet l’authentification par formulaires et toutes les demandes sont authentifiées en tant qu’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="1b745-118">The JavaScript object model allows Forms authentication, and all requests are authenticated as the current user.</span></span> <span data-ttu-id="1b745-119">Pour plus d’informations sur la sécurité et d’autres considérations pour la conception d’applications et de solutions personnalisées, voir l’authentification, l’autorisation et la sécurité dans [SharePoint 2013](https://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx), des aspects importants de l’architecture et du développement des applications [sharePoint](https://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx)et des applications SharePoint par rapport aux [solutions SharePoint.](https://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b745-119">For more information about security and other considerations for designing custom apps and solutions, see [Authentication, authorization, and security in SharePoint 2013](https://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx), [Important aspects of the SharePoint Add-in architecture and development landscape](https://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx), and [SharePoint Add-ins compared with SharePoint solutions](https://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx).</span></span>
  
> [!NOTE]
> <span data-ttu-id="1b745-120">Pour accéder aux données à partir d’un site SharePoint à distance, SharePoint 2013 fournit une bibliothèque entre domaines qui vous permet d’effectuer des appels côté client entre domaines.</span><span class="sxs-lookup"><span data-stu-id="1b745-120">To access data from a SharePoint site remotely, SharePoint 2013 provides a cross-domain library that enables you to make client-side cross-domain calls.</span></span> <span data-ttu-id="1b745-121">Pour plus d’informations, [voir Données Access SharePoint 2013](https://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx)à partir de l’utilisation de la bibliothèque entre domaines.</span><span class="sxs-lookup"><span data-stu-id="1b745-121">For more information, see [Access SharePoint 2013 data from add-ins using the cross-domain library](https://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx).</span></span> 
  
<span data-ttu-id="1b745-122">De nombreux concepts et processus d’utilisation du modèle objet JavaScript pour Project Server 2013 ressemblent à ceux des modèles objet client associés.</span><span class="sxs-lookup"><span data-stu-id="1b745-122">Many concepts and processes for using the JavaScript object model for Project Server 2013 resemble those in related client object models.</span></span> <span data-ttu-id="1b745-123">Pour plus d’informations sur le modèle objet client géré Project Server 2013, voir **Microsoft.ProjectServer.Client**.</span><span class="sxs-lookup"><span data-stu-id="1b745-123">For more information about the Project Server 2013 managed client object model, see **Microsoft.ProjectServer.Client**.</span></span> <span data-ttu-id="1b745-124">Pour plus d’informations sur le modèle objet SharePoint 2013JavaScript et le modèle objet client géré, voir Effectuer des opérations de base à l’aide de code de bibliothèque JavaScript dans [SharePoint 2013](https://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx) et Effectuer des opérations de base à l’aide du code de bibliothèque client [SharePoint 2013.](https://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b745-124">For more information about the SharePoint 2013JavaScript object model and managed client object model, see [Complete basic operations using JavaScript library code in SharePoint 2013](https://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx) and [Complete basic operations using SharePoint 2013 client library code](https://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx).</span></span>
  
## <a name="walkthrough-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a><span data-ttu-id="1b745-125">Procédure : Création d’une page d’application qui récupère et parcourt les projets</span><span class="sxs-lookup"><span data-stu-id="1b745-125">Walkthrough: Creating an application page that retrieves and iterates through projects</span></span>
<span data-ttu-id="1b745-126"><a name="pj15_GetStartedJSOM_UseJSOM"> </a></span><span class="sxs-lookup"><span data-stu-id="1b745-126"><a name="pj15_GetStartedJSOM_UseJSOM"> </a></span></span>

<span data-ttu-id="1b745-127">Apprenez à créer une page d’application qui affiche l’ID, le nom et la date de création de chaque projet publié dans un site.</span><span class="sxs-lookup"><span data-stu-id="1b745-127">Learn how to create an application page that displays the ID, name, and created date of each published project in a site.</span></span>
  
### <a name="prerequisites-for-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a><span data-ttu-id="1b745-128">Conditions préalables à la création d’une page d’application qui récupère et parcourt les projets</span><span class="sxs-lookup"><span data-stu-id="1b745-128">Prerequisites for creating an application page that retrieves and iterates through projects</span></span>
<span data-ttu-id="1b745-129"><a name="pj15_GetStartedJSOM_Prereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="1b745-129"><a name="pj15_GetStartedJSOM_Prereqs"> </a></span></span>

<span data-ttu-id="1b745-130">Pour développer la page d’application décrite dans cette rubrique, vous devez installer et configurer les produits suivants :</span><span class="sxs-lookup"><span data-stu-id="1b745-130">To develop the application page that is described in this topic, you must install and configure the following products:</span></span>
  
- <span data-ttu-id="1b745-131">SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="1b745-131">SharePoint Server 2013</span></span>
- <span data-ttu-id="1b745-132">Project Server 2013 avec au moins un projet publié</span><span class="sxs-lookup"><span data-stu-id="1b745-132">Project Server 2013 with at least one published project</span></span>
- <span data-ttu-id="1b745-133">Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="1b745-133">Visual Studio 2012</span></span>
- <span data-ttu-id="1b745-134">Outils de développement Office pour Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="1b745-134">Office Developer Tools for Visual Studio 2012</span></span>
    
<span data-ttu-id="1b745-135">Vous devez également avoir les autorisations pour déployer l’extension sur SharePoint Server 2013 et récupérer des projets.</span><span class="sxs-lookup"><span data-stu-id="1b745-135">You must also have permissions to deploy the extension to SharePoint Server 2013 and to retrieve projects.</span></span>
  
> [!NOTE]
> <span data-ttu-id="1b745-136">Ces instructions supposent que vous développez sur l’ordinateur qui exécute Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1b745-136">These instructions assume that you are developing on the computer that is running Project Server 2013.</span></span> 
  
### <a name="creating-the-application-page-in-visual-studio-2012"></a><span data-ttu-id="1b745-137">Création de la page d’application Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="1b745-137">Creating the application page in Visual Studio 2012</span></span>
<span data-ttu-id="1b745-138"><a name="pj15_GetStartedJSOM_CreateVS"> </a></span><span class="sxs-lookup"><span data-stu-id="1b745-138"><a name="pj15_GetStartedJSOM_CreateVS"> </a></span></span>

<span data-ttu-id="1b745-p108">Les étapes suivantes permettent de créer un projet SharePoint et une page d’application qui contient un tableau et un libellé. Le tableau affiche des informations sur les projets et le libellé affiche des messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="1b745-p108">The following steps create a SharePoint project and an application page that contains a table and label. The table displays information about the projects and the label displays error messages.</span></span>
  
1. <span data-ttu-id="1b745-141">Sur l’ordinateur qui exécute Project Server 2013, exécutez Visual Studio 2012 en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="1b745-141">On the computer that is running Project Server 2013, run Visual Studio 2012 as an administrator.</span></span>
    
2. <span data-ttu-id="1b745-142">Créez un projet SharePoint 2013 vide, comme suit :</span><span class="sxs-lookup"><span data-stu-id="1b745-142">Create an empty SharePoint 2013 project, as follows:</span></span>
    
    1. <span data-ttu-id="1b745-143">Dans la boîte de dialogue **Nouveau projet**, sélectionnez **.NET Framework 4.5** dans la liste déroulante située en haut de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="1b745-143">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
        
    2. <span data-ttu-id="1b745-144">Dans la liste des catégories de modèles, choisissez la catégorie **Office SharePoint**, puis sélectionnez le modèle **SharePoint 2013 Project**.</span><span class="sxs-lookup"><span data-stu-id="1b745-144">In the list of template categories, choose the **Office SharePoint** category, and then choose the **SharePoint 2013 Project** template.</span></span> 
        
    3. <span data-ttu-id="1b745-145">Nommez le projet GetProjectsJSOM, puis choisissez le **bouton OK.**</span><span class="sxs-lookup"><span data-stu-id="1b745-145">Name the project GetProjectsJSOM, and then choose the **OK** button.</span></span> 
        
    4. <span data-ttu-id="1b745-146">Dans la boîte de dialogue **Assistant Personnalisation de SharePoint**, choisissez **Déployer en tant que solution de batterie**, puis sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="1b745-146">In the **SharePoint Customization Wizard** dialog box, choose **Deploy as a farm solution**, and then choose the **OK** button.</span></span> 
    
3. <span data-ttu-id="1b745-147">Dans l’Explorateur de solutions, modifiez la valeur de la propriété URL du **site** pour le **projet ProjectsJSOM** afin qu’elle corresponde à l’URL de l’instance de Project Web App (par exemple,  `https://ServerName/PWA` ).</span><span class="sxs-lookup"><span data-stu-id="1b745-147">In Solution Explorer, edit the value of the **Site URL** property for the **ProjectsJSOM** project to match the URL of the Project Web App instance (for example,  `https://ServerName/PWA`).</span></span>
    
4. <span data-ttu-id="1b745-148">Ouvrez le menu contextuel pour le projet **GetProjectsJSOM**, puis ajoutez un dossier mappé SharePoint nommé « Dispositions ».</span><span class="sxs-lookup"><span data-stu-id="1b745-148">Open the shortcut menu for the **GetProjectsJSOM** project, and then add a SharePoint "Layouts" mapped folder.</span></span> 
    
5. <span data-ttu-id="1b745-149">Dans le **dossier Layouts,** ouvrez le menu raccourci du dossier **GetProjectsJSOM,** puis ajoutez une nouvelle page d’application SharePoint nommée ProjectsList.aspx.</span><span class="sxs-lookup"><span data-stu-id="1b745-149">In the **Layouts** folder, open the shortcut menu for the **GetProjectsJSOM** folder, and then add a new SharePoint application page named ProjectsList.aspx.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="1b745-150">Cet exemple n’utilise pas le fichier code-behind que Visual Studio 2012 crée pour la page d’application.</span><span class="sxs-lookup"><span data-stu-id="1b745-150">This example does not use the code-behind file that Visual Studio 2012 creates for the application page.</span></span> 
  
6. <span data-ttu-id="1b745-151">Ouvrez le menu contextuel de la page **ProjectsList.aspx** et choisissez **Définir comme élément de démarrage**.</span><span class="sxs-lookup"><span data-stu-id="1b745-151">Open the shortcut menu for the **ProjectsList.aspx** page and choose **Set as Startup Item**.</span></span>
    
7. <span data-ttu-id="1b745-152">Dans le balisage pour la page **ProjectsList.aspx**, définissez un tableau et un espace réservé de message dans les balises **asp:Content** « principales », comme suit.</span><span class="sxs-lookup"><span data-stu-id="1b745-152">In the markup for the **ProjectsList.aspx** page, define a table and a message placeholder inside the "Main" **asp:Content** tags, as follows.</span></span> 
    
    ```HTML
    <table width="100%" id="tblProjects">
        <tr id="headerRow">
            <th width="25%" align="left">Project name</th>
            <th width="25%" align="left">Created date</th>
            <th width="50%" align="left">Project ID</th>
        </tr>
    </table>
    <div id="divMessage">
        <br/>
        <span id="spanMessage" style="color: #FF0000;"></span>
    </div>
    ```

### <a name="retrieving-the-projects-collection"></a><span data-ttu-id="1b745-153">Récupération de la collection de projets</span><span class="sxs-lookup"><span data-stu-id="1b745-153">Retrieving the projects collection</span></span>
<span data-ttu-id="1b745-154"><a name="pj15_GetStartedJSOM_RetrieveProjs"> </a></span><span class="sxs-lookup"><span data-stu-id="1b745-154"><a name="pj15_GetStartedJSOM_RetrieveProjs"> </a></span></span>

<span data-ttu-id="1b745-155">Les étapes suivantes permettent de récupérer et d’initialiser la collection de projets.</span><span class="sxs-lookup"><span data-stu-id="1b745-155">The following steps retrieve and initialize the projects collection.</span></span>
  
1. <span data-ttu-id="1b745-156">Après la fermeture de la balise **div**, ajoutez une balise **SharePoint:ScriptLink** qui fait référence au fichier PS.js, comme suit.</span><span class="sxs-lookup"><span data-stu-id="1b745-156">After the closing **div** tag, add a **SharePoint:ScriptLink** tag that references the PS.js file, as follows.</span></span> 
    
   ```HTML
    <SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
   ```

2. <span data-ttu-id="1b745-157">Sous la balise **SharePoint:ScriptLink**, ajoutez des balises **script**, comme suit.</span><span class="sxs-lookup"><span data-stu-id="1b745-157">Below the **SharePoint:ScriptLink** tag, add **script** tags, as follows.</span></span> 
    
   ```HTML
    <script type="text/javascript">
        // Paste the remaining code snippets here, in the order that they are presented.
    </script>
   ```

3. <span data-ttu-id="1b745-158">Choisissez une variable globale pour stocker la collection de projets, comme suit.</span><span class="sxs-lookup"><span data-stu-id="1b745-158">Declare a global variable to store the projects collection, as follows.</span></span>
    
   ```js
   var projects;
   ```

4. <span data-ttu-id="1b745-159">Appelez la méthode **SP.SOD.executeOrDelayUntilScriptLoaded** pour vous assurer que le fichier PS.js est chargé avant l’exécution de votre code personnalisé.</span><span class="sxs-lookup"><span data-stu-id="1b745-159">Call the **SP.SOD.executeOrDelayUntilScriptLoaded** method to ensure that the PS.js file is loaded before your custom code runs.</span></span> 
    
   ```js
   SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
   ```

5. <span data-ttu-id="1b745-160">Ajoutez une fonction qui se connecte au contexte actuel et qui récupère la collection de projets, comme suit.</span><span class="sxs-lookup"><span data-stu-id="1b745-160">Add a function that connects to the current context and retrieves the projects collection, as follows.</span></span>
    
   ```js
    function GetProjects() {
        // Initialize the current client context.
        var projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the
        // Name, CreatedDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, CreatedDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(onQuerySucceeded, onQueryFailed);
    }
   ```

   <span data-ttu-id="1b745-161">Certains objets clients que vous récupérez dans le contexte ne contiennent aucune donnée tant qu’ils n’ont pas été initialisés ; Autrement dit, vous ne pouvez pas accéder aux valeurs de propriété de l’objet tant que l’objet n’a pas été initialisé.</span><span class="sxs-lookup"><span data-stu-id="1b745-161">Some client objects that you retrieve through the context contain no data until they are initialized; that is, you cannot access the property values of the object until the object is initialized.</span></span> <span data-ttu-id="1b745-162">En outre, pour les propriétés de type **ValueObject,** vous devez demander explicitement la propriété avant de pouvoir accéder à sa valeur.</span><span class="sxs-lookup"><span data-stu-id="1b745-162">Moreover, for properties of type **ValueObject**, you must explicitly request the property before you can access its value.</span></span> <span data-ttu-id="1b745-163">(Si vous essayez d’accéder à une propriété avant son initialisation, vous recevez une exception **PropertyOrFieldNotInitializedException.)**</span><span class="sxs-lookup"><span data-stu-id="1b745-163">(If you try to access a property before it is initialized, you receive a **PropertyOrFieldNotInitializedException** exception.)</span></span> 
    
   <span data-ttu-id="1b745-164">Pour initialiser un objet, appelez la méthode **load** (ou la méthode **loadQuery**), puis la méthode **executeQueryAsync**.</span><span class="sxs-lookup"><span data-stu-id="1b745-164">To initialize an object, you call the **load** method (or the **loadQuery** method) and then the **executeQueryAsync** method.</span></span> 
    
   - <span data-ttu-id="1b745-165">L’appel de la fonction **load** ou **loadQuery** permet d’enregistrer une demande que vous souhaitez exécuter sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="1b745-165">Calling the **load** function or the **loadQuery** function registers a request that you want to run on the server.</span></span> <span data-ttu-id="1b745-166">Vous transmettez un paramètre qui représente l’objet que vous souhaitez récupérer.</span><span class="sxs-lookup"><span data-stu-id="1b745-166">You pass in a parameter that represents the object that you want to retrieve.</span></span> <span data-ttu-id="1b745-167">Si vous utilisez une propriété **ValueObject**, vous devez également demander la propriété dans le paramètre.</span><span class="sxs-lookup"><span data-stu-id="1b745-167">If you are working with a **ValueObject** property, then you also request the property in the parameter.</span></span> 
    
   - <span data-ttu-id="1b745-168">L’appel de la fonction **executeQueryAsync** envoie la demande de requête au serveur de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="1b745-168">Calling the **executeQueryAsync** function sends the query request to the server asynchronously.</span></span> <span data-ttu-id="1b745-169">Vous transmettez une fonction de rappel de succès et d’échec à invoquer lorsque vous recevez la réponse du serveur.</span><span class="sxs-lookup"><span data-stu-id="1b745-169">You pass in a success callback function and a failure callback function to invoke when the server response is received.</span></span> 
    
   <span data-ttu-id="1b745-170">Pour réduire le trafic réseau, demandez uniquement les propriétés que vous souhaitez utiliser lorsque vous appelez la fonction **load**.</span><span class="sxs-lookup"><span data-stu-id="1b745-170">To reduce network traffic, request only the properties that you want to work with when you call the **load** function.</span></span> <span data-ttu-id="1b745-171">En outre, si vous utilisez plusieurs objets, si possible, regroupez plusieurs appels de la fonction **load** avant d’appeler la fonction **executeQueryAsync**.</span><span class="sxs-lookup"><span data-stu-id="1b745-171">In addition, if you are working with multiple objects, group multiple calls to the **load** function before you call the **executeQueryAsync** function when it is possible.</span></span> 
    
### <a name="iterating-through-the-projects-collection"></a><span data-ttu-id="1b745-172">Parcourir la collection de projets</span><span class="sxs-lookup"><span data-stu-id="1b745-172">Iterating through the projects collection</span></span>
<span data-ttu-id="1b745-173"><a name="pj15_GetStartedJSOM_IterateProjs"> </a></span><span class="sxs-lookup"><span data-stu-id="1b745-173"><a name="pj15_GetStartedJSOM_IterateProjs"> </a></span></span>

<span data-ttu-id="1b745-174">Les étapes suivantes permettent de parcourir la collection de projets (si l’appel au serveur aboutit) ou d’afficher un message d’erreur (si l’appel échoue).</span><span class="sxs-lookup"><span data-stu-id="1b745-174">The following steps iterate through the projects collection (if the server call is successful) or render an error message (if the call fails).</span></span>
  
1. <span data-ttu-id="1b745-175">Ajoutez une fonction de rappel de succès qui parcourt la collection de projets, comme suit.</span><span class="sxs-lookup"><span data-stu-id="1b745-175">Add a success callback function that iterates through the projects collection, as follows.</span></span>
    
   ```js
    function onQuerySucceeded(sender, args) {
        // Get the enumerator and iterate through the collection.
        var projectEnumerator = projects.getEnumerator();
        while (projectEnumerator.moveNext()) {
            var project = projectEnumerator.get_current();
            // Create the row for the project's information.
            var row = tblProjects.insertRow();
            // Insert cells for the Id, Name, and CreatedDate properties.
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_createdDate();
            row.insertCell().innerText = project.get_id();
        }
    }
   ```

2. <span data-ttu-id="1b745-176">Ajoutez une fonction de rappel d’échec qui affiche un message d’erreur, comme suit.</span><span class="sxs-lookup"><span data-stu-id="1b745-176">Add a failure callback function that renders an error message, as follows.</span></span>
    
    ```js
    function onQueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
    ```

3. <span data-ttu-id="1b745-p113">Pour tester la page d’application, dans la barre de menus, sélectionnez **Déboguer**, puis **Démarrer le débogage**. Si vous êtes invité à modifier le fichier web.config, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="1b745-p113">To test the application page, on the menu bar, choose **Debug**, **Start Debugging**. If you are prompted to modify the web.config file, choose **OK**.</span></span>

<span data-ttu-id="1b745-179"><a name="pj15_GetStartedJSOM_CompleteExample"> </a></span><span class="sxs-lookup"><span data-stu-id="1b745-179"><a name="pj15_GetStartedJSOM_CompleteExample"> </a></span></span>

## <a name="complete-code-example"></a><span data-ttu-id="1b745-180">Exemple de code complet</span><span class="sxs-lookup"><span data-stu-id="1b745-180">Complete code example</span></span>

<span data-ttu-id="1b745-181">Vous trouverez ci-dessous l’ensemble du code du fichier ProjectsList.aspx.</span><span class="sxs-lookup"><span data-stu-id="1b745-181">Following is the complete code from the ProjectsList.aspx file.</span></span>
  
```js
<%@ Assembly Name="$SharePoint.Project.AssemblyFullName$" %>
<%@ Import Namespace="Microsoft.SharePoint.ApplicationPages" %>
<%@ Register Tagprefix="SharePoint" Namespace="Microsoft.SharePoint.WebControls" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="Utilities" Namespace="Microsoft.SharePoint.Utilities" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="asp" Namespace="System.Web.UI" Assembly="System.Web.Extensions, Version=3.5.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35" %>
<%@ Import Namespace="Microsoft.SharePoint" %>
<%@ Assembly Name="Microsoft.Web.CommandUI, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="ProjectsList.aspx.cs" Inherits="GetProjectsJSOM.Layouts.GetProjectsJSOM.ProjectsList" DynamicMasterPageFile="~masterurl/default.master" %>
<asp:Content ID="PageHead" ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">
</asp:Content>
<asp:Content ID="Main" ContentPlaceHolderID="PlaceHolderMain" runat="server">
    <table width="100%" id="tblProjects">
    <tr id="headerRow">
        <th width="25%" align="left">Project name</th>
        <th width="25%" align="left">Created date</th>
        <th width="50%" align="left">Project ID</th>
    </tr>
</table>
<div id="divMessage">
    <br/>
    <span id="spanMessage" style="color: #FF0000;"></span>
</div>
<SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
<script type="text/javascript">
    // Declare a variable to store the published projects that exist
    // in the current context.
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
    // Get the projects collection.
    function GetProjects() {
        // Initialize the current client context.
        var projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the
        // Name, CreatedDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, CreatedDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(onQuerySucceeded, onQueryFailed);
    }
    function onQuerySucceeded(sender, args) {
        // Get the enumerator and iterate through the collection.
        var projectEnumerator = projects.getEnumerator();
        while (projectEnumerator.moveNext()) {
            var project = projectEnumerator.get_current();
            // Create the row for the project's information.
            var row = tblProjects.insertRow();
            // Insert cells for the Id, Name, and CreatedDate properties.
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_createdDate();
            row.insertCell().innerText = project.get_id();
        }
    }
    function onQueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
</script>
</asp:Content>
<asp:Content ID="PageTitle" ContentPlaceHolderID="PlaceHolderPageTitle" runat="server">
Application Page
</asp:Content>
<asp:Content ID="PageTitleInTitleArea" ContentPlaceHolderID="PlaceHolderPageTitleInTitleArea" runat="server" >
My Application Page
</asp:Content>

```

<span data-ttu-id="1b745-182"><a name="pj15_GetStartedJSOM_AR"> </a></span><span class="sxs-lookup"><span data-stu-id="1b745-182"><a name="pj15_GetStartedJSOM_AR"> </a></span></span>

## <a name="see-also"></a><span data-ttu-id="1b745-183">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b745-183">See also</span></span>

- [<span data-ttu-id="1b745-184">Créer, récupérer, mettre à jour et supprimer des projets à l’aide du modèle objet JavaScript Project Server</span><span class="sxs-lookup"><span data-stu-id="1b745-184">Create, retrieve, update, and delete projects by using the Project Server JavaScript object model</span></span>](create-retrieve-update-delete-projects-using-project-server-javascript.md)  
- [<span data-ttu-id="1b745-185">Modèle objet côté client (CSOM) pour Project 2013</span><span class="sxs-lookup"><span data-stu-id="1b745-185">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)
- [<span data-ttu-id="1b745-186">Prise en main du modèle CSOM Project Server et de .NET</span><span class="sxs-lookup"><span data-stu-id="1b745-186">Getting started with the Project Server CSOM and .NET</span></span>](getting-started-with-the-project-server-csom-and-net.md)
    

