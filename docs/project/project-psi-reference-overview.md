---
title: Présentation des références de projet PSI
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- Admin
- Archive
- Authentication
- Calendar
- CubeAdmin
- CustomFields
- Events
- LoginForms
- LoginWindows
- LookupTable
- Notifications
- ObjectLinkProvider
- Project
- Project Server Interface
- Project Server Web services
- PSI
- PSI reference
- PSI Web services
- PWA
- QueueSystem
- Resource
- ResourcePlan
- Rules
- Security
- Statusing
- StatusReports
- TimeSheet
- Version
- View
- Web service
- Web services
- WinProj
- WssInterop
keywords:
- service Web, calendrier, l’authentification, service, ResourcePlan, Web Services, StatusReports, Web service Web, PSI, les espaces de noms, les gestionnaires d’événements, Project Server, service Web, les Notifications, QueueSystem, service, Project 2013, plate-forme, Web LoginWindows, Web service, service Web, état, service Web, ressources, WinProj, WssInterop, service Web service Web, service, Winproj, événement gestionnaires, LookupTable, Web PWA, service Web service Web, Web service, la sécurité, les Notifications, service Web, service Web Feuille de temps, Web service, QueueSystem, PSI, services Web, service Web, les événements, PSI, programmation, service Web, LookupTable, Version, service Web, CustomFields, service Web, service Web, PWA, PSI, ressource, service Web, service Web, ResourcePlan, feuille de temps, Web service, service Web, les règles, PSI, géré service Web de référence, la sécurité, de code, service, CustomFields, URL Web, pour l’interface PSI, Web service, WssInterop, service, Admin, service Web de Web PSI, référence Web, CubeAdmin, View, calendrier, service Web service Web, Web service, afficher, d’administration, le service Web, LoginForms, Web service, service Web, LoginForms, PSI, URL, ObjectLinkProvider, Web service, archivage, service, CubeAdmin, service Web de Web service, les règles, Web, Web services, authentification, du service Web, PSI, Project Server , événements, événements, service Web, service Web, Project, état, Web service, service Web, ObjectLinkProvider, Interface de Project Server, méthodes PSI, Web Services, StatusReports, Web service Web, archivage, Project, Web service, service Web, LoginWindows
localization_priority: Normal
ms.assetid: d3c33089-0cbe-48c3-bfc0-0be819ca4d73
description: L’Interface de Project Server (PSI) est l’API à utiliser pour le développement d’applications qui s’intègrent à Project Server 2013 sur site.
ms.openlocfilehash: 58235e16afd208d0d4415e28ad200cc7ff62ac8b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390120"
---
# <a name="project-psi-reference-overview"></a>Présentation des références de projet PSI

L’Interface de Project Server (PSI) est l’API à utiliser pour le développement d’applications qui s’intègrent à Project Server 2013 sur site.
  
Cet article est une vue d’ensemble des assemblys documentées, espaces de noms et services dans l’interface PSI. La [classe Project Server 2013 service web et de la bibliothèque de référence](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) dans le Kit de développement contient toute la documentation de code managé pour l’interface PSI et l’espace de noms [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) dans Project Server 2013. Pour développer des applications pour Project Online, vous devez utiliser l’espace de noms **Microsoft.ProjectServer.Client** au lieu de la PSI. 

