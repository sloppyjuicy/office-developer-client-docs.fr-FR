---
title: Créer, récupérer, mettre à jour et supprimer des projets à l’aide Project JavaScript pour serveur
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 6b690938-05bc-46a3-a40e-30f081403767
description: Obtenir l’instance ProjectContext actuelle ; récupérer et itérer dans la collection de projets publiés sur le serveur ; créer, récupérer, extraire et supprimer un projet à l’aide du modèle objet JavaScript Project Server et modifier les propriétés d’un projet.
ms.openlocfilehash: a66b34529e12f61dcf71aa1e7941310b72f2ebbe
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63369526"
---
# <a name="create-retrieve-update-and-delete-projects-using-project-server-javascript"></a>Créer, récupérer, mettre à jour et supprimer des projets à l’aide Project JavaScript pour serveur

Les scénarios de cet article montrent comment obtenir l’instance **ProjectContext** actuelle ; récupérer et itérer dans la collection de projets publiés sur le serveur ; créer, récupérer, extraire et supprimer un projet à l’aide du modèle objet JavaScript Project Server et modifier les propriétés d’un projet.
  
> [!NOTE]
> Ces scénarios définissent du code personnalisé dans le code d’une page d’application SharePoint, mais n’utilisent pas le fichier code-behind créé par Visual Studio 2012 pour la page.
  
## <a name="prerequisites-for-working-with-project-server-2013-projects-in-the-javascript-object-model"></a>Conditions préalables à l’Project projets Server 2013 dans le modèle objet JavaScript

Pour effectuer les scénarios décrits dans cet article, vous devez installer et configurer les produits suivants :
  
- SharePoint Server 2013
- Project Server 2013
- Visual Studio 2012
- Outils de développement Office pour Visual Studio 2012

Vous devez également être autorisé à déployer l’extension sur SharePoint Server 2013 et à contribuer aux projets.
  
> [!NOTE]
> Ces instructions supposent que vous développez sur l’ordinateur qui exécute Project Server 2013.
  
## <a name="create-the-visual-studio-solution"></a>Créer la solution Visual Studio de projet

<a name="pj15_CRUDProjectsJSOM_Setup"> </a>

Les étapes suivantes créent une solution Visual Studio 2012 contenant un projet SharePoint et une page d’application. La page contient la logique pour travailler avec des projets.
  
### <a name="to-create-the-sharepoint-project-in-visual-studio"></a>Pour créer le projet SharePoint dans Visual Studio

1. Sur l’ordinateur qui exécute Project Server 2013, exécutez Visual Studio 2012 en tant qu’administrateur.

2. On the menu bar, choose **File**, **New**, **Project**.

3. Dans la boîte de dialogue **Nouveau projet**, sélectionnez **.NET Framework 4.5** dans la liste déroulante située en haut de la boîte de dialogue.

4. Dans la **catégorie Office/SharePoint**, choisissez SharePoint **Solutions**, puis choisissez SharePoint **modèle Project 2013**.

5. Nommez le projet ProjectsJSOM, puis choisissez le **bouton OK** .

6. Dans la boîte de dialogue **Assistant Personnalisation de SharePoint**, sélectionnez **déployer en tant qu'une solution de batterie de serveurs**, puis cliquez sur le bouton **Terminer**.

7. Modifiez la valeur de la propriété **URL du site** pour le **projet ProjectsJSOM** afin qu’elle corresponde à l’URL de l’instance Project Web App (par exemple, `https://ServerName/PWA`).

### <a name="to-create-the-application-page-in-visual-studio"></a>Pour créer la page d’application dans Visual Studio

1. Dans **l’Explorateur** de solutions, ouvrez le menu raccourci du projet **ProjectsJSOM**, puis ajoutez SharePoint dossier « Layouts » mappé.

2. Dans le **dossier Layouts**, ouvrez le menu raccourci du dossier **ProjectsJSOM**, puis ajoutez une nouvelle page d’application SharePoint nommée ProjectsList.aspx.

3. Ouvrez le menu contextuel de la page **ProjectsList.aspx** et choisissez **Définir comme élément de démarrage**.

4. Dans le code de la page **ProjectsList.aspx** , définissez les contrôles d’interface utilisateur à l’intérieur des balises **asp:Content** « Main », comme suit.

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
   > [!REMARQUE] Ces contrôles ne peuvent pas être utilisés dans tous les scénarios. Par exemple, le scénario « Créer des projets » n’utilise pas les contrôles **de zone de texte** **et de** bouton.
  
5. Après la balise **span** de fermeture, ajoutez une **balise SharePoint:ScriptLink**, une **balise SharePoint:FormDigest** et des balises **de script**, comme suit.

   ```HTML
    <SharePoint:ScriptLink id="ScriptLink" name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
    <SharePoint:FormDigest id="FormDigest" runat="server" />
    <script type="text/javascript">
        // Replace this comment with the code for your scenario.
    </script>
   ```

   La **balise SharePoint:ScriptLink** fait référence au fichier PS.js, qui définit le modèle objet JavaScript pour Project Server 2013. La balise **SharePoint:FormDigest** génère un résumé du message de validation de la sécurité lorsque cela est nécessaire par les opérations qui mettent à jour le contenu du serveur.

