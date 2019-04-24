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
- exemples de code, Project Server, Project Server, programmation, PSI, compiler des exemples de code, PSI, programmation
localization_priority: Normal
ms.assetid: df584b25-4460-46c8-89a8-3b2c94d20bba
description: Découvrez des informations pour vous aider à créer des projets dans Visual Studio à l'aide des exemples de code ASMX qui sont inclus dans les rubriques de référence de l'interface PSI (Project Server Interface).
ms.openlocfilehash: 26ad2e388b7e7f6f19e028b47c7f6d1a3fbd020c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357079"
---
# <a name="prerequisites-for-asmx-based-code-samples-in-project"></a>Conditions préalables pour les exemples de code basés sur ASMX

Découvrez des informations pour vous aider à créer des projets dans Visual Studio à l'aide des exemples de code ASMX qui sont inclus dans les rubriques de référence de l'interface PSI (Project Server Interface).
  
De nombreux exemples de code inclus dans la [bibliothèque de classes de Project Server 2013 et la référence de service Web](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) ont été créés à l'origine pour le kit de développement logiciel (SDK) Office Project 2007, et utilisent un format standard pour les services Web ASMX. Les exemples fonctionnent toujours dans Project Server 2013 et sont conçus pour être copiés dans une application console et exécutés en tant qu'unité complète. Les exceptions sont indiquées dans l'exemple. 
  
Les nouveaux exemples PSI dans le kit de développement logiciel (SDK) Project 2013 sont conformes à un format qui utilise des services Windows Communication Foundation (WCF). Les exemples basés sur ASMX peuvent également être adaptés pour utiliser les services WCF. Cet article explique comment utiliser les exemples avec les services Web ASMX. Pour plus d'informations sur l'utilisation des exemples avec les services WCF, reportez-vous à la section [conditions préalables pour les exemples de code basés sur WCF dans Project](prerequisites-for-wcf-based-code-samples-in-project.md).
  
> [!NOTE]
> L’interface de service web ASMX de la PSI déconseillé dans Project Server 2013, mais est toujours prise en charge. Si le modèle objet côté client (CSOM) inclut les méthodes dont votre application a besoin, les nouvelles applications doivent être développées avec le CSOM. Le CSOM permet aux applications de fonctionner avec Project Online ou une installation locale de Project Server 2013. Dans le cas contraire, si votre application utilise la PSI, elle doit utiliser l'interface WCF, qui est la technologie recommandée pour les communications réseau. Les applications qui utilisent l'interface ASMX ou l'interface WCF peuvent fonctionner uniquement pour les installations locales de Project Server 2013. Pour plus d'informations sur les CSOM, consultez la rubrique [Project Server 2013 architecture](project-server-2013-architecture.md) and [Client-Side Object Model (CSOM) for Project 2013](client-side-object-model-csom-for-project-2013.md). 
  
Avant d'exécuter les exemples de code, vous devez configurer l'environnement de développement, configurer l'application et modifier les valeurs des constantes génériques en fonction de votre environnement.
  
## <a name="setting-up-the-development-environment"></a>Configuration de l'environnement de développement
<a name="pj15_PrerequisitesASMX_Setup"> </a>

1. **Configurez un système Project Server de test**.
    
   Utilisez un système Project Server de test chaque fois que vous effectuez des tests ou des développements. Même si votre code fonctionne parfaitement, les dépendances entre projets, la création de rapports ou d'autres facteurs environnementaux peuvent avoir des conséquences inattendues. 
    
   > [!NOTE]
   > Assurez-vous que vous êtes un utilisateur valide sur le serveur et vérifiez que vous disposez des autorisations suffisantes pour les appels PSI que votre application utilise. La rubrique de référence pour chaque méthode PSI inclut une table d'autorisations de Project Server. Par exemple, la méthode [Project. QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) nécessite l'autorisation globale **NewProject** et l'autorisation **SaveProjectTemplate** . 
  
   Dans certains cas, vous devrez peut-être effectuer un débogage à distance sur le serveur. Vous devrez peut-être également configurer un gestionnaire d'événements en installant un assembly de gestionnaire d'événements sur chaque ordinateur Project Server de la batterie de serveurs SharePoint, puis en configurant le gestionnaire d'événements pour l'instance de Project Web App à l'aide de la page Paramètres de Project Server dans le grand Paramètres d'application de l'administration centrale de SharePoint.
    
