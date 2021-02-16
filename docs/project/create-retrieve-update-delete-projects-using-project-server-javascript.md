---
title: Créer, récupérer, mettre à jour et supprimer des projets à l’aide de Project Server JavaScript
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6b690938-05bc-46a3-a40e-30f081403767
description: Obtenir l’instance ProjectContext actuelle ; récupérer et itérer dans la collection de projets publiés sur le serveur ; créer, récupérer, extraire et supprimer un projet à l’aide du modèle objet JavaScript Project Server ; et modifier les propriétés d’un projet.
ms.openlocfilehash: 10dac7edfa3e84cebfd0585bc8c4bff1ea22ea44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322665"
---
# <a name="create-retrieve-update-and-delete-projects-using-project-server-javascript"></a><span data-ttu-id="6468d-103">Créer, récupérer, mettre à jour et supprimer des projets à l’aide de Project Server JavaScript</span><span class="sxs-lookup"><span data-stu-id="6468d-103">Create, retrieve, update, and delete projects using Project Server JavaScript</span></span>

<span data-ttu-id="6468d-104">Les scénarios de cet article montrent comment obtenir l’instance **ProjectContext** actuelle ; récupérer et itérer dans la collection de projets publiés sur le serveur ; créer, récupérer, extraire et supprimer un projet à l’aide du modèle objet JavaScript Project Server ; et modifier les propriétés d’un projet.</span><span class="sxs-lookup"><span data-stu-id="6468d-104">The scenarios in this article show how to get the current **ProjectContext** instance; retrieve and iterate through the collection of published projects on the server; create, retrieve, check out, and delete a project by using the Project Server JavaScript object model; and change a project's properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6468d-105">Ces scénarios définissent du code personnalisé dans le code d’une page d’application SharePoint, mais n’utilisent pas le fichier code-behind créé par Visual Studio 2012 pour la page.</span><span class="sxs-lookup"><span data-stu-id="6468d-105">These scenarios define custom code in the markup of a SharePoint application page but do not use the code-behind file that Visual Studio 2012 creates for the page.</span></span> 
  
## <a name="prerequisites-for-working-with-project-server-2013-projects-in-the-javascript-object-model"></a><span data-ttu-id="6468d-106">Conditions préalables à l’emploi de projets Project Server 2013 dans le modèle objet JavaScript</span><span class="sxs-lookup"><span data-stu-id="6468d-106">Prerequisites for working with Project Server 2013 projects in the JavaScript object model</span></span>

<span data-ttu-id="6468d-107">Pour effectuer les scénarios décrits dans cet article, vous devez installer et configurer les produits suivants :</span><span class="sxs-lookup"><span data-stu-id="6468d-107">To perform the scenarios that are described in this article, you must install and configure the following products:</span></span>
  
- <span data-ttu-id="6468d-108">SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="6468d-108">SharePoint Server 2013</span></span>
- <span data-ttu-id="6468d-109">Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="6468d-109">Project Server 2013</span></span>
- <span data-ttu-id="6468d-110">Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="6468d-110">Visual Studio 2012</span></span>
- <span data-ttu-id="6468d-111">Outils de développement Office pour Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="6468d-111">Office Developer Tools for Visual Studio 2012</span></span>
    
<span data-ttu-id="6468d-112">Vous devez également avoir les autorisations pour déployer l’extension sur SharePoint Server 2013 et contribuer à des projets.</span><span class="sxs-lookup"><span data-stu-id="6468d-112">You must also have permissions to deploy the extension to SharePoint Server 2013 and to contribute to projects.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6468d-113">Ces instructions supposent que vous développez sur l’ordinateur qui exécute Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6468d-113">These instructions assume that you are developing on the computer that is running Project Server 2013.</span></span> 
  
## <a name="create-the-visual-studio-solution"></a><span data-ttu-id="6468d-114">Créer la Visual Studio solution</span><span class="sxs-lookup"><span data-stu-id="6468d-114">Create the Visual Studio solution</span></span>
<span data-ttu-id="6468d-115"><a name="pj15_CRUDProjectsJSOM_Setup"> </a></span><span class="sxs-lookup"><span data-stu-id="6468d-115"><a name="pj15_CRUDProjectsJSOM_Setup"> </a></span></span>

