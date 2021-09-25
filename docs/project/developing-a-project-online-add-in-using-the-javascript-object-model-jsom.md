---
title: Développement d’Project Online à l’aide du modèle objet JavaScript (JSOM)
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 4a4b1ad2-de46-421d-a698-53c20c90b93a
description: Cet article décrit Microsoft Project Online développement de Project Online. Le projet de développement est implémenté comme une walkthrough. Le add-in utilisé pour cet article lit et affiche les noms de projet et les ID des projets publiés à partir de votre compte Project Online et vous permet d’extraire les tâches associées à des projets individuels.
ms.openlocfilehash: b30350a0d78531e304545e551ff61257e52386e8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560220"
---
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a>Développement d’Project Online à l’aide du modèle objet JavaScript (JSOM)

Cet article décrit Microsoft Project Online développement de Project Online. Le projet de développement est implémenté comme une walkthrough. Le add-in utilisé pour cet article lit et affiche les noms de projet et les ID des projets publiés à partir de votre compte Project Online et vous permet d’extraire les tâches associées à des projets individuels.
  
Au moment de l’exécuter, la liste des modules de recherche ressemble à l’illustration suivante :
  
![Capture d’écran montrant une liste de tâches et projets JSOM](media/766e5914-f048-48f4-9282-291f55e6e90d.png "Capture d’écran montrant une liste de tâches et projets JSOM")
  
L’objectif de l’exemple est l’interaction avec le Project Online, l’établissement de requêtes et la définition du contexte pour chaque demande à partir du service. Les éléments d’interface utilisateur (IU) reçoivent une attention minimale. Au lieu de cela, les listes source fournissent des commentaires concernant l’interface utilisateur.
  
> [!NOTE]
> Les fichiers sources de l’exemple de Visual Studio, un projet de projet, sont disponibles à l’Visual Studio https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks.... : Gardez les fichiers sources à portée de main en tant que référence pendant que vous lisez l’article, car chacun d’eux complète l’autre. Les fichiers dans la build Visual Studio projet et sont exécutables avec des modifications minimales, en remplaçant l’URL de votre client Project Online au dossier PWA dossier. 
  
## <a name="background"></a>Contexte

Project Online est un service Office 365 qui fournit aux entreprises une solution de gestion de portefeuille de projets (PPM) et de bureau de gestion de projet (PMO) pour coordonner et gérer des portefeuilles, des programmes et des projets. Project Online offre est différente de celle des éditions Project bureau ; toutefois, Project Online contient toujours la fonctionnalité de maintenance et de suivi des détails d’un projet tout au long de la durée de vie d’un projet. Project Online repose sur SharePoint Online.
  
Un Project Online hébergé se compose de fichiers JavaScript et de ressources qui interagissent avec l’API du modèle objet côté client. Lorsque l’utilisateur visite le add-in, le JavaScript et les ressources sont téléchargés et exécutés dans le navigateur. Le add-In effectue des appels asynchrones à Project Online pour interagir avec le service, que ce soit la création, la récupération, la mise à jour ou la suppression de données. 
  
Project Online effectue une action de plus pour protéger les informations qui appartiennent à d’autres locataires du module complémentaire ; en d’autres Project Online crée un site isolé pour interagir avec les demandes du module. Aucun code personnalisé ne s’exécute sur l Project Online hôte. 
  
Le programme d’installation Project Online de développement utilise le type Visual Studio SharePoint de projet de l’autre. Le add-in est écrit en JavaScript et utilise le modèle Project objet JavaScript (JSOM) pour interagir avec le service Project Online. Le JSOM hérite de la plupart de ses fonctionnalités du SharePoint JSOM.
  
