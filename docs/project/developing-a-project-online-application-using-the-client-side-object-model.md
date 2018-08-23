---
title: Développement d’une application Project Online à l’aide du modèle objet côté client
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5740d0b2-5d36-40e4-9e83-577cb186359f
description: Cet article décrit le développement d’applications Microsoft Project Online pour les applications bureautiques à l’aide de .NET Framework 4.0. L’application décrite dans cet article récupère des informations à partir du serveur d’hébergement.
ms.openlocfilehash: a65dbbdedb371fae9b8f0b99ea113ae38cbaffb5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572878"
---
# <a name="developing-a-project-online-application-using-the-client-side-object-model"></a>Développement d’une application Project Online à l’aide du modèle objet côté client

Cet article décrit le développement d’applications Microsoft Project Online pour les applications bureautiques à l’aide de .NET Framework 4.0. L’application décrite dans cet article récupère des informations à partir du serveur d’hébergement. 
  
## <a name="background"></a>Arrière-plan

Microsoft Project en route en tant qu’application de bureau de début des années 90. Aujourd'hui, Project est beaucoup plus, comme l’atteste son plusieurs variétés :
  
- Project standard edition est une application de bureau qui s’exécute en tant qu’application autonome.
    
- Project professionnelle édition est une application de bureau qui permettre interagir et partager des données avec un serveur à grande échelle, ainsi effectuer les fonctionnalités de Project Édition standard.
    
- Project Online est un service hébergé par Microsoft qui permet aux entreprises avec une solution de niveau PMO pour coordonner et gérer des portefeuilles, programmes et projets. Une offre différente versions du bureau, Project Online permettre gérer et suivre les détails du projet dans toute la durée de vie d’un projet. 
    
- Project Server est un service hébergé de contenu d’entreprise dans lequel l’entreprise gère et sécurise le serveur contenant le projet, programme et informations de portefeuille. Project Server, en raison de la sécurisation du serveur interne, offre le projet, programme et les fonctionnalités de portefeuille orienté de hébergé en externe Project Online avec une capacité supérieure pour la personnalisation.
    
Project Online comprend trois ensembles d’API en ligne : modèle d’objet côté Client (CSOM) et modèle d’objet JavaScript (JSOM) Representational State Transfer (REST). 
  
- L’implémentation du modèle CSOM .NET est l’interface par défaut lors du développement d’applications Windows qui interagissent avec les clients Project Online. Environnements standard pour les applications orientées utilisateur incluent des ordinateurs de bureau Windows et les appareils Microsoft Surface. Applications principale écrites avec CSOM .NET peuvent se connecter aux autres serveurs de l’entreprise logique et sources de données externes à Project Online. Les demandes de récupération pour Project Online utilisent un système de requête LINQ comparables à celles qui offre plusieurs améliorations par rapport à des fonctions de récupération de base.
    
- L’interface de modèle d’objet JavaScript (JSOM) prend en charge élargie des navigateurs compléments Project Online. Un complément est une application web qui est stockée dans le client Project Online. Lorsqu’un utilisateur souhaite exécuter une macro complémentaire, le code de la macro complémentaire télécharge et s’exécute dans le navigateur sur l’ordinateur de l’utilisateur. 
    
- Le modèle REST/Odata fournit la communication basé sur HTTP, cette interface est recommandée pour les applications dans des environnements non Windows. Points de terminaison de communication sont les objets dans le site Project Web Application (PWA). Résultats fournissent des codes d’état HTTP normales.
    
Cet article se concentre sur une application qui utilise l’interface CSOM .NET.
  
## <a name="prerequisites"></a>Conditions préalables

Démarrer avec un système de base Windows 10 en cours d’exécution, puis ajoutez les éléments suivants :
  
- .NET framework 4.0 ou version ultérieure--utilisent l’infrastructure complète. Le site de téléchargement est https://msdn.microsoft.com/en-us/vstudio/aa496123.aspx.
    
- Visual Studio 2013 ou version ultérieure, n’importe quelle édition est acceptable. L’édition de la Communauté de Visual Studio 2015 a été utilisée pour développer l’exemple d’application. L’édition de la Communauté est disponible à l’adresse https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.
    
