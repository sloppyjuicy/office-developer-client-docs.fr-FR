---
title: Développement d’un complément Project Online à l’aide du modèle objet JavaScript (JSOM)
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 4a4b1ad2-de46-421d-a698-53c20c90b93a
description: Cet article décrit Microsoft Project Online développement de compléments pour améliorer votre expérience avec Project Online. Le projet de développement est implémenté en tant que procédure pas à pas. Le complément utilisé pour cet article lit et affiche les noms de projet et les ID des projets publiés à partir de votre compte Project Online et vous permet d’explorer les tâches associées à des projets individuels.
ms.openlocfilehash: 6df5d9d4e03fb4551953f1b8eea94c1ea5dd3f21
ms.sourcegitcommit: a6d13fdae7eb2e503236c1b629a59b36a4fb76f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2022
ms.locfileid: "66083484"
---
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a>Développement d’un complément Project Online à l’aide du modèle objet JavaScript (JSOM)

Cet article décrit Microsoft Project Online développement de compléments pour améliorer votre expérience avec le Project Online. Le projet de développement est implémenté en tant que procédure pas à pas. Le complément utilisé pour cet article lit et affiche les noms de projet et les ID des projets publiés à partir de votre compte Project Online et vous permet d’explorer les tâches associées à des projets individuels.
  
Au moment de l’exécution, la liste des compléments ressemble à l’illustration suivante :
  
![Capture d’écran montrant une liste de tâches et projets JSOM](media/766e5914-f048-48f4-9282-291f55e6e90d.png "Capture d’écran montrant une liste de tâches et projets JSOM")
  
L’objectif de l’exemple est l’interaction avec le Project Online, la création de requêtes et la définition du contexte pour chaque requête du service. Les éléments d’interface utilisateur reçoivent une attention minimale. Au lieu de cela, les listes sources fournissent des commentaires concernant l’interface utilisateur.
  
> [!NOTE]
> Les fichiers sources de l’exemple de complément, un projet Visual Studio, sont disponibles à l’adresse suivante : <https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks>..... Gardez les fichiers sources à portée de main en tant que référence pendant que vous lisez l’article, car chacun complète l’autre. Les fichiers de la génération de projet Visual Studio sont exécutables avec des modifications minimales, en remplaçant l’URL de votre locataire Project Online par le dossier PWA.
  
## <a name="background"></a>Contexte

Project Online est un service Office 365 qui fournit aux entreprises une solution de gestion de portefeuille de projets (PPM) et de bureau de gestion de projet (PMO) pour coordonner et gérer des portefeuilles, des programmes et des projets. Project Online est une offre différente des éditions de bureau Project ; toutefois, Project Online contient toujours les fonctionnalités permettant de gérer et de suivre les détails du projet tout au long de la vie d’un projet. Project Online repose sur SharePoint Online.
  
Un complément hébergé Project Online se compose de fichiers JavaScript et de ressources qui interagissent avec l’API Client-Side-Object-Model. Lorsque l’utilisateur visite le complément, le code JavaScript et les ressources sont téléchargés et exécutés dans le navigateur. Le complément effectue des appels asynchrones à Project Online pour interagir avec le service, qu’il s’agisse de créer, récupérer, mettre à jour ou supprimer des données.
  
Project Online effectue une autre action pour protéger les informations qui appartiennent à d’autres locataires du complément; à savoir, Project Online crée un site isolé pour interagir avec les demandes du complément. Aucun code personnalisé ne s’exécute sur l’hôte Project Online.
  
La configuration du développement pour Project Online compléments utilise le type de projet Visual Studio SharePoint complément. Le complément est écrit en JavaScript et utilise le Project modèle objet JavaScript (JSOM) pour interagir avec le service Project Online. Le modèle JSOM hérite d’une grande partie de ses fonctionnalités du SharePoint JSOM.
  
> [!NOTE]
> Les compléments peuvent être publiés et vendus dans le Office Store ou déployés dans un catalogue d’applications privées sur SharePoint. Pour plus d’informations, consultez [Déployer et publier votre complément Office](/office/dev/add-ins/publish/publish).
>
> Le complément utilisé dans cet article est un exemple pour les développeurs ; il n’est pas destiné à être utilisé dans un environnement de production. L’objectif principal est de montrer un exemple de développement d’applications pour Project Online.
  
## <a name="prerequisites"></a>Conditions préalables

Ajoutez les éléments suivants à un environnement Windows pris en charge :
  
- **.NET Framework 4.0 ou version ultérieure** : les versions complètes du framework de la version 4.0 sont compatibles. Le site de téléchargement est <https://msdn.microsoft.com/vstudio/aa496123.aspx>.

- **Visual Studio 2013 ou version ultérieure** :  

  - L’édition professionnelle de Visual Studio 2015 est prête à être prête à l’emploi et est disponible à <https://www.visualstudio.com/products/visual-studio-professional-with-msdn-vs.aspx>l’adresse .

  - L’édition community de Visual Studio 2015 est disponible à l’adresse <https://www.visualstudio.com/products/visual-studio-community-vs.aspx>. Cette édition nécessite une installation manuelle des outils de développement Microsoft Office pour Visual Studio.

   Les outils de développement Microsoft Office pour Visual Studio sont disponibles à l’adresse <https://www.visualstudio.com/features/office-tools-vs.aspx>.