<span data-ttu-id="6468d-116">Les étapes suivantes créent une solution Visual Studio 2012 contenant un projet SharePoint et une page d’application.</span><span class="sxs-lookup"><span data-stu-id="6468d-116">The following steps create a Visual Studio 2012 solution that contains a SharePoint project and an application page.</span></span> <span data-ttu-id="6468d-117">La page contient la logique pour travailler avec des projets.</span><span class="sxs-lookup"><span data-stu-id="6468d-117">The page contains the logic for working with projects.</span></span>
  
### <a name="to-create-the-sharepoint-project-in-visual-studio"></a><span data-ttu-id="6468d-118">Pour créer le projet SharePoint dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6468d-118">To create the SharePoint project in Visual Studio</span></span>

1. <span data-ttu-id="6468d-119">Sur l’ordinateur qui exécute Project Server 2013, exécutez Visual Studio 2012 en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="6468d-119">On the computer that is running Project Server 2013, run Visual Studio 2012 as an administrator.</span></span>
    
2. <span data-ttu-id="6468d-120">On the menu bar, choose **File**, **New**, **Project**.</span><span class="sxs-lookup"><span data-stu-id="6468d-120">On the menu bar, choose **File**, **New**, **Project**.</span></span>
    
3. <span data-ttu-id="6468d-121">Dans la boîte de dialogue **Nouveau projet**, sélectionnez **.NET Framework 4.5** dans la liste déroulante située en haut de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="6468d-121">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
    
4. <span data-ttu-id="6468d-122">Dans la catégorie des modèles **Office/SharePoint,** choisissez **Solutions SharePoint,** puis le modèle **Projet SharePoint 2013.**</span><span class="sxs-lookup"><span data-stu-id="6468d-122">In the **Office/SharePoint** template category, choose **SharePoint Solutions**, and then choose the **SharePoint 2013 Project** template.</span></span> 
    
5. <span data-ttu-id="6468d-123">Nommez le projet ProjectsJSOM, puis choisissez le **bouton OK.**</span><span class="sxs-lookup"><span data-stu-id="6468d-123">Name the project ProjectsJSOM, and then choose the **OK** button.</span></span> 
    
6. <span data-ttu-id="6468d-124">Dans la boîte de dialogue **Assistant Personnalisation de SharePoint**, sélectionnez **déployer en tant qu'une solution de batterie de serveurs**, puis cliquez sur le bouton **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="6468d-124">In the **SharePoint Customization Wizard** dialog box, choose **Deploy as a farm solution**, and then choose the **Finish** button.</span></span> 
    
7. <span data-ttu-id="6468d-125">Modifiez la valeur de la propriété URL du **site** pour le **projet ProjectsJSOM** afin qu’elle corresponde à l’URL de l’instance de Project Web App (par exemple,  `https://ServerName/PWA` ).</span><span class="sxs-lookup"><span data-stu-id="6468d-125">Edit the value of the **Site URL** property for the **ProjectsJSOM** project to match the URL of the Project Web App instance (for example,  `https://ServerName/PWA`).</span></span>
    
### <a name="to-create-the-application-page-in-visual-studio"></a><span data-ttu-id="6468d-126">Pour créer la page d’application dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6468d-126">To create the application page in Visual Studio</span></span>

1. <span data-ttu-id="6468d-127">Dans **l’Explorateur** de solutions, ouvrez le menu raccourci du **projet ProjectsJSOM,** puis ajoutez un dossier « Dispositions » SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6468d-127">In **Solution Explorer**, open the shortcut menu for the **ProjectsJSOM** project, and then add a SharePoint "Layouts" mapped folder.</span></span> 
    