- Les composants SharePoint Client SDK--Project Online et Project Server trouvent sur SharePoint et SharePoint assemblys. Les composants Client SharePoint sont inclus dans les éditions de Visual Studio Professional et d’entreprise. Si vous utilisez Visual Studio Community edition, la dernière version du SDK des outils pour développeurs Office est disponible sur le site suivant : https://www.microsoft.com/en-us/download/details.aspx?id=35585.
    
- Un compte Project Online : cela offre un accès au site d’hébergement. Pour plus d’informations sur l’obtention d’un compte Project Online, voir https://products.office.com/en-us/Project/project-online-portfolio-management.
    
- Projets sont remplies avec les informations sur le site d’hébergement
    
> [!NOTE]
> La norme .NET Framework (4.0 ou version ultérieure) est l’infrastructure correcte à utiliser. N’utilisez pas le .NET Framework 4 Client Profile. 
  
## <a name="develop-the-application"></a>Développer l’application

Dans le développement d’une application de bureau pour SharePoint, l’interface par défaut est le modèle d’objet projet client (CSOM). 
  
Vous pouvez télécharger l’exemple complet à https://github.com/OfficeDev/Project-CSOM-List-Projects-Tasks.
  
Les deux premières rubriques traitent des problèmes de base : création d’un projet Visual Studio avec les espaces de noms appropriés et des assemblys et l’accès au serveur d’hébergement. Les autres rubriques traitent avec la récupération des informations à l’aide du modèle CSOM, à partir d’un et plusieurs objets. 
  
Récupérer des informations sur l’hôte est un processus double action à partir d’applications clientes. Tout d’abord, l’application spécifie et envoie une ou plusieurs demandes de récupération pour le serveur. Deuxièmement, l’application envoie une notification au serveur pour exécuter les requêtes soumis. Le serveur répond en envoyant les résultats de requête au client.
  
### <a name="set-up-the-visual-studio-project"></a>Configurer le projet Visual Studio

Configuration de l’application se compose de création d’un nouveau projet, lier les assemblys appropriés et déclarer les espaces de noms nécessaires. Visual Studio présente plusieurs types de projets de développement. 
  
#### <a name="select-a-visual-studio-project"></a>Sélectionnez le projet Visual Studio

1. Démarrez Visual Studio et sélectionnez **Démarrer un nouveau projet** dans la Page de démarrage. 
    
   La boîte de dialogue Nouveau projet affiche les modèles d’application disponibles et les champs de données pour n’importe quel modèle sélectionné. 
    
2. Pour cette application, spécifiez les éléments suivants. Mots clés rencontrés dans l’écran ont un attribut gras :
    
   1. À partir des modèles installés dans le volet gauche, sélectionnez **c#** => **Windows** => **Bureau classique**. 
    
   2. En haut du volet central, sélectionnez **.NET Framework 4**. 
    
   3. Dans les types d’application dans le volet central, sélectionnez **Application Console**. 
    
   4. Dans la section inférieure, spécifiez un nom et un emplacement pour le projet et un nom de solution. 
    
   5. Également dans la section inférieure, cochez la case de **créer le répertoire pour la solution** . 
    
3. Cliquez sur **OK** pour créer le projet initial. 
    
#### <a name="add-assemblies"></a>Ajouter des assemblys

La solution VS doit le 2103 Project SDK, deux assemblys dans le SDK SharePoint et l’assembly .NET Framework System.Security de l’assembly ProjectServerClient.
  
1. Dans l’Explorateur de solutions VS, avec le bouton droit de la saisie de références et sélectionnez **Ajouter une référence** dans le menu contextuel. 
    
2. Vérifier la **Microsoft.ProjectServer.Client.dll**. 
    
   Si nécessaire, cliquez sur **Parcourir...** en bas de la boîte de dialogue et accédez au répertoire d’installation du SDK de Project 2013 pour rechercher l’assembly. 
    
3. Cliquez sur **OK**. 
    
4. Dans le fichier .cs, ajoutez l’espace de noms PrjoctServer Client.
    
   ```cs
    using Microsoft.ProjectServer.Client;
   ```

Ajoutez les assemblys du Kit de développement SharePoint 2013 à l’aide de la Console du Gestionnaire de Package NuGet. 
  
1. Dans le menu Outils VS, cliquez sur les menus suivants : **outils =\> Gestionnaire de Package NuGet =\> Console du Gestionnaire de Package**. 
    