- **Un compte Project Online** : cela permet d’accéder au service d’hébergement. Pour plus d’informations sur l’obtention d’un compte Microsoft Project Online, visitez le site <https://products.office.com/Project/project-online-portfolio-management>.

   Vérifiez que l’utilisateur du complément dispose d’une autorisation suffisante pour accéder à certains projets dans le locataire Project Online.

- **Projets sur le site d’hébergement** qui sont remplis avec des informations.

> [!NOTE]
> Le .NET Framework standard est le framework approprié à utiliser. N’utilisez pas le « profil client .NET Framework 4 ».
  
### <a name="set-up-the-visual-studio-project"></a>Configurer le projet Visual Studio

La configuration de l’application consiste à créer un projet, à lier les bibliothèques appropriées et à déclarer les espaces de noms nécessaires. Visual Studio présente plusieurs types de projets de développement. La section est brève et très basique. La valeur est que les informations sont coalescées au même endroit.
  
#### <a name="select-a-visual-studio-project"></a>Sélectionner un projet Visual Studio

Pour créer un projet du type approprié pour le complément, vous devez effectuer les étapes suivantes. Les mots clés rencontrés à l’écran ont un attribut **gras** :
  
1. Dans le menu Fichier, choisissez **Nouveau** >  >  **fichier Project**.

2. Dans les modèles installés dans le volet gauche, sélectionnez **C#** > **Office/SharePoint** >  **Web Add-ins**.

3. En haut du volet central, sélectionnez **.NET Framework 4** ou version ultérieure ; la version actuelle est 4.6.

4. Dans les types d’application du volet central, choisissez **SharePoint complément**.

5. Dans la section inférieure, spécifiez un nom et un emplacement pour le projet et un nom de solution.

6. Dans la section inférieure, cochez la case **Créer le répertoire pour la solution**.

7. Cliquez sur **OK** pour créer le projet initial.

L’Assistant Visual Studio pose quelques questions de suivi sur le site de paramètres Project Online (appelé paramètres SharePoint dans les boîtes de dialogue) dans quelques dialogues qui suivent. Voici les questions suivantes :
  
1. Quel SharePoint site souhaitez-vous utiliser pour déboguer votre complément ? Spécifiez l’URL de votre site PWA, par <https://contoso.sharepoint.com/sites/pwa>exemple .

2. Comment voulez-vous héberger votre complément SharePoint ? Choisissez [X] **SharePoint hébergé**.

   Pour plus d’informations sur les compléments SharePoint, y compris les options d’hébergement, consultez [SharePoint compléments](/sharepoint/dev/sp-add-ins/sharepoint-add-ins).

3. Cliquez sur **Suivant**.

La deuxième boîte de dialogue supplémentaire vous demande de spécifier la version SharePoint Online pour le complément :
  
1. Quelle est la première version de SharePoint que vous souhaitez que votre complément cible ? Choisissez [X] S **harePoint-Online**.

2. Cliquez sur **Terminer**.

Visual Studio crée le projet et accède au site Project Online.
  
### <a name="enable-sideloading-on-the-project-online-site"></a>Activer le chargement indépendant sur le site Project Online

Le chargement indépendant est le mécanisme de test et de débogage Project Online compléments. Vous avez besoin de deux scripts pour le chargement indépendant : l’un pour activer le chargement indépendant sur votre site Project Online et l’autre pour désactiver le chargement indépendant une fois que vous avez terminé le test et le débogage du complément.
  
Pour plus d’informations sur la configuration du chargement indépendant, consultez Activer le chargement [indépendant de l’application dans votre collection de sites non développeur](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/).
  
> [!NOTE]
> Le chargement indépendant d’applications est une fonctionnalité de développement/test. Il **n’est pas destiné à une utilisation en production**. Ne chargez pas d’applications de manière régulière ou laissez le chargement indépendant des applications activé pendant plus longtemps que vous n’utilisez activement la fonctionnalité.
  
## <a name="add-content-to-the-add-in-project"></a>Ajouter du contenu au projet de complément

Après avoir créé un projet et configuré le mécanisme de débogage, l’ajout de contenu à l’application inclut les tâches suivantes :
  
- Définition de l’étendue de l’application

- Liaison de la bibliothèque JSOM

- Ajout d’éléments d’interface utilisateur au complément

- Initialisation et connexion au service Project Online

- Récupération de projets et de détails/propriétés

- Affichage des projets

- Affichage des tâches pour un Project

Le projet de complément se compose de nombreux fichiers. Dans cet exemple, vous devez modifier les fichiers suivants :
  
- AppManifest.xml

- Default.aspx

- App.js

- App.css - facultatif ; contient des définitions de style développées pour le complément