L’interface PSI dans Project Server 2013 possède une interface double. L’interface ASMX pour les services web est défini par la découverte et des fichiers Web Services Description Language (disco et WSDL) dans le `https://ServerName/ProjectServerName/_vti_bin/psi/` répertoire virtuel (par exemple, Projectdisco.aspx et Projectwsdl.aspx). Vous pouvez accéder à l’interface ASMX uniquement par le biais de l’URL d’une installation locale de Project Web App (par exemple, `https://ServerName/ProjectServerName/_vti_bin/psi/project.asmx?wsdl)`. Pour afficher le service web dans un navigateur, vous devez inclure le `?wsdl` option URL. Étant donné que l’interface ASMX est généré à l’aide de l’infrastructure Windows Communication Foundation (WCF), les fichiers .asmx pour les services web de Project Server n’existent pas réellement dans le répertoire virtuel de la PSI. 
  
L’interface de services WCF est définie par les fichiers .svc dans le serveur principal `https://ServerName:32843/GUID/PSI/` répertoire virtuel de l’application de Services Web SharePoint. Les services de l’URL de la PSI dans le répertoire virtuel d’Application de Service Project (par exemple, `https://ServerName:32843/GUID/PSI/project.svc`) inclut les fichiers .svc. Mais vous ne pouvez pas utiliser directement l’URL principale pour définir une référence de service WCF. Pour développer une application ou un composant qui utilise les services WCF de la PSI, vous pouvez utiliser un assembly de proxy ou d’un fichier proxy. Le téléchargement du Kit de développement Project 2013 inclut des fichiers de proxy pour les services WCF dans Project Server 2013 et génère des scripts pour obtenir des fichiers de proxy WCF mis à jour et pour compiler les fichiers dans un assembly de proxy pour les plus récentes de Project Server.
  
Le nom de répertoire d’Application de Service Project est une valeur GUID, qui est le même que le GUID de l’instance de Project Web App sur site. Dans la fenêtre du **Gestionnaire des Services Internet (IIS)** , développez le nœud **Services Web SharePoint** , cliquez sur le nom du répertoire GUID, puis cliquez sur **Paramètres avancés** pour copier la valeur de **Chemin d’accès virtuel** . 
  
> [!IMPORTANT]
> L’interface ASMX du service web de la PSI est déconseillé dans Project Server 2013, mais est toujours prise en charge. Nouvelles applications doivent utiliser l’interface WCF de la PSI ou le modèle CSOM. Pour plus d’informations sur les fonctionnalités déconseillées, consultez [mises à jour pour les développeurs dans Project 2013](updates-for-developers-in-project-2013.md)
> 
> Nouvelles applications et les composants logiciels intermédiaires s’exécuter uniquement sur une installation locale de Project Server, doivent utiliser l’interface WCF, qui est la technologie que nous recommandons pour les communications réseau. Les applications héritées qui utilisent l’interface ASMX doivent utiliser l’URL par le biais de Project Web App, qui vérifie les autorisations Project Server. 
> 
> Pour plus d’informations sur l’interface ASMX et comment utiliser l’interface WCF, voir [conditions préalables pour les exemples de code basées sur ASMX dans Project](prerequisites-for-asmx-based-code-samples-in-project.md) et les [conditions préalables pour les exemples de code basée sur WCF dans Project](prerequisites-for-wcf-based-code-samples-in-project.md). 
  
Pour développer des applications qui utilisent l’interface WCF, vous pouvez utiliser Visual Studio 2010 ou Visual Studio 2012. Pour la création de flux de travail déclaratifs Project Server, vous pouvez utiliser SharePoint Designer 2013. Flux de travail Project Server qui nécessite un accès à l’interface PSI ou le modèle CSOM peut être développées avec Visual Studio 2012.
  
### <a name="using-the-psi-reference"></a>À l’aide de la référence de la PSI
<a name="pj15_PSIRefOverview_Using"> </a>

Le modèle d’objet PSI est volumineux, et les nombreuses classes et membres sont à usage interne uniquement. Par conséquent, il peut être déroutant pour rechercher les rubriques que vous souhaitez dans [Project Server 2013 classe web et bibliothèque une référence de service](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx). La plupart des rubriques de référence que vous utiliserez pour le développement sont dans les groupes suivants :
  
- **Méthodes de la classe principale :** Chaque service dans l’interface PSI comprend une classe principale qui est appelée pour le nom du service. Par exemple, le service de **ressources** contient la classe de [ressource](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) , qui se trouve dans l’espace de noms [WebSvcResource](https://msdn.microsoft.com/library/WebSvcResource.aspx) . Pour afficher la liste des méthodes qui sont disponibles dans la classe de **ressources** , développez le nœud de classe dans le volet contenu, puis choisissez la rubrique **Méthodes de ressource** . 
    
- **Propriétés DataRow :** Nombreuses méthodes de la classe principal ou un **jeu de données**. Chaque objet **DataTable** dans un **jeu de données** contient des données dans un ou plusieurs objets **DataRow** . Dans la plupart des cas, vous devez voir uniquement les propriétés de ligne, tous les autres membres des classes **DataSet**, **DataTable**ou **DataRow** . Par exemple, la classe **ResourceAssignmentDataSet** comprend les sous-classes pour la **ResourceAssignmentDataTable** et la classe [ResourceAssignmentDataSet.ResourceAssignmentRow](https://msdn.microsoft.com/library/WebSvcResource.ResourceAssignmentDataSet.ResourceAssignmentRow.aspx) . Pour afficher la liste des propriétés qui se trouvent dans la classe **ResourceAssignmentRow** , développez le nœud de classe dans le volet contenu, puis cliquez sur la rubrique **ResourceAssignmentDataSet.ResourceAssignmentRow des propriétés** . 
    
Outre les espaces de noms de service, les liens de rubrique de [référence de classe Project Server 2013 service web et de bibliothèque](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) aux trois assemblys qui sont utilisés dans le développement de solutions tierces pour Project Server installations locales. Nous fournissons uniquement une documentation minimale de ces assemblys. La référence PSI documente les principales classes et les membres dans les services publics 23. Services PSI six sont à usage interne uniquement et ne sont pas documentés. 
  
> [!NOTE]
> Classes dans le modèle objet côté client (CSOM) peuvent être utilisées indépendamment d’autres assemblys de Project Server et services. Vous pouvez utiliser l’espace de noms **Microsoft.ProjectServer.Client** dans un environnement de développement à distance à partir de l’ordinateur Project Server et développer des applications qui s’intègrent avec Project Online ou avec une installation locale de Project Server. Toutefois, le modèle CSOM contient un sous-ensemble des fonctionnalités de l’interface PSI terminée. Le modèle CSOM permet de développer des scénarios plus courants pour l’intégration de Project Server. Pour plus d’informations, voir [ce que le modèle et](what-the-csom-does-and-does-not-do.md) n’et [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
  
Développement de la plupart des applications qui utilisent la PSI, vous n’avez pas à développer sur un ordinateur de Project Server, ou définir des références aux assemblys de Project Server dans le global assembly cache. Vous pouvez copier les assemblys de Project Server nécessaires à votre ordinateur de développement. Project Server 2013 installe les assemblys suivants dans _[Program Files]_ `\Microsoft Office Servers\15.0\Bin`: 
  
- Microsoft.Office.Project.Server.Events.Receivers.dll 
- Microsoft.Office.Project.Server.Library.dll
- Microsoft.Office.Project.Server.Workflow.dll
    
Espaces de noms pour les services PSI ont des noms arbitraires créées pour un assembly de proxy PSI, ProjectServerServices.dll, qui est généré pour les besoins de documentation. Dans la référence PSI, chaque espace de noms de service a un nom d’espace réservé (par exemple _[service web de projet]_) et une référence web (tel que `https://ServerName/ProjectServerName/_vti_bin/psi/Project.asmx?wsdl`). 
  
## <a name="project-server-assemblies-and-namespaces"></a>Espaces de noms et assemblys de project Server
<a name="pj15_PSIRefOverview_Assemblies"> </a>

De nombreux assemblys sont installés lorsque vous installez Project Server ; quatre uniquement des assemblys Project Server sont documentés. Les développeurs tiers utilisent généralement uniquement quelques classes et membres de ces assemblys. Les assemblys de Project Server non documentées sont les espaces de noms et classes par Project Server en interne, tels que les classes pour Project Web App, les entités métier, et la couche (DAL) data access. Lorsque vous définissez une référence dans Visual Studio à un des assemblys documentées Project Server, vous pouvez voir tous les espaces de noms, des classes et des membres dans l’Explorateur d’objets Visual Studio.
  
> [!NOTE]
> De nombreux membres de l’espace de noms Project Server documentées sont utilisés uniquement en interne et ont une documentation minimale. 
  
Lors du développement pour Project Online, vous pouvez utiliser uniquement le modèle CSOM pour accéder aux fonctionnalités de Project Server. Vous n’avez pas accès à des services PSI ou les autres assemblys de Project Server.
  
La [classe Project Server 2013 service web et de la bibliothèque de référence](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) pour l’interface PSI inclut les espaces de noms à partir des assemblys suivants : 
  
- **Microsoft.Office.Project.Server.Library.dll** cet assembly contient un espace de noms documentée et trois espaces de noms non documentées, comme suit : 
    
  - L’espace de noms [Microsoft.Office.Project.Server.Library](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.aspx) inclut de nombreuses énumérations et des champs de la classe et des propriétés qui sont souvent utilisées dans les applications locales pour Project Server. Par exemple, les développeurs utilisent généralement des énumérations telles que **CustomField.Type**et les classes **PSClientError**, **PSErrorInfo**et **filtre** . 
    
    L’espace de noms **Microsoft.Office.Project.Server.Library** inclut également les classes suivantes de la sept propriété, qui incluent les sous-classes plus de 3 200 : 
    
      - **AssignmentProperties**  
      - **CalendarProperties**
      - **ConstraintProperties**
      - **LookupTableProperties**
      - **ProjectProperties**
      - **ResourceProperties**
      - **TaskProperties**
    
    Les classes de propriétés sont utilisées en interne et ne sont pas documentés. Les classes de propriétés sont utilisées pour la sérialisation entre Project Professional 2013 et Project Server. Lorsque vous travaillez avec l’espace de noms **Microsoft.Office.Project.Server.Library** dans Visual Studio, l’Explorateur d’objets affiche toutes les classes de propriété, ce qui rend plus difficiles à trouver les classes qui sont utiles pour le développement de tiers. Étant donné que les développeurs tiers n’ont pas d’utiliser les classes de propriété, le SDK ne documente pas les. 
    
  - **Microsoft.Office.Project.Server.DataServices** les classes et les membres de cet espace de noms sont utilisés en interne par le service **OData** dans Project Online pour l’accès aux tables de création de rapports dans la base de données de projet. Les classes **DataServices** ne sont pas documentés. 
    
  - **Microsoft.Office.Project.Server.Administration** la classe et membres de cet espace de noms utilisés en interne pour la journalisation des diagnostics et ne sont pas documentés. 
    
  - **Microsoft.Office.Project.Server.Base** les classes et les membres de cet espace de noms utilisés en interne comme classes de base et ne sont pas documentés. 
    
  - **Microsoft.Office.Project.Server.Library.FilterSchema** cet espace de noms est utilisé en interne pour générer des schémas de filtre et n’est pas documentée. 
    
- **Microsoft.Office.Project.Server.Workflow.dll** cet assembly est utilisé pour les flux de travail Project Server 2010 hérité qui peut fonctionnent toujours dans Project Server 2013. Pour créer un nouveau flux de travail, vous devez utiliser SharePoint Designer 2013, ou vous pouvez également utiliser Visual Studio 2012 avec la classe [Microsoft.ProjectServer.Client.WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.WorkflowActivities.aspx) . L’assembly Microsoft.Office.Project.Server.Workflow.dll inclut trois espaces de noms suivants : 
    
  - [Microsoft.Office.Project.Server.Workflow](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Workflow.aspx) cet espace de noms inclut des classes qui sont utilisés pour les activités de flux de travail Project Server. Activités sont lecture, comparer et mettre à jour les propriétés du projet. Autres classes de gérer les flux de travail et incluent les rappels de flux de travail lorsque les projets sont modifiées. 
    
  - **Microsoft.Office.Project.PWA** cet espace de noms inclut un proxy interne pour l’interface PSI, pour une utilisation avec Project Web App et activités de flux de travail personnalisé ; Il n’est pas documentée. 
    
    Une activité de flux de travail personnalisé requiert une référence à **Microsoft.Office.Project.PWA** pour accéder à toutes les classes de services PSI. Par exemple, la classe **Microsoft.Office.Project.PWA.PSI** inclut la propriété **ProjectWebService** , qui permet d’obtenir un proxy pour l’espace de noms [WebSvcProject](https://msdn.microsoft.com/library/WebSvcProject.aspx) . 
    
  - **Microsoft.Office.Project.Server.WebServiceProxy** cet espace de noms inclut des classes proxy interne pour la classe principale dans chaque service PSI. En utilisant les autorisations de l’utilisateur de flux de travail avec élévation de privilèges, le flux de travail peut appeler les méthodes PSI par le biais de classes proxy. Les classes proxy ne sont pas documentés. 
    
- **Microsoft.Office.Project.Server.Events.Receivers.dll** [Microsoft.Office.Project.Server.Events](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.aspx) est l’espace de noms uniquement dans cet assembly. Il inclut le récepteur d’événements et les classes d’argument d’événement pour les services PSI et d’autres classes internes. 
    
  Les développeurs écrire des gestionnaires d’événements qui dérivent de classes de récepteur d’événements. La plupart des classes principales dans les services PSI ont une classe de récepteur d’événements correspondant. Par exemple, la classe **ProjectEventReceiver** contient les méthodes de récepteur d’événements avant et après l’événement qui correspondent aux méthodes de la classe de **projet** dans l’interface PSI. La méthode **OnCreating** et la méthode **OnCreated** sont les méthodes de récepteur d’événements avant et après l’événement de la méthode **QueueCreateProject** . 
    
  Les développeurs utilisent généralement les classes de récepteur d’événements suivants :
  <br/>  
  - [AdminEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.AdminEventReceiver.aspx)
  - [CalendarEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.CalendarEventReceiver.aspx)
  - [CubeAdminEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.CubeAdminEventReceiver.aspx)
  - [CustomFieldsEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.CustomFieldsEventReceiver.aspx)
  - [LookupTableEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.LookupTableEventReceiver.aspx)
  - [ProjectEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.ProjectEventReceiver.aspx)
  - [OptimizerEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.OptimizerEventReceiver.aspx)
  - [ReportingEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.ReportingEventReceiver.aspx)
  - [ResourceEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.ResourceEventReceiver.aspx)
  - [SecurityEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.SecurityEventReceiver.aspx)
  - [StatusingEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.StatusingEventReceiver.aspx)
  - [TimesheetEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.TimesheetEventReceiver.aspx)
  - [UserDelegationEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.UserDelegationEventReceiver.aspx)
  - [WorkflowEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.WorkflowEventReceiver.aspx)
  - [WssInteropEventReceiver](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Events.WssInteropEventReceiver.aspx)
    
  La classe **RulesEventReceiver** et la classe **StatusReportsEventReceiver** sont utilisés en interne dans Project Web App. 
    
- **Microsoft.ProjectServer.Client.dll** cet assembly contient le modèle pour le développement avec le .NET Framework 4. L’assembly se trouve dans `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\Microsoft.ProjectServer.Client.dll`. Développement d’applications avec l’espace de noms **Microsoft.ProjectServer.Client** est indépendant de l’API de local Project Server et services, bien que les applications peuvent travailler avec un site ou d’une installation en ligne de Project Server. Pour les assemblys CSOM associés qui peuvent être utilisés pour Windows Phone 8, Microsoft Silverlight ou JavaScript avec des applications web, voir [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
    
- **Microsoft.Office.Project.Server.Schema.dll** le Kit de développement Project 2013 ne documente pas l’espace de noms **Microsoft.Office.Project.Server.Schema** , qui se trouve dans le `[Windows]\Microsoft.NET\assembly\GAC_MSIL\Microsoft.Office.Project.Schema\v4.0_15.0.0.0__71e9bce111e9429c\Microsoft.Office.Project.Schema.dll` assembly. L’espace de noms contient les définitions de toutes les classes **DataSet**, **DataTable**et **DataRow** utilisées dans l’interface PSI, ainsi que de nombreuses autres classes similaires en interne par Project Server. Les classes publiques de chaque service PSI sont décrits dans la référence de service spécifique. Par exemple, la classe **DriverDataSet.DriverRow** est documentée dans l’espace de noms [WebSvcDriver](https://msdn.microsoft.com/library/WebSvcDriver.aspx) . 
    
  > [!NOTE]
  > Applications qui utilisent le modèle CSOM, utilisent des gestionnaires d’événements distants ni accéder à Project Online n’utilisent pas l’espace de noms **Microsoft.Office.Project.Server.Schema** . 
  
  Dans certaines applications qui utilisent des gestionnaires d’événements de confiance totale, où les gestionnaires d’événements sont installés sur l’ordinateur Project Server, il est nécessaire définir une référence à l’assembly Microsoft.Office.Project.Schema.dll. Voici deux exemples :
    
  - Dans un gestionnaire d’événements postérieurs à confiance totale **OnCreated** pour les champs personnalisés, vous pouvez utiliser l’argument d’événement **e.CustomFieldInformation** avec une référence à l’espace de noms **Microsoft.Office.Project.Server.Schema** pour la **CustomFieldDataSet **et définitions **CustomFieldsRow** . 
   
     ```cs
        using PSLibrary = Microsoft.Office.Project.Server.Library;
        using Microsoft.Office.Project.Server.Schema;
        . . .
        // Event handler for the OnCreated event of a custom field.
        public override void OnCreated(
            PSLibrary.PSContextInfo contextInfo, 
            CustomFieldsPostEventArgs e)
        {
            // Get information from the event arguments. 
            string userName = contextInfo.UserName.ToString();
            CustomFieldDataSet customFieldDs = e.CustomFieldInformation;
            CustomFieldsRow customFieldRow = customFieldDs.CustomFields.Rows[0];
            string customFieldName = customFieldRow["MD_PROP_NAME"].ToString();
            byte customFieldType = (byte)customFieldRow["MD_PROP_TYPE_ENUM"];
            Guid customFieldUid = (Guid)customFieldRow["MD_PROP_UID"];
            . . .
        }
     ```

  - Une activité de flux de travail personnalisé peut nécessiter qu’une référence à **Microsoft.Office.Project.Server.Schema** pour les définitions de **jeu de données** . 
    
## <a name="psi-services"></a>Services PSI
<a name="pj15_PSIRefOverview_PSI"> </a>

L’interface PSI est un ensemble de services WCF et les services web ASMX identiques pour Project Server 2013. Pour utiliser un service dans un projet Visual Studio, vous définissez une référence à l’URL de la `.svc` fichier ou `.asmx?wsdl` service à l’aide d’un nom pour le nameservice arbitraire. L’utilitaire wsdl.exe ou l’utilitaire svcutil.exe génère ensuite le code source pour cet espace de noms proxy, et le compilateur crée un assembly de service proxy à inclure dans votre application. 
  
> [!NOTE]
> La référence PSI inclut des noms de nameservice d’espace réservé pour les services PSI comme _[service web d’administration]_, _[service web de pilote]_ et _[service web de projet]_. Chaque nameservice PSI comprend une classe principale qui contient les méthodes web pour ce service. Par exemple, si vous définissez une référence au service **d’administration** et nommez **WebSvcAdmin**, puis dans votre application l' **WebSvcAdmin** nameservice inclut la classe **Admin** principale qui possède les méthodes web **GetServerCurrency**, **ListInstalledLanguages**, **ReadServerVersion**et ainsi de suite. Voir les [mises à jour pour les développeurs dans Project 2013](updates-for-developers-in-project-2013.md) pour une liste des services PSI obsolètes. 
  
Services PSI total 30, **l’authentification**, **ExchangeSync**, **OData**, **P12Upgrade**, **psiserviceapp**, **PWA**, **affichage**et **WinProj** sont pour une utilisation interne par Project Web App et Project Professionnel et ne sont pas documentés. Bien que vous pouvez créer des fichiers de proxy ou un assembly de proxy qui inclut des services PSI internes, les services internes ne sont pas pour une utilisation tierce ; la référence PSI ne documente pas ces services. La figure suivante montre l’emplacement des services PSI principal dans le Gestionnaire des Services Internet. 
  
**Emplacement des services PSI dans IIS**

![Services PSI dans le Gestionnaire IIS] (media/pj15_PSIReference_IIS.gif "Services PSI dans le Gestionnaire IIS")
  
Toutes les classes qui contiennent des méthodes web dans les services PSI sont les suivantes :
  
1. [Admin](https://msdn.microsoft.com/library/WebSvcAdmin.Admin.aspx) Inclut des méthodes qui sont utilisés dans les pages **d’Administration de Project Server** dans Project Web App. Définit les prochaines années, gère les paramètres de devise et état, rapports des périodes, le journal d’audit et les paramètres pour Active Directory. 
    
2. [Archive](https://msdn.microsoft.com/library/WebSvcArchive.Archive.aspx) Inclut des méthodes pour la gestion de la sauvegarde et restauration de projets, catégories de sécurité, des champs personnalisés, ressources, paramètres système, les vues et le projet global d’entreprise. Lit et met à jour de la planification de l’archivage. Archive tous les projets ou supprime des projets archivés spécifiés. Enregistre les objets de sauvegarde dans les tables de base de données d’archivage et les restaurations sauvegardées des objets dans les tables de base de données publiée. 
    
3. **authentification** Inclut des méthodes pour une utilisation interne uniquement par Project Professionnel et Project Web App. 
    
4. [Calendrier](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx) Gère les exceptions de calendrier d’entreprise. Extrait et archive les calendriers des ressources. Crée, supprime, répertorie tous les, met à jour ou retourne des exceptions de calendrier. 
    
5. [CubeAdmin](https://msdn.microsoft.com/library/WebSvcCubeAdmin.CubeAdmin.aspx) Gère les paramètres de cube OLAP. Obtient la liste des cubes, état de la base de données et serveur d’analyse. Place une demande de Service de construction du Cube sur la file d’attente. Lit et met à jour des définitions de membres calculés et les paramètres de champ pour les dimensions et mesures du cube. 
    
6. [CustomFields](https://msdn.microsoft.com/library/WebSvcCustomFields.CustomFields.aspx) Gère les champs personnalisés d’entreprise. Inclut l’extraction et vérifier les méthodes et créer, lecture, mise à jour, et les méthodes de suppression (CRUD) pour les champs personnalisés d’entreprise. 
    
7. [Pilote](https://msdn.microsoft.com/library/WebSvcDriver.Driver.aspx) Gère les pilotes d’analyse de portefeuille et définition des priorités pour la création de projet et de gestion de la demande. Inclut les méthodes CRUD pour les pilotes de projet. 
    
8. [Événements](https://msdn.microsoft.com/library/WebSvcEvents.Events.aspx) Gère les associations de gestionnaire d’événements Project Server. Inclut les méthodes CRUD pour les associations pour un événement spécifique, ou pour toutes les associations de gestionnaire d’événements de gestionnaire d’événements Project Server. 
    
9. **ExchangeSync** Il s’agit d’un service interne de Project Server qui gère les événements du serveur Exchange. Project Web App utilise **ExchangeSync** pour synchroniser des attributions entre Project Server et Exchange Server, au lieu de la synchronisation directe avec le client Outlook comme dans Office Project Server 2007. 
    
    Accès au service **ExchangeSync** est disponible uniquement par le biais de l’URL **ProjectServiceApplication** . Les classes **ExchangeSync** et les membres ne sont pas pris en charge pour le développement de tiers. 
    
10. [LoginForms](https://msdn.microsoft.com/library/WebSvcLoginForms.LoginForms.aspx) Fournit les méthodes de **connexion** et de **fermeture de session** avec l’authentification basée sur les formulaires. Accès au service **LoginForms** est disponible uniquement sur un site Project Web App frontal. 
    
11. [LoginWindows](https://msdn.microsoft.com/library/WebSvcLoginWindows.LoginWindows.aspx) Fournit les méthodes de **connexion** et de **fermeture de session** sont utilisés pour l’authentification Windows avec les applications basées sur ASMX pour l’authentification plusieurs (basée sur les revendications et basée sur les formulaires) des installations de Project Server 2013. Accès au service **LoginWindows** est disponible uniquement sur un site Project Web App frontal. 
    
    > [!CAUTION]
    > Le service **LoginWindows** n’est pas utilisé dans les applications basées sur WCF, ou pour les applications qui s’exécutent sur les installations de Project Server qui utilisent uniquement l’authentification par revendications ou **OAuth**; Dans ce cas, la méthode de **connexion** renvoie toujours **false**. L’authentification par revendications gère l’authentification Windows intégrée. 
  
12. [LookupTable](https://msdn.microsoft.com/library/WebSvcLookupTable.LookupTable.aspx) Gère les tables de choix, tables de choix multilingues et de leurs masques de code correspondant. Extrait, archive, lit, crée, supprime et met à jour. 
    
13. [Notifications](https://msdn.microsoft.com/library/WebSvcNotifications.Notifications.aspx) Gère les alertes et rappels. Inclut des méthodes qui obtient, définir, enregistrement et annuler l’inscription des résultats de l’alerte. 
    
14. [ObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.ObjectLinkProvider.aspx) Gère les objets web et des liens pour les documents et éléments de liste sur des sites SharePoint. Crée, supprime ou lit le projet, projet lié, tâche ou les objets web liée à la tâche. 
    
    > [!NOTE]
    > Le service **ObjectLinkProvider** est déconseillé dans Project Server 2013. Pour plus d’informations, consultez la section *fonctionnalités déconseillées* dans [mises à jour pour les développeurs dans Project 2013](updates-for-developers-in-project-2013.md). 
  
15. **OData** Fournit l’interface **OData** interne pour les tables et les affichages de rapports. Accès au service **OData** est disponible uniquement par le biais de l’URL de **ProjectServiceApplication** principale. Le service **OData** privé dans l’interface PSI fournit une méthode, **ODataClient.ProcessOdataMessage**, qui repose sur Project Server en interne pour traiter les demandes pour les données de rapports. Les demandes HTTP passent par le service **ProjectData** frontal. 
    
    Pour plus d’informations sur le service **ProjectData** et le protocole OData pour lire les données de création de rapports, voir [ProjectData - référence de service OData Project](https://msdn.microsoft.com/library/office/jj163015.aspx).
    
16. **P12Upgrade** Fournit des méthodes internes pour le programme d’installation de Project Server 2013 mise à niveau une installation Office Project Server 2007. Accès au service **P12Upgrade** est disponible uniquement par le biais de l’URL **ProjectServiceApplication** . Les méthodes **P12Upgrade** ne sont pas pris en charge pour le développement de tiers. 
    
17. [PortfolioAnalyses](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.aspx) Inclut les méthodes CRUD pour les dépendances du projet et les solutions de l’optimiseur, planificateur et l’analyse. 
    
18. [Projet](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx) Gère les projets. Extrait, archive, crée, supprime, lit ou met à jour des projets dans les tables de projet de base de données Project tables publiées. Place un message dans la file d’attente pour la publication. 
    
    Crée ou supprime des entités dans les projets (tâches, ressources, affectations, etc.). Obtient des informations sur ou met à jour de l’équipe de projet ou une adresse de site de projet. Obtient une liste de projets dans les tableaux de brouillon, toutes les tâches récapitulatives, les tâches qui sont disponibles pour l’affectation à une ressource spécifiée ou tous les projets, état du projet où une ressource comporte des affectations.
    
    Crée et gère les engagements, crée des propositions de projets et des projets à partir de listes de tâches SharePoint et recherche les relations de projet/principal du projet.
    
19. **psiserviceapp** Utilisé en interne par Project Online. Les classes **psiserviceapp** et les membres ne sont pas pris en charge pour le développement de tiers. 
    
20. **PWA** Contient plusieurs méthodes qui sont optimisés pour Project Web App, y compris les méthodes de règles d’approbation de mise à jour de tâches et de gestion des rapports d’état. Les méthodes **PWA** sont souvent spécialisés et quelque peu redondant par rapport aux méthodes équivalentes dans d’autres services PSI. Méthodes de **PWA** ou la plupart des jeux de données de même que les autres méthodes PSI. 
    
    Accès au service **PWA** est disponible uniquement par le biais de l’URL **ProjectServiceApplication** . Les classes de **PWA** et les membres ne sont pas pris en charge pour le développement de tiers. 
    
21. [QueueSystem](https://msdn.microsoft.com/library/WebSvcQueueSystem.QueueSystem.aspx) Gère la file d’attente de Project Server. Obtient le nombre de tâches, tâche et temps d’attente de groupe de travail, l’état de tous les travaux, travaux spécifiés, les travaux détenus par l’appelant ou travaux pour les projets spécifiés. Gère la corrélation de travail et configure la file d’attente. 
    
22. [Ressource](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) Gère les ressources d’entreprise. Extrait, archive, met à jour ou crée des ressources ou utilisateurs de Project Server et leurs paramètres d’autorisation ; recherche des ressources par nom ou GUID ; lit la ressource ou données utilisateur et la structure de répartition des ressources (RBS) et les informations de sécurité associées ; Obtient toutes les affectations d’une ressource ; et réinitialise les mots de passe utilisateur. La classe de **ressource** inclut des méthodes CRUD pour délégations de l’utilisateur. 
    
23. [ResourcePlan](https://msdn.microsoft.com/library/WebSvcResourcePlan.ResourcePlan.aspx) Gère les plans de ressources. Extrait, archive, publie et inclut les méthodes CRUD pour les plans de ressources. 
    
24. [Sécurité](https://msdn.microsoft.com/library/WebSvcSecurity.Security.aspx) Inclut les méthodes CRUD pour les modèles de sécurité, les catégories de sécurité, les autorisations globales et d’organisation et les autorisations de groupe. La classe de **sécurité** inclut des méthodes pour les catégories de projet. 
    
25. [État](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.aspx) Gère les mises à jour d’état et les affectations. Applique les mises à jour de l’état ou les approbations, envoie état des mises à jour, définit les informations de synthèse des mises à jour soumis, supprime l’historique d’approbation pour un utilisateur spécifié ou des mises à jour du statut approuvé ou supprime toutes les informations d’état pour un ensemble de projets. Crée, obtient ou délégués affectations ; définit la durée de travail d’affectation. Obtient les nouvelles affectations de l’utilisateur actuel ; Obtient l’historique des transactions affectation ou une tâche, les chiffres réels chronologiques ou la hiérarchie de la tâche récapitulative. 
    
    Affiche un aperçu ou importe des données de feuille de temps ou lit le travail d’un utilisateur et les périodes chômées de planification. Recherche des mises à jour d’état, informations mises à jour soumis ou un enregistrement de la transaction des modifications apportées à une mise à jour envoyé en attente. État de l’équipe lectures.
    
26. [Feuille de temps](https://msdn.microsoft.com/library/WebSvcTimeSheet.TimeSheet.aspx) Gère les feuilles de temps. Inclut les méthodes CRUD de feuilles de temps et envoie ou rappelle des feuilles de temps. Recherche des feuilles de temps qui sont en retard ou en attente d’approbation ; recherche des feuilles de temps par période ou de date. Obtient la liste des feuilles de temps approbateurs. Précharge les chiffres réels de la feuille de temps et valide d’une ligne de feuille de temps. La classe de **feuille de temps** inclut la méthode **ReadProjectTimesheetLines** et la méthode **SubmitTimesheetLines** pour la lecture et l’envoi de feuilles de temps pour une autre ressource sans nécessiter l’emprunt d’identité. 
    
27. **Affichage** Le service **d’affichage** est conçu pour utiliser uniquement dans Project Web App. Méthodes de la classe **View** gérer les affichages et afficher les rapports et lire les champs dans les affichages. 
    
    Accès au service **d’affichage** est disponible uniquement par le biais de l’URL **ProjectServiceApplication** . Les méthodes **d’affichage** ne sont pas pris en charge pour le développement de tiers. 
    
28. **WinProj** Le service de **WinProj** est conçu pour une utilisation uniquement par Project Professionnel. Les développeurs tiers ne doivent pas utiliser les méthodes de **Winproj au cours** de la programmation avec Project Server. 
    
    Certaines méthodes de **WinProj** utilisent des jeux de données telles que **ProjectRelationsDataSet** et **ResourceDataSet** que les services de **projets** et des **ressources** également utilisent, mais nécessitent des propriétés spécifiques et des fonctions de Project Professionnel. 
    
    Accès au service **WinProj** est disponible uniquement par le biais de l’URL **ProjectServiceApplication** . Les méthodes de **WinProj** ne sont pas pris en charge pour le développement de tiers. 
    
29. [Flux de travail](https://msdn.microsoft.com/library/WebSvcWorkflow.Workflow.aspx) Inclut les méthodes CRUD pour les types de projets d’entreprise et pour la gestion des étapes et phases du flux de travail. Exécute le flux de travail, définit les informations d’état et gère les stades de page (PDP) détails de projet dans le flux de travail gestion de la demande. Pour développer des flux de travail Project Server, les développeurs peuvent utiliser SharePoint Designer 2013 pour les flux de travail déclaratifs ou utiliser les outils de développement Office pour Visual Studio 2012 pour le développement avec .NET Framework 4 et la [ Microsoft.ProjectServer.Client.WorkflowActivities](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.WorkflowActivities.aspx) classe dans le modèle CSOM. 
    
30. [WssInterop](https://msdn.microsoft.com/library/WebSvcWssInterop.WssInterop.aspx) Gère les sites de projet. Crée et supprime les sites de projet. Obtient des informations sur et met à jour les paramètres de SharePoint et les sites d’administration. Synchronise et met à jour les appartenances aux sites de projet et les groupes. 
    
Chaque espace de noms service inclut tous les **jeux de données de** schéma et les événements classes de gestionnaire qui utilise le service. Par exemple, `Calendar.svc` (ou `Calendar.asmx?wsdl` pour le ASMX service web) décrit le **calendrier** de service. Si vous nommez la référence **WebSvcCalendar**, l’espace de noms proxy contient la classe avec les méthodes **CheckInCalendars**, **CheckOutCalendars**et ainsi de suite **calendrier** principal. L’espace de noms proxy **WebSvcCalendar** inclut également la classe **CalendarDataSet** et toutes ses sous-classes. 
  
Certains services PSI contiennent les classes de **jeu de données** en double. Par exemple, le service de **projet** et le service **d’état** incluent tous deux la classe **ProjectDataSet** . Il s’agit, car les méthodes dans le service de **projet** et le service **d’état** incluent des références à **ProjectDataSet**et les assemblys de proxy que vous créez lorsque vous définissez des références et compilez une application connexe. jeux de données. Le service de **projet** et le service **d’état** peuvent nécessitent des valeurs pour d’autres champs dans la classe **ProjectDataSet.ProjectRow** . 
  
Lorsque vous naviguez les espaces de noms et les classes de la référence PSI, par exemple, pour voir les méthodes web du service de **projet** , puis développez l’espace de noms **[service web du projet]** dans la liste de **contenu** et le **projet** classe. 
  
## <a name="see-also"></a>Voir aussi

- [Architecture Project Server 2013](project-server-2013-architecture.md)
- [Programmabilité de Project Server](project-server-programmability.md)   
- [Fonctionnalités de l’interface PSI](what-the-psi-does-and-does-not-do.md)   
- [Conditions préalables pour les exemples de code basées sur ASMX dans Project](prerequisites-for-asmx-based-code-samples-in-project.md)   
- [Conditions préalables pour les exemples de code basée sur WCF dans Project](prerequisites-for-wcf-based-code-samples-in-project.md)   
- [Centre de développement .NET Framework](https://msdn.microsoft.com/netframework/aa496123.aspx)
    