2. Dans la Console du Gestionnaire de Package, saisissez les commandes et appuyez sur suivants \<entrée\>:
    
   ```cs
    Install-Package Microsoft.SharePointOnline.CSOM
   ```

   La **Console du Gestionnaire de Package** fournit une description des résultats de la commande ; et les assemblys SharePoint pour afficher l’Explorateur de solutions VS dans les références de projet. 
    
3. Ajoutez les espaces de noms au fichier .cs :
    
   ```cs
    using Microsoft.SharePoint.Client;
   ```

L’assembly System.Security fait partie de .NET Framework et a été installé avec l’infrastructure. L’exemple d’application a besoin d’un espace de noms plus qui fournit une chaîne chiffrée pour le système d’hébergement pour l’authentification. Une fois authentifiée, l’application peut accéder aux projets sur le système d’hébergement. Ajoutez l’espace de noms System.Security au fichier .cs de cette façon :
  
1. Dans l’Explorateur de solutions VS, avec le bouton droit de la saisie de références et sélectionnez **Ajouter une référence** dans le menu contextuel. 
    
2. Sélectionnez **assemblys =\> Framework** dans le volet gauche de la boîte de dialogue Gestionnaire de références, puis vérifiez **System.Security**. 
    
3. Cliquez sur **OK**. 
    
4. Dans le fichier .cs, ajoutez l’espace de noms System.Security :
    
   ```cs
    using System.Security;
   ```

Le début du fichier .cs doit contenir des espaces de noms suivants :
  
- Système
    
- System.Collections.Generic
    
- System.Linq
    
- System.Test
    
- Microsoft.ProjectServer.Client
    
- Microsoft.SharePoint.Client
    
- System.Security
    
### <a name="connect-to-the-host-system"></a>Se connecter au système hôte

Project Online est une application SharePoint, à l’aide de l’authentification SharePoint est l’approche correcte. Le fragment de code suivant prépare accéder à l’environnement hébergé.
  
```cs
    class Program
    {
        private static ProjectContext projContext;
        static void Main (string[] args)
        {
            using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
            {
                SecureString password - new SecureString();
                foreach (char c in "password".ToCharArray()) password.AppendChar(c);
                //Using SharePoint method to load Credentials
                projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);

```

Préparations pour accéder à l’environnement hébergé incluent les éléments suivants :
  
1. Créer un objet de contexte pour les projets : est contenu dans le code suivant de l’extrait de code précédent. 
    
   ```cs
    private static ProjectContext projContext;
    
   ```

   Le contexte est hérité par d’autres composants, autoriser le système à gérer le contexte du modèle objet Project.
    
