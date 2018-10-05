---
title: Développement d’un complément Project Online à l’aide du modèle objet JavaScript (JSOM)
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4a4b1ad2-de46-421d-a698-53c20c90b93a
description: Cet article décrit le complément Microsoft Project Online développement afin d’améliorer votre expérience avec Project Online. Le projet de développement est implémenté comme une procédure pas à pas. Le complément utilisé pour cet article lit et affiche les noms de projet et les ID des projets publiés à partir de votre compte Project Online et vous permet d’atteindre de récupérer les tâches associées à des projets individuels.
ms.openlocfilehash: 0a472a6300f18aaa65649f44d944445642a59e1a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399304"
---
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a>Développement d’un complément Project Online à l’aide du modèle objet JavaScript (JSOM)

Cet article décrit le complément Microsoft Project Online développement afin d’améliorer votre expérience avec Project Online. Le projet de développement est implémenté comme une procédure pas à pas. Le complément utilisé pour cet article lit et affiche les noms de projet et les ID des projets publiés à partir de votre compte Project Online et vous permet d’atteindre de récupérer les tâches associées à des projets individuels.
  
Au moment de l’exécution, la liste de compléments ressemble à l’illustration suivante :
  
![Capture d’écran montrant une liste de tâches et des projets JSOM] (media/766e5914-f048-48f4-9282-291f55e6e90d.png "Capture d’écran montrant une liste de tâches et des projets JSOM")
  
L’objectif de l’exemple est l’interaction avec le Project Online, rendant des requêtes et en définissant le contexte de chaque demande à partir du service. Des éléments de l’interface utilisateur d’une attention minimal. Au lieu de cela, les listes source fournissent des commentaires relatifs à l’interface utilisateur.
  
> [!NOTE]
> Les fichiers source pour le complément logiciel exemple, un projet Visual Studio, sont disponibles à : https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks..... Conserver les fichiers source pratique comme référence pendant la lecture de l’article, comme chacun vient s’ajouter à l’autre. Les fichiers dans Visual Studio project build et peuvent être exécutées avec peu de modifications, en remplaçant l’URL de votre client Project Online jusqu’au dossier PWA. 
  
## <a name="background"></a>Arrière-plan

Project Online est un service d’Office 365 qui permet aux entreprises une solution project management office (PMO) pour coordonner et gérer des portefeuilles, programmes et projets et de gestion de portefeuille de projets (PPM). Project Online est une offre différente versions de bureau de projet ; encore, Project Online toujours contient les fonctionnalités pour mettre à jour et suivre les détails du projet dans toute la durée de vie d’un projet. Project Online repose sur SharePoint Online.
  
Un complément Project Online hébergé se compose des fichiers JavaScript et des ressources qui interagissent avec l’API côté Client-modèle objet. Lorsque l’utilisateur visite la macro complémentaire, le JavaScript et les ressources sont téléchargés et exécutées dans le navigateur. Le complément effectue des appels asynchrones vers Project Online pour interagir avec le service, si la création, la récupération, mise à jour ou suppression de données. 
  
Project Online effectue une action supplémentaire pour protéger les informations appartenant à d’autres clients à partir de la macro complémentaire ; à savoir, Project Online crée un site isolé pour interagir avec les demandes à partir de la macro complémentaire. Pas de code personnalisé s’exécute sur l’hôte de Project Online. 
  
Le paramétrage de développement pour Project Online compléments utilise le type de projet Visual Studio SharePoint Add-in. Le complément est écrit en JavaScript et utilise le modèle d’objet Project JavaScript (JSOM) pour interagir avec le service de Project Online. Le JSOM hérite la plupart de ses fonctionnalités du JSOM SharePoint.
  