2. **ConFigurez un ordinateur de développement.**
    
   En règle générale, vous accédez à l'interface PSI via un réseau. Les exemples de code sont conçus pour être exécutés sur un client distinct du serveur, sauf indication contraire.
    
   1. **Installez la version appropriée de Visual Studio.** Sauf indication contraire, les exemples de code sont écrits en Visual C#. Elles peuvent être utilisées avec Visual Studio 2010 ou Visual Studio 2012. Assurez-vous que le Service Pack le plus récent est installé. 
        
   2. **Copiez les dll Project Server sur l'ordinateur de développement.** Copiez les assemblys suivants `[Program Files]\Microsoft Office Servers\15.0\Bin` de sur l'ordinateur Project Server vers l'ordinateur de développement: 
        
      - Microsoft.Office.Project.Server.Events.Receivers.dll
      - Microsoft.Office.Project.Server.Library.dll
        
   3. Pour plus d'informations sur la compilation et l'utilisation de l'assembly de proxy ProjectServerServices. dll pour les services Web ASMX dans le PSI, voir [utilisation d'un assembly de proxy PSI et descriptions IntelliSense](#pj15_PrerequisitesASMX_BuildingProxy).
    
3. **Installez les fichiers IntelliSense.**
    
    Pour utiliser les descriptions IntelliSense pour les classes et les membres des assemblys Project Server, copiez les fichiers XML IntelliSense mis à jour à partir du téléchargement du kit de développement logiciel (SDK) Project 2013 dans le même répertoire où se trouvent les assemblys Project Server. Par exemple, copiez le fichier Microsoft. Office. Project. Server. Library. xml dans le répertoire dans lequel votre application définira une référence à l'assembly Microsoft. Office. Project. Server. Library. dll.
    
    Pour les services Web PSI, les descriptions IntelliSense vous obligent à créer un assembly de proxy PSI à l'aide du `Documentation\IntelliSense\WSDL` script CompileASMXProxyAssembly. cmd dans le sous-répertoire du téléchargement du kit de développement logiciel (SDK) de Project 2013. Le script crée l'assembly de proxy ProjectServerServices. dll basé sur ASMX. Pour plus d'informations, consultez le fichier [ReadMe_IntelliSense] dans le téléchargement du kit de développement logiciel (SDK). 
    
## <a name="creating-the-application-and-adding-a-web-service-reference"></a>Création de l'application et ajout d'une référence de service Web
<a name="pj15_PrerequisitesASMX_Configure"> </a>

1. **Créez une application console**.
    
   Lorsque vous créez une application console, dans la liste déroulante de la boîte de dialogue **nouveau projet** , sélectionnez **.NET Framework 4**. Vous pouvez copier l'exemple de code PSI dans la nouvelle application.
    
2. **Ajoutez la référence requise pour ASMX.**
    
   Dans l'Explorateur de solutions, ajoutez une référence à **System. Web. services** (voir figure 1). 
    
   **Figure 1. Ajout d'une référence dans Visual Studio**

   ![Ajout d'une référence dans Visual Studio] (media/pj15_PrerequisitesASMX_AddReference.gif "Ajout d'une référence dans Visual Studio")
  
3. **Copiez le code**.
    
   Copiez l'exemple de code complet dans le fichier Program.cs de l'application console.
    
4. **Définissez l'espace de noms pour l'exemple d'application**.
    
   Vous pouvez modifier l'espace de noms mentionné en haut de l'exemple pour l'espace de noms de l'application par défaut ou modifier l'espace de noms de l'application par défaut pour qu'il corresponde à l'exemple. Vous pouvez modifier l'espace de noms de l'application par défaut en modifiant les propriétés de l'application.
    
   Par exemple, l'exemple de code pour [QueueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx) a l'espace de noms **Microsoft. Sdk. Project. Samples. RenameProject**. Si le nom du projet Visual Studio est **RenameProject**, copiez l'espace de noms à partir du fichier Program.cs, puis ouvrez le volet des **Propriétés** du projet (dans le menu **projet** , choisissez **Propriétés RenameProject**). Dans l'onglet **application** , copiez l'espace de noms dans la zone de texte **espace de noms par défaut** . 
    
5. **Définissez les références Web**.
    
   La plupart des exemples nécessitent une référence à un ou plusieurs des services Web PSI. Celles-ci sont répertoriées dans l'exemple lui-même ou dans les commentaires qui précèdent l'exemple. Pour obtenir l'espace de noms approprié des références Web, vérifiez que vous avez d'abord défini l'espace de noms de l'application par défaut.
    
   Il existe trois façons d'ajouter une référence de service Web ASMX pour la PSI:
    
   - Créez un assembly de proxy PSI nommé ProjectServerServices. dll, puis définissez une référence à l'assembly. Pour obtenir IntelliSense, il est recommandé d'ajouter une référence PSI. Voir [utilisation d'un assembly de proxy PSI et descriptions IntelliSense](#pj15_PrerequisitesASMX_BuildingProxy).
    
   - Ajoutez un fichier proxy à partir de la sortie WSDL. exe vers la solution Visual Studio. Consultez [la rubrique Ajout d'un fichier proxy PSI](#pj15_PrerequisitesASMX_AddingProxyFile).
    
   - Ajoutez une référence de service Web à l'aide de Visual Studio. Consultez [la rubrique Ajout d'une référence de service Web](#pj15_PrerequisitesASMX_AddingServiceReference).

<a name="pj15_PrerequisitesASMX_BuildingProxy"> </a>

### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a>Utilisation d'un assembly de proxy PSI et descriptions IntelliSense

Vous pouvez créer et utiliser l'assembly de proxy ProjectServerServices. dll pour tous les services Web ASMX dans le PSI, en utilisant le script CompileASMXProxyAssembly. cmd dans `Documentation\IntelliSense\WSDL` le dossier du téléchargement du kit de développement logiciel (SDK) de Project 2013. Pour obtenir un lien vers le téléchargement, reportez-vous à la [documentation du développeur Project 2013](project-2013-developer-documentation.md).
  
> [!NOTE]
> Lorsque vous extrayez les fichiers sources proxy à partir du fichier. zip source, les `Documentation\IntelliSense\WSDL\Source` fichiers du dossier sont actualisés à la date de publication du téléchargement du kit de développement logiciel (SDK) Project 2013. Pour générer des fichiers sources de proxy PSI mis à jour, exécutez le script GenASMXProxyAssembly. cmd sur l'ordinateur Project Server. Les scripts du `Documentation\IntelliSense\WCF` dossier ne fonctionnent pas pour les applications basées sur ASMX. Le script GenWCFProxyAssembly. cmd appelle SvcUtil. exe, qui génère des fichiers de code source pour les services WCF. Les fichiers de proxy WCF incluent différents attributs, l'interface de canal et une classe client pour chaque service PSI. Par exemple, le service de ressources basées sur WCF inclut l'interface **ResourceChannel** , l'interface de **ressource** et la classe **ResourceClient** . Le site Web de ressource ASMX inclut la classe de **ressource** avec certaines propriétés. 
  
Voici le script GenASMXProxyAssembly. cmd qui génère des fichiers de sortie WSDL pour les services Web PSI, puis compile l'assembly.
  
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

Le script utilise le fichier ClassList_asmx. txt, qui contient la liste des services Web disponibles pour les développeurs tiers.
  
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

Les scripts créent un assembly nommé ProjectServerServices. dll. Évitez de le confondre avec ProjectServerServices. dll pour l'assembly basé sur WCF. Les noms d'assembly sont les mêmes, pour permettre l'utilisation de l'assembly avec le fichier IntelliSense ProjectServerServices. Xml.
  
L'espace de noms arbitraire créé par les scripts pour les services Web ASMX et les services WCF est le même, de sorte que le fichier ProjectServerServices. XML IntelliSense fonctionne avec l'un ou l'autre assembly. Par exemple, l'espace de noms du service de ressources dans l'assembly de proxy basé sur WCF et dans l'assembly de proxy ASMX est **SvcResource**. Vous pouvez bien sûr modifier les noms d'espace de noms — si vous vous assurez qu'ils correspondent dans l'assembly de proxy et dans le fichier ProjectServerServices. XML IntelliSense.
  
Si un exemple de code utilise un nom différent pour un espace de noms de service Web PSI, par exemple **ProjectWebSvc**, pour qu'IntelliSense fonctionne, vous devez modifier l'exemple afin qu'il utilise **SvcProject** afin que l'espace de noms corresponde à l'assembly de proxy. 
  
L'un des avantages de l'utilisation de l'assembly de proxy basé sur ASMX est qu'il inclut tous les espaces de noms de service Web PSI; Il n'est pas nécessaire de créer plusieurs références Web. Un autre avantage est que, si vous ajoutez le fichier ProjectServerServices. xml dans le même répertoire où vous avez défini une référence à l'assembly de proxy ProjectServerServices. dll, vous pouvez obtenir des descriptions IntelliSense pour les classes et les membres PSI. La figure 2 illustre le texte IntelliSense de la méthode **Project. QueueCreateProject** . Pour plus d'informations, consultez le fichier [ReadMe_IntelliSense] dans le dossier IntelliSense du téléchargement du kit de développement logiciel (SDK) de Project 2013. 
  
**Figure 2. Utilisation d'IntelliSense pour une méthode dans le service Web de projet**

![Utilisation d'IntelliSense pour une méthode dans un service PSI] (media/pj15_PrerequisitesASMX_Intellisense.gif "Utilisation d'IntelliSense pour une méthode dans un service PSI")
  
Les inconvénients de l'utilisation de l'assembly de proxy sont les suivants: la solution est plus grande et vous devez distribuer et installer l'assembly de proxy avec la solution. Vous devez également utiliser les mêmes espaces de noms que ceux qui se trouvent dans l'assembly de proxy et les fichiers IntelliSense, sauf si vous modifiez le fichier ProjectServerServices. xml et le script pour utiliser des espaces de noms différents.
  
### <a name="adding-a-psi-proxy-file"></a>Ajout d'un fichier proxy PSI
<a name="pj15_PrerequisitesASMX_AddingProxyFile"> </a>

Le téléchargement du kit de développement logiciel (SDK) Project 2013 inclut les fichiers sources générés par la commande WSDL. exe pour l'assembly de proxy. Les fichiers sources se trouvent dans le fichier source. `Documentation\IntelliSense\ASMX` zip, dans le sous-répertoire. Au lieu de définir une référence à l'assembly de proxy, vous pouvez ajouter un ou plusieurs fichiers sources à une solution Visual Studio. Par exemple, après avoir exécuté le script GenASMXProxyAssembly. cmd, ajoutez le WSDL. Fichier Project.cs à la solution. Au lieu d'exécuter le script, vous pouvez exécuter les commandes suivantes pour générer un fichier source unique, par exemple: 
  
```MS-DOS
set VDIR=https://ServerName/ProjectServerName/_vti_bin/psi
set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe"
%WSDL% /nologo /l:cs /namespace:SvcProject /out:wsdl.Project.cs %VDIR%/Project.asmx?wsdl
```

Pour définir un objet **Project** en tant que variable de classe nommée **Project**, utilisez le code suivant. La méthode **AddContextInfo** ajoute les informations de contexte à l'objet **Project** pour l'authentification Windows et l'authentification basée sur les formulaires. 
  
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
> Que vous utilisiez un assembly de proxy PSI ou que vous ajoutiez un fichier proxy pour une référence de service Project nommée **SvcProject**, vous devez utiliser le même code pour créer un objet **Project** . 
  
### <a name="adding-a-web-service-reference"></a>Ajout d'une référence de service Web
<a name="pj15_PrerequisitesASMX_AddingServiceReference"> </a>

Si vous n'utilisez pas l'assembly de proxy basé sur ASMX ou si vous ajoutez un fichier de sortie WSDL, vous pouvez définir une ou plusieurs références Web individuelles. Les étapes suivantes montrent comment définir une référence Web à l'aide de Visual Studio 2012.
  
1. Dans l' **Explorateur de solutions**, cliquez avec le bouton droit sur le dossier **références** , puis choisissez Ajouter une **référence de service**. 
    
2. Dans la boîte de dialogue **Ajouter une référence de service** , sélectionnez **avancé**.
    
3. Dans la boîte de dialogue **paramètres de référence de service** , sélectionnez Ajouter une **référence Web**.
    
4. Dans la zone de texte **URL** , `https:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl`tapez, puis appuyez sur **entrée** ou cliquez sur l'icône **OK** . Si le protocole SSL (Secure Sockets Layer) est installé, vous devez utiliser le protocole HTTPs au lieu du protocole HTTP. 

   Par exemple, utilisez l'URL suivante pour le service Project sur le `https://MyServer/pwa` site pour Project Web App:`https://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`
    
   Ou ouvrez votre navigateur Web et accédez à `https://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl`. Enregistrez le fichier dans un répertoire local, tel que `C:\Project\WebServices\ServiceName.wsdl`. Dans la boîte de dialogue **Ajouter une référence Web** , dans **URL**, tapez le protocole de fichier et le chemin d'accès au fichier. Par exemple, tapez `file://C:\Project\WebServices\Project.wsdl`. 
    
5. Une fois que la référence est résolue, tapez le nom de la référence dans la zone de texte nom de la **référence Web** . Les exemples de code dans la documentation du développeur Project 2013 utilisent le nom de référence standard arbitraire ** _ServiceName_**. Par exemple, le service Web de projet est nommé **SvcProject** (voir figure 3). 
    
   **Figure 3. Ajout d'une référence de service Web ASMX**

   ![Ajout d'une référence de service Web ASMX] (media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "Ajout d'une référence de service Web ASMX")
  
Pour les composants d'application qui doivent s'exécuter sur l'ordinateur Project Server, utiliser l'emprunt d'identité ou avoir des autorisations élevées, utilisez une référence de service WCF au lieu d'une référence Web ASMX. Pour plus d'informations, reportez-vous à la rubrique [conditions préalables pour les exemples de code basés sur WCF dans Project](prerequisites-for-wcf-based-code-samples-in-project.md).
  
## <a name="setting-other-references"></a>Définition d'autres références
<a name="pj15_PrerequisitesASMX_OtherReferences"> </a>

Les applications Project Server utilisent souvent d'autres services, tels que les services Web SharePoint Server 2013. Si d'autres services sont requis, ils sont indiqués dans l'exemple.
  
Les références locales de l'exemple de code sont répertoriées dans instructions **using** en haut de l'exemple: 
  
1. Dans l' **Explorateur de solutions**, cliquez avec le bouton droit sur le dossier **références** , puis choisissez Ajouter une **référence**.
    
2. Choisissez **Parcourir**, puis accédez à l'emplacement où vous avez stocké les dll Project Server que vous avez copiées précédemment. Choisissez les dll dont vous avez besoin, puis choisissez **OK**.
    
> [!NOTE]
> Assurez-vous que les versions d'assembly de votre ordinateur de développement correspondent exactement à celles de l'ordinateur Project Server cible. 
  
## <a name="using-multiple-authentication"></a>Utilisation de l'authentification multiple
<a name="pj15_PrerequisitesASMX_ClaimsMultiAuth"> </a>

L'authentification des utilisateurs Project Server locaux, qu'il s'agisse de l'authentification Windows ou de l'authentification par formulaires, est réalisée via le traitement des revendications dans SharePoint Server 2013. L'authentification multiple signifie que l'application Web sur laquelle est configuré Project Web App prend en charge l'authentification Windows et l'authentification basée sur les formulaires. Si c'est le cas, un appel à un service Web ASMX qui utilise l'authentification Windows échouera avec l'erreur suivante, car le processus de revendications ne peut pas déterminer le type d'utilisateur à authentifier:
  
`The server was unable to process the request due to an internal error. . . .`

Pour résoudre le problème pour ASMX, tous les appels aux méthodes PSI doivent être effectués sur une classe dérivée définie pour chaque service Web PSI. La classe dérivée doit également utiliser la classe **SvcLoginWindows. serviceloginwindowsest** pour obtenir un cookie pour la classe de service PSI dérivée. Dans l'exemple suivant, la classe **ProjectDerived** dérive de la classe **SvcProject. Project** . La classe dérivée ajoute la propriété **EnforceWindowsAuth** et remplace l'en-tête de requête Web pour chaque appel à une méthode dans la classe **Project** . Si la propriété **EnforceWindowsAuth** a la **valeur true**, la méthode **GetWebRequest** ajoute un en-tête qui désactive l'authentification par formulaire. Si **EnforceWindowsAuth** a la **valeur false**, l'authentification par formulaire peut se poursuivre.
  
Pour utiliser l'exemple **ASMXLogon_MultiAuth** suivant, créez une application console, suivez les étapes de [création de l'application et d'ajout d'une référence de service Web](#pj15_PrerequisitesASMX_Configure), puis ajoutez le WSDL. Fichier proxy LoginWindows.cs et WSDL. Fichier proxy Project.cs. La méthode **main** crée l'instance de **projet** de la classe **ProjectDerived** . L'exemple doit utiliser la classe dérivée **LoginWindowsDerived** pour obtenir un objet **CookieContainer** pour le **projet. Propriété CookieContainer** , qui distingue l'authentification par formulaire de l'authentification Windows. L'objet **Project** peut ensuite être utilisé pour effectuer des appels à n'importe quelle méthode dans la classe **SvcProject. Project** . 
  
> [!NOTE]
> Le service **serviceloginwindowsest** est uniquement requis pour les applications asmx dans un environnement à plusieurs authentifications. Dans l'exemple **ASMXLogon_MultiAuth** , la méthode **GetLogonCookie** obtient un cookie pour l'objet **serviceloginwindowsest** . Le **projet. **La propriété CookieContainer est définie sur la valeur **Serviceloginwindowsest. CookieContainer** . 
  
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

L'utilisation de la classe **serviceloginwindowsest** dérivée et la création d'appels PSI avec un en-tête de requête Web qui désactive l'authentification par formulaires sont requises pour les applications qui s'exécutent dans un environnement à authentification multiple. Si Project Server utilise uniquement l'authentification basée sur les revendications, il n'est pas nécessaire de dériver une classe qui ajoute un en-tête de requête Web. L'exemple précédent s'exécute dans les deux environnements. 
  
Le correctif pour une application basée sur WCF est différent. Pour plus d'informations, reportez-vous à la section *utilisation de plusieurs authentifications* dans les [exemples de code basés sur WCF dans Project](prerequisites-for-wcf-based-code-samples-in-project.md).
  
## <a name="changing-the-values-of-generic-constants"></a>Modification des valeurs des constantes génériques
<a name="pj15_PrerequisitesASMX_ChangeValues"> </a>

La plupart des exemples contiennent une ou plusieurs variables que vous devez mettre à jour pour que l'exemple fonctionne correctement dans votre environnement. Dans l'exemple suivant, si SSL est installé, utilisez le protocole HTTPs au lieu du protocole HTTP. Remplacez _ServerName_ par le nom du serveur que vous utilisez. Remplacez _ProjectServerName_ par le nom du répertoire virtuel de votre site Project Server, par exemple, PWA. 
  
```cs
const string PROJECT_SERVER_URI = "https://ServerName/ProjectServerName/";
```

Toutes les autres variables que vous devez modifier ou d'autres conditions préalables sont indiquées dans la partie supérieure de l'exemple de code.
  
## <a name="verifying-the-results"></a>Vérification des résultats
<a name="pj15_PrerequisitesASMX_Verify"> </a>

L'obtention et l'interprétation de résultats à partir d'un exemple de code n'est pas toujours simple. Par exemple, si vous créez un projet, vous devez publier le projet avant de pouvoir l'afficher sur la page Centre de projets dans Project Web App.
  
Vous pouvez vérifier les résultats de l'exemple de code de plusieurs façons, par exemple:
  
- Utilisez le client Project Professional 2013 pour ouvrir le projet à partir de l'ordinateur Project Server et afficher les éléments de votre choix.
    
- Affichez les projets publiés sur la page Centre de projets de Project `https://ServerName/ProjectServerName/projects.aspx`Web App ().
    
- Affichez le journal de la file d'attente dans Project Web App. Ouvrez la page Paramètres du serveur (cliquez sur l'icône **paramètres** dans le coin supérieur droit), puis choisissez **mes travaux en file d'attente** sous la section **paramètres personnels** ( `https://ServerName/ProjectServerName/MyJobs.aspx`). Dans la liste déroulante **affichage** , vous pouvez trier en fonction de l'état du travail. L'État par défaut est **en cours et échecs de travaux au cours de la semaine précédente**. 
    
- Utilisez la page Paramètres du serveur dans Project Web App `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`() pour gérer tous les travaux en file d'attente et supprimer ou forcer l'archivage des objets d'entreprise. Vous devez disposer d'autorisations d'administration pour accéder à ces liens sur la page Paramètres du serveur.
    
- Utilisez **Microsoft SQL Server Management Studio** pour exécuter une requête sur une table dans la base de données Project. Par exemple, utilisez la requête suivante pour sélectionner les premières 200 lignes du pub. MSP_WORKFLOW_STAGE_PDPS table pour afficher les informations sur les pages de détails de projet (PDP) dans les étapes du flux de travail. 
    
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

Une fois que vous avez testé certains exemples de code, il existe des objets d'entreprise et des paramètres qui doivent être supprimés ou réinitialisés. Vous pouvez utiliser la page Paramètres du serveur dans Project Web App pour gérer les données `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`d'entreprise (). Les liens de la page Paramètres du serveur vous permettent de supprimer les anciens éléments, de forcer l'archivage des projets, de gérer la file d'attente des travaux pour tous les utilisateurs et d'effectuer d'autres tâches d'administration.
  
Voici quelques-uns des liens figurant sur la page Paramètres du serveur que vous pouvez utiliser pour les activités de nettoyage classiques après l'exécution d'exemples de code:
  
- **Champs personnalisés d’entreprise et tables de choix**
    
- **Gérer les travaux en file d’attente**
    
- **Supprimer des objets d’entreprise**
    
- **Forcer l'archivage des objets d'entreprise**
    
- **Types de projets d’entreprise**
    
- **Phases du flux de travail**
    
- **Étapes du flux de travail**
    
- **Pages de détails de projet**
    
- **Périodes de rapports de temps**
    
- **Paramètres et valeurs par défaut de la feuille de temps**
    
- **Classifications de ligne**
    
Les paramètres supplémentaires sont gérés par SharePoint Server 2013 pour chaque instance Project Web App, et non par une page de paramètres de serveur Project Web App spécifique. Dans l'application Administration centrale de SharePoint, choisissez **paramètres généraux**de l'application, choisissez **gérer** sous **paramètres de Project Server**, puis choisissez l'instance de Project Web App dans la liste déroulante de la page Paramètres du serveur. . Par exemple, choisissez **gestionnaires d'événements côté serveur** pour ajouter ou supprimer des gestionnaires d'événements pour l'instance Project Web App sélectionnée. 
  
## <a name="see-also"></a>Voir aussi
<a name="pj15_PrerequisitesASMX_AR"> </a>

- [Conditions préalables pour les exemples de code basés sur WCF](prerequisites-for-wcf-based-code-samples-in-project.md)
- [Utiliser l'emprunt d'identité avec WCF](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)
- [Vue d’ensemble de la référence Project PSI](project-psi-reference-overview.md)
- [Centre pour développeurs SharePoint](https://msdn.microsoft.com/sharepoint/default.aspx)
    