> [!NOTE]
> Les applications peuvent être publiées et vendues dans Office Store ou déployées dans un catalogue d’applications privé sur SharePoint. Pour plus d’informations, [voir Deploy and publish your Office Add-in](https://docs.microsoft.com/office/dev/add-ins/publish/publish).
> 
> Le add-in utilisé dans cet article est un exemple pour les développeurs ; il n’est pas destiné à être utilisé dans un environnement de production. L’objectif principal est d’afficher un exemple de développement d’applications pour Project Online. 
  
## <a name="prerequisites"></a>Conditions préalables

Ajoutez les éléments suivants à un environnement Windows pris en charge :
  
- **.NET Framework version 4.0** ou ultérieure : les versions complètes de l’infrastructure de la version 4.0 sont compatibles. Le site de téléchargement est https://msdn.microsoft.com/vstudio/aa496123.aspx.
    
- **Visual Studio 2013 ou ultérieure**:  
    
   - L’édition professionnelle Visual Studio 2015 est prête à l’emploi et est disponible sur https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx .
    
   - L’édition communautaire Visual Studio 2015 est disponible sur https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx . Cette édition nécessite l’installation manuelle des outils Microsoft Office développeur pour Visual Studio.
    
   Les outils Microsoft Office développeur pour Visual Studio sont disponibles sur https://www.visualstudio.com/en-us/features/office-tools-vs.aspx .
    
- **Un Project Online :** cela permet d’accéder au service d’hébergement. Pour plus d’informations sur l’obtention d’un compte Microsoft Project Online, visitez le site https://products.office.com/en-us/Project/project-online-portfolio-management.
    
   Assurez-vous que l’utilisateur du add-in dispose d’une autorisation suffisante pour accéder à certains projets dans le Project Online client. 
    
- **Projets sur le site d’hébergement** qui sont remplis avec des informations.
    
> [!NOTE]
> La .NET Framework standard est l’infrastructure correcte à utiliser. N’utilisez pas le .NET Framework profil client 4. 
  
### <a name="set-up-the-visual-studio-project"></a>Configurer le projet Visual Studio

La configuration de l’application consiste à créer un projet, à lier les bibliothèques appropriées et à déclarer les espaces de noms nécessaires. Visual Studio présente plusieurs types de projets de développement. La section est brève et très simple. La valeur est que les informations sont resserées à un seul endroit.
  
#### <a name="select-a-visual-studio-project"></a>Sélectionner un projet Visual Studio

Pour créer un projet du type approprié pour le add-in, vous devez suivre les étapes suivantes. Les mots clés rencontrés à l’écran ont un **attribut gras** : 
  
1. Dans le menu Fichier, choisissez **Fichier**  >    >  **nouveau Project**. 
    
2. Dans les modèles installés dans le volet gauche, sélectionnez C#  >  **Office/SharePoint** des  >  **applications web.** 
    
3. En haut du volet central, sélectionnez **.NET Framework 4 ou** ultérieur ; la version actuelle est 4.6. 
    
4. Dans les types d’applications dans le volet central, choisissez **SharePoint du module.** 
    
5. Dans la section inférieure, spécifiez un nom et un emplacement pour le projet et un nom de solution. 
    
6. Dans la section inférieure, cochez la case **Créer le répertoire pour la solution**. 
    
7. Cliquez sur **OK** pour créer le projet initial. 
    
L’Assistant Visual Studio pose quelques questions de suivi sur le site de paramètres Project Online (appelé paramètres SharePoint dans les boîtes de dialogue) dans quelques boîtes de dialogue qui suivent. Voici les questions suivantes :
  
1. Quel site SharePoint souhaitez-vous utiliser pour le débogage de votre add-in ? Spécifiez l’URL de votre site PWA, par https://contoso.sharepoint.com/sites/pwa exemple.
    
2. Comment souhaitez-vous héberger votre SharePoint de serveur ? Choose [X] **SharePoint-hosted**.
    
   Pour plus d’informations sur SharePoint des modules complémentaires, notamment sur les options d’hébergement, [voir SharePoint les modules complémentaires.](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins)
    
3. Cliquez sur **Suivant**. 
    
La deuxième boîte de dialogue supplémentaire vous demande de spécifier la version SharePoint Online pour le complément : 
  
1. Quelle est la version la plus ancienne de SharePoint que vous souhaitez que votre add-in cible ? Choose [X] S **harePoint-Online**. 
    
2. Cliquez sur **Terminer**. 
    
Visual Studio crée le projet et accède au site Project Online site. 
  
### <a name="enable-sideloading-on-the-project-online-site"></a>Activer le chargement de version de version Project Online site

Le chargement de version test est le mécanisme permettant de tester et de déboguer des Project Online de test. Vous avez besoin de deux scripts pour le chargement de version test : un pour activer le chargement de version test sur votre site Project Online et un autre pour désactiver le chargement de version test une fois que vous avez terminé le test et déboguer le module.
  
Pour plus d’informations sur la configuration du chargement indépendant, voir Activer le chargement indépendant d’application dans votre collection de [sites non-développeur.](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/)
  
> [!NOTE]
> Le chargement indépendant d’applications est une fonctionnalité de développement/test. Il **n’est pas destiné à une utilisation en production.** Ne chargez pas les applications de manière régulière ou maintenez le chargement de version d’application activé plus longtemps que vous n’utilisez activement la fonctionnalité. 
  
## <a name="add-content-to-the-add-in-project"></a>Ajouter du contenu au projet de add-in

Après la création d’un projet et la configuration du mécanisme de débogage, l’ajout de contenu à l’application comprend les tâches suivantes :
  
- Définition de l’étendue de l’application
    
- Liaison de la bibliothèque JSOM
    
- Ajout d’éléments d’interface utilisateur au add-in
    
- Initialisation et connexion au service Project Online service
    
- Récupération des projets et des détails/propriétés
    
- Affichage des projets
    
- Affichage des tâches pour une Project
    
Le projet de add-in se compose de nombreux fichiers. Dans cet exemple, vous devez modifier les fichiers suivants : 
  
- AppManifest.xml
    
- Default.aspx
    
- App.js
    
- App.css - facultatif ; contient des définitions de style développées pour le add-in
    
Si le client Project Online change, par exemple en passant d’une version d’essai à un site d’abonnement, vous pouvez mettre à jour les propriétés du projet, y compris la connexion au serveur et l’URL du site, à l’aide de la fenêtre Propriétés disponible via la commande Fenêtre Afficher les  >   propriétés. 
  
Vous pouvez également ajouter des fichiers au projet. Si c’est le cas, vous devez mettre à jour le fichier Elements.xml situé dans le même groupe (Contenu, Images, Pages ou Scripts) pour inclure les nouveaux fichiers. Pour plus d’informations sur les fichiers de projet, voir Explorer la structure du manifeste de l’application et le [package d’un SharePoint.](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in)
  
### <a name="set-application-scope"></a>Définir l’étendue de l’application

Le add-in a besoin de niveaux d’étendue ou d’autorisation définis avant que le service renvoie des informations dans les résultats de requête. Pour ce module, utilisez l’étendue suivante pour Visual Studio projet. Cette modification est réalisée dans le fichier AppManifest.xml sous l’onglet Autorisations :

|Portée|Autorisation|
|:-----|:-----|
|Plusieurs projets (Project Server)  <br/> |Lecture  <br/> |
   
Enregistrez le fichier après avoir définir l’étendue de l’application. Sinon, aucune donnée n’est renvoyée à partir du service. 
  
### <a name="link-the-jsom-library"></a>Lier la bibliothèque JSOM

Les bibliothèques Project Online runtime, PS.js et PS.debug.js, sont fournies par Project Online et sont toujours la version la plus récente. Les add-ins JavaScript qui utilisent JSOM doivent établir un lien avec l’une de ces bibliothèques. Les définitions de liaison sont ajoutées dans le fichier Default.aspx. Les commandes d’utilisation des PS.js et/ou PS.debug.js font partie du code situé dans le App.js fichier.
  
Ajoutez la commande suivante pour PS.js définition PS.debug.js dans l’élément suivant la commande `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` « SharePoint:ScriptLink » pour sp.js. 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> **L’attribut OnDemand** pour PS.js ou PS.debug.js sur **false**. 
  
### <a name="add-ui-elements-to-the-add-in"></a>Ajouter des éléments d’interface utilisateur au add-in

L’exemple de add-in se compose de quelques composants. Les descriptions des éléments statiques se trouvent dans le fichier Default.aspx. Les descriptions des éléments dynamiques et le code de tous les composants se trouvent dans App.js fichier. Pour obtenir des commentaires sur les composants, reportez-vous aux listes de code source. Voici la liste des composants de l’interface utilisateur dans le composant :
  
- Titre
    
- Introduction du verbiage
    
- Bouton pour supprimer des tâches du tableau
    
- Tableau répertoriant l’ID et le nom du projet, ainsi que les informations sur la tâche.
    
- Bouton Tâches (cloné une fois pour chaque projet) qui importe les données de tâche dans la table.
    
Pour plus d’informations sur l’interface utilisateur, telles que le titre et la partie en-tête de la table de projet, voir le fichier de projet Default.aspx.
  
### <a name="initialize-and-connect-to-the-host-system"></a>Initialiser et se connecter au système hôte

Le App.js contient le code JavaScript. Le add-in charge PS.js dans le navigateur, puis appelle la fonction initializePage. InitializePage récupère un contexte au point de terminaison Project Online et démarre la fonction loadProjects.
  
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

La fonction loadProjects interroge le service pour les noms et les ID de projet. 
  
L’application récupère le nom du projet et l’ID de projet. D’autres informations sur le projet sont disponibles et sont accessibles en modifiant la méthode de chargement pour identifier explicitement les propriétés à récupérer. Un exemple est fourni dans le code en tant que commentaire. 
  
Si la requête réussit, le add-in continue en appelant displayProjects. 
  
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

La fonction displayProjects crée un tableau, une ligne par projet et un bouton pour afficher les tâches pour le projet spécifique. 
  
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
> La boucle While accède aux propriétés d’ID et de nom. Ceci est légèrement différent du projet de code source qui appelle une fonction qui, à son tour, accède aux mêmes propriétés. 
  
### <a name="display-the-tasks-for-a-project"></a>Afficher les tâches d’un projet

Les tâches, qui font partie du add-in, ne font pas partie du chargement initial. Si les tâches associées à un projet intéressent l’utilisateur, le fait de cliquer sur le bouton « Afficher les tâches » entraîne l’affichage des tâches dans la liste à l’aide du handler d’événement btnLoadTasks. 
  
Le handler d’événement btnLoadTasks, avec l’ID de projet approprié, demande les tâches pour le projet spécifié au serveur. Une fois récupéré, btnLoadTasks transmet la liste des tâches à displayTasks pour présenter les tâches à l’écran.
  
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

La fonction displayTasks affiche les tâches associées à un projet spécifié immédiatement sous l’entrée du projet.
  
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
> La boucle While accède à l’ID de tâche et aux propriétés de nom. Ceci est légèrement différent du projet de code source qui appelle une fonction qui, à son tour, accède aux mêmes propriétés. 
  
Un exemple de sortie pour les tâches d’un seul projet suit.
  
![Capture d’écran montrant la sortie pour une tâche de projet](media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Capture d’écran montrant la sortie pour une tâche de projet")
  
## <a name="see-also"></a>Voir aussi

Pour obtenir de la documentation et des exemples relatifs à Microsoft Project Online et au développement d’applications à l’aide de CSOM, consultez le [Portail de développement Project](https://developer.microsoft.com/en-us/project).
    


