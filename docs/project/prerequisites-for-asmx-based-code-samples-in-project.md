---
title: Conditions préalables pour les exemples de code basées sur ASMX dans Project
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- code samples
- Project Server code samples
- Project Server programming
- PSI code samples
- PSI programming
keywords:
- exemples de code, le serveur de project, Project Server, programmation, PSI, compilation des exemples de code, PSI, programmation
localization_priority: Normal
ms.assetid: df584b25-4460-46c8-89a8-3b2c94d20bba
description: Découvrez des informations pour vous aider à créer des projets dans Visual Studio en utilisant les exemples de code basées sur ASMX qui sont inclus dans les rubriques de référence d’Interface de Project Server (PSI).
ms.openlocfilehash: 73d097211dc3c68e1066c2ea1ad8d51a616184d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787935"
---
# <a name="prerequisites-for-asmx-based-code-samples-in-project"></a>Conditions préalables pour les exemples de code basées sur ASMX dans Project

Découvrez des informations pour vous aider à créer des projets dans Visual Studio en utilisant les exemples de code basées sur ASMX qui sont inclus dans les rubriques de référence d’Interface de Project Server (PSI).
  
De nombreux exemples de code inclus dans la [référence de classe Project Server 2013 service web et de bibliothèque](http://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) ont été créés pour le Kit de développement Office Project 2007 et utilisent un format standard pour les services web ASMX. Les exemples de toujours utiliser dans Project Server 2013 et sont conçus pour être copiés dans une application de console et exécuter en tant qu’une unité complète. Exceptions sont indiquées dans l’exemple. 
  
Nouveaux exemples PSI dans le Kit de développement Project 2013 est conforme à un format qui utilise les services Windows Communication Foundation (WCF). Les exemples de basées sur ASMX peuvent également être adaptées pour utiliser les services WCF. Cet article explique comment utiliser les exemples avec des services web ASMX. Pour plus d’informations sur l’utilisation des exemples avec les services WCF, consultez [conditions préalables pour les exemples de code basée sur WCF dans le projet](prerequisites-for-wcf-based-code-samples-in-project.md).
  
> [!NOTE]
> L’interface ASMX du service web de la PSI est déconseillé dans Project Server 2013, mais est toujours prise en charge. Si le modèle objet côté client (CSOM) comprend les méthodes requis par votre application, les nouvelles applications doivent être développées avec le modèle CSOM. Le modèle CSOM permet aux applications fonctionner avec Project Online ou une installation locale de Project Server 2013. Sinon, si votre application utilise l’interface PSI, elle doit utiliser l’interface WCF, qui est la technologie que nous recommandons pour les communications réseau. Applications qui utilisent l’interface ASMX ou WCF peuvent fonctionner uniquement pour les installations locales de Project Server 2013. Pour plus d’informations sur le modèle CSOM, voir [architecture de Project Server 2013](project-server-2013-architecture.md) et [modèle d’objet côté Client (CSOM) pour Project 2013](client-side-object-model-csom-for-project-2013.md). 
  
Avant d’exécuter les exemples de code, vous devez configurer l’environnement de développement, configurer l’application et modifier les valeurs de constante génériques correspondant à votre environnement.
  
## <a name="setting-up-the-development-environment"></a>Configuration de l'environnement de développement
<a name="pj15_PrerequisitesASMX_Setup"> </a>

1. **Configurer un système de Project Server de test**.
    
   Utilisez un test système Project Server lorsque vous développez ou de test. Même lorsque votre code fonctionne parfaitement, dépendances interprojets, création de rapports ou d’autres facteurs environnementaux peuvent entraîner des conséquences inattendues. 
    
   > [!NOTE]
   > Assurez-vous que vous êtes un utilisateur valide sur le serveur et vérifiez que vous disposez des autorisations suffisantes pour les appels PSI par votre application. La rubrique de référence pour chaque méthode PSI comprend un tableau d’autorisations Project Server. Par exemple, la méthode [Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) nécessite l’autorisation **NewProject** globale et l’autorisation **SaveProjectTemplate** . 
  
   Dans certains cas, vous devrez effectuer un débogage distant sur le serveur. Vous devrez également configurer un gestionnaire d’événements à l’installation d’un assembly du Gestionnaire d’événements sur chaque ordinateur de Project Server dans la batterie de serveurs SharePoint, puis configurer le Gestionnaire d’événements pour l’instance Project Web App à l’aide de la page Paramètres de Project Server général Paramètres de l’application de l’Administration centrale de SharePoint.
    
2. **Configurer un ordinateur de développement.**
    
   Vous accédez généralement la PSI via un réseau. Les exemples de code sont conçus pour être exécutée sur un client qui est différent du serveur, sauf indication contraire.
    
   1. **Installer la version appropriée de Visual Studio.** Sauf mention contraire, les exemples de code sont écrits en Visual c#. Ils peuvent être utilisés avec Visual Studio 2010 ou Visual Studio 2012. Assurez-vous d’avoir le service pack le plus récent. 
        
   2. **Copiez la DLL de Project Server sur l’ordinateur de développement.** Copiez les assemblys suivants à partir de `[Program Files]\Microsoft Office Servers\15.0\Bin` sur l’ordinateur Project Server sur l’ordinateur de développement : 
        
      - Microsoft.Office.Project.Server.Events.Receivers.dll
      - Microsoft.Office.Project.Server.Library.dll
        
   3. Pour plus d’informations sur la compilation et l’utilisation de l’assembly de proxy ProjectServerServices.dll pour les services web ASMX dans PSI, voir [l’aide d’un assembly de proxy PSI et descriptions IntelliSense](#pj15_PrerequisitesASMX_BuildingProxy).
    
3. **Installez les fichiers IntelliSense.**
    
    Pour utiliser les descriptions IntelliSense pour les classes et membres dans les assemblys de Project Server, copie les fichiers XML IntelliSense mis à jour à partir du Kit de développement Project 2013 téléchargement dans le même répertoire où se trouvent les assemblys de Project Server. Par exemple, copiez le fichier Microsoft.Office.Project.Server.Library.xml dans le répertoire où votre application sera défini une référence à l’assembly Microsoft.Office.Project.Server.Library.dll.
    
    Les descriptions IntelliSense pour les services web PSI requièrent la création d’un assembly de proxy PSI à l’aide du script CompileASMXProxyAssembly.cmd dans les `Documentation\IntelliSense\WSDL` sous-répertoire dans le téléchargement du Kit de développement Project 2013. Le script crée l’assembly de proxy ProjectServerServices.dll basées sur ASMX. Pour plus d’informations, consultez le fichier [ReadMe_IntelliSense] dans le téléchargement SDK. 
    
## <a name="creating-the-application-and-adding-a-web-service-reference"></a>Création de l’application et l’ajout d’une référence de service web
<a name="pj15_PrerequisitesASMX_Configure"> </a>

1. **Créer une application console**.
    
   Lorsque vous créez une application console, dans la liste déroulante de la boîte de dialogue **Nouveau projet** , sélectionnez **.NET Framework 4**. Vous pouvez copier le code d’exemple PSI dans la nouvelle application.
    
2. **Ajoutez la référence requise pour ASMX.**
    
   Dans l’Explorateur de solutions, ajoutez une référence à **System.Web.Services** (voir Figure 1). 
    
   **La figure 1. Ajout d’une référence dans Visual Studio**

   ![Ajout d’une référence dans Visual Studio] (media/pj15_PrerequisitesASMX_AddReference.gif "Ajout d’une référence dans Visual Studio")
  
3. **Copiez le code**.
    
   Copiez l’exemple de code complet dans le fichier Program.cs de l’application console.
    
4. **Définir l’espace de noms pour l’exemple d’application**.
    
   Vous pouvez modifier l’espace de noms répertorié dans la partie supérieure de l’échantillon à l’espace de noms par défaut application, ou modifier l’espace de noms par défaut application correspondant à l’exemple. Vous pouvez modifier l’espace de noms par défaut application en modifiant les propriétés de l’application.
    
   Par exemple, l’exemple de code pour [QueueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx) a l’espace de noms **Microsoft.SDK.Project.Samples.RenameProject**. Si le nom du projet Visual Studio est **RenameProject**, copiez l’espace de noms à partir du fichier Program.cs et puis ouvrez le volet de **Propriétés** de projet (dans le menu **projet** , choisissez **Propriétés RenameProject**). Sous l’onglet **Application** , copiez l’espace de noms dans la zone de texte **par défaut d’espace de noms** . 
    
5. **Définir les références web**.
    
   La plupart des exemples requièrent une référence à une ou plusieurs des services web PSI. Ils sont répertoriés dans l’exemple lui-même ou dans des commentaires qui précèdent l’échantillon. Pour obtenir l’espace de noms correct des références web, vérifiez que tout d’abord définir l’espace de noms par défaut application.
    
   Il existe trois façons d’ajouter une référence de service web ASMX pour l’interface PSI :
    
   - Créer un assembly de proxy PSI nommé ProjectServerServices.dll, puis définir une référence à l’assembly. Pour obtenir IntelliSense, il s’agit de la méthode recommandée pour ajouter une référence de la PSI. Consultez [l’aide d’un assembly de proxy PSI et descriptions IntelliSense](#pj15_PrerequisitesASMX_BuildingProxy).
    
   - Ajoutez un fichier de proxy à partir de la sortie wsdl.exe à la solution Visual Studio. Consultez la rubrique [Ajout d’un fichier de proxy PSI](#pj15_PrerequisitesASMX_AddingProxyFile).
    
   - Ajouter une référence de service web à l’aide de Visual Studio. Consultez la rubrique [Ajout d’un site web de référence de service](#pj15_PrerequisitesASMX_AddingServiceReference).

<a name="pj15_PrerequisitesASMX_BuildingProxy"> </a>

### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>À l’aide d’un assembly de proxy PSI et descriptions IntelliSense

Vous pouvez créer et utiliser l’assembly de proxy ProjectServerServices.dll pour tous les services web basées sur ASMX dans l’interface PSI, à l’aide du script CompileASMXProxyAssembly.cmd dans les `Documentation\IntelliSense\WSDL` dossier du téléchargement du Kit de développement Project 2013. Pour un lien vers le téléchargement, voir la [documentation du développeur Project 2013](project-2013-developer-documentation.md).
  
> [!NOTE]
> Lorsque vous extrayez les fichiers source du proxy de le Source.zip de fichiers, les fichiers dans le `Documentation\IntelliSense\WSDL\Source` dossier sont en cours à la date de publication du téléchargement du Kit de développement Project 2013. Pour générer les fichiers de sources de proxy PSI, exécutez le script GenASMXProxyAssembly.cmd sur l’ordinateur Project Server mis à jour. Les scripts dans les `Documentation\IntelliSense\WCF` dossier ne fonctionnent pas pour les applications basées sur ASMX. Le script GenWCFProxyAssembly.cmd appelle SvcUtil.exe, qui génère des fichiers de code source pour les services WCF. Les fichiers de proxy WCF incluent des attributs différents, l’interface de canal et une classe client pour chaque service PSI. Par exemple, le service de ressources WCF inclut l’interface **ResourceChannel** , l’interface de la **ressource** et la classe **ResourceClient** . Le site web ressources basées sur ASMX inclut la classe de **ressource** avec certaines des propriétés différentes. 
  
Voici le script GenASMXProxyAssembly.cmd qui génère des fichiers de sortie WSDL pour les services web PSI et puis compile l’assembly.
  
```MS-DOS
@echo off
@ECHO ---------------------------------------------------
@ECHO Creating C# files for the ASMX-based proxy assembly
@ECHO ---------------------------------------------------
REM Replace ServerName with the name of the server and 
REM the instance name of Project Web App. Do not use localhost.
(set VDIR=http://ServerName/pwa/_vti_bin/psi)
(set OUTDIR=.\Source)
REM ** Wsdl.exe is the same version in the v6.0A and v7.0A subdirectories. 
(set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe")
if not exist %OUTDIR% (
md %OUTDIR%
)
for /F %%i in (Classlist_asmx.txt) do %WSDL% /nologo /l:CS /namespace:Svc%%i /out:%OUTDIR%\wsdl.%%i.cs %VDIR%/%%i.asmx?wsdl 
@ECHO ----------------------------
@ECHO Compiling the proxy assembly
@ECHO ----------------------------
(set SOURCE=%OUTDIR%\wsdl)
(set CSC=%WINDIR%\Microsoft.NET\Framework64\v4.0.30319\csc.exe)
(set ASSEMBLY_NAME=ProjectServerServices.dll)
%CSC% /t:library /out:%ASSEMBLY_NAME% %SOURCE%*.cs
```

Le script utilise le fichier ClassList_asmx.txt, qui contient la liste des services web qui sont disponibles pour les développeurs tiers.
  
```text
Admin
Archive
Calendar
CubeAdmin
CustomFields
Driver
Events
LoginForms
LoginWindows
LookupTable
Notifications
ObjectLinkProvider
PortfolioAnalyses
Project
QueueSystem
ResourcePlan
Resource
Security
Statusing
TimeSheet
Workflow
WssInterop
```

Les scripts de créent un assembly nommé ProjectServerServices.dll. Éviter la confusion avec ProjectServerServices.dll pour l’assembly basée sur WCF. Les noms d’assemblys sont les mêmes, pour permettre à l’aide de l’assembly avec le fichier ProjectServerServices.xml IntelliSense.
  
L’espace de noms arbitraire créé par les scripts pour les services WCF et les services web ASMX est la même, afin que le fichier ProjectServerServices.xml IntelliSense fonctionne avec l’assembly. Par exemple, l’espace de noms du service de ressource dans l’assembly de proxy basée sur WCF et l’assembly de proxy basées sur ASMX est **SvcResource**. Vous pouvez bien sûr, modifier les noms d’espace de noms — si vous assurer qu’ils correspondent dans l’assembly de proxy et dans le fichier ProjectServerServices.xml IntelliSense.
  
Si un exemple de code utilise un nom différent pour un espace de noms du service web PSI, par exemple **ProjectWebSvc**, pour IntelliSense fonctionne vous devez modifier l’exemple pour utiliser **SvcProject** afin que l’espace de noms correspond à l’assembly de proxy. 
  
L’avantage de l’aide de l’assembly de proxy basées sur ASMX est qu’il inclut toutes les PSI web service espaces de noms ; vous n’êtes pas obligé de créer plusieurs références web. Un autre avantage est que, si vous ajoutez le fichier ProjectServerServices.xml dans le même répertoire où vous définissez une référence à l’assembly de proxy ProjectServerServices.dll, vous pouvez obtenir des descriptions IntelliSense des membres et classes PSI. La figure 2 illustre le texte IntelliSense pour la méthode **Project.QueueCreateProject** . Pour plus d’informations, consultez le fichier [ReadMe_IntelliSense] dans le dossier IntelliSense du téléchargement du Kit de développement Project 2013. 
  
**La figure 2. Utilisation d’IntelliSense pour une méthode dans le service web de projet**

![À l’aide d’Intellisense pour une méthode dans un service PSI] (media/pj15_PrerequisitesASMX_Intellisense.gif "À l’aide d’Intellisense pour une méthode dans un service PSI")
  
Inconvénients liés à l’aide de l’assembly de proxy sont la solution est plus importante que vous devez distribuer et installer l’assembly de proxy avec la solution. Vous devez également utiliser les mêmes espaces de noms qui se trouvent dans l’assembly de proxy et les fichiers IntelliSense, sauf si vous modifiez le script et le fichier ProjectServerServices.xml IntelliSense à utiliser les espaces de noms différents.
  
### <a name="adding-a-psi-proxy-file"></a>Ajout d’un fichier de proxy PSI
<a name="pj15_PrerequisitesASMX_AddingProxyFile"> </a>

Le téléchargement du Kit de développement Project 2013 inclut les fichiers source générés par la commande Wsdl.exe pour l’assembly de proxy. Les fichiers sources se trouvent dans Source.zip dans les `Documentation\IntelliSense\ASMX` sous-répertoire. Au lieu d’une référence à l’assembly de proxy, vous pouvez ajouter une ou plusieurs des fichiers sources pour une solution Visual Studio. Par exemple, après avoir exécuté le script GenASMXProxyAssembly.cmd, ajoutez le fichier wsdl. Fichier Project.cs à la solution. Au lieu d’exécuter le script, vous pouvez exécuter les commandes suivantes pour générer un fichier source unique, par exemple : 
  
```MS-DOS
set VDIR=http://ServerName/ProjectServerName/_vti_bin/psi
set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe"
%WSDL% /nologo /l:cs /namespace:SvcProject /out:wsdl.Project.cs %VDIR%/Project.asmx?wsdl
```

Pour définir un objet **Project** comme une variable de classe nommée **projet**, utilisez le code suivant. La méthode **AddContextInfo** ajoute les informations de contexte à l’objet **project** pour l’authentification Windows et l’authentification basée sur les formulaires. 
  
```cs
private static SvcProject.Project project;
private static SvcLoginForms.LoginForms loginForms =
            new SvcLoginForms.LoginForms();
. . .
public void AddContextInfo()
{
    // Add the Url property.
    project.Url = "http://ServerName /ProjectServerName /_vti_bin/psi/project.asmx";
    // Add Windows credentials.
    project.Credentials = CredentialCache.DefaultCredentials;
    // If Forms authentication is used, add the Project Server cookie.
    project.CookieContainer = loginForms.CookieContainer;
}
```

> [!NOTE]
> Si vous utilisez un assembly de proxy PSI ou ajoutez un fichier de proxy pour une référence de service Project nommé **SvcProject**, vous utiliseriez le même code pour créer un objet **project** . 
  
### <a name="adding-a-web-service-reference"></a>Ajout d’une référence de service web
<a name="pj15_PrerequisitesASMX_AddingServiceReference"> </a>

Si vous ne pas utiliser l’assembly de proxy basées sur ASMX ou ajouter un fichier de sortie WSDL, vous pouvez définir une ou plusieurs références web individuelles. Les étapes suivantes indiquent comment définir une référence web à l’aide de Visual Studio 2012.
  
1. Dans **L’Explorateur de solutions**, cliquez sur le dossier **références** , puis cliquez sur **Ajouter une référence de Service**. 
    
2. Dans la boîte de dialogue **Ajouter une référence de Service** , choisissez **Options avancées**.
    
3. Dans la boîte de dialogue **Paramètres de référence de Service** , choisissez **Ajouter une référence Web**.
    
4. Dans la zone de texte **URL** , tapez `http:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl`, puis appuyez sur **entrée** ou cliquez sur l’icône **accédez** . Si vous avez couche SSL (Secure Sockets) installé, vous devez utiliser le protocole HTTPS au lieu du protocole HTTP. 

   Par exemple, utilisez l’URL suivante pour le service de projet sur la `http://MyServer/pwa` site Project Web App :`http://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`
    
   Ou bien, ouvrez votre navigateur web et accédez à `http://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl`. Enregistrez le fichier dans un répertoire local, tel que `C:\Project\WebServices\ServiceName.wsdl`. Dans la boîte de dialogue **Ajouter une référence Web** pour l' **URL**, tapez le protocole de fichier et le chemin d’accès au fichier. Par exemple, tapez `file://C:\Project\WebServices\Project.wsdl`. 
    
5. Une fois la référence est résolue, tapez le nom de référence dans la zone de texte **nom de la référence Web** . Exemples de code dans la documentation du développeur Project 2013 utilisent le nom de référence standard arbitraire **Svc _ServiceName_**. Par exemple, le service web de projet est nommé **SvcProject** (voir Figure 3). 
    
   **La figure 3. Ajout d’une référence de service web ASMX**

   ![Ajout d’une référence de service web ASMX] (media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "Ajout d’une référence de service web ASMX")
  
Pour les composants d’application qui doivent s’exécuter sur l’ordinateur Project Server, utiliser l’emprunt d’identité, ou disposer d’autorisations élevées, utilisez une référence de service WCF au lieu d’une référence web ASMX. Pour plus d’informations, voir [conditions préalables pour les exemples de code basée sur WCF dans le projet](prerequisites-for-wcf-based-code-samples-in-project.md).
  
## <a name="setting-other-references"></a>Autres références
<a name="pj15_PrerequisitesASMX_OtherReferences"> </a>

Project Server applications utilisent souvent les autres services, tels que des services web de SharePoint Server 2013. Si d’autres services sont nécessaires, elles sont indiquées dans l’exemple.
  
Références locales pour l’exemple de code sont répertoriées dans les instructions **using** en haut de l’exemple : 
  
1. Dans **L’Explorateur de solutions**, cliquez sur le dossier **références** , puis cliquez sur **Ajouter une référence**.
    
2. Cliquez sur **Parcourir**, puis naviguez jusqu'à l’emplacement où vous avez stocké les DLL Project Server que vous avez copié précédemment. Choisissez les DLL que vous avez besoin, puis cliquez sur **OK**.
    
> [!NOTE]
> Assurez-vous que les versions de l’assembly sur votre ordinateur de développement correspond exactement à ceux présents sur l’ordinateur de Project Server cible. 
  
## <a name="using-multiple-authentication"></a>À l’aide de l’authentification multiples
<a name="pj15_PrerequisitesASMX_ClaimsMultiAuth"> </a>

L’authentification des utilisateurs de Project Server sur site, par l’authentification Windows ou l’authentification par formulaires, s’effectue via les revendications dans SharePoint Server 2013. Authentification plusieurs signifie que l’application web sur lequel est mis en service Project Web App prend en charge l’authentification Windows et l’authentification basée sur les formulaires. Si tel est le cas, un appel à un service web ASMX qui utilise l’authentification Windows échoue avec l’erreur suivante, car le processus ne peut pas déterminer le type d’authentification utilisateur :
  
`The server was unable to process the request due to an internal error. . . .`

Pour résoudre le problème pour ASMX, tous les appels aux méthodes PSI doivent être pour une classe dérivée qui est définie pour chaque service web PSI. La classe dérivée doit également utiliser la classe **SvcLoginWindows.LoginWindows** pour obtenir un cookie pour la classe de service PSI dérivée. Dans l’exemple suivant, la classe **ProjectDerived** dérive de la classe **SvcProject.Project** . La classe dérivée ajoute la propriété **EnforceWindowsAuth** et remplace l’en-tête de requête web pour chaque appel à une méthode dans la classe du **projet** . Si la propriété **EnforceWindowsAuth** est **true**, la méthode **GetWebRequest** ajoute un en-tête qui désactive l’authentification par formulaires. Si **EnforceWindowsAuth** a la **valeur false**, l’authentification par formulaires peut s’exécuter.
  
Pour utiliser l’exemple suivant **ASMXLogon_MultiAuth** , créez une application console, suivez les étapes de [Création de l’application et l’ajout d’une référence de service web](#pj15_PrerequisitesASMX_Configure), puis ajoutez le fichier wsdl. Fichier de proxy LoginWindows.cs et le fichier wsdl. Fichier de proxy Project.cs. La méthode **Main** crée l’instance de **projet** de la classe **ProjectDerived** . L’exemple doit utiliser la classe **LoginWindowsDerived** dérivée pour obtenir un objet **CookieContainer** pour le projet **. CookieContainer** propriété, qui le distingue de l’authentification par formulaires à partir de l’authentification Windows. L’objet **project** puis utilisable pour effectuer des appels à une méthode dans la classe **SvcProject.Project** . 
  
> [!NOTE]
> Le service **LoginWindows** est requis uniquement pour les applications ASMX dans un environnement d’authentification. Dans l’exemple **ASMXLogon_MultiAuth** , la méthode **GetLogonCookie** Obtient un cookie pour l’objet **loginWindows** . Le projet **. CookieContainer** propriété est définie sur la valeur **loginWindows.CookieContainer** . 
  
```cs
using System;
using System.Net;
using PSLibrary = Microsoft.Office.Project.Server.Library;
namespace ASMXLogon_MultiAuth
{
    class Program
    {
        private const string PROJECT_SERVER_URL = 
            "http://ServerName/ProjectServerName/_vti_bin/psi/";
        static void Main(string[] args)
        {
            bool isWindowsUser = true;
            // Create an instance of the project object.
            ProjectDerived project = new ProjectDerived();
            project.Url = PROJECT_SERVER_URL + "Project.asmx";
            project.Credentials = CredentialCache.DefaultCredentials;
            try
            {
                // The program works on a Windows-auth-only computer if you comment-out the
                // following line. The line is required for multiple authentication.
                project.CookieContainer = GetLogonCookie();
                project.EnforceWindowsAuth = isWindowsUser;
                // Get a list of all published projects. 
                // Use ReadProjectStatus instead of ReadProjectList,
                // because the permission requirements are lower.
                SvcProject.ProjectDataSet projectDs =
                    project.ReadProjectStatus(Guid.Empty,
                        SvcProject.DataStoreEnum.PublishedStore,
                        string.Empty,
                        (int)PSLibrary.Project.ProjectType.Project);
                Console.WriteLine(string.Format(
                    "There are {0} published projects.", 
                    projectDs.Project.Rows.Count));
            }
            catch (UnauthorizedAccessException ex)
            {
                Console.WriteLine(ex.Message);
            }
            catch (WebException ex)
            {
                Console.WriteLine(ex.Message);
            }
            finally
            {
                Console.Write("Press any key to continue...");
                Console.ReadKey(false);
            }
        }
        private static CookieContainer GetLogonCookie()
        {
            // Create an instance of the loginWindows object.
            LoginWindowsDerived loginWindows = new LoginWindowsDerived();
            loginWindows.EnforceWindowsAuth = true;
            loginWindows.Url = PROJECT_SERVER_URL + "LoginWindows.asmx";
            loginWindows.Credentials = CredentialCache.DefaultCredentials;
            loginWindows.CookieContainer = new CookieContainer();
            if (!loginWindows.Login())
            {
                // Login failed; throw an exception.
                throw new UnauthorizedAccessException("Login failed.");
            }
            return loginWindows.CookieContainer;
        }
    }
    // Derive from LoginWindows class; include additional property and 
    // override the web request header.
    class LoginWindowsDerived : SvcLoginWindows.LoginWindows
    {
        public bool EnforceWindowsAuth { get; set; }
        protected override WebRequest GetWebRequest(Uri uri)
        {
            WebRequest request = base.GetWebRequest(uri);
            if (this.EnforceWindowsAuth)
            {
                request.Headers.Add("X-FORMS_BASED_AUTH_ACCEPTED", "f");
            }
            return request;
        }
    }
    // Derive from Project class; include additional property and 
    // override the web request header.
    class ProjectDerived : SvcProject.Project
    {
        public bool EnforceWindowsAuth { get; set; }
        protected override WebRequest GetWebRequest(Uri uri)
        {
            WebRequest request = base.GetWebRequest(uri);
            if (this.EnforceWindowsAuth)
            {
                request.Headers.Add("X-FORMS_BASED_AUTH_ACCEPTED", "f");
            }
            return request;
        }
    }
}
```

À l’aide de la classe dérivée de **LoginWindows** et l’émission d’appels PSI avec un en-tête de requête web qui désactive l’authentification par formulaires, sont requis pour les applications qui s’exécutent dans un environnement d’authentification. Si Project Server utilise uniquement l’authentification basée sur les revendications, il n’est pas nécessaire de dériver une classe qui ajoute un en-tête de requête web. L’exemple précédent s’exécute dans les deux environnements. 
  
Le correctif pour une application basée sur WCF est différent. Pour plus d’informations, consultez la section *à l’aide de l’authentification multiples* dans les [conditions préalables pour les exemples de code basée sur WCF dans Project](prerequisites-for-wcf-based-code-samples-in-project.md).
  
## <a name="changing-the-values-of-generic-constants"></a>Modification des valeurs des constantes génériques
<a name="pj15_PrerequisitesASMX_ChangeValues"> </a>

La plupart des exemples ont une ou plusieurs variables que vous devez mettre à jour pour l’exemple de fonctionner correctement dans votre environnement. Dans l’exemple suivant, si vous avez installé SSL, utilisez le protocole HTTPS au lieu du protocole HTTP. Remplacez _ServerName_ par le nom du serveur que vous utilisez. Remplacez _ProjectServerName_ par le nom du répertoire virtuel de votre site Project Server, tels que PWA. 
  
```cs
const string PROJECT_SERVER_URI = "http://ServerName/ProjectServerName/";
```

Toutes les variables que vous devez modifier ou autres conditions préalables sont indiquées dans la partie supérieure de l’exemple de code.
  
## <a name="verifying-the-results"></a>Vérification des résultats
<a name="pj15_PrerequisitesASMX_Verify"> </a>

Obtention et l’interprétation des résultats à partir d’un exemple de code ne sont pas toujours simple. Par exemple, si vous créez un projet, vous devez publier le projet avant d’apparaître dans la page Centre de projets dans Project Web App.
  
Vous pouvez vérifier les résultats des exemples de code de plusieurs façons, par exemple :
  
- Utilisez le client Project Professional 2013 pour ouvrir le projet à partir de l’ordinateur Project Server et afficher les éléments que vous souhaitez.
    
- Afficher les projets publiés sur la page Centre de projets de Project Web App ( `http://ServerName/ProjectServerName/projects.aspx`).
    
- Afficher le journal de file d’attente dans Project Web App. Ouvrez la page Paramètres du serveur (dans le coin supérieur droit, choisissez l’icône **paramètres** ), puis cliquez sur **Mes travaux en file d’attente** sous la section **Paramètres personnels** ( `http://ServerName/ProjectServerName/MyJobs.aspx`). Dans la liste déroulante **affichage** , vous pouvez trier par l’état du travail. L’état par défaut est **en cours et l’échec des travaux de la semaine**. 
    
- Utilisez la page Paramètres du serveur dans Project Web App ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) pour gérer tous les travaux en file d’attente et de supprimer ou de forcer l’archivage des objets d’entreprise. Vous devez disposer des autorisations d’administration pour accéder à ces liens dans la page Paramètres du serveur.
    
- **Microsoft SQL Server Management Studio** permet d’exécuter une requête sur une table dans la base de données de projet. Par exemple, utilisez la requête suivante pour sélectionner les 200 premières lignes de la publication. Table MSP_WORKFLOW_STAGE_PDPS pour afficher des informations sur le projet de pages de détails (PDP) dans les étapes de flux de travail. 
    
   ```sql
    SELECT TOP 200 [STAGE_UID]
            ,[PDP_UID]
            ,[PDP_NAME]
            ,[PDP_POSITION]
            ,[PDP_ID]
            ,[PDP_STAGE_DESCRIPTION]
            ,[PDP_REQUIRES_ATTENTION]
        FROM [ProjectService].[pub].[MSP_WORKFLOW_STAGE_PDPS]
   ```

## <a name="cleaning-up"></a>Nettoyage
<a name="pj15_PrerequisitesASMX_Cleanup"> </a>

Après avoir testé des exemples de code, des objets d’entreprise et qui doivent être supprimés ou réinitialiser les paramètres. Vous pouvez utiliser la page Paramètres du serveur dans Project Web App pour gérer les données d’entreprise ( `http://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`). Liens dans la page Paramètres du serveur permettent de supprimer les anciens éléments, forcer l’archivage des projets, gérer la file d’attente pour tous les utilisateurs et effectuer d’autres tâches d’administration.
  
Voici certains des liens dans la page Paramètres du serveur que vous pouvez utiliser pour les activités de nettoyage par défaut après l’exécution des exemples de code :
  
- **Tables de choix et champs personnalisés d’entreprise**
    
- **Gérer les travaux de file d’attente**
    
- **Supprimer des objets d’entreprise**
    
- **Forcer l’archivage des objets d’entreprise**
    
- **Types de projets d’entreprise**
    
- **Phases du flux de travail**
    
- **Étapes du flux de travail**
    
- **Pages de détails de projet**
    
- **Périodes de rapports**
    
- **Valeurs par défaut et les paramètres de la feuille de temps**
    
- **Classifications de lignes**
    
Paramètres supplémentaires sont gérés par SharePoint Server 2013 pour chaque instance de Project Web App, plutôt que par une page spécifique de paramètres de Project Web App. Dans l’application Administration centrale de SharePoint, sélectionnez **Paramètres généraux de l’Application**, cliquez sur **Gérer les** sous **Paramètres de Project Server**, puis l’instance Project Web App dans la liste déroulante dans la page Paramètres du serveur . Par exemple, choisissez de **Gestionnaires d’événements côté serveur** pour ajouter ou supprimer des gestionnaires d’événements pour l’instance Project Web App sélectionnée. 
  
## <a name="see-also"></a>Voir aussi
<a name="pj15_PrerequisitesASMX_AR"> </a>

- [Conditions préalables pour les exemples de code basée sur WCF dans Project](prerequisites-for-wcf-based-code-samples-in-project.md)
- [Utiliser l’emprunt d’identité avec WCF](http://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)
- [Présentation des références de projet PSI](project-psi-reference-overview.md)
- [Centre pour développeurs SharePoint](http://msdn.microsoft.com/en-us/sharepoint/default.aspx)
    

