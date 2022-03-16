---
title: Mises à jour pour les développeurs dans Project
manager: lindalu
ms.date: 12/03/2019
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 5b2b22cd-6e28-43a8-9092-b411da8bfb53
description: Les nouvelles fonctionnalités comprennent un modèle objet client (CSOM), des interfaces REST, un service OData pour la génération de rapports, des récepteurs d’événements à distance, des flux de travail déclaratifs et des compléments du volet de tâches.
ms.openlocfilehash: cef867ca59ef0da0df0c9523976318b9786f7044
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63507855"
---
# <a name="updates-for-developers-in-project"></a>Mises à jour pour les développeurs dans Project

Les fonctionnalités d’extensibilité dans Project Server 2013 fonctionnent avec des Project Online et des installations sur site. Les nouvelles fonctionnalités comprennent un modèle objet client (CSOM), des interfaces REST, un service OData pour la génération de rapports, des récepteurs d’événements à distance, des flux de travail déclaratifs et des compléments du volet de tâches. Découvrez également les fonctions déconseillées qui ne doivent pas être utilisées si vous commencez un nouveau développement.
  
Project Server 2013 s’appuie sur l’infrastructure introduite avec Microsoft Office Project Server 2007 et étendue par Project Server 2010. Project Server 2013 ajoute un modèle objet côté client (CSOM) refactorisant et simplifié à partir de l’interface PSI (Project Server Interface), et inclut une bibliothèque JavaScript et des bibliothèques .NET Framework 4 pour les applications Windows, Windows Phone 8 et Microsoft Silverlight. Le CSOM est conçu pour le développement pour Project Online et fonctionne également avec une installation Project Server en local.

Les bases de données Project Server sont combinées en une seule base de données ; vous pouvez donc accéder aux vues et tables de rapports en ligne via un service OData. Le modèle objet client et le service OData incluent une interface REST. Project flux de travail serveur peuvent être créés à l’aide de SharePoint Designer 2013. Project Professionnel 2013 peut s’intégrer aux données de rapports Project Server, aux listes de tâches SharePoint et à d’autres contenus externes à l’aide du modèle d’extensibilité des Office Pour les volets Des tâches. Project Standard 2013 peut utiliser des add-ins du volet Des tâches pour intégrer du contenu externe général.
  
Pour obtenir des diagrammes et plus d’informations sur les principales modifications apportées à Project Server 2013, voir [Project Server 2013 architecture](project-server-2013-architecture.md).
  
