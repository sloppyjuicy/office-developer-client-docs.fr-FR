---
title: Prise en main du modèle CSOM Project Server et de .NET
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5ce73baa-dfb6-41d0-918d-b0c3a498815f
description: Vous pouvez utiliser le modèle objet côté client de Project Server 2013 (CSOM) pour développer des solutions Project Online et sur site avec le .NET Framework 4. Cet article explique comment créer une application console qui utilise le modèle pour créer et publier des projets. Après la publication d’un projet, l’application attend que le Service de file d’attente de Project Server terminer l’action de publication, puis répertorie les projets publiés.
ms.openlocfilehash: f4e40cb3165bb2b3caf05b01736d90c21b6ac881
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401739"
---
# <a name="getting-started-with-the-project-server-csom-and-net"></a>Prise en main du modèle CSOM Project Server et de .NET

Vous pouvez utiliser le modèle objet côté client de Project Server 2013 (CSOM) pour développer des solutions Project Online et sur site avec le .NET Framework 4. Cet article explique comment créer une application console qui utilise le modèle pour créer et publier des projets. Après la publication d’un projet, l’application attend que le Service de file d’attente de Project Server terminer l’action de publication, puis répertorie les projets publiés.
  
Pour une présentation générale de Project Server CSOM, voir [mises à jour pour les développeurs dans Project 2013](updates-for-developers-in-project-2013.md). Les rubriques de référence dans l’espace de noms CSOM, voir [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
  
## <a name="creating-a-csom-project-in-visual-studio"></a>Création d’un projet CSOM dans Visual Studio
<a name="pj15_GettingStartedCSOM_CreatingVSProject"> </a>

Vous pouvez utiliser Visual Studio 2010 ou Visual Studio 2012 pour développer des solutions qui utilisent le Project Server CSOM. Project Server CSOM inclut trois assemblys pour le développement d’applications clientes, des applications Microsoft Silverlight et des applications Windows Phone 8 à l’aide de .NET Framework 4. Le modèle CSOM inclut également un fichier JavaScript pour le développement d’applications web, comme décrit dans [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
  
Vous pouvez copier l’assembly CSOM dont vous avez besoin de l’ordinateur Project Server ou à partir du téléchargement du Kit de développement Project 2013 sur un ordinateur de développement à distance. L’application de console **QueueCreateProject** qui est décrite dans cette rubrique n’est pas une application Silverlight ou une application Windows Phone 8, vous devez l’assembly Microsoft.ProjectServer.Client.dll. Étant donné que le modèle est indépendant de la basées sur ASMX ou WCF Project Server Interface (PSI), il est inutile définir des références de service de l’interface PSI ou utiliser l’espace de noms **Microsoft.Office.Project.Server.Library** . 
  
L’application **QueueCreateProject** utilise des arguments de ligne de commande pour le nom du projet à créer et pour le délai d’expiration de la file d’attente. Dans la procédure 1, vous créez l’application console de base, ajoutez une routine pour analyser la ligne de commande et ajoutez un message d’utilisation s’il existe des erreurs dans la ligne de commande. 
  
### <a name="procedure-1-to-create-a-csom-project-in-visual-studio"></a>Procédure 1. Pour créer un projet SCOM dans Visual Studio

1. Copiez l’assembly Microsoft.ProjectServer.Client.dll à partir de la `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\` dossier sur votre ordinateur de développement. Copiez l’assembly dans un dossier pour les autres Project Server et les assemblys de référence SharePoint que vous utiliserez, tel que `C:\Project\Assemblies`.
    
2. Copiez l’assembly Microsoft.SharePoint.Client.dll et l’assembly Microsoft.SharePoint.Client.Runtime.dll du même dossier source vers votre ordinateur de développement. L’assembly Microsoft.ProjectServer.Client.dll possède des dépendances sur les assemblys SharePoint associés.
    
3. Dans Visual Studio, créez une application de console Windows et définir le framework cible sur .NET Framework 4. Par exemple, nom de l’application QueueCreateProject.
    
   > [!NOTE]
   > Si vous oubliez de définir la cible correcte, une fois que Visual Studio crée le projet, ouvrez **QueueCreateProject propriétés** dans le menu **Projet**. Sous l’onglet **Application**, dans la liste déroulante **Framework cible**, choisissez **.NET Framework 4**. N’utilisez pas le **profil client .NET Framework 4**. 
  
4. Dans l’Explorateur de solutions, définissez des références aux assemblys suivants :
    
   - Microsoft.ProjectServer.Client.dll
   - Microsoft.SharePoint.Client.dll
   - Microsoft.SharePoint.Client.Runtime.dll
    
5. Dans le fichier Program.cs, modifiez le `using` instructions, comme suit. 
    
   ```cs
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using Microsoft.ProjectServer.Client;
   ```

6. Ajoutez des méthodes pour analyser les arguments de ligne de commande pour le nom du projet et le nombre de secondes du délai d’expiration de la file d’attente, afficher les informations sur l’utilisation et quitter l’application. Remplacez le corps principal du code du fichier Program.cs par le code suivant.
    
   ```cs
    namespace QueueCreateProject
    {
        class Program
        {
            static void Main(string[] args)
            {
                if (!ParseCommandLine(args))
                {
                    Usage();
                    ExitApp();
                }
                /* Add calls to methods here to get the project context and create a project. */
                ExitApp();
            }
            // Parse the command line. Return true if there are no errors.
            private static bool ParseCommandLine(string[] args)
            {
                bool error = false;
                int argsLen = args.Length;
                try
                {
                    for (int i = 0; i < argsLen; i++)
                    {
                        if (error) break;
                        if (args[i].StartsWith("-") || args[i].StartsWith("/"))
                            args[i] = "*" + args[i].Substring(1).ToLower();
                        switch (args[i])
                        {
                            case "*projname":
                            case "*n":
                                if (++i >= argsLen) return false;
                                projName = args[i];
                                break;
                            case "*timeout":
                            case "*t":
                                if (++i >= argsLen) return false;
                                timeoutSeconds = Convert.ToInt32(args[i]);
                                break;
                            case "*?":
                            default:
                                error = true;
                                break;
                        }
                    }
                }
                catch (FormatException)
                {
                    error = true;
                }
                if (string.IsNullOrEmpty(projName)) error = true;
                return !error;
            }
            private static void Usage()
            {
                string example = "Usage: QueueCreateProject -projName | -n \"New project name\" [-timeout | -t sec]";
                example += "\nExample: QueueCreateProject -n \"My new project\"";
                example += "\nDefault timeout seconds = " + timeoutSeconds.ToString();
                Console.WriteLine(example);
            }
            private static void ExitApp()
            {
                Console.Write("\nPress any key to exit... ");
                Console.ReadKey(true);
                Environment.Exit(0);
            }
        }
    }
   ```

## <a name="getting-the-project-context"></a>Obtenir le contexte de projet
<a name="pj15_GettingStartedCSOM_GettingContext"> </a>

Développement de CSOM nécessite l’objet **ProjectContext** pour être initialisé avec l’URL Project Web App. Le code de procédure 2 utilise la constante **pwaPath** . Si vous prévoyez d’utiliser l’application de plusieurs instances de Project Web App, vous pouvez rendre **pwaPath** une variable et ajouter un autre argument de ligne de commande. 
  
### <a name="procedure-2-to-get-the-project-context"></a>Procédure 2. Pour obtenir le contexte de projet

1. Ajouter des variables qui utilise l’application **QueueCreateProject** et les constantes de classe de **programme** . Outre l’URL Project Web App, l’application utilise le nom du type de projet d’entreprise par défaut (TPE), le nom du projet pour créer et un délai d’expiration maximal de file d’attente en secondes. Dans ce cas, la variable **timeoutSeconds** vous permet de tester l’application d’affecter des valeurs différentes pour le délai d’attente. L’objet **ProjectContext** est l’objet principal pour l’accès aux CSOM. 
    
   ```cs
    private const string pwaPath = "https://ServerName /pwa/"; // Change the path to your Project Web App instance.
    private static string basicEpt = "Enterprise Project";   // Basic enterprise project type.
    private static string projName = string.Empty;
    private static int timeoutSeconds = 10;  // The maximum wait time for a queue job, in seconds.
    private static ProjectContext projContext;
   ```

2. Remplacez le `/* Add calls to methods here to get the project context and create a project. */` commentaire par le code suivant. L’objet **Microsoft.ProjectServer.Client.ProjectContext** est initialisée avec l’URL Project Web App. La méthode **CreateTestProject** et la méthode **ListPublishedProjects** sont indiqués dans la procédure 4 et 5 de la procédure. 
    
   ```cs
    projContext = new ProjectContext(pwaPath);
    if (CreateTestProject())
        ListPublishedProjects();
    else
        Console.WriteLine("\nProject creation failed: {0}", projName);
   ```

## <a name="getting-an-enterprise-project-type"></a>Obtenir un type de projet d’entreprise
<a name="pj15_GettingStartedCSOM_GettingEPT"> </a>

L’exemple d’application **QueueCreateProject** sélectionne explicitement le type de projet d’entreprise (EPT), pour représenter la manière dont une application peut sélectionner le type d’un projet. Si les informations de création du projet ne spécifient pas le GUID EPT, une application utilise la valeur EPT par défaut. La méthode **GetEptUid** est utilisée par la méthode **CreateTestProject** décrite dans la procédure 4. 
  
La méthode **GetEptUid** interroge l’objet **ProjectContext** pour la collection de **EnterpriseProjectTypes** où le nom EPT est égal au nom spécifié. Après l’exécution de la requête, la variable **eptUid** est définie sur le GUID du premier objet **EnterpriseProjectType** de la collection **eptList**. Étant donné que les noms EPT sont uniques, un seul objet **EnterpriseProjectType** a le nom spécifié. 
  
### <a name="procedure-3-to-get-the-guid-of-an-ept-for-a-new-project"></a>Procédure 3. Pour obtenir le GUID d’un EPT pour un nouveau projet

- Ajoutez la méthode **GetEptUid** à la classe **Program**. 
    
   ```cs
    // Get the GUID of the specified enterprise project type.
    private static Guid GetEptUid(string eptName)
    {
        Guid eptUid = Guid.Empty;
        try
        {
            // Get the list of EPTs that have the specified name. 
            // If the EPT name exists, the list will contain only one EPT.
            var eptList = projContext.LoadQuery(
                projContext.EnterpriseProjectTypes.Where(
                    ept => ept.Name == eptName));
            projContext.ExecuteQuery();
            eptUid = eptList.First().Id;
        }
        catch (Exception ex)
        {
            string msg = string.Format("GetEptUid: eptName = \"{0}\"\n\n{1}",
                eptName, ex.GetBaseException().ToString());
            throw new ArgumentException(msg);
        }
        return eptUid;
    }
   ```

Vous pouvez trouver le GUID EPT de plusieurs manières. La requête affichée dans la méthode **GetEptUid** est efficace , car elle télécharge uniquement l’objet **EnterpriseProjectType** qui correspond au nom EPT. La routine secondaire suivante est moins efficace, car elle télécharge la liste complète des EPT dans l’application cliente et parcourt la liste. 

```cs
foreach (EnterpriseProjectType ept in projSvr.EnterpriseProjectTypes)
{
    if (ept.Name == eptName)
    {
        eptUid = ept.Id;
        break;
    }
}
```

La routine suivante utilise une requête LINQ et une expression lambda pour sélectionner l’objet EPT, mais télécharge toujours tous les objets **EnterpriseProjectType**. 

```cs
var eptList = projContext.LoadQuery(projContext.EnterpriseProjectTypes);
projContext.ExecuteQuery();
eptUid = eptList.First(ept => ept.Name == eptName).Id;
```

## <a name="setting-the-creation-information-and-publishing-the-project"></a>Définir les informations de création et publier le projet
<a name="pj15_GettingStartedCSOM_ProjectCreation"> </a>

La méthode **CreateTestProject** crée un objet **ProjectCreationInformation** et spécifie les informations nécessaires pour créer un projet. Le nom et le GUID du projet sont requis. La date de début, la description du projet et le GUID EPT sont facultatifs. 
  
Après avoir défini les nouvelles propriétés de projet, la méthode **Projects.Add** ajoute le projet à la collection **Projects**. Pour enregistrer et publier le projet, vous devez appeler la méthode **Projects.Update** pour envoyer un message dans la file d’attente Project Server et créer le projet. 
  
### <a name="procedure-4-to-set-the-new-project-properties-create-the-project-and-publish-the-project"></a>Procédure 4. Pour définir les nouvelles propriétés du projet, créez et publiez le projet.

1. Ajoutez la méthode **CreateTestProject** à la classe **Program**. Le code suivant crée et publie un projet, mais n’attend pas la fin du travail de file d’attente. 
    
   ```cs
    // Create a project.
    private static bool CreateTestProject()
    {
        bool projCreated = false;
        try
        {
            Console.Write("\nCreating project: {0} ...", projName);
            ProjectCreationInformation newProj = new ProjectCreationInformation();
            newProj.Id = Guid.NewGuid();
            newProj.Name = projName;
            newProj.Description = "Test creating a project with CSOM";
            newProj.Start = DateTime.Today.Date;
            // Setting the EPT GUID is optional. If no EPT is specified, Project Server  
            // uses the default EPT. 
            newProj.EnterpriseProjectTypeId = GetEptUid(basicEpt);
            PublishedProject newPublishedProj = projContext.Projects.Add(newProj);
            QueueJob qJob = projContext.Projects.Update();
            /* Add code here to wait for the queue. */
        }
        catch(Exception ex)
        {
            Console.ForegroundColor = ConsoleColor.Red;
            Console.WriteLine("\nError: {0}", ex.Message);
            Console.ResetColor();
        }
        return projCreated;
    }
   ```

2. Remplacez le `/* Add code here to wait for the queue. */` commentaire par le code suivant pour attendre le travail en file d’attente. La routine attend un maximum de nombre de secondes spécifié **timeoutSeconds** ou se poursuit si le travail en file d’attente soit terminée avant le délai d’attente. Pour les États de travail de file d’attente possibles, voir [Microsoft.ProjectServer.Client.JobState](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.JobState.aspx) . 
    
   L’appel de la méthode **Load** et de la méthode **ExecuteQuery** pour l’objet **QueueJob** est facultatif. Si l’objet **QueueJob** n’est pas initialisé lorsque vous appelez la méthode **WaitForQueue**, Project Server l’initialise. 
    
   ```cs
    // Calling Load and ExecuteQuery for the queue job is optional.
    // projContext.Load(qJob);
    // projContext.ExecuteQuery();
    JobState jobState = projContext.WaitForQueue(qJob, timeoutSeconds);
    if (jobState == JobState.Success)
    {
        projCreated = true;
    }
    else
    {
        Console.ForegroundColor = ConsoleColor.Yellow;
        Console.WriteLine("\nThere is a problem in the queue. Timeout is {0} seconds.", 
            timeoutSeconds);
        Console.WriteLine("\tQueue JobState: {0}", jobState.ToString());
        Console.ResetColor();
    }
    Console.WriteLine();
   ```

## <a name="listing-the-published-projects"></a>Liste des projets publiés
<a name="pj15_GettingStartedCSOM_ListingPublished"> </a>

La méthode **ListPublishedProjects** Obtient la collection de tous les projets sont publiés dans Project Web App. Si le travail en file d’attente qui crée un projet dans la procédure 4 ne se termine pas correctement ou arrive à expiration, le nouveau projet n’est pas inclus dans la collection de **projets** . 
  
### <a name="procedure-5-to-list-the-published-projects"></a>Procédure 5. Pour répertorier les projets publiés

1. Ajoutez la méthode **ListPublishedProjects** à la classe **Program**. 
    
   ```cs
    // List the published projects.
    private static void ListPublishedProjects()
    {
        // Get the list of projects on the server.
        projContext.Load(projContext.Projects);
        projContext.ExecuteQuery();
        Console.WriteLine("\nProject ID : Project name : Created date");
        foreach (PublishedProject pubProj in projContext.Projects)
        {
            Console.WriteLine("\n\t{0} :\n\t{1} : {2}", pubProj.Id.ToString(), pubProj.Name,
                pubProj.CreatedDate.ToString());
        }
    }
   ```

2. Définir la valeur correcte pour votre URL Project Web App, compilez l’application **QueueCreateProject** , puis tester l’application, comme dans les 6 de la procédure. 
    
## <a name="testing-the-queuecreateproject-application"></a>Test de l’application QueueCreateProject
<a name="pj15_GettingStartedCSOM_Testing"> </a>

Lors de la première exécution de l’application **QueueCreateProject** sur une instance de test de Project Web App, surtout si Project Server est installé sur un ordinateur virtuel, l’application peut nécessiter plus de temps à exécuter que le délai d’attente de la file d’attente par défaut de dix secondes. 
  
### <a name="procedure-6-to-test-the-queuecreateproject-application"></a>Procédure 6. Pour tester l’application QueueCreateProject

1. Ouvrir la fenêtre **Propriétés QueueCreateProject** , sélectionnez l’onglet **Déboguer** , puis ajoutez les arguments de ligne de commande suivantes dans la section **Options de démarrage** :`-n "Test proj 1" -t 20`
    
   Exécuter l’application (par exemple, appuyez sur **F5**). Si la valeur du délai d’attente est assez long, l’application affiche la sortie suivante (en présence d’autres projets publiés dans votre instance Project Web App, elles sont également être affichées) :
    
   ```MS-DOS
    Creating project: Test proj 1 ...
    Project ID : Project name : Created date
            b34d7009-753f-4abb-9191-f4b15a82aac3 :
            Test proj 1 : 9/22/2011 11:27:57 AM
    Press any key to exit...
   ```

2. Exécutez le test d’une autre avec les arguments de ligne de commande suivants, pour utiliser le délai d’attente de la file d’attente de 10 secondes par défaut :`-n "Test proj 1"`
    
   Étant donné que le projet de test 1 existe déjà, l’application affiche le résultat suivant.
    
   ```MS-DOS
    Creating project: Test proj 1 ...
    Error: PJClientCallableException: ProjectNameAlreadyExists
    ProjectNameAlreadyExists
    projName = Test proj 1
    Project creation failed: Test proj 1
    Press any key to exit...
   ```

3. Exécutez le test d’une autre avec les arguments de ligne de commande suivants, pour utiliser le délai d’attente de la file d’attente de 10 secondes par défaut :`-n "Test proj 2"`
    
   L’application **QueueCreateProject** crée et publie le projet nommé Projet de test 2. 
    
4. Exécutez un autre test avec les arguments de ligne de commande suivants et définir le délai d’attente pour être trop court pour le travail de file d’attente à la fin :`-n "Test proj 3" -t 1`
    
   Étant donné que le délai d’expiration de file d’attente est trop court, le projet n’est pas créé. L’application affiche le résultat suivant.
    
   ```MS-DOS
    Creating project: Test proj 3 ...
    There is a problem in the queue. Timeout is 1 seconds.
            Queue JobState: Unknown
    Project creation failed: Test proj 3
    Press any key to exit...
   ```

5. Modifier le code afin que l’application n’attend pas le travail en file d’attente. Par exemple, commentez le code qui attend que la file d’attente, à l’exception de la `projCreated = true` de ligne, comme suit. 
    
   ```cs
    //JobState jobState = projContext.WaitForQueue(qJob, timeoutSeconds);
    //if (jobState == JobState.Success)
    //{
    projCreated = true;
    //}
    //else
    //{
    //    Console.ForegroundColor = ConsoleColor.Yellow;
    //    Console.WriteLine("\nThere is a problem in the queue. Timeout is {0} seconds.",
    //        timeoutSeconds);
    //    Console.WriteLine("\tQueue JobState: {0}", jobState.ToString());
    //    Console.ResetColor();
    //}
    
   ```

6. Recompiler l’application et exécutez une autre test avec les arguments de ligne de commande suivants :`-n "Test proj 4"`
    
   Étant donné que la routine **WaitForQueue** est commentée, l’application n’utilise pas la valeur de délai d’expiration par défaut. Bien que l’application n’attende pas la file d’attente, elle peut afficher Projet de test 4 si l’action de publication dans Project Server est suffisamment rapide. 
    
   ```MS-DOS
    Creating project: Test proj 4 ...
    Project ID : Project name : Created date
            cdd54103-082f-425c-b075-9ff52ac7d4e6 :
            Test proj 2 : 9/25/2011 4:28:55 PM
            b34d7009-753f-4abb-9191-f4b15a82aac3 :
            Test proj 1 : 9/22/2011 11:27:57 AM
            5c0c73f2-f5dd-499b-8bd8-ebb74bf8c122 :
            Test proj 4 : 9/25/2011 4:39:21 PM
    Press any key to exit...
   ```

Actualisez la page Centre de projets dans Project Web App (`https://ServerName/ProjectServerName/Projects.aspx`), pour afficher les projets publiés. La figure suivante montre que les projets de test sont publiés.

**Vérification des projets publiés dans Project Web App**

![Vérification des projets publiés dans Project Web App] (media/pj15_GetStartedCSOMNET_pwa.gif "Vérification des projets publiés dans Project Web App")
  
L’exemple d’application **QueueCreateProject** présente un exemple typique de création d’une entité de projet avec le modèle à l’aide de la classe **ProjectCreationInformation** , comment ajouter le projet à la collection publiée, l’attente d’un travail de file d’attente par à l’aide de la méthode **WaitForQueue** et comment énumérer la collection de projets publiés. 
  
## <a name="complete-code-example"></a>Exemple de code complet
<a name="pj15_GettingStartedCSOM_CompleteCode"> </a>

Voici le code complet de l’exemple d’application **QueueCreateProject** . La référence de classe [Microsoft.ProjectServer.Client.ProjectCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectCreationInformation.aspx) inclut également le code dans cette rubrique. 
  
```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Microsoft.ProjectServer.Client;
namespace QueueCreateProject
{
    class Program
    {
        private const string pwaPath = "https://ServerName /pwa/"; // Change the path to your Project Web App instance.
        private static string basicEpt = "Enterprise Project";   // Basic enterprise project type.
        private static string projName = string.Empty;
        private static int timeoutSeconds = 10;  // The maximum wait time for a queue job, in seconds.
        private static ProjectContext projContext;
        static void Main(string[] args)
        {
            if (!ParseCommandLine(args))
            {
                Usage();
                ExitApp();
            }
            projContext = new ProjectContext(pwaPath);
            if (CreateTestProject())
                ListPublishedProjects();
            else
                Console.WriteLine("\nProject creation failed: {0}", projName);
            ExitApp();
        }
        // Create a project.
        private static bool CreateTestProject()
        {
            bool projCreated = false;
            try
            {
                Console.Write("\nCreating project: {0} ...", projName);
                ProjectCreationInformation newProj = new ProjectCreationInformation();
                newProj.Id = Guid.NewGuid();
                newProj.Name = projName;
                newProj.Description = "Test creating a project with CSOM";
                newProj.Start = DateTime.Today.Date;
                // Setting the EPT GUID is optional. If no EPT is specified, Project Server uses 
                // the default EPT. 
                newProj.EnterpriseProjectTypeId = GetEptUid(basicEpt);
                PublishedProject newPublishedProj = projContext.Projects.Add(newProj);
                QueueJob qJob = projContext.Projects.Update();
                // Calling Load and ExecuteQuery for the queue job is optional. If qJob is 
                // not initialized when you call WaitForQueue, Project Server initializes it.
                // projContext.Load(qJob);
                // projContext.ExecuteQuery();
                JobState jobState = projContext.WaitForQueue(qJob, timeoutSeconds);
                if (jobState == JobState.Success)
                {
                    projCreated = true;
                }
                else
                {
                    Console.ForegroundColor = ConsoleColor.Yellow;
                    Console.WriteLine("\nThere is a problem in the queue. Timeout is {0} seconds.", 
                        timeoutSeconds);
                    Console.WriteLine("\tQueue JobState: {0}", jobState.ToString());
                    Console.ResetColor();
                }
                Console.WriteLine();
            }
            catch(Exception ex)
            {
                Console.ForegroundColor = ConsoleColor.Red;
                Console.WriteLine("\nError: {0}", ex.Message);
                Console.ResetColor();
            }
            return projCreated;
        }
        // Get the GUID of the specified enterprise project type.
        private static Guid GetEptUid(string eptName)
        {
            Guid eptUid = Guid.Empty;
            try
            {
                // Get the list of EPTs that have the specified name. 
                // If the EPT name exists, the list will contain only one EPT.
                var eptList = projContext.LoadQuery(
                    projContext.EnterpriseProjectTypes.Where(
                        ept => ept.Name == eptName));
                projContext.ExecuteQuery();
                eptUid = eptList.First().Id;
                // Alternate routines to find the EPT GUID. Both (a) and (b) download the entire list of EPTs.
                // (a) Using a foreach block:
                //foreach (EnterpriseProjectType ept in projSvr.EnterpriseProjectTypes)
                //{
                //    if (ept.Name == eptName)
                //    {
                //        eptUid = ept.Id;
                //        break;
                //    }
                //}
                // (b) Querying for the EPT list, and then using a lambda expression to select the EPT:
                //var eptList = projContext.LoadQuery(projContext.EnterpriseProjectTypes);
                //projContext.ExecuteQuery();
                //eptUid = eptList.First(ept => ept.Name == eptName).Id;
            }
            catch (Exception ex)
            {
                string msg = string.Format("GetEptUid: eptName = \"{0}\"\n\n{1}",
                    eptName, ex.GetBaseException().ToString());
                throw new ArgumentException(msg);
            }
            return eptUid;
        }
        // List the published projects.
        private static void ListPublishedProjects()
        {
            // Get the list of projects on the server.
            projContext.Load(projContext.Projects);
            projContext.ExecuteQuery();
            Console.WriteLine("\nProject ID : Project name : Created date");
            foreach (PublishedProject pubProj in projContext.Projects)
            {
                Console.WriteLine("\n\t{0} :\n\t{1} : {2}", pubProj.Id.ToString(), pubProj.Name,
                    pubProj.CreatedDate.ToString());
            }
        }
        // Parse the command line. Return true if there are no errors.
        private static bool ParseCommandLine(string[] args)
        {
            bool error = false;
            int argsLen = args.Length;
            try
            {
                for (int i = 0; i < argsLen; i++)
                {
                    if (error) break;
                    if (args[i].StartsWith("-") || args[i].StartsWith("/"))
                        args[i] = "*" + args[i].Substring(1).ToLower();
                    switch (args[i])
                    {
                        case "*projname":
                        case "*n":
                            if (++i >= argsLen) return false;
                            projName = args[i];
                            break;
                        case "*timeout":
                        case "*t":
                            if (++i >= argsLen) return false;
                            timeoutSeconds = Convert.ToInt32(args[i]);
                            break;
                        case "*?":
                        default:
                            error = true;
                            break;
                    }
                }
            }
            catch (FormatException)
            {
                error = true;
            }
            if (string.IsNullOrEmpty(projName)) error = true;
            return !error;
        }
        private static void Usage()
        {
            string example = "Usage: QueueCreateProject -projName | -n \"New project name\" [-timeout | -t sec]";
            example += "\nExample: QueueCreateProject -n \"My new project\"";
            example += "\nDefault timeout seconds = " + timeoutSeconds.ToString();
            Console.WriteLine(example);
        }
        private static void ExitApp()
        {
            Console.Write("\nPress any key to exit... ");
            Console.ReadKey(true);
            Environment.Exit(0);
        }
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Mises à jour pour les développeurs Project 2013](updates-for-developers-in-project-2013.md) 
- [Modèle objet côté client (CSOM) pour Project 2013](client-side-object-model-csom-for-project-2013.md)
    