Si le client Project Online change, par exemple en passant d’une version d’évaluation à un site d’abonnement, vous pouvez mettre à jour les propriétés du projet, y compris la connexion serveur et l’URL du site, à l’aide de la fenêtre Propriétés disponible via la commande **Afficher** >  la **fenêtre Propriétés**.
  
Vous pouvez également ajouter des fichiers au projet. Si c’est le cas, vous devez mettre à jour le fichier Elements.xml situé dans le même groupe (contenu, images, pages ou scripts) pour inclure les nouveaux fichiers. Pour plus d’informations sur les fichiers projet, consultez [Explorer la structure du manifeste d’application et le package d’un complément SharePoint](/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in).
  
### <a name="set-application-scope"></a>Définir l’étendue de l’application

Le complément a besoin d’une étendue ou de niveaux d’autorisation définis avant que le service retourne des informations dans les résultats de la requête. Pour ce complément, utilisez l’étendue suivante pour le projet Visual Studio. Cette modification est apportée au fichier AppManifest.xml sous l’onglet Autorisations :

|Portée|Autorisation|
|:-----|:-----|
|Plusieurs projets (serveur Project)  <br/> |Lecture  <br/> |

Enregistrez le fichier après avoir défini l’étendue de l’application. Sinon, aucune donnée ne sera retournée à partir du service.
  
### <a name="link-the-jsom-library"></a>Lier la bibliothèque JSOM

Les bibliothèques Project Online d’exécution, PS.js et PS.debug.js, sont fournies par Project Online et sont toujours la version la plus récente. Les compléments JavaScript qui utilisent JSOM doivent être liés à l’une de ces bibliothèques. Les définitions de liaison sont ajoutées dans le fichier Default.aspx. Les commandes à utiliser PS.js et/ou PS.debug.js font partie du code situé dans le fichier App.js.
  
Ajoutez la commande suivante pour PS.js ou PS.debug.js définition dans l’élément `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` suivant le SharePoint:ScriptLink pour sp.js.
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> L’attribut **OnDemand** pour PS.js ou PS.debug.js défini sur **false**.
  
### <a name="add-ui-elements-to-the-add-in"></a>Ajouter des éléments d’interface utilisateur au complément

L’exemple de complément se compose de quelques composants. Les descriptions d’éléments statiques se trouvent dans le fichier Default.aspx. Les descriptions d’éléments dynamiques et le code de tous les composants se trouvent dans le fichier App.js. Pour obtenir des commentaires sur les composants, reportez-vous aux listes de code source. Voici une liste des composants de l’interface utilisateur dans le complément :
  
- Titre

- Verbiage d’introduction

- Bouton permettant de supprimer des tâches de la table

- Tableau qui répertorie l’ID et le nom du projet, ainsi que les informations de tâche.

- Bouton Tâches (cloné une fois pour chaque projet) qui importe les données des tâches dans la table.

Pour plus d’informations sur l’interface utilisateur, telles que le titre et la partie d’en-tête de la table de projet, consultez le fichier projet Default.aspx.
  
### <a name="initialize-and-connect-to-the-host-system"></a>Initialiser et se connecter au système hôte

Le fichier App.js contient le code JavaScript. Le complément charge PS.js dans le navigateur, puis appelle la fonction initializePage. InitializePage récupère un contexte vers le point de terminaison Project Online et démarre la fonction loadProjects.
  
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

La fonction loadProjects interroge le service pour les noms et ID de projet.
  
L’application récupère le nom du projet et l’ID de projet. D’autres informations sur le projet sont disponibles et sont accessibles en modifiant la méthode de chargement pour identifier explicitement les propriétés à récupérer. Un exemple est fourni dans le code en tant que commentaire.
  
Si la requête réussit, le complément continue en appelant displayProjects.
  
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
> La boucle While accède aux propriétés d’ID et de nom. Ceci est légèrement différent du projet de code source qui appelle une fonction qui, à son tour, accède aux mêmes propriétés.
  
### <a name="display-the-tasks-for-a-project"></a>Afficher les tâches d’un projet

Les tâches, bien qu’faisant partie du complément, ne font pas partie du chargement initial. Si l’utilisateur est intéressé par les tâches associées à un projet, le fait de cliquer sur le bouton « Afficher les tâches » entraîne l’affichage des tâches dans la liste à l’aide du gestionnaire d’événements btnLoadTasks.
  
Le gestionnaire d’événements btnLoadTasks, avec l’ID de projet approprié, demande les tâches pour le projet spécifié au serveur. Une fois récupéré, btnLoadTasks transmet la liste des tâches à displayTasks pour présenter les tâches à l’écran.
  
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
  
Voici un exemple de sortie pour les tâches d’un seul projet.
  
![Capture d’écran montrant la sortie pour une tâche de projet](media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Capture d’écran montrant la sortie pour une tâche de projet")
  
## <a name="see-also"></a>Voir aussi

Pour obtenir de la documentation et des exemples relatifs à Microsoft Project Online et au développement d’applications à l’aide de CSOM, consultez le [Portail de développement Project](https://developer.microsoft.com/project).