> [!NOTE]
> Project Server 2013 est basé sur la plateforme SharePoint Server 2013 et Project 2013 inclut pratiquement la même infrastructure que les autres applications Office 2013. Pour obtenir de la documentation sur le modèle de SharePoint Add-ins, des flux de travail basés sur SharePoint, des composants WebPart, du développement avec d’autres fonctionnalités SharePoint et de la documentation des Office Add-ins, voir [SharePoint Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins), [ Office des SharePoint](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins) et une vue [d’ensemble du développement 2013](https://msdn.microsoft.com/library/jj164084%28office.15%29.aspx).
  
## <a name="major-new-features-in-project-2013"></a>Principales nouvelles fonctionnalités de Project 2013

<a name="pj15_WhatsNew_MajorNewFeatures"> </a>

Les nouvelles fonctionnalités de Project Standard 2013 et Project Professionnel 2013 incluent une interface utilisateur améliorée qui correspond à d’autres applications Office 2013 et prend en charge l’interface utilisateur de style moderne dans Windows 8, l’intégration avec Office  Objets Art pour les rapports, les rapports de gravement et les nouvelles fonctionnalités de programmabilité pour les rapports. Project Professionnel 2013 permet le partage et la synchronisation de projets plus étendus sur SharePoint Server 2013, ainsi que les applications du volet Des tâches qui sont également implémentées dans d’autres applications Office 2013 telles que Word, Excel et Outlook.
  
Il existe de nombreuses nouvelles fonctionnalités dans Project Server 2013. Certains n’ont pas d’article de programmabilité majeur, par exemple la nouvelle chronologie dans Project Web App. Ces fonctionnalités seront documentées dans l’aide du produit et les documents destinés aux utilisateurs finaux sur Microsoft Office Online, ainsi que dans les rubriques destinées aux administrateurs et professionnels de l’informatique sur Microsoft TechNet. D’autres nouvelles fonctionnalités, telles que les feuilles de temps améliorées, facilitent l’interaction des développeurs tiers avec les feuilles de temps et les états via l’interface Project Server (PSI).
  
L’ajout de Project Online et du Office Store (<https://office.microsoft.com/store>) pour les compléments Project est une évolution importante, où Project Server est accessible via Microsoft Azure. L’accès basé sur le cloud à Project Server utilise un modèle objet côté client (CSOM) pour le développement de add-ins avec microsoft .NET Framework, Microsoft Silverlight, Windows Phone et les applications web qui utilisent JavaScript. L’une Project Online est que les quatre bases de données Project Server des versions précédentes soient fusionnées dans une seule base de données.
  
Project Server 2013 performance and scalability is improved in many areas such as task status, timesheets, and project management. Project flux de travail serveur ont été repensés avec la version 4 de Windows Workflow Foundation (WF4). L’utilisation des .NET Framework 4 et Windows Communication Foundation (WCF) avec l’interface PSI améliore la sécurité, les performances et l’évolutivité. Par exemple, vous pouvez modifier le protocole de transport des applications basées sur WCF à l’aide des fichiers de configuration, sans modifier le code d’application ou recompiler. Project Web App met en cache la plupart des appels PSI pour lequel les données ne changent pas considérablement.
  
> [!NOTE]
> Pour le développement avec Project Server 2013, vous pouvez utiliser Visual Studio avec les extensions des outils Office et SharePoint, qui peuvent créer des modules pour les produits Office 2013 en natif. Project Server 2013 nécessite des Visual Studio pour permettre le développement complet de fonctionnalités telles que des pages de détails de projet et des applications WCF. Les extensions SharePoint outils de Visual Studio peuvent déployer composants WebPart et d’autres fonctionnalités SharePoint directement sur Project Web App sites SharePoint sites.
>
> Visual Studio n’est plus nécessaire pour développer des flux de travail Project Server qui utilisent des champs personnalisés, des étapes, des phases et des types de projets d’entreprise qui peuvent être gérés Project Web App. Bien que vous pouvez utiliser Visual Studio pour développer des flux de travail, ils sont souvent plus faciles et plus rapides à créer à l’aide de SharePoint Designer. Visual Studio peut être utilisé pour les flux de travail qui nécessitent un accès au modèle objet client ou à d’autres API externes.
  
### <a name="project-add-ins"></a>Compléments Project

<a name="pj15_WhatsNew_Apps"> </a>

La distribution et la commercialisation de logiciels ont été révolutionnées par le concept du complément. Pour Project 2013, les applications peuvent être disponibles à l’achat et au téléchargement à partir du magasin Office public ou distribuées dans un catalogue privé sur SharePoint. Un complément est un programme interactif autonome qui effectue un petit nombre de tâches connexes. Un Project peut être un add-in du volet Des tâches pour les clients Project Standard 2013 ou Project Standard 2013, ou un module pour Project Server 2013 ou Project Online.
  
Pour plus d’informations sur les compléments pour les clients du Bureau à distance Project, voir la section relative aux [compléments du volet de tâches dans Project](#pj15_WhatsNew_Agave). Pour obtenir un Project Server 2013, consultez la SharePoint créer un Project [Server hébergé par un serveur.](create-a-sharepoint-hosted-project-server-add-in.md) Outre les articles du [SDK des compléments Office et SharePoint](https://msdn.microsoft.com/library/fp161507.aspx), le [blog Office](https://blogs.office.com/dev/) propose de nombreux billets qui sont également pertinents pour Project 2013 et Project Online.
  
Un add-in pour Project Server 2013 peut fonctionner avec une installation sur site et une Project Online. Les compléments Project Server peuvent inclure des composants WebPart, des récepteurs d’événements à distance et une logique métier. L’accès au modèle objet Project Server dans un complément se fait par l’intermédiaire du modèle objet client, et pas de l’interface PSI. Le stockage des données peut être basé sur le cloud, par exemple avec SQL Azure, externe par exemple via Microsoft Business Connectivity Services (BCS), interne avec une base de données locale ou mixte.
  
#### <a name="add-in-security"></a>Sécurité des add-ins

En règle générale, les actions effectuées par un add-in sont effectuées au nom de l’utilisateur qui exécute le module. vous n’utilisez pas explicitement l’emprunt d’identité ou spécifiez qui peut exécuter le module. Les actions ne peuvent pas dépasser le niveau d’autorisation de l’utilisateur qui exécute le module.
  
Dans Office Outils de développement pour Visual Studio 2012, le fichier AppManifext.xml possède un éditeur graphique dans lequel vous pouvez définir l’étendue de la demande d’autorisation. Par exemple, pour créer un complément qui permet aux chefs de projets de mettre à jour leurs projets, dans l’onglet **Autorisations** du volet Concepteur du fichier **AppManifest.xml**, sélectionnez **Projets multiples** pour la portée et **Écriture** pour l’autorisation. Si l’utilisateur du complément dispose des autorisations de chef de projets, il peut exécuter le complément pour les projets qu’il gère. Le code du fichier AppManifest.xml comprendrait les éléments suivants :
  
```XML
  <AppPermissionRequests>
    <AppPermissionRequest Scope="https://sharepoint/projectserver/projects" Right="Write" />
  </AppPermissionRequests>
```

**Tableau 1. Portées des demandes d’autorisations pour les compléments Project Server**

|Portée|Autorisations|
|:-----|:-----|
|**Project Server** <br/> |**Gestion** (Nécessite les autorisations d’administrateur Project Server.)  <br/> |
|**Projets multiples** <br/> |**Lecture**, **Écriture** (Nécessite les autorisations du chef de projet pour certaines opérations, ainsi que les autorisations des membres de l’équipe du projet pour les opérations de lecture de base, telles que les affectations de tâches.)  <br/> |
|**Projet unique** <br/> |**Lecture**, **Écriture** (Nécessite au moins les autorisations des membres de l’équipe du projet. L’accès à certaines données d’un projet dépend d’autres niveaux d’autorisations.)  <br/> |
|**Ressources de l’entreprise** <br/> |**Lecture**, **Écriture** (Nécessite les autorisations du gestionnaire de ressources.)  <br/> |
|**Statusing** <br/> |**SubmitStatus** (Nécessite l’autorisation de soumettre l’état de vos projets.)  <br/> |
|**Rapports** <br/> |**Lecture** (Nécessite l’autorisation de se connecter à Project Server.)  <br/> |
|**Flux de travail** <br/> |**Élever** (Nécessite l’autorisation d’exécuter des flux de travail. Le complément fonctionne avec des autorisations élevées afin de permettre des transitions d’une étape à une autre dans un flux de travail. Dans le complément, la logique métier contrôle les transitions d’étapes.)<br/> |

> [!NOTE]
> Project Server 2013 et Project Online n’utilisent pas le modèle d’authentification d’application uniquement dans SharePoint 2013 (voir types de stratégie d’autorisation de SharePoint [2013](https://msdn.microsoft.com/library/124879c7-a746-4c10-96a7-da76ad5327f0%28Office.15%29.aspx)).
  
Pour plus d’informations sur le développement, la distribution, l’hébergement et la gestion des [add-ins, voir SharePoint Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins) and [Office Add-ins](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins), ainsi que des rubriques connexes dans la documentation du développeur SharePoint Server 2013 et Office 2013. Pour plus d’informations sur l’étendue de demande d’autorisation pour SharePoint d’autres SharePoint, voir [Autorisations de SharePoint 2013](https://msdn.microsoft.com/library/5f7a8440-3c09-4cf8-83ec-c236bfa2d6c4%28Office.15%29.aspx).
  
### <a name="integrating-with-sharepoint-server"></a>Intégration à SharePoint Server

<a name="pj15_WhatsNew_IntegrationWSS"> </a>

De nombreuses fonctionnalités de Project Web App nécessitent la nouvelle infrastructure dans SharePoint Server 2013, telles que OAuth et l’authentification basée sur les revendications, l’autorisation et les autorisations Project Server via des groupes SharePoint, la synchronisation des projets avec des listes de tâches SharePoint et les Project  Flux de travail déclaratifs de serveur. L’application de service du projet peut être associée à une collection de sites dans une batterie de serveurs SharePoint. La synchronisation du projet peut être réalisée avec une liste de tâches SharePoint, où SharePoint gère le projet. Un projet d’entreprise peut également être synchronisé avec une liste de tâches SharePoint, où Project Server maintient un contrôle total. Pour obtenir des diagrammes architecturaux et une explication de la synchronisation de projet, voir [Project Server 2013 Architecture](project-server-2013-architecture.md).
  
Il existe de nombreuses nouvelles fonctionnalités dans SharePoint Server 2013. Pour plus d’informations, [voir SharePoint pour les développeurs](https://msdn.microsoft.com/sharepoint).
  
### <a name="integrating-with-workflows"></a>Intégration aux flux de travail

<a name="pj15_WhatsNew_Workflow"> </a>

Les flux de travail représentent une fonctionnalité essentielle de la gestion de portefeuille de projets. Un cycle de vie du projet peut inclure des processus de longue durée qui couvrent de nombreuses phases. Les phases de gouvernance comprennent les propositions de projet, les analyses de l’impact de l’entreprise, ainsi que la sélection, la création, la planification, la gestion et le suivi des projets.
  
Project flux de travail Server 2013 sont créés sur la plateforme SharePoint 2013, qui utilise WF4. Contrairement aux versions précédentes, les flux de travail déclaratifs pour Project Server 2013 peuvent être créés à l’aide de SharePoint Designer 2013 et sont accessibles à la fois en local et en ligne. Project flux de travail de serveur utilisent SharePoint modèle de sécurité de flux de travail avec OAuth et peuvent être installés sur Project Web App site. La figure 1 montre que SharePoint Designer 2013 peut ajouter des étapes à un flux de travail de site pour la gestion de la demande, où les étapes sont définies dans Project Web App.
  
**Figure 1. Utilisation de SharePoint Designer pour ajouter une étape à un flux de travail pour Project Web App**

![Ajout d’une étape à un flux de travail dans SPD](media/pj15_CreateWorkflowSPD_AddStageInSPD.gif "Ajout d’une étape à un flux de travail dans SPD")

Vous créez un flux de travail déclaratif en ajoutant des étapes, des actions, des conditions et d’autres éléments de flux de travail dans un outil de conception, qui peut être SharePoint Designer 2013 ou Visual Studio 2012. L’outil de conception enregistre ensuite le flux de travail en tant que code XAML qui est interprété au moment de l’exécution. Les flux de travail déclaratifs peuvent s’exécuter dans Project Server 2013 local ou dans Project Online. En utilisant Visual Studio 2012, vous pouvez également créer des actions et des formulaires personnalisés pour un contrôle supplémentaire, et enregistrer des modèles de flux de travail à réutiliser avec plusieurs instances Project Web App personnalisées. SharePoint Designer 2013 peut utiliser des actions personnalisées créées dans Visual Studio 2012.
  
Un flux de travail Project Server 2013 agit comme une application, où un administrateur, qui dispose d’autorisations de conception pour Project Web App, peut publier un flux de travail déclaratif et l’associer à un type de projet d’entreprise (EPT). L’EPT doit être pour un projet d’entreprise, où Project Server conserve un contrôle total. Une liste SharePoint tâches ne peut pas utiliser un flux de travail Project Server.
  
OAuth permet aux chefs de projets qui disposent d’autorisations de création de projets d’appeler le flux de travail sans utiliser l’emprunt d’identité. Les appels du flux de travail à Project Server, par exemple pour lire une valeur de champ personnalisé afin de décider quelle branche à suivre, sont réalisés au nom du chef de projets. Pour éviter que le chef de projets ne crée un flux de travail qui passe automatiquement à l’étape suivante, l’appel pour passer à l’étape suivante de flux de travail s’exécute comme l’auteur du flux de travail (l’administrateur). En revanche, les utilisateurs de flux de travail Project Server 2010 hérités font des appels dont l’identité a été usurpée via le compte d’utilisateur proxy du flux de travail pour accéder à l’ensemble du flux de travail.
  
Bien que Project Server 2013 local puisse utiliser des flux de travail WF3.5 compilés, nous vous recommandons de mettre à niveau les flux de travail hérités vers des flux de travail déclaratifs basés sur WF4. La nouvelle technologie est plus robuste et évolutive. Les analystes d’entreprise et le personnel PMO peuvent créer ou mettre à jour des conceptions de flux de travail à l’aide de Visio 2013 et implémenter des flux de travail Project Server sans codage à l’aide de SharePoint Designer 2013.
  
Pour plus d’informations sur la création d’un flux de travail déclaratif pour Project Web App, voir [Getting started developing Project Server workflows](getting-started-developing-project-server-workflows.md). Pour une comparaison des fonctionnalités SharePoint Designer et Visual Studio pour les flux de travail, voir [Develop SharePoint 2013 workflows using Visual Studio](https://msdn.microsoft.com/library/office/jj163199.aspx).
  
### <a name="client-side-object-model"></a>Modèle objet côté client

<a name="pj15_WhatsNew_CSOM"> </a>

L’accès par programme Project Online nécessite un CSOM qui repose sur le SharePoint CSOM. Project Online’authentification sera avec OAuth à l’aide d’un Windows Live ID, et non d’une authentification par formulaires Project serveur ou Windows’authentification.
  
Voici les principes et fonctionnalités du CSOM dans Project Server 2013 :
  
- Le modèle objet client est conçu pour faciliter l’utilisation. Par exemple, les méthodes et les propriétés utilisent ou fournissent directement des données par nom, plutôt que d’exiger plusieurs GUID ou paramètres _changeXml_, ou de transmettre des jeux de données.
- Le modèle objet client Project Server implémente un sous-ensemble de la fonctionnalité de l’interface PSI, en se basant sur les exigences les plus courantes des solutions tierces.
- Le modèle objet client appelle l’interface PSI en interne, mais cela est pris en compte différemment. Par exemple, les mises à jour pour toutes les modifications d’état sont effectuées via la méthode **StatusAssignmentCollection.SubmitAllStatusUpdates**, et non via la méthode PSI **Statusing.SubmitStatus** pour l’utilisateur ou la méthode **SubmitStatusForResource** pour d’autres ressources.
- Le modèle objet client est accessible par un service WCF (Client.svc), plutôt que par les 22 services publics de l’interface PSI.
- L’initialisation du CSOM Project Server se fait directement par le biais de la classe [ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) avec l’URL Project Web App, et non à l’aide d’une référence WCF ou d’un assembly proxy.
- Le modèle objet client implémente plusieurs interfaces et bibliothèques clientes, qui sont prises en charge par l’infrastructure CSOM SharePoint interne. Les interfaces et bibliothèques clientes sont les suivantes :

  - Bibliothèque cliente Microsoft .NET dans l’assembly Microsoft.ProjectServer.Client.dll

  - Bibliothèque Silverlight dans l’assembly Microsoft.ProjectServer.Client.Silverlight.dll assembly

  - Bibliothèque Windows Phone 8 dans l’assembly Microsoft.ProjectServer.Client.Phone.dll

  - Bibliothèque JavaScript pour les applications web dans PS.js fichier ou PS.debug.js fichier

  - Points de terminaison REST pour l’accès avec le protocole OData

  - Prise en charge native pour les requêtes LINQ avec filtrage afin de limiter la quantité de données renvoyées

- Le CSOM peut être utilisé à la fois pour les solutions Project Online et pour les solutions locales, indépendamment de l’interface PSI et d’autres assemblys Project Server tels que Microsoft.Office.Project.Server.Library.dll.
- Des fonctionnalités supplémentaires du CSOM Project Server 2013 peuvent être envisagées pour les mises à jour cumulatives et les Service Packs, en fonction des demandes des partenaires Project Server et de la communauté des développeurs.

> [!NOTE]
> Le modèle objet client représente l’interface privilégiée pour les développeurs tiers de Project Server. Nous vous recommandons d’utiliser le modèle objet client pour développer de nouvelles applications, si celui-ci inclut les fonctionnalités dont votre application a besoin.
  
Pour plus d’informations sur le développement avec le modèle CSOM, voir [Client-side object model (CSOM) for Project 2013](client-side-object-model-csom-for-project-2013.md). Pour plus d’informations sur l’interface REST dans SharePoint applications, voir Programmation à l’aide du _service REST SharePoint_ dans la documentation SharePoint 2013 pour les développeurs.
  
### <a name="changes-in-the-reporting-database"></a>Changements dans la base de données de rapports

<a name="pj15_WhatsNew_RDBChanges"> </a>

Les quatre bases de données de Project Server 2010 sont combinées en une seule base de données Project dans Project Server 2013. Le nom par défaut de la base de données Project est ProjectService. Les tables et vues de génération de rapports conservent leurs noms précédents, et les tables et vues des bases de données provisoire, publiée et d’archivage ont les préfixes `draft`et `pub``ver` dans la base de données ProjectService. Par exemple, la table de projets publiés s’intitule pub.MSP_PROJECTS.
  
> [!IMPORTANT]
> L’accès direct n’est pas`draft` pris en charge pour les tables et vues provisoires (préfixes), publiées (`pub`) et archivées (`ver`). Les rapports doivent utiliser uniquement les tables et les vues de création de rapports, qui ont le préfixe `dbo`. Par exemple, le dbo. MSP_EpmProject tableau inclut la liste des projets dans l’instance Project Web App instance.
>
> Rien ne vous empêche d’utiliser activement l’accès direct à la base de données par programme pour mettre à jour les données dans l’une des tables et vues dans la base de données Project. Vous devez être conscient que le cache Project Professionel, les tables des données brouillon et publiées, ainsi que les tables de rapport reposent tous sur un protocole de synchronisation de cache qui peut être perturbé par la modification directe de données. Toutefois, si vous endommagez vos bases de données Project Server ou les caches côté client Project Professionnel suite à un accès direct pour modifier les données, notez que le support technique ne sera pas en mesure de vous aider.
  
Project Server 2013 introduit un service OData pour l’accès en ligne et local. Les vues et tables de rapports en ligne sont exposées uniquement par l’interface OData ; Pour une utilisation sur site, vous pouvez utiliser l’interface OData ou accéder directement aux tables et vues de rapports dans la base de données ProjectService dans la batterie de serveurs SharePoint. Project Online ne prend pas en charge une base de données à plusieurs clients. Autrement dit, plusieurs instances de Project Web App ont chacune leur propre base de données Project données. Le service OData exécute en interne SQL requêtes sur les tables et vues de rapports et fournit une charge utile XML ou JSON. Pour une introduction au service OData pour la création de rapports dans Project Server 2013 et pour la référence de schéma **ProjectData**, voir [ProjectData - Project service OData reference](https://msdn.microsoft.com/library/office/jj163015.aspx).
  
Pour obtenir des informations générales sur les requêtes OData, voir [OData : conventions d’URI](https://www.odata.org/documentation/). Par exemple, vous pouvez voir tous les projets dans une instance sur site de Project Web App où le nom du projet commence par « Test » à l’aide de la requête suivante dans un navigateur. Cliquez avec le bouton droit sur la page du navigateur, puis cliquez sur **Afficher la source**.
  
```html
https://ServerName /ProjectServerName /_api/ProjectData/Projects?$filter=startswith(ProjectName, 'Test') eq true
```

Pour importer des données de projet dans PowerPivot dans Excel 2013, dans le ruban DATA, sélectionnez Flux de données **OData** dans le menu déroulant Autres **sources**. Dans la boîte **de dialogue Assistant Connexion** de données, <https://ServerName/ProjectServerName/_api/ProjectData/> tapez l’emplacement du flux de données, choisissez **Suivant, puis** sélectionnez la table **Projets** dans la page Sélectionner des **tables** de l’Assistant. Nommez et enregistrez le fichier .odc, puis choisissez **Terminer**. Dans la boîte de dialogue **Importation de données**, choisissez **Rapport de tableau croisé dynamique**. Dans la feuille de calcul Excel, choisissez des champs pour les lignes et colonnes du tableau croisé dynamique que vous souhaitez afficher.
  
Les utilisateurs Project Server locaux, qui ont les autorisations correctes, peuvent accéder directement aux tables et vues de création de rapports via Microsoft SQL Server pour créer des rapports, comme ils le font dans Project Server 2010. Dans Project Server 2013, les utilisateurs peuvent également accéder aux tables de rapports sur site via l’interface OData. Vous pouvez récupérer des données Project Server en ligne ou en local via des points de terminaison REST pour le service OData. Par exemple, la table dbo.MSP_PROJECT et la vue dbo.MSP_EpmProject_UserView peuvent être utilisées pour les rapports. Toutes les tables ou vues qui ont `draft`un préfixe ou `pub``ver` un préfixe sont pour une utilisation interne par Project Server uniquement et ne sont pas pour une utilisation de rapport. Par exemple, la table draft.MSP_TASKS et la vue pub.MSP_PROJECTS_WORKING_VIEW ne sont pas documentées et sont destinées à une utilisation interne uniquement.
  
> [!NOTE]
> Vous pouvez étendre la création de rapports en local en ajoutant des tables, vues, champs et procédures stockées dans une base de données distincte. Vous ne devez pas modifier les tables et vues de création de rapports existantes dans la base de données Project Server.
  
Les tables, vues et champs de rapports de la base de données Project seront documentés dans un fichier d’aide HTML dans une mise à jour ultérieure du téléchargement du SDK Project 2013. Pour obtenir de la documentation sur le schéma XML OData pour le service **ProjectData**, voir [ProjectData - Project de service OData](https://msdn.microsoft.com/library/office/jj163015.aspx). Dans la plupart des cas, les requêtes des tables et vues de création de rapports créées pour Project Server 2010 fonctionnent avec la base de données Project dans Project Server 2013. Les utilisateurs locaux peuvent accéder aux cubes OLAP Project Server dans SQL Server Analysis Services, comme ils le font actuellement. Dans Project Online, les cubes OLAP ne sont pas disponibles.
  
### <a name="task-pane-add-ins-in-project"></a>Compléments du volet de tâches dans Project

<a name="pj15_WhatsNew_Agave"> </a>

Les Project Standard 2013 et Project Professionnel 2013 peuvent prendre en charge les applications du volet Des tâches, qui peuvent être utilisées pour intégrer et afficher du contenu externe dans une page web. Le volet Des tâches affiche le contenu de la page web qui a accès via JavaScript aux tâches, ressources, affichages et données de projet générales. Le modèle objet JavaScript pour Project peut obtenir des informations sur une tâche ou une ressource sélectionnée, et peut obtenir des données dans une cellule sélectionnée dans la grille pour des affichages tels que le diagramme de Gantt. Les compléments du volet de tâches pour Project peuvent également implémenter des gestionnaires d’événements pour des événements modifiés de sélection de tâche, de ressource ou de vue.
  
La figure 2 illustre le complément du volet de tâches **Hello ProjectData** qui interroge le service **ProjectData**, puis compare les données du projet actuel avec les moyennes de tous les projets. Le Project SDK 2013 inclut le code source complet du compl?ment.
  
**Figure 2. Un complément du volet de tâches dans Project Professionel peut accéder à des données dans Project Server**

![Comparaison du projet actuel avec tous les projets](media/pj15_RestQueryApp_CompareProject.gif "Comparaison du projet actuel avec tous les projets")
  
> [!NOTE]
> Project Standard 2013 ne peut pas s’intégrer directement à Project Server 2013 via des add-ins du volet Des tâches.
  
Les applications de volet de tâches dans Project Professionnel peuvent prendre en charge des composants WebPart conçues pour Project Server 2013, afin que les développeurs peuvent créer une extension une fois qu’elle s’exécute avec Project Web App et Project Professionnel. Les autres produits Office 2013 peuvent également être utilisés avec Project Standard 2013 et Project Professionnel 2013. Pour plus d’informations, voir [Task pane add-ins for Project](task-pane-add-ins-for-project.md).
  
### <a name="project-server-event-receivers"></a>Récepteurs d’événements Project Server

<a name="pj15_WhatsNew_Events"> </a>

Il peut y avoir plusieurs serveurs Project Web App serveurs web (également appelés serveurs web frontux ou WPF) dans une batterie de serveurs SharePoint qui inclut l’application de service Project frontale. Les récepteurs d’événements peuvent également être appelés gestionnaires d’événements. Les gestionnaires d’événements locaux peuvent être implémentés avec le code de confiance totale et déployés sur l’ensemble des WFE pour une installation Project Server locale. Les récepteurs d’événements à distance peuvent être implémentés dans les services web sur des serveurs locaux ou à distance et accessibles par l’intermédiaire de plusieurs WFE et installations de Project Server. Project Online pouvez utiliser uniquement des récepteurs d’événements distants.
  
Project d’événements serveur sont gérés par SharePoint pour chaque instance Project Web App, plutôt que par une page Project Web App Paramètres spécifique. Dans l’application Administration centrale de SharePoint, choisissez Application générale **Paramètres**, choisissez Gérer sous **PWA Paramètres**,  puis sélectionnez l’instance dans la liste Project Web App Instance sur le PWA Paramètres   page. Pour ajouter un gestionnaire d’événements local ou un récepteur d’événements à distance, choisissez **Gestionnaires d’événements côté serveur**.
  
Pour une installation sur site de Project Server, vous pouvez créer un récepteur d’événements distant en tant que fonctionnalité SharePoint qui utilise la classe [Microsoft.ProjectServer.Client.EventHandlerCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx) dans le CSOM, puis gérer par programme le récepteur d’événements à l’aide des méthodes de la classe [EventHandlerCollection](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCollection.aspx). Pour les récepteurs d’événements à distance, les pré-événements sont synchrones, les post-événements sont asynchrones et il existe un délai si le récepteur d’événements à distance ne renvoie rien.
  
> [!NOTE]
> L’Administration centrale de SharePoint est disponible uniquement pour les installations locales. Pour Project Online et SharePoint Online, vous pouvez ajouter ou supprimer des récepteurs d’événements distants à l’aide d’un package d’application basé sur CSOM.
  
Dans la page Des handlers d’événements côté serveur, le processus d’ajout d’un handler d’événements local pour une installation Project Server locale est presque le même que celui décrit dans le processus de création d’un handler d’événements [Project Server](https://msdn.microsoft.com/library/gg615466.aspx) et journalisation d’une rubrique d’événements pour Project Server 2010. La différence est que la page Nouveau handler d’événements dispose d’options supplémentaires. Par exemple, choisissez **Project création dans** la liste **Événements**, puis **sélectionnez NOUVEAU HANDLER D’ÉVÉNEMENTs**. Dans la page Nouveau handler d’événements, les deux seuls champs obligatoires sont **Name** et **Order** (voir figure 3). Si vous ajoutez un handler d’événements de confiance totale local, ajoutez les champs **Nom de l’assembly** et **Nom** de classe ; laissez **l’URL du point de** terminaison vide. Si vous ajoutez un récepteur d’événements distant, ajoutez une **URL** de point de terminaison et laissez le nom de **l’assembly** et le **nom de classe** vides.
  
> [!CAUTION]
> Si _vous spécifiez_ à la fois le nom de l’assembly/le nom de la classe et l’URL du point de terminaison, Project Server appelle uniquement le handler d’événements local (local). Le récepteur d’événements à distance est ignoré.
>
> Si vous créez deux gestionnaires d’événements pour le même événement, où un gestionnaire d’événements est local et l’autre est un récepteur d’événements à distance, et que la valeur **Ordre** est identique pour les deux, Project Server ignore le récepteur d’événements à distance.
  
**Figure 3. Ajout d’un gestionnaire d’événements local ou d’un récepteur d’événements à distance**

![Configuration d’un gestionnaire d’événements ou d’un récepteur d’événements](media/pj15_EventHandlers_NewEventHandler.gif "Configuration d’un gestionnaire d’événements ou d’un récepteur d’événements")

Si vous avez besoin d’accéder à des jeux de données PSI pour un handler d’événements local, vous pouvez copier l’assembly Microsoft.Office.Project.Schema.dll à partir de l’assembly [Windows]\Microsoft.NET\assembly\GACMSIL\_\Microsoft.Office. Project. Schéma\v4.0_15.0.0.0__71e9bce111e9429c.

Au lieu de l’interface PSI, nous vous recommandons d’utiliser les classes d’événements dans l’espace de noms **Microsoft.ProjectServer.Client** ; le développement avec le CSOM ne nécessite pas la manipulation des jeux de données. Pour développer des récepteurs d’événements distants pour Project Online, vous devez utiliser la classe [Event](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.Event.aspx) et la classe [EventHandlerCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx) dans le CSOM.
  
Avant de déployer un gestionnaire d’événements Project Server, installez et testez le gestionnaire d’événements dans le cadre d’une installation test de Project Server. Pour une installation Project Server sur site, si le handler d’événements local que vous ajoutez devient inopérant, le service d’événements Project Server 2013 ne parvient pas à charger les autres serveurs d’événements personnalisés valides. Dans ce cas, vous devez supprimer le gestionnaire d’événements à l’origine du problème et redémarrer le service d’événements.
  
> [!NOTE]
> Pour une installation de Project Server locale, nous vous recommandons de migrer vers les récepteurs d’événements à distance à l’aide du modèle objet client pour développer les récepteurs d’événements. Étant donné que les récepteurs d’événements à distance ne disposent pas de code tiers en cours d’exécution au sein du service d’événements Project Server, les récepteurs d’événements à distance sont plus stables. Les administrateurs locaux n’ont plus la responsabilité de gérer le service d’événements Project Server.
  
Pour obtenir des informations générales sur les événements, voir [Gestion des événements dans les applications pour SharePoint](https://msdn.microsoft.com/library/jj220048%28office.15%29.aspx).
  
## <a name="deprecated-features"></a>Fonctionnalités déconseillées

<a name="pj15_WhatsNew_Deprecated"> </a>

> [!NOTE]
> Pour plus [d’informations](https://docs.microsoft.com/project/what-s-deprecated-or-removed-in-project-server-2016) sur les fonctionnalités et les API qui sont supprimées ou supprimées dans Project Server 2016 Preview, voir Les fonctionnalités supprimées ou supprimées dans Project Server 2016 Preview.
  
Les fonctionnalités dépréciées sont toujours disponibles dans Project 2013 pour certaines solutions, mais ne doivent pas être utilisées pour le nouveau développement. La plupart des fonctionnalités et pratiques suivantes ne fonctionnent pas avec Project Online ou avec l’installation sur site par défaut de Project Server 2013 en mode d SharePoint’autorisation. Les solutions existantes qui utilisent ces fonctionnalités peuvent ne pas fonctionner pour une mise à niveau de Project Server 2010 vers Project Server 2013. Bien que les solutions qui utilisent des fonctionnalités dépréciées continuent de fonctionner dans certains cas, elles ne sont pas entièrement pris en charge pour toutes les installations Project 2013.
  
Si vos solutions utilisent des fonctionnalités déconseillées, elles doivent être testées avant le déploiement et vous devez les modifier pour utiliser les fonctionnalités prises en charge dès que cela est possible. Pour plus d’informations sur la configuration de la sécurité Project Server 2013 sur site pour le mode d’autorisation Project, voir la section _mode_ d’autorisation SharePoint dans Nouveautés pour les professionnels de l’informatique dans [Project Server 2013](https://docs.microsoft.com/project/what-s-new-for-it-pros-in-project-server-2016).
  
- **Les scénarios** [d’extension PSI des extensions](https://docs.microsoft.com/previous-versions/office/developer/office-2010/ff843378(v=office.14)) sont supprimés et ne seront pas pris en charge dans les prochaines publication. Ces scénarios locaux Project Server 2013 permettaient l’intégration à l’aide de services WINDOWS Communication Foundation (WCF) personnalisés.
  
- **Project PSI** [La Project de l’interface](https://docs.microsoft.com/office/client-developer/project/project-psi-reference-overview) PSI est dépréciée. Pour tous les nouveaux développements, utilisez le [modèle objet Project](client-side-object-model-csom-for-project-2013.md). Project Server 2013 qui utilisent l’interface PSI Project continuera de fonctionner, mais les applications Project Online devront remplacer les méthodes PSI de classe Project par leurs méthodes CSOM équivalentes.
  
- **PSI du plan de ressources** [L’interface PSI du plan](https://docs.microsoft.com/previous-versions/office/project-class/gg240019(v=office.15)) de ressources est dépréciée. Il continuera à être pris en charge pour Project 2013, mais ne sera pas pris en charge dans les prochaines publication.
  
- **Interface ASMX pour l’interface PSI** L’interface PSI inclut des interfaces en double pour le développement d’extensions serveur Project locaux. L’interface des services web ASMX a été introduite avec la première implémentation de l’interface PSI dans Office Project Server 2007. Project Server 2010 a ajouté l’interface des services WCF, où le modèle objet duplique essentiellement les services web ASMX. Bien Project Server 2013 continue de prendre en charge ASMX et WCF, les nouvelles solutions qui nécessitent l’interface PSI doivent utiliser les services WCF. Si possible, les nouvelles solutions doivent être écrites en utilisant le modèle objet client.
  
  Les services web ASMX psi sont supprimés dans Project Server 2013. Pour qu’elles fonctionnent dans les futures versions de Project Server, les solutions utilisant les services web ASMX doivent être réécrites afin d’utiliser soit les services WCF, soit le modèle objet client. Pour plus d’informations, voir la section Mise à niveau des _applications avec les API Project Server_ dans [Project Server programmabilité](project-server-programmability.md).
  
- **Object Link Provider (OLP)** Dans les versions précédentes de Project Server, le service **ObjectLinkProvider** dans l’interface PSI (voir [WebSvcObjectLinkProvider](https://docs.microsoft.com/previous-versions/office/ms481347(v=office.14)) permet de gérer les liens d’objets web entre les tâches de projet d’entreprise et les listes de SharePoint spécialisées dans le site de projet pour les problèmes, les risques, les livrables et les documents. Dans Project Server 2013, OLP est supprimé.
  
  Vous pouvez utiliser la classe **[RelatedItemManager](https://docs.microsoft.com/previous-versions/office/sharepoint-server/jj168020(v=office.15))** dans le CSOM SharePoint pour créer, lire et supprimer des liens d’objet web entre les éléments de la liste de tâches et les autres listes dans un site de projet. Par exemple, pour ajouter un lien d’un élément de tâche à un problème, vous pouvez utiliser la méthode **[AddSingleLink](https://docs.microsoft.com/previous-versions/office/sharepoint-server/jj166451(v=office.15))** ou l’une des deux méthodes similaires, **AddSingleLinkFromUrl** ou **AddSingleLinkToUrl**. La classe **RelatedItemManager** inclut également des méthodes pour supprimer une liaison d’objet web et pour lire les éléments associés. Pour la classe équivalente dans le JSOM (modèle objet JavaScript), voir [SP. Objet RelatedItemManager (sp.js)](https://docs.microsoft.com/previous-versions/office/sharepoint-visio/jj838582(v=office.15)).
  
  Nous vous recommandons d’utiliser le modèle CSOM SharePoint pour créer des applications de type OLP pour une installation sur site de Project Server 2013 et pour Project Online. [L’espace de noms Microsoft.SharePoint](https://docs.microsoft.com/previous-versions/office/sharepoint-server/ms464984(v=office.15)) n’inclut pas de classe **RelatedItemManager** ****.
  
- **Autorisations personnalisées** Les autorisations de sécurité personnalisées pour accéder à des fonctionnalités ou extensions de serveur Project spécifiques étaient pris en charge dans Office Project Server 2007, où un article du SDK expliquait comment les créer en modifiant directement la base de données publiée. Dans Project Server 2010, les autorisations personnalisées fonctionnent toujours mais sont dépréciées. Dans Project Server 2013, les autorisations personnalisées ne fonctionnent pas avec le mode d’autorisation SharePoint par défaut pour les installations locales. Pour le mode d’autorisation Project, les autorisations personnalisées sont prises en charge. Avec Project Online, l’accès direct à la base de données n’est pas possible.
  
- **Emprunt d’identité** L’emprunt d’identité dans les applications psi, où l’utilisateur d’une application peut assumer les autorisations de sécurité d’un autre utilisateur Project Server, est supprimé dans Project Server 2013. Comme indiqué précédemment, une installation Project Server 2013 sur site par défaut utilise le mode d’autorisation SharePoint, qui n’autorise pas l’emprunt d’identité dans les groupes de sécurité Project Server. Pour plus d’informations, [voir Authentification, autorisation et sécurité dans SharePoint 2013](https://docs.microsoft.com/sharepoint/dev/general-development/authentication-authorization-and-security-in-sharepoint).
  
  Les applications de gestion des états sont des extensions par défaut qui ont peut-être déjà utilisé l’emprunt d’identité dans les versions précédentes de Project Server. Project Server 2010 a introduit la méthode **ReadStatusForResource** et la méthode **SubmitStatusForResource** dans l’interface PSI, ainsi que l’autorisation globale **StatusBrokerPermission**, ce qui élimine le besoin d’emprunt d’identité pour lire et mettre à jour l’état pour le compte d’un autre utilisateur. Le CSOM dans Project Server 2013 utilise l’interface PSI sous-jacente pour activer de manière transparente les extensions d’état et peut être utilisé pour les installations Project Online ou sur site.
  
- **Extensions de base de données de rapports** L’ajout de tables et d’affichages personnalisés à la base de données de création de rapports est une pratique courante avec les versions précédentes de Project Server. Étant donné que Project Server 2013 combine les quatre bases de données des versions précédentes en une seule base de données, les mises à niveau ne transfèrent pas les tables, vues ou SPROCs personnalisés vers les tables de création de rapports dans la base de données Project Server 2013.
  
  Nous vous recommandons d’utiliser une base de données SQL Azure ou une base de données SQL Server distincte pour les vues et tables de création de rapports personnalisées, où vous pouvez gérer les sauvegardes et mises à jour de base de données. Pour Project Online, cela est obligatoire.
  
- **Rapports** Les tables et vues de rapports locales dans la base de données Project Server et les cubes OLAP ne sont  pas supprimés et restent entièrement pris en charge. Toutefois, les tables et vues de rapports (la base de données de rapports dans les versions Project Server précédentes) ne sont pas accessibles Project Online. De même, les cubes OLAP sont disponibles uniquement avec les installations sur site de Project Server 2013. Pour les applications de Project Online, vous pouvez utiliser le service **ProjectData**, via des requêtes REST avec le protocole OData.
  
- **Project Guide** du Project est une fonctionnalité standard des applications de bureau Office Project 2007, où le contenu HTML et JavaScript dans un volet De tâches fournit des instructions interactives pour la création et la gestion de projets. Dans Project 2010, le guide Project n’est pas disponible dans une installation par défaut, mais peut être activé via VBA ou un VSTO de recherche. Le Project SDK 2010 inclut les fichiers modifiés Project guide.
  
  Modèle objet VBA et **Microsoft.Office. Le modèle objet Interop.MSProject** dans Project 2013 inclut toujours les 22 membres de la classe **Application** et la classe **Project** qui peuvent gérer le Guide Project. Toutefois, Project applications de volet de tâches 2013 peuvent être en conflit avec des actions dans un volet Des tâches du Guide Project et le contenu du guide Project ne peut pas être facilement distribué ou vendu dans le Office Store. Nous vous recommandons vivement de développer des solutions de Project du volet Des tâches avec des Office, et non des Project du Guide. Pour plus d’informations sur le Guide Project, voir la [documentation du SDK Project 2010](https://msdn.microsoft.com/library/ms512767.aspx).
  
## <a name="comparing-project-server-on-premises-with-project-online"></a>Comparaison de Project Server local avec Project Online

<a name="pj15_WhatsNew_Comparing"> </a>

Pour vous aider à décider s’il faut utiliser Project Server local ou Project Online et les types d’extensions que vous pouvez développer dans les deux cas, le tableau 2 compare les fonctionnalités extensibles d’une installation sur site de Project Server 2013 à Project Online. Le tableau 2 ne comprend pas les différences en matière de déploiement, d’administration ou d’utilisation. Pour plus d’informations sur Project Online et Project Server 2013, voir [Project 2013](https://developer.microsoft.com/project/docs) pour les développeurs et [Project Online](https://developer.microsoft.com/project).
  
**Tableau 2. Extensibilité de Project Server local et de Project Online**

| Fonctionnalité |Project Server local | Project Online |
|:-----|:-----|:-----|
|**Programmabilité** <br/> |Applications basées sur le modèle objet client ; modèle de programmation cohérent  <br/>- Bibliothèques clientes .NET, Silverlight Windows Phone client  <br/>- Bibliothèque JavaScript pour les extensions de page, composants WebPart et ruban personnalisées  <br/>- Protocoles OData et REST<br/><br/> Applications basées sur l’interface PSI ; modèle de programmation complexe, pouvant également créer des applications pour l’administration, l’analyse de portefeuille, les notifications, la sécurité en mode Project, le système de file d’attente, ainsi que d’autres domaines<br/><br/>Extensions de l’interface PSI  <br/><br/>Autorisations personnalisés avec la sécurité en mode Project (déconseillé)  <br/><br/>Emprunt d’identité avec l’interface PSI (déconseillé)  <br/><br/>Code de confiance totale ; installation d’extensions dans une batterie de serveurs SharePoint  <br/> |Applications basées sur le modèle objet client ; modèle de programmation cohérent  <br/>- Bibliothèques clientes .NET, Silverlight Windows Phone client<br/>- Bibliothèque JavaScript pour les extensions de page, composants WebPart et ruban personnalisées<br/>- Protocoles OData et REST<br/><br/>Possibilité d’utiliser l’interface PSI, mais elle n’est pas prise en charge : aucune connexion OAuth et service-à-service<br/><br/>Aucune extension de l’API CSOM<br/><br/>Aucune autorisation personnalisée<br/><br/>Aucun emprunt d’identité<br/><br/>Aucun code de confiance totale  <br/> |
|**Bases de données personnalisées** <br/> |- SQL Azure  <br/>- SQL Server (la modification des tables et vues de rapports dans la base de données Project Server n’est pas prise en charge)  <br/> |- SQL Azure  <br/>- SQL Server (la modification des tables et vues de rapports dans la base de données Project Server n’est pas prise en charge)  <br/> |
|**Rapports** <br/> |- **Service ProjectData** ; Protocoles OData et REST  <br/>- Tables et vues de rapports dans la base de données Project Server<br/>- Base de données OLAP  <br/> |- **Service ProjectData** ; Protocoles OData et REST  <br/> |
|**Gestionnaires d’événements** <br/> |- Récepteurs d’événements distants, accessibles via les points de terminaison WCF<br/>- Des handlers d’événements de confiance totale, installés dans SharePoint batterie de serveurs  <br/> | - Récepteurs d’événements distants, accessibles via les points de terminaison WCF  <br/> |
|**Flux de travail** <br/> |Flux de travail déclaratifs, créés avec SharePoint Designer 2013<br/>- Utiliser uniquement sur une instance Project Web App spécifique<br/>- Peut importer une conception de flux de travail Visio 2013<br/>- Peut importer et utiliser des actions personnalisées<br/><br/> Flux de travail déclaratifs, créés avec Visual Studio 2012<br/>- Créer une application qui peut inclure des flux de travail<br/>- Créer un package SharePoint solution (.wsp) qui peut inclure des flux de travail<br/>- Créer des modèles de flux de travail à réutiliser<br/>- Créer et utiliser des actions personnalisées  <br/><br/>Possibilité d’utiliser des flux de travail compilés et hérités créés avec WF3.5 (mise à niveau recommandée vers un flux de travail WF4 déclaratif)  <br/> |Flux de travail déclaratifs, créés avec SharePoint Designer 2013<br/>- Utiliser uniquement sur une instance Project Web App spécifique<br/>- Peut importer une conception de flux de travail Visio 2013<br/>- Peut importer et utiliser des actions personnalisées  <br/><br/>Flux de travail déclaratifs, créés avec Visual Studio 2012<br/>- Créer une application qui peut inclure des flux de travail  <br/>- Créer un package SharePoint solution (.wsp) qui peut inclure des flux de travail<br/>- Créer des modèles de flux de travail à réutiliser <br/>- Créer et utiliser des actions personnalisées  <br/> |
|**Distribution** <br/> |- Office Store (pour les applications basées sur CSOM)<br/>- Catalogue d’applications privé sur SharePoint<br/>- Partage de fichiers intranet  <br/> |- Office Store<br/>- Catalogue d’applications privé sur SharePoint  <br/> |

## <a name="conclusion"></a>Conclusion

<a name="pj15_WhatsNew_Conclusion"> </a>

Project Server 2013 offre une multitude de nouvelles fonctionnalités et scénarios de développement que les partenaires et les clients peuvent utiliser pour adapter et étendre les fonctionnalités et l’utilité de Project Server dans les grandes entreprises et les petites organisations. Vous pouvez utiliser l’infrastructure pour Office 2013 et SharePoint 2013 pour vous aider à créer et distribuer des applications pour Project 2013 qui peuvent  grandement étendre la c marketabilité et l’utilisation des applications personnalisées. Certaines fonctionnalités et pratiques d’extensibilité des versions précédentes sont dépréciées dans Project 2013, en particulier les services web ASMX de l’interface PSI et les fonctionnalités qui impliquent l’emprunt d’identité ou les modifications directes de base de données, qui ne peuvent pas être utilisées avec Project Online.
  
L’introduction du modèle CSOM permet d’accéder par programme à Project Online pour un large éventail d’appareils et à l’aide de JavaScript dans les applications web. Le modèle objet client fournit un modèle de programmation plus cohérent par rapport à l’interface PSI. Les données de Project Server peuvent être consultées de nombreuses autres façons que dans les versions précédentes, y compris à travers le service OData en ligne et par le biais de points de terminaison REST pour les données de création de rapports dans la base de données Project. Les rapports existants fonctionnent toujours de la même manière qu’en local et les nouveaux rapports ont plus de flexibilité.
  
Office des applications fournissent une nouvelle solution pour vendre des solutions et intégrer Project Standard 2013 au contenu web et à d’autres produits Office 2013. Vous pouvez également créer de nouvelles façons d’intégrer Project Professionnel 2013 aux données Project Server et aux listes SharePoint par le biais de Office de volet de tâches.
  
Pour plus d’informations sur le développement d’applications et l’utilisation des fonctionnalités de programmabilité et du CSOM de SharePoint Server 2013, voir [SharePoint for developers](https://docs.microsoft.com/sharepoint/dev/) and [Office for developers](https://developer.microsoft.com/office/docs).
  
## <a name="see-also"></a>Voir aussi

- [Architecture Project Server 2013](project-server-2013-architecture.md)  
- [Tâches de programmation Project](project-programming-tasks.md)
- [Modèle objet côté client (CSOM) pour Project 2013](client-side-object-model-csom-for-project-2013.md)
- [ProjectData – Référence de service Project OData](https://msdn.microsoft.com/library/office/jj163015.aspx)  
- [Compléments du volet Office pour Project](task-pane-add-ins-for-project.md)
- [OData : conventions d’URI](https://www.odata.org/documentation/uri-conventions#FilterSystemQueryOption)
- [SharePoint pour les développeurs](https://msdn.microsoft.com/sharepoint)
- [Office pour les développeurs](https://msdn.microsoft.com/office)
- [Gestion des événements dans les applications pour SharePoint](https://msdn.microsoft.com/library/jj220048%28office.15%29.aspx)
- [AppSource](https://appsource.microsoft.com/marketplace/apps?product=office)
- [Project Online](https://developer.microsoft.com/project)