> [!NOTE]
> Compléments peuvent être publiés et vendus dans l’Office Store ou déployés dans un catalogue d’applications privé sur SharePoint. Pour plus d’informations, voir [déployer et publier votre complément Office](https://docs.microsoft.com/office/dev/add-ins/publish/publish).
> 
> Le complément utilisé dans cet article est un exemple pour les développeurs ; elle n’est pas destinée à utiliser dans un environnement de production. Le principal objectif consiste à afficher un exemple de développement d’applications pour Project Online. 
  
## <a name="prerequisites"></a>Conditions préalables

Dans un environnement Windows pris en charge, ajoutez les éléments suivants :
  
- **.NET framework 4.0 ou version ultérieure**: les versions complètes de l’infrastructure de la version 4.0 sont compatibles. Le site de téléchargement est https://msdn.microsoft.com/vstudio/aa496123.aspx.
    
- **Visual Studio 2013 ou version ultérieure**:  
    
   - L’édition professionnelle de Visual Studio 2015 est prête à commencer la mise à l’emploi et est disponible à l’adresse https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx.
    
   - L’édition de la Communauté de Visual Studio 2015 est disponible à l’adresse https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx. Cette édition nécessite une installation manuelle des outils de développement Microsoft Office pour Visual Studio.
    
   Les outils de développement Microsoft Office pour Visual Studio sont disponibles sur https://www.visualstudio.com/en-us/features/office-tools-vs.aspx.
    
- **Compte A Project Online**: Cela permet d’accéder au service d’hébergement. Pour plus d’informations sur l’obtention d’un compte Project Online, voir https://products.office.com/en-us/Project/project-online-portfolio-management.
    
   Assurez-vous que l’utilisateur dispose d’autorisations suffisantes pour accéder à des projets dans le client Project Online. 
    
- **Projets sur le site d’hébergement** sont remplies avec les informations.
    
> [!NOTE]
> La norme .NET Framework est l’infrastructure correcte à utiliser. N’utilisez pas le « .NET Framework 4 Client Profile ». 
  
### <a name="set-up-the-visual-studio-project"></a>Configurer le projet Visual Studio

Configuration de l’application se compose de création d’un nouveau projet, lier les bibliothèques appropriées et déclarer les espaces de noms nécessaires. Visual Studio présente plusieurs types de projets de développement. La section est brève et très simple. La valeur a les informations est fusionné dans un seul endroit.
  
#### <a name="select-a-visual-studio-project"></a>Sélectionnez le projet Visual Studio

Pour créer un projet de type approprié pour le complément, vous devez effectuer les étapes suivantes. Mots clés rencontrés dans l’écran ont un attribut **gras** : 
  
1. Dans le menu fichier, choisissez **fichier** > **New** > **Project**. 
    
2. À partir des modèles installés dans le volet gauche, sélectionnez **c#** > **Office/SharePoint** > **Web Add-ins**. 
    
3. En haut du volet central, sélectionnez **.NET Framework 4** ou version ultérieure ; la version actuelle est 4.6. 
    
4. Les types d’application dans le volet central, choisissez **Ajouter dans SharePoint**. 
    
5. Dans la section inférieure, spécifiez un nom et un emplacement pour le projet et un nom de solution. 
    
6. Également dans la section inférieure, cochez la case de **créer le répertoire pour la solution** . 
    
7. Cliquez sur **OK** pour créer le projet initial. 
    
L’Assistant Visual Studio demande quelques questions de suivi sur le site de paramètres Project Online (appelé SharePoint paramètres dans les boîtes de dialogue) dans les deux boîtes de dialogue qui suivent. Voici les questions :
  
1. Quel site SharePoint que vous souhaitez utiliser pour le débogage de votre complément ? Spécifier l’URL de votre site PWA, tel que https://contoso.sharepoint.com/sites/pwa.
    
2. Comment voulez-vous héberger votre Add-in SharePoint ? Sélectionnez [X] **hébergée par SharePoint**.
    
   Pour plus d’informations sur les compléments SharePoint, y compris les options d’hébergement, voir [SharePoint Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins).
    
3. Cliquez sur **Suivant**. 
    
La seconde boîte de dialogue supplémentaire vous invite à spécifier la version de SharePoint Online pour le complément : 
  
1. Qu’est la version la plus ancienne de SharePoint que vous souhaitez votre complément à cibler ? Sélectionnez [X] S **HarePoint-en ligne**. 
    
2. Cliquez sur **Terminer**. 
    
Visual Studio crée le projet et accède au site de projet en ligne. 
  
### <a name="enable-sideloading-on-the-project-online-site"></a>Activer le chargement de version test sur le site Project Online

Chargement de version test est le mécanisme pour tester et déboguer des compléments Project Online. Deux scripts sont nécessaires pour le chargement de version test : un pour activer le chargement de version test sur votre site Project Online et un autre pour désactiver le chargement de version test une fois que vous avez terminé de tester et déboguer l’application add-in.
  
Pour plus d’informations sur la configuration de chargement de version test, voir [Activer l’application de chargement de version test dans votre collection de sites non-développeurs](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/).
  
> [!NOTE]
> Applications de chargement de version test est une fonctionnalité de développement/test. Il est **pas destiné à l’utilisation de production**. Ne pas sideload applications régulièrement, ou conservez le chargement de version test application activée pendant plus de vous sont activement à l’aide de la fonctionnalité. 
  
## <a name="add-content-to-the-add-in-project"></a>Ajouter du contenu dans le projet de complément

Après avoir créé un projet et configurer le mécanisme de débogage, l’ajout de contenu à l’application comprend les tâches suivantes :
  
- Définition de l’étendue d’application
    
- Liaison de la bibliothèque JSOM
    
- Ajout d’éléments d’interface utilisateur pour le complément
    
- L’initialisation et connexion au service Project Online
    
- Récupération des projets et les propriétés des détails
    
- Affichage de projets
    
- Affichage des tâches pour un projet
    
Le projet de complément se compose de plusieurs fichiers. Dans cet exemple, vous devrez modifier les fichiers suivants : 
  
- Fichier AppManifest.xml
    
- Default.aspx
    
- App.js
    
- App.CSS - facultatif ; contient des définitions de style développées pour le complément
    
Si le client Project Online change, telles que le déplacement d’une version d’évaluation vers un site d’abonnement, vous pouvez mettre à jour les propriétés du projet, y compris la connexion au serveur et l’URL du Site, à l’aide de la fenêtre Propriétés disponibles par le biais de l' **affichage** > **Propriétés Fenêtre** commande. 
  
Vous pouvez également ajouter des fichiers au projet. Dans ce cas, vous devrez mettre à jour le fichier Elements.xml situé dans le même groupe (contenu, Images, Pages ou Scripts) pour inclure les nouveaux fichiers. Pour plus d’informations sur les fichiers de projet, voir [Explorer la structure de manifeste d’application et le package d’un complément SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in).
  
### <a name="set-application-scope"></a>Étendue d’application Set

Le complément a besoin de niveaux de portée ou d’autorisation définis avant le service retourne des informations dans les résultats de la requête. Pour ce complément, utilisez l’étendue suivante au projet Visual Studio. Cette modification est apportée au fichier AppManifest.xml dans l’onglet autorisations :

|Domaine d’application|Autorisation|
|:-----|:-----|
|Plusieurs projets (Project Server)  <br/> |Read  <br/> |
   
Enregistrez le fichier après la définition de l’étendue de l’application. Dans le cas contraire, aucune donnée n’est renvoyées depuis le service. 
  
### <a name="link-the-jsom-library"></a>Lier la bibliothèque JSOM

Les bibliothèques de Project Online runtime, PS.js et PS.debug.js, sont fournis par Project Online et sont toujours la version la plus récente. Compléments JavaScript qui utilisent le JSOM doivent être liée à une de ces bibliothèques. Les définitions de liaison sont ajoutées dans le fichier Default.aspx. Les commandes à utiliser le PS.js et/ou PS.debug.js font partie du code situé dans le fichier App.js.
  
Ajoutez la commande suivante pour la définition de PS.js ou PS.debug.js dans les `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` élément suivant « SharePoint:ScriptLink » pour sp.js. 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> L’attribut **à la demande** pour PS.js ou PS.debug.js défini sur **false**. 
  
### <a name="add-ui-elements-to-the-add-in"></a>Ajouter des éléments d’interface utilisateur pour le complément

L’exemple complément se compose de certains composants. Description des éléments statiques se trouvent dans le fichier Default.aspx. Descriptions des éléments dynamiques et code pour tous les composants se trouvent dans le fichier App.js. Pour les commentaires concernant les composants, consultez les exemples de code source. Voici une liste des composants de l’interface utilisateur dans le complément :
  
- Title
    
- Formulation de présentation
    
- Pour supprimer des tâches à partir de la table
    
- Tableau qui répertorie les informations sur la tâche et nom et l’ID du projet.
    
- Bouton (cloné en une seule fois pour chaque projet) qui importe les données de tâche dans le tableau des tâches.
    
Pour plus d’informations de l’interface utilisateur, telles que le titre et l’en-tête de la table de projet, consultez le fichier de projet Default.aspx.
  
### <a name="initialize-and-connect-to-the-host-system"></a>Initialiser et se connecter au système hôte

Le fichier App.js contient le code JavaScript. Le complément PS.js est chargé dans le navigateur, puis appelle la fonction initializePage. InitializePage récupère un contexte au point de terminaison Project Online et démarre la fonction loadProjects.
  
```js
    'use strict';
    SP.SOD.executeOrDelayUntilScriptLoaded(initializePage, "PS.js");
    //Project PWA Context and published projects in PWA
    var projContext;
    var projects;
    function initializePage() {
        //Get the Project context for this web
        projContext = PS.ProjectContext.get_current();
        loadProjects();
    }
    //General CSOM failure event handler
    //Invoked when ExecuteQueryAsync returns unsuccessfully
    function onRequestFailed(sender, args) {
        alert("Failed to execute: " + args.get_message());
        return;
    };

```

### <a name="retrieve-the-projects"></a>Récupérer les projets

La fonction loadProjects demande au service de l’ID et noms de projets. 
  
L’application extrait le nom du projet et le projet de code. Autres informations sur le projet est disponibles et est accessible en modifiant la méthode load pour identifier explicitement les propriétés à récupérer. Un exemple est fourni dans le code comme un commentaire. 
  
Si la requête aboutit, le complément se poursuit en appelant displayProjects. 
  
```js
    //Query CSOM and get the list of projects in PWA
    function loadProjects() {
        projects = projContext.get_projects();
    //Request to server - identifies what to retrieve
        projContext.load(projects, 'Include(Name, Id)');
        //Notice to server to execute query
        projContext.executeQueryAsync(displayProjects, onRequestFailed);
        // Syntax for requesting more fields to pull down from server
        // projContext.load(projects, 'Include(Name, Description, StartDate, 
        // Id, IsCheckedOut)');
    }

```

### <a name="display-the-projects"></a>Afficher les projets

La fonction displayProjects crée une table, une ligne par projet et un bouton pour afficher les tâches du projet spécifique. 
  
```js
    //Display the projects with names and ids in a table
    function displayProjects() {
        //Current published project and ID
        var p, projId;
        //Project table rows to publish collectively
        var pTable = []; 
        var pEnum = projects.getEnumerator();
        //Build a 3-column table, with one project per row.
        while (pEnum.moveNext()) {
            p = pEnum.get_current();
        
            //Items used in getting information for table rows:
            //Current published project object, and ID and name
            // var project = p;
            // var projId = p.get_id();
            // var projName = p.get_name();
        
            //Continue processing/working with project object as needed.
        }
    }

```

> [!NOTE]
> La boucle while accède à l’ID et des propriétés de nom. Il s’agit légèrement différent de celui du projet de code source qui appelle une fonction qui, à son tour, accède aux propriétés de la même. 
  
### <a name="display-the-tasks-for-a-project"></a>Afficher les tâches pour un projet

Les tâches, lors de la partie de la macro complémentaire, ne font pas partie du chargement initial. Si l’utilisateur est intéressée par les tâches associées à un projet, cliquez sur le bouton « Afficher les tâches » entraîne les tâches à afficher dans la liste en utilisant le Gestionnaire d’événements btnLoadTasks. 
  
Le Gestionnaire d’événements btnLoadTasks, avec l’ID de projet approprié, demande les tâches pour le projet spécifié à partir du serveur. Une fois récupéré, btnLoadTasks transmet la liste des tâches à displayTasks pour présenter les tâches à l’écran.
  
```js
    //Query CSOM and get the list of tasks for a specific project
    function btnLoadTasks(pid) {
        //Event handler for the "Show tasks" buttons. 
        //
        //The project ID is the sole argument and is used to get the appropriate task 
        //info from the service.
        //The project ID is also the button name, and is used to identify where to place
        //the task information in the table.
        //
        //Project ID to pass to the event handler
        var projId = pid;
        //
        //Get the project reference
        var pProj = projects.getById(projId);
        //
        //Get the tasks collection reference associated with the project.
        var tasks = pProj.get_tasks();
        //
        projContext.load(tasks, 'Include(Id, Name, Start, ScheduledStart, Completion)');
        //
        //If the query succeeds, displayTasks presents the tasks to the user.
        projContext.executeQueryAsync(function () { displayTasks(tasks, projId) }, onRequestFailed);
    }

```

La fonction displayTasks affiche les tâches associées à un projet spécifié immédiatement après l’écriture du projet.
  
```js
    //Insert tasks for the specified project immediately underneath the project entry 
    //in the table.
    function displayTasks(tasks, projId) {
        //selected project ID
        var pId = projId;
        //individual task
        var t;
        //Task table rows to publish collectively
        var tTable = [];
        var tEnum = tasks.getEnumerator();
        //Build table one task per row.
        while (tEnum.moveNext()) {
            t = tEnum.get_current();
            //
            //Items used in getting information for table rows:
            //Current task object, and ID and name
            // var task = t;
            // var taskId = t.get_id();
            // var taskName = t.get_name();
            
            //Continue processing/working with task object as needed.
        }
    }

```

> [!NOTE]
> La boucle while accède à l’ID de tâche et les propriétés de nom. Il s’agit légèrement différent de celui du projet de code source qui appelle une fonction qui, à son tour, accède aux propriétés de la même. 
  
Exemple de sortie pour les tâches d’un projet unique suit.
  
![Capture d’écran montrant la sortie d’une tâche de projet] (media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Capture d’écran montrant la sortie d’une tâche de projet")
  
## <a name="see-also"></a>Voir aussi

Pour la documentation et des exemples relatifs à Project Online et développement d’applications à l’aide de CSOM, voir le [Portail de développement Project](https://developer.microsoft.com/en-us/project).
    


