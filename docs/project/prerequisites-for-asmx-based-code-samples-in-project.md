---
title: Conditions préalables pour les exemples de code basés sur ASMX
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
- exemples de code, serveur de projet, serveur Project, programmation,PSI, compilation d’exemples de code,PSI, programmation
localization_priority: Normal
ms.assetid: df584b25-4460-46c8-89a8-3b2c94d20bba
description: Découvrez des informations pour vous aider à créer des projets dans Visual Studio à l’aide des exemples de code ASMX inclus dans les rubriques de référence psi (Project Server Interface).
ms.openlocfilehash: 26ad2e388b7e7f6f19e028b47c7f6d1a3fbd020c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357079"
---
# <a name="prerequisites-for-asmx-based-code-samples-in-project"></a>Conditions préalables pour les exemples de code basés sur ASMX

Découvrez des informations pour vous aider à créer des projets dans Visual Studio à l’aide des exemples de code ASMX inclus dans les rubriques de référence psi (Project Server Interface).
  
La plupart des exemples de code inclus dans la bibliothèque de classes et la référence de [service web Project Server 2013](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) ont été initialement créés pour le SDK Office Project 2007 et utilisent un format standard pour les services web ASMX. Les exemples fonctionnent toujours dans Project Server 2013 et sont conçus pour être copiés dans une application console et exécutés en tant qu’unité complète. Des exceptions sont notées dans l’exemple. 
  
Les nouveaux exemples PSI du SDK Project 2013 sont conformes à un format qui utilise les services WCF (Windows Communication Foundation). Les exemples ASMX peuvent également être adaptés pour utiliser les services WCF. Cet article montre comment utiliser les exemples avec les services web ASMX. Pour plus d’informations sur l’utilisation des exemples avec les services WCF, voir [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).
  
> [!NOTE]
> L’interface de service web ASMX de la PSI déconseillé dans Project Server 2013, mais est toujours prise en charge. Si le modèle objet côté client (CSOM) inclut les méthodes dont votre application a besoin, de nouvelles applications doivent être développées avec le modèle CSOM. Le CSOM permet aux applications de fonctionner avec Project Online ou une installation sur site de Project Server 2013. Dans le cas contraire, si votre application utilise l’interface PSI, elle doit utiliser l’interface WCF, qui est la technologie recommandée pour les communications réseau. Les applications qui utilisent l’interface ASMX ou l’interface WCF ne peuvent fonctionner que pour les installations sur site de Project Server 2013. Pour plus d’informations sur le modèle CSOM, voir [Project Server 2013 architecture](project-server-2013-architecture.md) and [Client-side object model (CSOM) for Project 2013](client-side-object-model-csom-for-project-2013.md). 
  
Avant d’exécutez les exemples de code, vous devez configurer l’environnement de développement, configurer l’application et modifier les valeurs de constante génériques pour qu’elle corresponde à votre environnement.
  
## <a name="setting-up-the-development-environment"></a>Configuration de l'environnement de développement
<a name="pj15_PrerequisitesASMX_Setup"> </a>

1. **Configurer un système de test Project Server.**
    
   Utilisez un système de test Project server chaque fois que vous développez ou testez. Même lorsque votre code fonctionne parfaitement, l’interprojet des dépendances, des rapports ou d’autres facteurs environnementaux peut entraîner des conséquences inattendues. 
    
   > [!NOTE]
   > Vérifiez que vous êtes un utilisateur valide sur le serveur et que vous avez les autorisations suffisantes pour les appels PSI que votre application utilise. La rubrique de référence pour chaque méthode PSI inclut une table Project Server Permissions. Par exemple, le [Project. La méthode QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) nécessite l’autorisation **NewProject** globale et **l’autorisation SaveProjectTemplate.** 
  
   Dans certains cas, vous de devez peut-être déboguer à distance sur le serveur. Il se peut également que vous de dû configurer un programme de gestion d’événements en installant un assembly de ce dernier sur chaque ordinateur Project Server de la batterie de serveurs SharePoint, puis en configurant le handler d’événements pour l’instance Project Web App à l’aide de la page Project Server Paramètres de l’Paramètres d’application générale de l’Administration centrale de SharePoint.
    