2. <span data-ttu-id="6468d-128">Dans le **dossier Layouts,** ouvrez le menu raccourci du dossier **ProjectsJSOM,** puis ajoutez une nouvelle page d’application SharePoint nommée ProjectsList.aspx.</span><span class="sxs-lookup"><span data-stu-id="6468d-128">In the **Layouts** folder, open the shortcut menu for the **ProjectsJSOM** folder, and then add a new SharePoint application page named ProjectsList.aspx.</span></span>
    
3. <span data-ttu-id="6468d-129">Ouvrez le menu contextuel de la page **ProjectsList.aspx** et choisissez **Définir comme élément de démarrage**.</span><span class="sxs-lookup"><span data-stu-id="6468d-129">Open the shortcut menu for the **ProjectsList.aspx** page and choose **Set as Startup Item**.</span></span>
    
4. <span data-ttu-id="6468d-130">Dans le code de la page **ProjectsList.aspx,** définissez les contrôles d’interface utilisateur à l’intérieur des balises **asp:Content** « Main », comme suit.</span><span class="sxs-lookup"><span data-stu-id="6468d-130">In the markup for the **ProjectsList.aspx** page, define user interface controls inside the "Main" **asp:Content** tags, as follows.</span></span> 
    
   ```HTML
    <table width="100%" id="tblProjects">
        <tr id="headerRow">
            <th width="25%" align="left">Name</th>
            <th width="25%" align="left">Description</th>
            <th width="25%" align="left">Start Date</th>
            <th width="25%" align="left">ID</th>
        </tr>
    </table>
    <textarea id="txtGuid" rows="1" cols="35">Paste the project GUID here.</textarea>
    <button id="btnSend" type="button"></button><br />
    <span id="spanMessage" style="color: #FF0000;"></span>
   ```

   > [!NOTE]
   > <span data-ttu-id="6468d-131">[!REMARQUE] Ces contrôles ne peuvent pas être utilisés dans tous les scénarios.</span><span class="sxs-lookup"><span data-stu-id="6468d-131">These controls may not be used in every scenario.</span></span> <span data-ttu-id="6468d-132">Par exemple, le scénario « Créer des projets » n’utilise pas les contrôles de zone **de texte** **et de** bouton.</span><span class="sxs-lookup"><span data-stu-id="6468d-132">For example, the "Create projects" scenario does not use the **textarea** and **button** controls.</span></span> 
  
5. <span data-ttu-id="6468d-133">Après la balise **span** de fermeture, ajoutez une **balise SharePoint:ScriptLink,** une **balise SharePoint:FormDigest** et des balises **de script,** comme suit.</span><span class="sxs-lookup"><span data-stu-id="6468d-133">After the closing **span** tag, add a **SharePoint:ScriptLink** tag, a **SharePoint:FormDigest** tag, and **script** tags, as follows.</span></span> 
    
   ```HTML
    <SharePoint:ScriptLink id="ScriptLink" name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
    <SharePoint:FormDigest id="FormDigest" runat="server" />
    <script type="text/javascript">
        // Replace this comment with the code for your scenario.
    </script>
   ```

   <span data-ttu-id="6468d-134">La **balise SharePoint:ScriptLink** fait référence au fichier PS.js, qui définit le modèle objet JavaScript pour Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6468d-134">The **SharePoint:ScriptLink** tag references the PS.js file, which defines the JavaScript object model for Project Server 2013.</span></span> <span data-ttu-id="6468d-135">La balise **SharePoint:FormDigest** génère un résumé du message de validation de la sécurité lorsque cela est nécessaire par les opérations qui mettent à jour le contenu du serveur.</span><span class="sxs-lookup"><span data-stu-id="6468d-135">The **SharePoint:FormDigest** tag generates a message digest for security validation when required by operations that update server content.</span></span> 
    
