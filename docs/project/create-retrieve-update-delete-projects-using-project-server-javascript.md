---
title: Créer, extraire, mettre à jour et supprimer des projets à l’aide de Project Server JavaScript
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6b690938-05bc-46a3-a40e-30f081403767
description: Obtenir de l’instance actuelle de ProjectContext ; récupérer et parcourir la collection de projets publiés sur le serveur ; créer, récupérer, extraire et supprimer un projet à l’aide du modèle objet de Project Server JavaScript ; et modifier les propriétés d’un projet.
ms.openlocfilehash: 966c1298d210cb608001e4ce2b390611a75bdb24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787791"
---
# <a name="create-retrieve-update-and-delete-projects-using-project-server-javascript"></a>Créer, extraire, mettre à jour et supprimer des projets à l’aide de Project Server JavaScript

Les scénarios de cet article indiquent comment obtenir l’instance actuelle de **ProjectContext** ; récupérer et parcourir la collection de projets publiés sur le serveur ; créer, récupérer, extraire et supprimer un projet à l’aide du modèle objet de Project Server JavaScript ; et modifier les propriétés d’un projet. 
  
> [!NOTE]
> Ces scénarios définissent le code personnalisé dans le balisage d’une page d’application SharePoint, mais n’utilisent pas le fichier code-behind qui crée de Visual Studio 2012 pour la page. 
  
## <a name="prerequisites-for-working-with-project-server-2013-projects-in-the-javascript-object-model"></a>Conditions requises pour l’utilisation de projets de Project Server 2013 dans le modèle objet JavaScript

Pour effectuer les scénarios décrits dans cet article, vous devez installer et configurer les produits suivants :
  
- SharePoint Server 2013
- Project Server 2013
- Visual Studio 2012
- Outils de développement Office pour Visual Studio 2012
    
Vous devez également disposer des autorisations pour déployer l’extension vers SharePoint Server 2013 et de contribuer aux projets.
  
> [!NOTE]
> Ces instructions supposent que vous développez sur l’ordinateur qui exécute Project Server 2013. 
  
## <a name="create-the-visual-studio-solution"></a>Créer la solution Visual Studio
<a name="pj15_CRUDProjectsJSOM_Setup"> </a>

Les étapes suivantes créent une solution Visual Studio 2012 qui contient un projet SharePoint et une page d’application. La page contient la logique de l’utilisation de projets.
  
### <a name="to-create-the-sharepoint-project-in-visual-studio"></a>Pour créer le projet SharePoint dans Visual Studio

1. Sur l’ordinateur qui exécute Project Server 2013, exécutez Visual Studio 2012 en tant qu’administrateur.
    
2. On the menu bar, choose **File**, **New**, **Project**.
    
3. Dans la boîte de dialogue **Nouveau projet**, sélectionnez **.NET Framework 4.5** dans la liste déroulante située en haut de la boîte de dialogue. 
    
4. Dans la catégorie de modèle **Office/SharePoint** , sélectionnez **Solutions SharePoint**, puis choisissez le modèle de **Projet SharePoint 2013** . 
    
5. Nommez le projet ProjectsJSOM, puis cliquez sur le bouton **OK** . 
    
6. Dans la boîte de dialogue **Assistant Personnalisation de SharePoint**, sélectionnez **déployer en tant qu'une solution de batterie de serveurs**, puis cliquez sur le bouton **Terminer**. 
    
7. Modifier la valeur de la propriété **URL du Site** pour le projet **ProjectsJSOM** correspondre à l’URL de l’instance Project Web App (par exemple, `http://ServerName/PWA`).
    
### <a name="to-create-the-application-page-in-visual-studio"></a>Pour créer la page d’application dans Visual Studio

1. Dans **L’Explorateur de solutions**, ouvrez le menu contextuel du projet **ProjectsJSOM** , puis ajoutez un SharePoint dossier mappé « Dispositions ». 
    
2. Dans le dossier **dispositions** , ouvrez le menu contextuel pour le dossier **ProjectsJSOM** , puis ajoutez une nouvelle page d’application SharePoint nommée ProjectsList.aspx.
    
3. Ouvrez le menu contextuel de la page **ProjectsList.aspx** et sélectionnez **définir comme élément de démarrage**.
    
4. Dans le balisage de la page **ProjectsList.aspx** , définissez les contrôles d’interface utilisateur dans les balises **Asp : contenu** « Main », comme suit. 
    
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
   > Ces contrôles ne peuvent pas être utilisés dans tous les scénarios. Par exemple, le scénario « Créer des projets » n’utilise pas les contrôles de **bouton** de **textarea** . 
  
5. Après la fermeture **de couvrir** , ajoutez une balise **SharePoint:ScriptLink** , une balise **SharePoint:FormDigest** et balises **script** , comme suit. 
    
   ```HTML
    <SharePoint:ScriptLink id="ScriptLink" name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
    <SharePoint:FormDigest id="FormDigest" runat="server" />
    <script type="text/javascript">
        // Replace this comment with the code for your scenario.
    </script>
   ```

   La balise **SharePoint:ScriptLink** fait référence au fichier de PS.js, qui définit le modèle objet JavaScript pour Project Server 2013. La balise **SharePoint:FormDigest** génère un résumé de message pour la validation de la sécurité nécessaire par les opérations de mise à jour du contenu du serveur. 
    