2. Identifiez le site hôte : cette opération est effectuée dans le code suivant dans le fragment de code précédent.
    
   ```cs
    using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
   ```

   Lors de l’instanciation le contexte de projets, l’application doit fournir la racine de la collection de sites de projets. L’application utilise une sous-chaîne de l’URL de la racine des projets. Une capture instantanée de cet emplacement est mise en surbrillance avec un rectangle rouge dans l’illustration suivante. L’authentification doit la chaîne à partir de son démarrage par le biais de la sous-chaîne « pwa ». Dans le code, l’application utilise la chaîne «https://XXXXXXXX.sharepoint.com/sites/pwa».
        
   ![Capture d’écran de l’URL de la collection de sites de projets au sein d’une bordure rouge.] (media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Capture d’écran de l’URL des projets de site collection au sein d’une bordure rouge")
  
3. Placer le mot de passe dans une chaîne sécurisée : cette opération est effectuée dans le code suivant dans le fragment de code précédent.
    
   ```cs
    SecureString password - new SecureString();
    foreach (char c in "password".ToCharArray()) password.AppendChar(c);
    
   ```

   Le compte d’utilisateur et mot de passe sont les informations d’identification pour accéder au site hôte. 
    
4. Ajouter le compte d’utilisateur et le mot de passe à la partie d’informations d’identification de l’objet context : cette opération est effectuée dans le code suivant dans le fragment de code précédent.
    
   ```cs
    projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);
   ```

Le contexte du projet instancié est prêt à utiliser.
  
### <a name="list-all-published-projects"></a>Liste des projets publiés tous les

Project Online ProjectServer proxys permet de communiquer avec le serveur pour créer, rapport, mise à jour et suppression (CRUD). Le serveur hôte/traite les demandes de manière efficace et comprend le client à effectuer les actions suivantes pour la communication avec le serveur :
  
1. Établir un contexte pour la communication. 
    
   Le contexte est utilisé par la collection de projets, ainsi que d’autres objets et collections par le biais de l’héritage des autorisations, y compris la collection tasks, collection assignments, l’objet stage et champs personnalisés. 
    
2. Utilisez le modèle objet pour spécifier un objet, collection ou aucune donnée à récupérer.
    
   Cette étape utilise LINQ sous la forme d’une requête ou une méthode. La spécification du contrôle que vous recevez. Souvent, cette étape est incorporée dans le corps de la méthode Load (étape 3). 
    
3. Charger la spécification de récupération à partir de l’étape précédente à l’aide de la méthode Load() ou LoadQuery().
    
   Pour charger des objets et collections, utilisez Load(). Pour les requêtes comportant des clauses comme « où » et « groupe », utilisez LoadQuery(). 
    
4. Exécute la demande à l’aide de la méthode ExecuteQuery().
    
   La méthode ExecuteQuery() avertit l’hôte que l’ou les requêtes sont prêts à être exécutés. Une fois que l’hôte reçoit une notification, il exécute les requêtes et envoie les résultats au client. 
    
Avec les informations sur le client, l’application peut utiliser. Le fragment de code suivant parcourt les projets publiés et imprime l’Id et le nom de chaque projet publié sur l’hôte.
  
```cs
// Get the list of projects in Project Web App.
var projects = projContext.Projects;
projContext.Load(projects);
projcontext.ExecuteQuery();
foreach (PublishedProject pubProj in projContext.Projects)
{
    Console.WriteLine("\n{0}. {1}   {2} \t{3} \n", j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
}

```

Sortie :
  
```cs
Published Project count:2
1. be80a848-b2ef-e511-80f4-00155dc84e01   A second Project     3/21/2016 10:14:40 PM
2. 9d730a1a-60ed-e511-80f6-00155dc87d01   Ent_Proj_1   3/18/2016 11:21:14 PM

```

### <a name="make-a-request"></a>Effectuer une demande

Utilisez les actions de fragment de code précédent, l’application récupère la liste des projets dans le compte spécifié sur le site d’hébergement. 
  
1. Le ProjectContext est spécifiée pour les projets à la liste. 
    
   ```cs
    var projects = projContext.Projects;
   ```

2. Spécifiez l’élément à récupérer. 
    
   ```cs
    projContext.Load(projects);
   ```

   En indiquant seulement la collection, le serveur récupère la collection de projet, remplir chaque projet avec des valeurs pour le jeu de propriétés par défaut. Accès aux propriétés qui font partie du jeu de propriétés par défaut donne les résultats. Accéder aux propriétés qui ne font pas partie de la valeur par défaut de définir les résultats dans une exception « Non initialisé ».
    
3. Chargez la demande (projContext.Load).
    
   Cela fait partie de l’étape précédente.
    
4. Exécuter la requête (ExecuteQuery). 
    
   ```cs
    projContext.ExecuteQuery();
   ```

### <a name="retrieve-high-level-project-information"></a>Récupérer des informations de haut niveau du projet

Propriétés qui ne sont pas des propriétés par défaut doivent être spécifiées dans la demande au serveur. Le fragment de code suivant charge le contexte de la collection projects comme dans l’exemple précédent. Ensuite, la spécification demande des propriétés supplémentaires non par défaut à inclure dans le résultat. 
  
```cs
var projects = projContext.Projects;
projContext.Load(projects,
    ps => ps.IncludeWithDefaultProperties(
        p => p.StartDate, p => p.Phase, p => p.Stage));
projContext.ExecuteQuery();

```

L’instruction load Spécifie le contexte de collection de projets et ajoute la date de début, Phase et étape le résultat de requête. Les propriétés supplémentaires peuvent être scalaires, objets et collections. Éléments scalaires sont accessibles directement. Objets et collections nécessitent un traitement supplémentaire, comme dans le fragment de code suivant.
  
```cs
// Using the previous definition and Load statement …
projContext.ExecuteQuery();
foreach (PublishedProject pubProj in projContext.Projects)
{
Console.WriteLine("\n\t{0}. \t{1} \n\t{2} \n\t{3} \n", j++, pubProj.Id, pubProj.Name,
    pubProj.CreatedDate);
             // The following statement generates an exception about the object 
             // reference not being set to an instance on the server. 
             // Console.WriteLine("\tCurrent Phase:\t{0}", pubProj.Phase.Name);
             // Phase and Stage are not published with the rest of the data. Need to pull these objects from the server.
             Phase oPhase = pubProj.Phase;
             projContext.Load(oPhase);
             projContext.ExecuteQuery();
             //if-else fails because the else case fails with "Microsoft.SharePoint.Client.ServerObjectNullReferenceException".
             //if (oPhase.ServerObjectIsNull != null)
             //Using try-catch instead
             try
             {
                  Console.WriteLine("\tCurrent Phase:\t{0}", oPhase.Name);
             }
             
             catch
             {
                  Console.WriteLine("\tCurrent Phase:\t Not available");
             }
             
             Stage oStage = pubProj.Stage;
             projContext.Load(oStage);
             projContext.ExecuteQuery();
             //Again, not using if-else combination for the same reason as above.
             try
             {
                  Console.WriteLine("\tCurrent Stage:\t{0}", oStage.Name);
             }
             
             catch
             {
                  Console.WriteLine("\tCurrent Stage:\t Not available");
    }

```

Sortie d’abord trois projets :
  
```cs
Project counts:31
1. Project ID:  957d5fcd-5cbf-e111-9f1e-00155d022681
        Name:           Acquisition Target Analysis
        CreatedDate:            3/22/2016 5:14:34 PM
        Current Phase:  3. Plan
        Current Stage:  6. Plan
2. Project ID:  16905202-5fbf-e111-9f1e-00155d022681
        Name:           Apparel ERP Upgrade
        CreatedDate:            3/22/2016 5:36:40 PM
        Current Phase:  3. Plan
        Current Stage:  6. Plan
3. Project ID:  dce23152-63bf-e111-9f1e-00155d022681
        Name:           Audit Tracking Solution
        CreatedDate:            3/22/2016 5:02:24 PM
        Current Phase:  2. Select
        Current Stage:  4. Select Gate

```

### <a name="retrieve-all-tasks-in-a-project"></a>Récupérer toutes les tâches dans un projet

Chaque projet comporte de nombreuses tâches. Par conséquent, extraire les tâches pour un seul projet comprend les éléments suivants :
  
1. Établir le contexte de la collection de projets.
    
   ```cs
    var projects = projContext.Projects;
   ```

2. Récupérer les informations de projet, y compris les propriétés de la tâche.
    
   ```cs
    projContext.Load(projects);
    ProjContext.ExecuteQuery();
    foreach (PublishedProject pubProj in projContext.Projects){
    
   ```

    Notez que l’application de gestion de projets publiés. Le contexte du projet publié en cours est pubProj. 
    
3. Établir le contexte de la collection Tasks.
    
   ```cs
    PublishedTaskCollection collTask = pubProj.Tasks;
   ```

   Le `pubProj.Tasks` propriété référence les tâches du projet publié en cours. 
    
4. Charger les spécifications pour récupérer la collection de tâches, y compris les propriétés par défaut appropriées.
    
   ```cs
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, t => t.Start,
            t => t.ScheduledStart, t => t.Completion));
    
   ```

5. Exécuter la requête pour récupérer la collection de tâches avec les propriétés appropriées.
    
   ```cs
    projContext.ExecuteQuery();
   ```

Les informations sont maintenant locales. Le fragment de code suivant traite de la collection tasks publié en écrivant les informations sur la console.
  
```cs
    Console.WriteLine("Task collection count: {0}", collTask.Count.ToString());
    if (collTask.Count > 0)
    {
        int k = 1;    //Task counter.
        foreach (PublishedTask t in collTask)
        {
            Console.WriteLine("{0}. Id:{1} \tName:{2}", k++, t.Id, t.Name);
            Console.WriteLine("\t ScheduledStart:{0} \tStart:{1} \tCompletion:{2}", k, t.ScheduledStart, t.Start, t.Completion);
        }
    }

```

Sortie de tâches pour un projet :
  
```cs
Task collection count: 5
1. Id:256fa850-b2ef-e511-80f6-00155dc87d01      Name:Load software onto computer
         ScheduledStart:2       Start:4/4/2016 8:00:00 AM       Completion:4/4/2016 8:00:00 AM
2. Id:266fa850-b2ef-e511-80f6-00155dc87d01      Name:Locate and load Project Online SDK
         ScheduledStart:3       Start:4/5/2016 8:00:00 AM       Completion:4/5/2016 8:00:00 AM
3. Id:276fa850-b2ef-e511-80f6-00155dc87d01      Name:Locate and load SP SDK
         ScheduledStart:4       Start:4/5/2016 1:00:00 PM       Completion:4/5/2016 1:00:00 PM
4. Id:286fa850-b2ef-e511-80f6-00155dc87d01      Name:Build app that accesses Proj Online
         ScheduledStart:5       Start:4/6/2016 8:00:00 AM       Completion:4/6/2016 8:00:00 AM
5. Id:296fa850-b2ef-e511-80f6-00155dc87d01      Name:Build app that accesses task assignments
         ScheduledStart:6       Start:4/7/2016 8:00:00 AM       Completion:4/7/2016 8:00:00 AM

```

### <a name="access-information-at-multiple-levels"></a>Informations d’accès à plusieurs niveaux

Chaque tâche peut avoir une ou plusieurs personnes (également appelé ressources) contribuer à son exécution. Les collections affectations et ressources contiennent ces informations pour chaque tâche. 
  
Le traitement comprend les éléments suivants :
  
1. Obtention d’un contexte pour la tâche du projet.
    
2. Créer une demande et chargez la demande pour les affectations de lié à la tâche. 
    
3. Exécuter la requête pour les affectations.
    
4. Créer une demande et chargez la demande pour la ressource associée à une affectation spécifique. 
    
5. Exécuter la requête pour la ressource.
    
> [!NOTE] 
> - La collection Assignments est demandée explicitement les informations à partir du serveur, car il n’est pas une propriété par défaut de la collection Tasks. En tant que collection, une requête ultérieure est effectuée pour extraire la collection à partir du serveur. 
> - La ressource est un objet. La requête pour une affectation inclut le nom de ressource associé à l’affectation.
    
```cs
PublishedTaskCollection collTask = pubProj.Tasks;
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, 
            t => t.Assignments));
    projContext.Load(collTask);
    projContext.ExecuteQuery();
    Console.WriteLine("Task collection count: {0}", collTask.Count.ToString());
    if (collTask.Count > 0)
    {
        int k = 1;    //Task counter.
        //Processing task list for current project
        foreach (PublishedTask t in collTask)
        {
            Console.WriteLine("{0}. Id:{1} \tName:{2}", k, t.Id, t.Name);
            k++;
            //Define and retrieve Assignments for current task
            PublishedAssignmentCollection collAssgns = t.Assignments;
            projContext.Load(collAssgns);
            projContext.ExecuteQuery();
            Console.WriteLine("    Assignment collection count: {0}", collAssgns.Count);
            if (collAssgns.Count > 0)
            {
                //Output string for resources assigned to task
                StringBuilder output = new StringBuilder();
                output.AppendFormat("\t Assignments: ");
                foreach (PublishedAssignment a in collAssgns)
                {
                    //Define and retrieve resource name for current assignment 
                    //(an object)
                    projContext.Load(a,
                        b => b.Resource.Name);
                    projContext.ExecuteQuery();
                    output.AppendFormat("{0}, ", a.Resource.Name);
                }
                Console.WriteLine(output);
            }
            else
            {
                Console.WriteLine("\t Assignments: None");
            }
        }
    }   // endif

```

Sortie pour les tâches 52, 75 et 76 d’un projet :
  
```cs
52. Id:2c729e96-54f0-e511-80c6-000d3a33235f     Name:Develop training materials
    Assignment collection count: 1
         Assignments: Robert Lyon,
75. Id:43729e96-54f0-e511-80c6-000d3a33235f     Name:Determine final deployment strategy
    Assignment collection count: 0
         Assignments: None
76. Id:44729e96-54f0-e511-80c6-000d3a33235f     Name:Develop deployment methodology
    Assignment collection count: 4
         Assignments: Molly Dempsey, Sara Davis, Shammi Mohamed, Zainal Arifin, 

```

### <a name="access-custom-enterprise-level-fields"></a>Champs de niveau entreprise personnalisés Access

Il existe des champs personnalisés pour Project Online. Il s’agit des champs de niveau entreprise qui peuvent être associés à des projets individuels. Cette section décrit comment accéder à ces champs. 
  
Champs personnalisés ne sont pas inclus dans le jeu de propriétés associées à un projet par défaut. Ainsi, ils doivent identification explicite de la spécification de récupération. La vue de haut niveau du processus se compose des éléments suivants :
  
1. Tunnel pour le champ personnalisé à l’aide de son nom commun.
    
2. Récupérez le nom interne du champ personnalisé.
    
3. Revenez au contexte global et interroger le système en utilisant le nom interne du champ personnalisé.
    
#### <a name="tunnel-to-the-custom-field-retrieve-its-internal-name-and-used-it-to-query-the-system"></a>Tunnel au champ personnalisé et récupérer son nom interne utilisé pour le système de requête

Cette tâche spécifie une récupération qui utilise une propriété par défaut avec un détail ajouté.
  
1. Commencez par utiliser le contexte de projets, comme décrit au début de cet article.
    
   ```cs
    // Get the list of published projects in Project Web App.
    var projects = projContext.Projects;
    
   ```

2. Ajoutez deux éléments à la demande de récupération de collection projets en plus de toutes les autres propriétés par défaut pour récupérer :
    
   ```cs
    projContext.Load(projects,
        ps => ps.IncludeWithDefaultProperties(
            p => p.Phase, p => p.Stage,                  // Other nondefault properties
            p => p.IncludeCustomFields,                  // Gets PublishedProject object 
                                                        // that contains custom fields
            p => p.IncludeCustomFields.CustomFields));   // Populates the custom fields
                    projContext.ExecuteQuery();
    
   ```

   Le `p => p.IncludeCustomFields` clause identifie la nécessité d’utiliser un objet project qui prend en charge les champs personnalisés. 
    
   Le `p => p.IncludeCustomFields.CustomFields` clause demande l’inclusion de données de champ personnalisé dans le résultat de requête. Cette information est utilisée après que le nom interne de champ personnalisé est extrait. 
    
3. Charger à la demande.
    
   Cela fait partie de l’étape précédente.
    
4. Exécuter la requête.
    
   ```cs
    projContext.ExecuteQuery()
   ```

5. Ces informations sur le client, de créer une demande pour récupérer les champs personnalisés associés au projet actuel.
    
   ```cs
    foreach (PublishedProject pubProj in projContext.Projects)
    {
        //Console.WriteLine("\n\t{0}. \t{1} \n\t\t{2} \n\t\t{3} \n", 
                j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
        CustomFieldCollection collCustF = pubProj.CustomFields;
                        
        projContext.Load(collCustF);
        projContext.ExecuteQuery();
    
   ```

6. Recherchez les champs personnalisés appropriée et extraire le nom interne du champ. 
    
   ```cs
        foreach (CustomField oCF in collCustF)
        {
            if (oCF.Name == "Project Health")
            {
                Console.WriteLine("Name: {0}", oCF.Name);
                Console.WriteLine("InternalName: {0}", oCF.InternalName);
    
   ```

   Le nom interne du champ personnalisé est extrait. Éléments de haut niveau 1 et 2 sont maintenant terminées.
    
7. Retournez dans le contexte du projet et récupérer la valeur du champ personnalisé.
    
   ```cs
    Console.WriteLine("Value: {0}", 
        pubProj.IncludeCustomFields.FieldValues[oCF.InternalName]);
    
   ```

   > [!NOTE]
   > La valeur du champ personnalisé est extraite en utilisant le nom interne sous forme d’index. 
  
Sortie de trois projets constituée de l’ID de projet, nom du projet, nom de champ personnalisé, nom interne de champ personnalisé et valeur de champ personnalisé.
  
```cs
Project counts:31
1. Project ID:  957d5fcd-5cbf-e111-9f1e-00155d022681
        Name:           Acquisition Target Analysis
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Green
2. Project ID:  16905202-5fbf-e111-9f1e-00155d022681
        Name:           Apparel ERP Upgrade
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Green
3. Project ID:  dce23152-63bf-e111-9f1e-00155d022681
        Name:           Audit Tracking Solution
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Red

```

## <a name="see-also"></a>Voir aussi

Pour la documentation et des exemples relatifs à Project Online et développement d’applications à l’aide de CSOM, voir le [Portail de développement Project](https://developer.microsoft.com/en-us/project).
    