6. <span data-ttu-id="6468d-136">Remplacez le commentaire de l’espace réservé par le code de l’une des procédures suivantes :</span><span class="sxs-lookup"><span data-stu-id="6468d-136">Replace the placeholder comment with the code from one of the following procedures:</span></span>
    
   - [<span data-ttu-id="6468d-137">Créer des projets Project Server 2013 à l’aide du modèle objet JavaScript</span><span class="sxs-lookup"><span data-stu-id="6468d-137">Create Project Server 2013 projects by using the JavaScript object model</span></span>](#pj15_CRUDProjectsJSOM_CreateProjects)
    
   - [<span data-ttu-id="6468d-138">Mettre à jour les projets Project Server 2013 à l’aide du modèle objet JavaScript</span><span class="sxs-lookup"><span data-stu-id="6468d-138">Update Project Server 2013 projects by using the JavaScript object model</span></span>](#pj15_CRUDProjectsJSOM_UpdateProjects)
    
   - [<span data-ttu-id="6468d-139">Supprimer des projets Project Server 2013 à l’aide du modèle objet JavaScript</span><span class="sxs-lookup"><span data-stu-id="6468d-139">Delete Project Server 2013 projects by using the JavaScript object model</span></span>](#pj15_CRUDProjectsJSOM_DeleteProjects)
    
7. <span data-ttu-id="6468d-p104">Pour tester la page d’application, dans la barre de menus, sélectionnez **Déboguer**, puis **Démarrer le débogage**. Si vous êtes invité à modifier le fichier web.config, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="6468d-p104">To test the application page, on the menu bar, choose **Debug**, **Start Debugging**. If you are prompted to modify the web.config file, choose **OK**.</span></span>
    
## <a name="create-project-server-2013-projects-by-using-the-javascript-object-model"></a><span data-ttu-id="6468d-142">Créer des projets Project Server 2013 à l’aide du modèle objet JavaScript</span><span class="sxs-lookup"><span data-stu-id="6468d-142">Create Project Server 2013 projects by using the JavaScript object model</span></span>
<span data-ttu-id="6468d-143"><a name="pj15_CRUDProjectsJSOM_CreateProjects"> </a></span><span class="sxs-lookup"><span data-stu-id="6468d-143"><a name="pj15_CRUDProjectsJSOM_CreateProjects"> </a></span></span>

<span data-ttu-id="6468d-144">La procédure de cette section crée des projets à l’aide du modèle objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6468d-144">The procedure in this section creates projects by using the JavaScript object model.</span></span> <span data-ttu-id="6468d-145">La procédure comprend les étapes de haut niveau suivantes :</span><span class="sxs-lookup"><span data-stu-id="6468d-145">The procedure includes the following high-level steps:</span></span>
  
1. <span data-ttu-id="6468d-146">Obtenir l’instance **ProjectContext** actuelle.</span><span class="sxs-lookup"><span data-stu-id="6468d-146">Get the current **ProjectContext** instance.</span></span> 
    
2. <span data-ttu-id="6468d-147">Créez **un objet ProjectCreationInformation** pour spécifier les propriétés initiales de votre projet.</span><span class="sxs-lookup"><span data-stu-id="6468d-147">Create a **ProjectCreationInformation** object to specify initial properties for your project.</span></span> <span data-ttu-id="6468d-148">Spécifiez la propriété **de nom** requise à l’aide ProjectCreationInformation.set_name fonction. </span><span class="sxs-lookup"><span data-stu-id="6468d-148">Specify the required **name** property by using the **ProjectCreationInformation.set_name** function.</span></span> 
    
3. <span data-ttu-id="6468d-149">Récupérez les projets publiés à partir du serveur à l’aide **ProjectContext.get_projects** fonction.</span><span class="sxs-lookup"><span data-stu-id="6468d-149">Retrieve the published projects from the server by using the **ProjectContext.get_projects** function.</span></span> <span data-ttu-id="6468d-150">La **get_projects** renvoie un **objet ProjectCollection.**</span><span class="sxs-lookup"><span data-stu-id="6468d-150">The **get_projects** function returns a **ProjectCollection** object.</span></span> 
    
4. <span data-ttu-id="6468d-151">Ajoutez le nouveau projet à la collection à l’aide de la fonction **ProjectCollection.add** et en passant l’objet **ProjectCreationInformation.**</span><span class="sxs-lookup"><span data-stu-id="6468d-151">Add the new project to the collection by using the **ProjectCollection.add** function and passing in the **ProjectCreationInformation** object.</span></span> 
    
5. <span data-ttu-id="6468d-152">Mettez à jour la collection à l’aide de la fonction **ProjectCollection.update** et de la fonction **ProjectContext.waitForQueueAsync.**</span><span class="sxs-lookup"><span data-stu-id="6468d-152">Update the collection by using the **ProjectCollection.update** function and the **ProjectContext.waitForQueueAsync** function.</span></span> <span data-ttu-id="6468d-153">La **fonction de** mise à jour renvoie un objet **QueueJob** que vous passez à **waitForQueueAsync**.</span><span class="sxs-lookup"><span data-stu-id="6468d-153">The **update** function returns a **QueueJob** object that you pass to **waitForQueueAsync**.</span></span> <span data-ttu-id="6468d-154">Cet appel publie également le projet.</span><span class="sxs-lookup"><span data-stu-id="6468d-154">This call also publishes the project.</span></span>
    
<span data-ttu-id="6468d-155">Collez le code suivant entre les **balises de script** que vous avez ajoutées dans la page Pour créer l’application dans **Visual Studio** procédure.</span><span class="sxs-lookup"><span data-stu-id="6468d-155">Paste the following code between the **script** tags that you added in the **To create the application page in Visual Studio** procedure.</span></span> 
  
```js
    // Declare a global variable to store the project collection.
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(CreateProject, "PS.js");
    // Add a project the projects collection.
    function CreateProject() {
        
        // Initialize the current client context.
        var projContext = PS.ProjectContext.get_current();
        // Initialize a ProjectCreationInformation object and specify properties
        // for the new project.
        // The Name property is required and must be unique.
        var creationInfo = new PS.ProjectCreationInformation();
        creationInfo.set_name("Test Project 1");
        // Specify optional properties for the new project.
        // If not specified, the Start property uses the current date and the
        // EnterpriseProjectTypeId property uses the default EPT.
        creationInfo.set_description("Created through the JSOM.");
        creationInfo.set_start("2013-10-01 09:00:00.000");
        // Get the projects collection.
        projects = projContext.get_projects();
        // Add the new project to the projects collection.
        projects.add(creationInfo);
        // Add a second project to use in the deleting projects procedure.
        creationInfo.set_name("Test Project 2");
        projects.add(creationInfo);
        // Submit the request to update the collection on the server
        var updateJob = projects.update();
        projContext.waitForQueueAsync(updateJob, 10, GetProjects);
    }
    // Get the projects collection.
    function GetProjects(response) {
        // This call demonstrates that you can get the context from the 
        // ProjectCollection object.
        var projContext = projects.get_context();
        // Register the request for information that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the Name, Description,
        // StartDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, Description, StartDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(IterateThroughProjects, QueryFailed);
    }
    // Iterate through the projects collection.
    function IterateThroughProjects(response) {
        // Get the enumerator and iterate through the collection.
        var enumerator = projects.getEnumerator();
        while (enumerator.moveNext()) {
            var project = enumerator.get_current();
            // Create and populate a row with the values for the project's Name, Description,
            // StartDate, and Id properties.
            var row = tblProjects.insertRow();
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_description();
            row.insertCell().innerText = project.get_startDate();
            row.insertCell().innerText = project.get_id();
        }
        // This scenario does not use the textarea or button controls.
        $get("txtGuid").disabled = true;
        $get("btnSend").disabled = true;
    }
    function QueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
```

## <a name="update-project-server-2013-projects-by-using-the-javascript-object-model"></a><span data-ttu-id="6468d-156">Mettre à jour les projets Project Server 2013 à l’aide du modèle objet JavaScript</span><span class="sxs-lookup"><span data-stu-id="6468d-156">Update Project Server 2013 projects by using the JavaScript object model</span></span>
<span data-ttu-id="6468d-157"><a name="pj15_CRUDProjectsJSOM_UpdateProjects"> </a></span><span class="sxs-lookup"><span data-stu-id="6468d-157"><a name="pj15_CRUDProjectsJSOM_UpdateProjects"> </a></span></span>

<span data-ttu-id="6468d-158">La procédure de cette section met à jour la **propriété startDate** d’un projet à l’aide du modèle objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6468d-158">The procedure in this section updates the **startDate** property of a project by using the JavaScript object model.</span></span> <span data-ttu-id="6468d-159">La procédure comprend les étapes de haut niveau suivantes :</span><span class="sxs-lookup"><span data-stu-id="6468d-159">The procedure includes the following high-level steps:</span></span> 
  
1. <span data-ttu-id="6468d-160">Obtenir l’instance **ProjectContext** actuelle.</span><span class="sxs-lookup"><span data-stu-id="6468d-160">Get the current **ProjectContext** instance.</span></span> 
    
2. <span data-ttu-id="6468d-161">Récupérez les projets publiés à partir du serveur à l’aide **ProjectContext.get_projects** fonction.</span><span class="sxs-lookup"><span data-stu-id="6468d-161">Retrieve the published projects from the server by using the **ProjectContext.get_projects** function.</span></span> <span data-ttu-id="6468d-162">La **get_projects** renvoie un **objet ProjectCollection.**</span><span class="sxs-lookup"><span data-stu-id="6468d-162">The **get_projects** function returns a **ProjectCollection** object.</span></span> 
    
3. <span data-ttu-id="6468d-163">Exécutez la demande sur le serveur à l’aide de la fonction **ProjectContext.load** et **de laProjectContext.executeQueryAsync.**</span><span class="sxs-lookup"><span data-stu-id="6468d-163">Run the request on the server by using the **ProjectContext.load** function and the **ProjectContext.executeQueryAsync** function.</span></span> 
    
4. <span data-ttu-id="6468d-164">Récupérez **un objet PublishedProject** à l’aide de **la fonction ProjectContext.getById.**</span><span class="sxs-lookup"><span data-stu-id="6468d-164">Retrieve a **PublishedProject** object by using the **ProjectContext.getById** function.</span></span> 
    
5. <span data-ttu-id="6468d-165">Consultez le projet cible à l’aide **de la fonction Project.checkOut.**</span><span class="sxs-lookup"><span data-stu-id="6468d-165">Check out the target project by using the **Project.checkOut** function.</span></span> <span data-ttu-id="6468d-166">La **fonction CheckOut** renvoie la version brouillon du projet publié.</span><span class="sxs-lookup"><span data-stu-id="6468d-166">The **checkOut** function returns the draft version of the published project.</span></span> 
    
6. <span data-ttu-id="6468d-167">Modifiez la date de début du projet à l’aide **DraftProject.set_startDate** fonction.</span><span class="sxs-lookup"><span data-stu-id="6468d-167">Change the project's start date by using the **DraftProject.set_startDate** function.</span></span> 
    
7. <span data-ttu-id="6468d-168">Publiez le projet à l’aide de la fonction **DraftProject.publish** et de la fonction **ProjectContext.waitForQueueAsync.**</span><span class="sxs-lookup"><span data-stu-id="6468d-168">Publish the project by using the **DraftProject.publish** function and the **ProjectContext.waitForQueueAsync** function.</span></span> <span data-ttu-id="6468d-169">La **fonction** de publication renvoie un **objet QueueJob** que vous passez à **waitForQueueAsync**.</span><span class="sxs-lookup"><span data-stu-id="6468d-169">The **publish** function returns a **QueueJob** object that you pass to **waitForQueueAsync**.</span></span>
    
<span data-ttu-id="6468d-170">Collez le code suivant entre les **balises de script** que vous avez ajoutées dans la page Pour créer l’application dans **Visual Studio** procédure.</span><span class="sxs-lookup"><span data-stu-id="6468d-170">Paste the following code between the **script** tags that you added in the **To create the application page in Visual Studio** procedure.</span></span> 
  
```js
    // Declare global variables.
    var projContext;
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
    // Get the projects collection.
    function GetProjects() {
        // Initialize the current client context.
        projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request for information that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the Name, Description,
        // StartDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, Description, StartDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(IterateThroughProjects, QueryFailed);
    }
    // Iterate through the projects collection.
    function IterateThroughProjects(response) {
        // Get the enumerator and iterate through the collection.
        var enumerator = projects.getEnumerator();
        while (enumerator.moveNext()) {
            var project = enumerator.get_current();
            // Create and populate a row with the values for the project's Name, Description,
            // StartDate, and Id properties.
            var row = tblProjects.insertRow();
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_description();
            row.insertCell().innerText = project.get_startDate();
            row.insertCell().innerText = project.get_id();
        }
        // Initialize button properties.
        $get("btnSend").onclick = function () { ChangeProject(); };
        $get("btnSend").innerText = "Update";
    }
    // Change the project's start date.
    function ChangeProject() {
        // Get the identifier of the target project.
        var targetGuid = $get("txtGuid").innerText;
        // Get the target project and then check it out. The checkOut function
        // returns the draft version of the project.
        var project = projects.getById(targetGuid);
        var draftProject = project.checkOut();
        // Set the new property value and then publish the project.
        // Specify "true" to also check the project in.
        draftProject.set_startDate("2013-12-31 09:00:00.000");
        var publishJob = draftProject.publish(true);
        // Register the job that you want to run on the server and specify the
        // timeout duration and callback function.
        projContext.waitForQueueAsync(publishJob, 10, QueueJobSent);
    }
    // Print the JobState return code, which gives the status of the queue job.
    function QueueJobSent(response) {
        $get("spanMessage").innerText = 'JobState = ' + response + '. Wait a few seconds, then refresh the page to see your changes.';
    }
    function QueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
```

## <a name="delete-project-server-2013-projects-by-using-the-javascript-object-model"></a><span data-ttu-id="6468d-171">Supprimer des projets Project Server 2013 à l’aide du modèle objet JavaScript</span><span class="sxs-lookup"><span data-stu-id="6468d-171">Delete Project Server 2013 projects by using the JavaScript object model</span></span>
<span data-ttu-id="6468d-172"><a name="pj15_CRUDProjectsJSOM_DeleteProjects"> </a></span><span class="sxs-lookup"><span data-stu-id="6468d-172"><a name="pj15_CRUDProjectsJSOM_DeleteProjects"> </a></span></span>

<span data-ttu-id="6468d-173">La procédure de cette section supprime un projet à l’aide du modèle objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6468d-173">The procedure in this section deletes a project by using the JavaScript object model.</span></span> <span data-ttu-id="6468d-174">La procédure comprend les étapes de haut niveau suivantes :</span><span class="sxs-lookup"><span data-stu-id="6468d-174">The procedure includes the following high-level steps:</span></span>
  
1. <span data-ttu-id="6468d-175">Obtenir l’instance **ProjectContext** actuelle.</span><span class="sxs-lookup"><span data-stu-id="6468d-175">Get the current **ProjectContext** instance.</span></span> 
    
2. <span data-ttu-id="6468d-176">Récupérez les projets publiés à partir du serveur à l’aide **ProjectContext.get_projects** fonction.</span><span class="sxs-lookup"><span data-stu-id="6468d-176">Retrieve the published projects from the server by using the **ProjectContext.get_projects** function.</span></span> <span data-ttu-id="6468d-177">La **get_projects** renvoie un **objet ProjectCollection.**</span><span class="sxs-lookup"><span data-stu-id="6468d-177">The **get_projects** function returns a **ProjectCollection** object.</span></span> 
    
3. <span data-ttu-id="6468d-178">Exécutez la demande sur le serveur à l’aide de la fonction **ProjectContext.load** et **de laProjectContext.executeQueryAsync.**</span><span class="sxs-lookup"><span data-stu-id="6468d-178">Run the request on the server by using the **ProjectContext.load** function and the **ProjectContext.executeQueryAsync** function.</span></span> 
    
4. <span data-ttu-id="6468d-179">Récupérez **un objet PublishedProject** à l’aide de **la fonction ProjectCollection.getById.**</span><span class="sxs-lookup"><span data-stu-id="6468d-179">Retrieve a **PublishedProject** object by using the **ProjectCollection.getById** function.</span></span> 
    
5. <span data-ttu-id="6468d-180">Supprimez le projet en le passant à **la fonction ProjectCollection.remove.**</span><span class="sxs-lookup"><span data-stu-id="6468d-180">Delete the project by passing it to the **ProjectCollection.remove** function.</span></span> 
    
6. <span data-ttu-id="6468d-181">Mettez à jour la collection à l’aide de la fonction **ProjectCollection.update** et de la fonction **ProjectContext.waitForQueueAsync.**</span><span class="sxs-lookup"><span data-stu-id="6468d-181">Update the collection by using the **ProjectCollection.update** function and the **ProjectContext.waitForQueueAsync** function.</span></span> <span data-ttu-id="6468d-182">La **fonction de** mise à jour renvoie un objet **QueueJob** que vous passez à **waitForQueueAsync**.</span><span class="sxs-lookup"><span data-stu-id="6468d-182">The **update** function returns a **QueueJob** object that you pass to **waitForQueueAsync**.</span></span>
    
<span data-ttu-id="6468d-183">Collez le code suivant entre les **balises de script** que vous avez ajoutées dans la page Pour créer l’application dans **Visual Studio** procédure.</span><span class="sxs-lookup"><span data-stu-id="6468d-183">Paste the following code between the **script** tags that you added in the **To create the application page in Visual Studio** procedure.</span></span> 
  
```js
    // Declare global variables.
    var projContext;
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
    // Get the projects collection.
    function GetProjects() {
        // Initialize the current client context.
        projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request for information that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the Name, Description,
        // StartDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, Description, StartDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(IterateThroughProjects, QueryFailed);
    }
    // Iterate through the projects collection.
    function IterateThroughProjects(response) {
        // Get the enumerator and iterate through the collection.
        var enumerator = projects.getEnumerator();
        while (enumerator.moveNext()) {
            var project = enumerator.get_current();
            // Create and populate a row with the values for the project's Name, Description,
            // StartDate, and Id properties.
            var row = tblProjects.insertRow();
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_description();
            row.insertCell().innerText = project.get_startDate();
            row.insertCell().innerText = project.get_id();
        }
        // Initialize button properties.
        $get("btnSend").onclick = function () { DeleteProject(); };
        $get("btnSend").innerText = "Delete";
    }
    // Delete the project.
    function DeleteProject() {
        // Get the identifier of the target project.
        var targetGuid = $get("txtGuid").innerText;
        // Get the target project and then remove it from the collection.
        var project = projects.getById(targetGuid);
        projects.remove(project);
        var removeJob = projects.update();
        // Register the job that you want to run on the server and specify the
        // timeout duration and callback function.
        projContext.waitForQueueAsync(removeJob, 10, QueueJobSent);
    }
    // Print the JobState return code, which gives the status of the queue job.
    function QueueJobSent(response) {
        $get("spanMessage").innerText = 'JobState = ' + response + '. Wait a few seconds, then refresh the page to see your changes.';
    }
    function QueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
```

<span data-ttu-id="6468d-184"><a name="pj15_CRUDProjectsJSOM_AR"> </a></span><span class="sxs-lookup"><span data-stu-id="6468d-184"><a name="pj15_CRUDProjectsJSOM_AR"> </a></span></span>

## <a name="see-also"></a><span data-ttu-id="6468d-185">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6468d-185">See also</span></span>

- [<span data-ttu-id="6468d-186">Tâches de programmation Project</span><span class="sxs-lookup"><span data-stu-id="6468d-186">Project programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="6468d-187">Modèle objet côté client (CSOM) pour Project 2013</span><span class="sxs-lookup"><span data-stu-id="6468d-187">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)
    