6. Remplacez le commentaire de l’espace réservé par le code de l’une des procédures suivantes :

   - [Créer Project server 2013 à l’aide du modèle objet JavaScript](#pj15_CRUDProjectsJSOM_CreateProjects)

   - [Mettre à Project projets Server 2013 à l’aide du modèle objet JavaScript](#pj15_CRUDProjectsJSOM_UpdateProjects)

   - [Supprimer Project projets Server 2013 à l’aide du modèle objet JavaScript](#pj15_CRUDProjectsJSOM_DeleteProjects)

7. Pour tester la page d’application, dans la barre de menus, sélectionnez **Déboguer**, puis **Démarrer le débogage**. Si vous êtes invité à modifier le fichier web.config, cliquez sur **OK**.

## <a name="create-project-server-2013-projects-by-using-the-javascript-object-model"></a>Créer Project server 2013 à l’aide du modèle objet JavaScript

<a name="pj15_CRUDProjectsJSOM_CreateProjects"> </a>

La procédure de cette section crée des projets à l’aide du modèle objet JavaScript. La procédure comprend les étapes de haut niveau suivantes :
  
1. Obtenir l’instance **ProjectContext** actuelle.

2. Créez **un objet ProjectCreationInformation** pour spécifier les propriétés initiales de votre projet. Spécifiez la propriété **de nom** requise à **l’aide ProjectCreationInformation.set_name** fonction.

3. Récupérez les projets publiés à partir du serveur à l’aide **ProjectContext.get_projects** fonction. La **get_projects** renvoie un **objet ProjectCollection** .

4. Ajoutez le nouveau projet à la collection à l’aide de la fonction **ProjectCollection.add** et en passant l’objet **ProjectCreationInformation** .

5. Mettez à jour la collection à l’aide de **la fonction ProjectCollection.update** et de **la fonction ProjectContext.waitForQueueAsync** . La **fonction de** mise à jour renvoie un **objet QueueJob** que vous passez à **waitForQueueAsync**. Cet appel publie également le projet.

Collez le code suivant entre les **balises de script** que vous avez ajoutées dans la page Pour créer **l’application dans Visual Studio** procédure.
  
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

## <a name="update-project-server-2013-projects-by-using-the-javascript-object-model"></a>Mettre à Project projets Server 2013 à l’aide du modèle objet JavaScript

<a name="pj15_CRUDProjectsJSOM_UpdateProjects"> </a>

La procédure de cette section met à jour la **propriété startDate** d’un projet à l’aide du modèle objet JavaScript. La procédure comprend les étapes de haut niveau suivantes :
  
1. Obtenir l’instance **ProjectContext** actuelle.

2. Récupérez les projets publiés à partir du serveur à l’aide **ProjectContext.get_projects** fonction. La **get_projects** renvoie un **objet ProjectCollection** .

3. Exécutez la demande sur le serveur à l’aide de **la fonction ProjectContext.load** et de la fonction **ProjectContext.executeQueryAsync** .

4. Récupérez **un objet PublishedProject** à l’aide de **la fonction ProjectContext.getById** .

5. Consultez le projet cible à l’aide **Project.checkOut**. La **fonction CheckOut** renvoie la version brouillon du projet publié.

6. Modifiez la date de début du projet à l’aide **DraftProject.set_startDate fonction** .

7. Publiez le projet à l’aide de **la fonction DraftProject.publish** et de **la fonction ProjectContext.waitForQueueAsync** . La **fonction** de publication renvoie un **objet QueueJob** que vous passez à **waitForQueueAsync**.

Collez le code suivant entre les **balises de script** que vous avez ajoutées dans la page Pour créer **l’application dans Visual Studio** procédure.
  
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

## <a name="delete-project-server-2013-projects-by-using-the-javascript-object-model"></a>Supprimer Project projets Server 2013 à l’aide du modèle objet JavaScript

<a name="pj15_CRUDProjectsJSOM_DeleteProjects"> </a>

La procédure de cette section supprime un projet à l’aide du modèle objet JavaScript. La procédure comprend les étapes de haut niveau suivantes :
  
1. Obtenir l’instance **ProjectContext** actuelle.

2. Récupérez les projets publiés à partir du serveur à l’aide **ProjectContext.get_projects** fonction. La **get_projects** renvoie un **objet ProjectCollection** .

3. Exécutez la demande sur le serveur à l’aide de **la fonction ProjectContext.load** et de la fonction **ProjectContext.executeQueryAsync** .

4. Récupérez **un objet PublishedProject** à l’aide de **la fonction ProjectCollection.getById** .

5. Supprimez le projet en le passant à **la fonction ProjectCollection.remove** .

6. Mettez à jour la collection à l’aide de **la fonction ProjectCollection.update** et de **la fonction ProjectContext.waitForQueueAsync** . La **fonction de** mise à jour renvoie un **objet QueueJob** que vous passez à **waitForQueueAsync**.

Collez le code suivant entre les **balises de script** que vous avez ajoutées dans la page Pour créer **l’application dans Visual Studio** procédure.
  
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

- [Tâches de programmation Project](project-programming-tasks.md)
- [Modèle objet côté client (CSOM) pour Project 2013](client-side-object-model-csom-for-project-2013.md)