2. **Configurer un ordinateur de développement.**
    
   Vous accédez généralement à l’interface PSI via un réseau. Les exemples de code sont conçus pour être exécutés sur un client distinct du serveur, sauf en cas de remarque.
    
   1. **Installez la version correcte de Visual Studio.** Sauf remarque, les exemples de code sont écrits dans Visual C#. Elles peuvent être utilisées avec Visual Studio 2010 ou Visual Studio 2012. Assurez-vous que le Service Pack le plus récent est installé. 
        
   2. **Copiez Project DLLs de serveur sur l’ordinateur de développement.** Copiez les assemblys suivants à partir de `[Program Files]\Microsoft Office Servers\15.0\Bin` l’ordinateur Project Server vers l’ordinateur de développement : 
        
      - Microsoft.Office.Project.Server.Events.Receivers.dll
      - Microsoft.Office.Project.Server.Library.dll
        
   3. Pour plus d’informations sur la compilation et l’utilisation de l’assembly de proxy ProjectServerServices.dll pour les services web ASMX dans l’interface PSI, voir Utilisation d’un assembly de proxy PSI et des [descriptions IntelliSense données.](#pj15_PrerequisitesASMX_BuildingProxy)
    
3. **Installez les IntelliSense fichiers.**
    
    Pour utiliser des descriptions IntelliSense pour les classes et les membres dans les assemblys Project Server, copiez les fichiers XML IntelliSense mis à jour à partir du téléchargement du SDK Project 2013 dans le même répertoire que les assemblys Project Server. Par exemple, copiez le fichier Microsoft.Office.Project.Server.Library.xml dans le répertoire où votre application définira une référence à l’assembly Microsoft.Office.Project.Server.Library.dll.
    
    IntelliSense descriptions des services web PSI nécessitent la création d’un assembly de proxy PSI à l’aide du script CompileASMXProxyAssembly.cmd dans le sous-dossier du téléchargement du `Documentation\IntelliSense\WSDL` SDK Project 2013. Le script crée l’assembly ProjectServerServices.dll proxy asmx. Pour plus d’informations, voir le fichier [ReadMe_IntelliSense] dans le téléchargement du SDK. 
    
## <a name="creating-the-application-and-adding-a-web-service-reference"></a>Création de l’application et ajout d’une référence de service web
<a name="pj15_PrerequisitesASMX_Configure"> </a>

1. **Créez une application console.**
    
   Lorsque vous créez une application console, dans la liste de la boîte de dialogue **Nouveau Project,** sélectionnez **.NET Framework 4**. Vous pouvez copier l’exemple de code PSI dans la nouvelle application.
    
2. **Ajoutez la référence requise pour ASMX.**
    
   Dans l’Explorateur de solutions, ajoutez une référence **à System.Web.Services** (voir figure 1). 
    
   **Figure 1. Ajout d’une référence dans Visual Studio**

   ![Ajout d’une référence dans Visual Studio](media/pj15_PrerequisitesASMX_AddReference.gif "ajout d’une référence dans Visual Studio")
  
3. **Copiez le code**.
    
   Copiez l’exemple de code complet dans le fichier Program.cs de l’application console.
    
4. **Définissez l’espace de noms pour l’exemple d’application.**
    
   Vous pouvez modifier l’espace de noms répertorié en haut de l’exemple en espace de noms par défaut de l’application ou modifier l’espace de noms d’application par défaut pour qu’il corresponde à l’exemple. Vous pouvez modifier l’espace de noms d’application par défaut en modifiant les propriétés de l’application.
    
   Par exemple, l’exemple de code [de QueueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx) possède l’espace de noms **Microsoft.SDK.Project. Samples.RenameProject**. Si le nom du projet Visual Studio est **RenameProject,** copiez l’espace de noms à  partir du fichier Program.cs, puis ouvrez le volet Propriétés du projet (dans le menu **Project,** choisissez **RenameProject Properties**). Sous **l’onglet Application,** copiez l’espace de noms dans la **zone de texte Espace de noms** par défaut. 
    
5. **Définissez les références web.**
    
   La plupart des exemples nécessitent une référence à un ou plusieurs des services web PSI. Ceux-ci sont répertoriés dans l’exemple lui-même ou dans les commentaires qui précèdent l’exemple. Pour obtenir l’espace de noms correct des références web, assurez-vous que vous définissez d’abord l’espace de noms d’application par défaut.
    
   Il existe trois façons d’ajouter une référence de service web ASMX pour l’interface PSI :
    
   - Créez un assembly de proxy PSI ProjectServerServices.dll, puis définissez une référence à l’assembly. Pour obtenir IntelliSense, il s’agit de la façon recommandée d’ajouter une référence PSI. Voir [l’utilisation d’un assembly de proxy PSI et IntelliSense descriptions.](#pj15_PrerequisitesASMX_BuildingProxy)
    
   - Ajoutez un fichier proxy à partir de la wsdl.exe à la solution Visual Studio’accès. Voir [Ajout d’un fichier proxy PSI.](#pj15_PrerequisitesASMX_AddingProxyFile)
    
   - Ajoutez une référence de service web à l’aide Visual Studio. Voir [Ajout d’une référence de service web.](#pj15_PrerequisitesASMX_AddingServiceReference)

<a name="pj15_PrerequisitesASMX_BuildingProxy"> </a>

### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>Utilisation d’un assembly de proxy PSI et de descriptions IntelliSense données

Vous pouvez créer et utiliser l’assembly proxy ProjectServerServices.dll pour tous les services web ASMX dans l’interface PSI, à l’aide du script CompileASMXProxyAssembly.cmd dans le dossier du téléchargement du `Documentation\IntelliSense\WSDL` SDK Project 2013. Pour obtenir un lien vers le téléchargement, voir [Project 2013 pour les développeurs.](project-2013-developer-documentation.md)
  
> [!NOTE]
> Lorsque vous extrayez les fichiers proxy sources du fichier Source.zip, les fichiers du dossier sont à jour à la date de publication du téléchargement du `Documentation\IntelliSense\WSDL\Source` SDK Project 2013. Pour générer des fichiers sources de proxy PSI mis à jour, exécutez le script GenASMXProxyAssembly.cmd sur l’ordinateur Project Server. Les scripts du dossier  `Documentation\IntelliSense\WCF` ne fonctionnent pas pour les applications ASMX. Le script GenWCFProxyAssembly.cmd appelle SvcUtil.exe, qui génère des fichiers de code source pour les services WCF. Les fichiers proxy WCF incluent différents attributs, l’interface de canal et une classe cliente pour chaque service PSI. Par exemple, le service de ressources WCF inclut l’interface **ResourceChannel,** l’interface **Resource** et la **classe ResourceClient.** Le site web de ressources ASMX inclut la classe **Resource** avec certaines propriétés différentes. 
  
Voici le script GenASMXProxyAssembly.cmd qui génère des fichiers de sortie WSDL pour les services web PSI, puis compile l’assembly.
  
```MS-DOS
@echo off
@ECHO ---------------------------------------------------
@ECHO Creating C# files for the ASMX-based proxy assembly
@ECHO ---------------------------------------------------
REM Replace ServerName with the name of the server and 
REM the instance name of Project Web App. Do not use localhost.
(set VDIR=https://ServerName/pwa/_vti_bin/psi)
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

Le script utilise le ClassList_asmx.txt, qui contient la liste des services web disponibles pour les développeurs tiers.
  
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

Les scripts créent un assembly nommé ProjectServerServices.dll. Évitez de le confondre avec ProjectServerServices.dll pour l’assembly WCF. Les noms d’assembly sont les mêmes, pour permettre l’utilisation de l’un ou l’autre assembly ProjectServerServices.xml IntelliSense fichier.
  
L’espace de noms arbitraire créé par les scripts pour les services web ASMX et les services WCF est le même, de sorte que le fichier ProjectServerServices.xml IntelliSense fonctionne avec l’un ou l’autre assembly. Par exemple, l’espace de noms du service ressource dans l’assembly de proxy WCF et dans l’assembly de proxy ASMX est **SvcResource**. Vous pouvez bien entendu modifier les noms des espaces de noms si vous vous assurez qu’ils correspondent dans l’assembly proxy et dans le ProjectServerServices.xml IntelliSense de noms.
  
Si un exemple de code utilise un nom différent pour un espace de noms de service web PSI, par exemple **ProjectWebSvc**, pour que IntelliSense fonctionne, vous devez modifier l’exemple pour utiliser **SvcProject** afin que l’espace de noms corresponde à l’assembly de proxy. 
  
L’un des avantages de l’assembly de proxy ASMX est qu’il inclut tous les espaces de noms du service web PSI ; vous n’avez pas besoin de créer plusieurs références Web. Un autre avantage est que, si vous ajoutez le fichier ProjectServerServices.xml au même répertoire où vous définissez une référence à l’assembly proxy ProjectServerServices.dll, vous pouvez obtenir des descriptions IntelliSense pour les classes et les membres PSI. La figure 2 montre le IntelliSense texte de la **Project. Méthode QueueCreateProject.** Pour plus d’informations, voir le fichier [ReadMe_IntelliSense] dans le dossier IntelliSense du téléchargement du SDK Project 2013. 
  
**Figure 2. Utilisation IntelliSense pour une méthode dans le service web Project web**

![Utilisation d’Intellisense pour une méthode dans un service PSI]à l’aide d’Intellisense pour une méthode dans un service(media/pj15_PrerequisitesASMX_Intellisense.gif "PSI")
  
Les inconvénients de l’utilisation de l’assembly de proxy sont que la solution est plus grande et que vous devez distribuer et installer l’assembly de proxy avec la solution. Vous devez également utiliser les mêmes espaces de noms que dans l’assembly proxy et les fichiers IntelliSense, sauf si vous modifiez le script et le fichier ProjectServerServices.xml IntelliSense pour utiliser des espaces de noms différents.
  
### <a name="adding-a-psi-proxy-file"></a>Ajout d’un fichier proxy PSI
<a name="pj15_PrerequisitesASMX_AddingProxyFile"> </a>

Le Project SDK 2013 inclut les fichiers sources générés par la commande Wsdl.exe pour l’assembly proxy. Les fichiers sources se Source.zip dans  `Documentation\IntelliSense\ASMX` le sous-dossier. Au lieu de définir une référence à l’assembly proxy, vous pouvez ajouter un ou plusieurs des fichiers sources à une solution Visual Studio de proxy. Par exemple, après l’exécution du script GenASMXProxyAssembly.cmd, ajoutez le wsdl. Project.cs à la solution. Au lieu d’exécuter le script, vous pouvez exécuter les commandes suivantes pour générer un fichier source unique, par exemple : 
  
```MS-DOS
set VDIR=https://ServerName/ProjectServerName/_vti_bin/psi
set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe"
%WSDL% /nologo /l:cs /namespace:SvcProject /out:wsdl.Project.cs %VDIR%/Project.asmx?wsdl
```

Pour définir un **objet Project** en tant que variable de classe nommée **projet,** utilisez le code suivant. La **méthode AddContextInfo** ajoute les  informations de contexte à l’objet de projet pour Windows’authentification basée sur les formulaires et l’authentification basée sur les formulaires. 
  
```cs
private static SvcProject.Project project;
private static SvcLoginForms.LoginForms loginForms =
            new SvcLoginForms.LoginForms();
. . .
public void AddContextInfo()
{
    // Add the Url property.
    project.Url = "https://ServerName /ProjectServerName /_vti_bin/psi/project.asmx";
    // Add Windows credentials.
    project.Credentials = CredentialCache.DefaultCredentials;
    // If Forms authentication is used, add the Project Server cookie.
    project.CookieContainer = loginForms.CookieContainer;
}
```

> [!NOTE]
> Que vous utilisez un assembly de proxy PSI ou que vous ajoutiez un fichier proxy pour une référence de service Project nommée **SvcProject,** vous utiliseriez le même code pour créer un **objet de** projet. 
  
### <a name="adding-a-web-service-reference"></a>Ajout d’une référence de service web
<a name="pj15_PrerequisitesASMX_AddingServiceReference"> </a>

Si vous n’utilisez pas l’assembly de proxy ASMX ou n’ajoutez pas de fichier de sortie WSDL, vous pouvez définir une ou plusieurs références web individuelles. Les étapes suivantes montrent comment définir une référence web à l’aide Visual Studio 2012.
  
1. Dans **l’Explorateur de** solutions, cliquez avec le bouton droit sur le dossier **Références,** puis choisissez **Ajouter une référence de service.** 
    
2. Dans la **boîte de dialogue Ajouter une référence de service,** choisissez **Avancé.**
    
3. Dans la **boîte de dialogue Référence Paramètres** service, choisissez Ajouter une référence **Web.**
    
4. Dans la zone de texte **URL,** tapez, puis appuyez sur `https:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl` **Entrée** ou choisissez **l’icône** Aller. Si le protocole SSL (Secure Sockets Layer) est installé, vous devez utiliser le protocole HTTPS au lieu du protocole HTTP. 

   Par exemple, utilisez l’URL suivante pour le service Project sur `https://MyServer/pwa` le site pour Project Web App :`https://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`
    
   Ou bien, ouvrez votre navigateur web et accédez à `https://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl` . Enregistrez le fichier dans un répertoire local, tel que `C:\Project\WebServices\ServiceName.wsdl` . Dans la **boîte de dialogue Ajouter une référence Web,** pour **l’URL,** tapez le protocole de fichier et le chemin d’accès au fichier. Par exemple, tapez `file://C:\Project\WebServices\Project.wsdl` . 
    
5. Une fois la référence résolue, tapez le nom de la référence dans la zone de texte **Nom de référence Web.** Les exemples de code de la documentation Project 2013 du développeur utilisent le nom de référence standard **arbitraire Svc _ServiceName_**. Par exemple, le service web Project est **nommé SvcProject** (voir figure 3). 
    
   **Figure 3. Ajout d’une référence de service web ASMX**

   ![Ajout d’une référence de service web ASMX Ajout](media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "d’une référence de service web ASMX")
  
Pour les composants d’application qui doivent s’exécuter sur l’ordinateur Project Server, utiliser l’emprunt d’identité ou avoir des autorisations élevées, utilisez une référence de service WCF au lieu d’une référence web ASMX. Pour plus d’informations, [voir Conditions préalables pour les exemples](prerequisites-for-wcf-based-code-samples-in-project.md)de code basés sur WCF dans Project .
  
## <a name="setting-other-references"></a>Définition d’autres références
<a name="pj15_PrerequisitesASMX_OtherReferences"> </a>

Project Les applications serveur utilisent souvent d’autres services, tels que SharePoint services web Server 2013. Si d’autres services sont requis, ils sont indiqués dans l’exemple.
  
Les références locales pour l’exemple de code sont répertoriées à l’aide d’instructions en haut de l’exemple :  
  
1. Dans **l’Explorateur de** solutions, cliquez avec le bouton droit sur le dossier **Références,** puis choisissez **Ajouter une référence.**
    
2. **Sélectionnez** Parcourir, puis accédez à l’emplacement où vous avez stocké les DLL du serveur Project que vous avez copiées précédemment. Choisissez les DLL dont vous avez besoin, puis **choisissez OK.**
    
> [!NOTE]
> Assurez-vous que les versions d’assembly sur votre ordinateur de développement correspondent exactement à celles de l’ordinateur Project Server cible. 
  
## <a name="using-multiple-authentication"></a>Utilisation de l’authentification multiple
<a name="pj15_PrerequisitesASMX_ClaimsMultiAuth"> </a>

L’authentification des utilisateurs Project Server locaux, que ce soit par l’authentification Windows ou l’authentification par formulaires, est effectuée par le biais du traitement des revendications dans SharePoint Server 2013. L’authentification multiple signifie que l’application web sur laquelle Project Web App est mise en service prend en charge l Windows’authentification basée sur les formulaires et l’authentification basée sur les formulaires. Si tel est le cas, un appel à un service web ASMX qui utilise l’authentification Windows échouera avec l’erreur suivante, car le processus de revendications ne peut pas déterminer le type d’utilisateur à authentifier :
  
`The server was unable to process the request due to an internal error. . . .`

Pour résoudre le problème d’ASMX, tous les appels aux méthodes PSI doivent être vers une classe dérivée définie pour chaque service web PSI. La classe dérivée doit également utiliser la classe **SvcLoginWindows.LoginWindows** pour obtenir un cookie pour la classe de service PSI dérivée. Dans l’exemple suivant, la **classe ProjectDerived** dérive de **la classe SvcProject.Project.** La classe dérivée ajoute la **propriété EnforceWindowsAuth** et remplace l’en-tête de requête web pour chaque appel à une méthode dans la **classe Project.** Si la **propriété EnforceWindowsAuth** est **true,** la **méthode GetWebRequest** ajoute un en-tête qui désactive l’authentification par formulaires. Si **EnforceWindowsAuth est** **faux,** l’authentification par formulaires peut continuer.
  
Pour utiliser l’exemple **de ASMXLogon_MultiAuth** suivant, créez une application console, suivez les étapes de Création de l’application et ajout d’une référence de [service web,](#pj15_PrerequisitesASMX_Configure)puis ajoutez le wsdl. Fichier proxy LoginWindows.cs et wsdl. Project.cs proxy. La **méthode Main** crée l’instance de **projet** de la **classe ProjectDerived.** L’exemple doit utiliser la classe **dérivée LoginWindowsDerived** pour obtenir un objet **CookieContainer** pour le **projet. Propriété CookieContainer,** qui distingue l’authentification par formulaires de l’Windows’authentification par formulaire. **L’objet** projet peut ensuite être utilisé pour appeler n’importe quelle méthode de la **classe SvcProject.Project.** 
  
> [!NOTE]
> Le service **LoginWindows est** requis uniquement pour les applications ASMX dans un environnement d’authentification multiple. Dans **l ASMXLogon_MultiAuth** exemple, la **méthode GetLogonCookie** obtient un cookie pour l’objet **loginWindows.** **Projet. La propriété CookieContainer** est définie sur la **valeur loginWindows.CookieContainer.** 
  
```cs
using System;
using System.Net;
using PSLibrary = Microsoft.Office.Project.Server.Library;
namespace ASMXLogon_MultiAuth
{
    class Program
    {
        private const string PROJECT_SERVER_URL = 
            "https://ServerName/ProjectServerName/_vti_bin/psi/";
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

L’utilisation de la classe **LoginWindows** dérivée et la réalisation d’appels PSI avec un en-tête de demande web qui désactive l’authentification par formulaires sont requises pour les applications qui s’exécutent dans un environnement d’authentification multiple. Si Project server utilise uniquement l’authentification basée sur les revendications, il n’est pas nécessaire de dériver une classe qui ajoute un en-tête de requête web. L’exemple précédent s’exécute dans les deux environnements. 
  
Le correctif d’une application WCF est différent. Pour plus d’informations, voir la section Utilisation de *l’authentification* multiple dans Conditions préalables pour les exemples de code basés sur [WCF dans Project](prerequisites-for-wcf-based-code-samples-in-project.md).
  
## <a name="changing-the-values-of-generic-constants"></a>Modification des valeurs des constantes génériques
<a name="pj15_PrerequisitesASMX_ChangeValues"> </a>

La plupart des exemples ont une ou plusieurs variables que vous devez mettre à jour pour que l’exemple fonctionne correctement dans votre environnement. Dans l’exemple suivant, si SSL est installé, utilisez le protocole HTTPS au lieu du protocole HTTP. Remplacez  _ServerName_ par le nom du serveur que vous utilisez. Remplacez _ProjectServerName_ par le nom du répertoire virtuel de votre site Project Server, tel que PWA. 
  
```cs
const string PROJECT_SERVER_URI = "https://ServerName/ProjectServerName/";
```

Toutes les autres variables que vous devez modifier ou d’autres conditions préalables sont notées en haut de l’exemple de code.
  
## <a name="verifying-the-results"></a>Vérification des résultats
<a name="pj15_PrerequisitesASMX_Verify"> </a>

L’obtention et l’interprétation des résultats à partir d’un exemple de code ne sont pas toujours simples. Par exemple, si vous créez un projet, vous devez le publier pour qu’il puisse apparaître sur la page centre Project dans Project Web App.
  
Vous pouvez vérifier les résultats des exemples de code de plusieurs manières, par exemple :
  
- Utilisez le client Project Professionnel 2013 pour ouvrir le projet à partir de l’ordinateur Project Server et afficher les éléments que vous souhaitez.
    
- Afficher les projets publiés sur la page Project centre de Project Web App ( `https://ServerName/ProjectServerName/projects.aspx` ).
    
- Affichez le journal de file d’attente Project Web App. Ouvrez la page Paramètres serveur (sélectionnez l’icône **Paramètres** dans le  coin supérieur droit), puis choisissez Mes travaux en file d’attente sous la section **Paramètres** personnel ( `https://ServerName/ProjectServerName/MyJobs.aspx` ). Dans la **liste de** listes de listes listes, vous pouvez trier en fonction de l’état du travail. L’état par défaut **est En cours et Travaux en échec de la semaine dernière.** 
    
- Utilisez la page Serveur Paramètres dans Project Web App ( ) pour gérer tous les travaux en file d’attente et supprimer ou forcer l’enregistrement des objets `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` d’entreprise. Vous devez avoir des autorisations administratives pour accéder à ces liens sur la page Paramètres serveur.
    
- Utilisez **Microsoft SQL Server Management Studio** pour exécuter une requête sur une table dans la base de données Project données. Par exemple, utilisez la requête suivante pour sélectionner les 200 premières lignes de la pub. MSP_WORKFLOW_STAGE_PDPS pour afficher des informations sur les pages de détails de projet (PDP) dans les étapes du flux de travail. 
    
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

Après avoir testé certains exemples de code, certains objets et paramètres d’entreprise doivent être supprimés ou réinitialisés. Vous pouvez utiliser la page Serveur Paramètres dans Project Web App pour gérer les données d’entreprise ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx` ). Les liens de la page Paramètres serveur vous permettent de supprimer les anciens éléments, de forcer l’enregistrement des projets, de gérer la file d’attente des travaux pour tous les utilisateurs et d’effectuer d’autres tâches administratives.
  
Voici quelques-uns des liens sur la page Serveur Paramètres que vous pouvez utiliser pour des activités de nettoyage classiques après l’exécution d’exemples de code :
  
- **Champs personnalisés d’entreprise et tables de choix**
    
- **Gérer les travaux en file d’attente**
    
- **Supprimer des objets d’entreprise**
    
- **Forcer l’Enterprise objets**
    
- **Types de projets d’entreprise**
    
- **Phases du flux de travail**
    
- **Étapes du flux de travail**
    
- **Pages de détails de projet**
    
- **Périodes de rapports de temps**
    
- **Paramètres et valeurs par défaut de la feuille de temps**
    
- **Classifications des lignes**
    
Les paramètres supplémentaires sont gérés par SharePoint Server 2013 pour chaque instance Project Web App, plutôt que par une page Project Web App Server Paramètres spécifique. In the SharePoint Central Administration application, choose **General Application Paramètres,** choose **Manage** under Project **Server Paramètres**, and then choose the Project Web App instance in the drop-down list on the Server Paramètres page. Par exemple, sélectionnez **Les handlers** d’événements côté serveur pour ajouter ou supprimer des handlers d’événements pour l’instance Project Web App sélectionnée. 
  
## <a name="see-also"></a>Voir aussi
<a name="pj15_PrerequisitesASMX_AR"> </a>

- [Conditions préalables pour les exemples de code basés sur WCF](prerequisites-for-wcf-based-code-samples-in-project.md)
- [Utiliser l’emprunt d’identité avec WCF](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)
- [Vue d’ensemble de la référence Project PSI](project-psi-reference-overview.md)
- [Centre de développement SharePoint](https://msdn.microsoft.com/sharepoint/default.aspx)
    