6. Remplacez le commentaire de l’espace réservé par le code à partir d’une des procédures suivantes :
    
   - [Créer des projets de Project Server 2013 à l’aide du modèle objet JavaScript](#pj15_CRUDProjectsJSOM_CreateProjects)
    
   - [Mettre à jour des projets de Project Server 2013 à l’aide du modèle objet JavaScript](#pj15_CRUDProjectsJSOM_UpdateProjects)
    
   - [Supprimer des projets de Project Server 2013 à l’aide du modèle objet JavaScript](#pj15_CRUDProjectsJSOM_DeleteProjects)
    
7. Pour tester la page applications, dans la barre de menus, choisissez **débogage**, **Démarrer le débogage**. Si vous êtes invité à modifier le fichier web.config, cliquez sur **OK**.
    
## <a name="create-project-server-2013-projects-by-using-the-javascript-object-model"></a>Créer des projets de Project Server 2013 à l’aide du modèle objet JavaScript
<a name="pj15_CRUDProjectsJSOM_CreateProjects"> </a>

La procédure décrite dans cette section crée des projets à l’aide du modèle objet JavaScript. La procédure comprend les étapes suivantes :
  
1. Obtenir l’instance actuelle de **ProjectContext** . 
    
2. Créer un objet **ProjectCreationInformation** pour spécifier les propriétés initiales pour votre projet. Spécifiez la propriété de **nom** à l’aide de la fonction **ProjectCreationInformation.set_name** . 
    
3. Récupérer les projets publiés à partir du serveur à l’aide de la fonction **ProjectContext.get_projects** . La fonction **get_projects** renvoie un objet **ProjectCollection** . 
    
4. Ajouter le nouveau projet à la collection à l’aide de la fonction **ProjectCollection.add** et en transmettant l’objet **ProjectCreationInformation** . 
    
5. Mise à jour de la collection à l’aide de la fonction **ProjectCollection.update** et la fonction **ProjectContext.waitForQueueAsync** . La fonction **mettre à jour** renvoie un objet **QueueJob** que vous passez à **waitForQueueAsync**. Cet appel publie également le projet.
    
Collez le code suivant entre les balises de **script** que vous avez ajoutée dans la procédure **pour créer la page d’application dans Visual Studio** . 
  
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

## <a name="update-project-server-2013-projects-by-using-the-javascript-object-model"></a>Mettre à jour des projets de Project Server 2013 à l’aide du modèle objet JavaScript
<a name="pj15_CRUDProjectsJSOM_UpdateProjects"> </a>

La procédure décrite dans cette section met à jour la propriété **date de début** d’un projet à l’aide du modèle objet JavaScript. La procédure comprend les étapes suivantes : 
  
1. Obtenir l’instance actuelle de **ProjectContext** . 
    
2. Récupérer les projets publiés à partir du serveur à l’aide de la fonction **ProjectContext.get_projects** . La fonction **get_projects** renvoie un objet **ProjectCollection** . 
    
3. Exécutez la requête sur le serveur à l’aide de la fonction **ProjectContext.load** et la fonction **ProjectContext.executeQueryAsync** . 
    
4. Récupérer un objet **PublishedProject** à l’aide de la fonction **ProjectContext.getById** . 
    
5. Extraire le projet cible à l’aide de la fonction **Project.checkOut** . La fonction **extraction** renvoie l’ébauche de version du projet publié. 
    
6. Modifier la date de début du projet à l’aide de la fonction **DraftProject.set_startDate** . 
    
7. Publier le projet à l’aide de la fonction **DraftProject.publish** et la fonction **ProjectContext.waitForQueueAsync** . La fonction **Publier** renvoie un objet **QueueJob** que vous passez à **waitForQueueAsync**.
    
Collez le code suivant entre les balises de **script** que vous avez ajoutée dans la procédure **pour créer la page d’application dans Visual Studio** . 
  
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

## <a name="delete-project-server-2013-projects-by-using-the-javascript-object-model"></a>Supprimer des projets de Project Server 2013 à l’aide du modèle objet JavaScript
<a name="pj15_CRUDProjectsJSOM_DeleteProjects"> </a>

La procédure décrite dans cette section supprime un projet à l’aide du modèle objet JavaScript. La procédure comprend les étapes suivantes :
  
1. Obtenir l’instance actuelle de **ProjectContext** . 
    
2. Récupérer les projets publiés à partir du serveur à l’aide de la fonction **ProjectContext.get_projects** . La fonction **get_projects** renvoie un objet **ProjectCollection** . 
    
3. Exécutez la requête sur le serveur à l’aide de la fonction **ProjectContext.load** et la fonction **ProjectContext.executeQueryAsync** . 
    
4. Récupérer un objet **PublishedProject** à l’aide de la fonction **ProjectCollection.getById** . 
    
5. Supprimer le projet à transmettre à la fonction **ProjectCollection.remove** . 
    
6. Mise à jour de la collection à l’aide de la fonction **ProjectCollection.update** et la fonction **ProjectContext.waitForQueueAsync** . La fonction **mettre à jour** renvoie un objet **QueueJob** que vous passez à **waitForQueueAsync**.
    
Collez le code suivant entre les balises de **script** que vous avez ajoutée dans la procédure **pour créer la page d’application dans Visual Studio** . 
  
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

<a name="pj15_CRUDProjectsJSOM_AR"> </a>

## <a name="see-also"></a>Voir aussi

- [Tâches de programmation du projet](project-programming-tasks.md)
- [Modèle objet côté client (CSOM) pour Project 2013](client-side-object-model-csom-for-project-2013.md)
    

