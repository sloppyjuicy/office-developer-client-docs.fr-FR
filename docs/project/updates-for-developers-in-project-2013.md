---
title: Mises à jour pour les développeurs dans Project
manager: lindalu
ms.date: 12/03/2019
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 5b2b22cd-6e28-43a8-9092-b411da8bfb53
description: Les nouvelles fonctionnalités comprennent un modèle objet client (CSOM), des interfaces REST, un service OData pour la génération de rapports, des récepteurs d’événements à distance, des flux de travail déclaratifs et des compléments du volet de tâches.
ms.openlocfilehash: 09977db533a1593f14a3b756002a2311c7fd40cc
ms.sourcegitcommit: a6d13fdae7eb2e503236c1b629a59b36a4fb76f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2022
ms.locfileid: "66083849"
---
# <a name="updates-for-developers-in-project"></a>Mises à jour pour les développeurs dans Project

Les fonctionnalités d’extensibilité de Project Server 2013 fonctionnent avec des compléments pour Project Online et avec des installations locales. Les nouvelles fonctionnalités comprennent un modèle objet client (CSOM), des interfaces REST, un service OData pour la génération de rapports, des récepteurs d’événements à distance, des flux de travail déclaratifs et des compléments du volet de tâches. Découvrez également les fonctions déconseillées qui ne doivent pas être utilisées si vous commencez un nouveau développement.
  
Project Server 2013 s’appuie sur l’infrastructure introduite avec Microsoft Office Project Server 2007 et étendue par Project Server 2010. Project Server 2013 ajoute un modèle objet côté client (CSOM) refactoris et simplifié à partir de l’interface de serveur Project (PSI) et inclut une bibliothèque JavaScript et des bibliothèques .NET Framework 4 pour les applications Windows, Windows Phone 8 et Microsoft Silverlight. Le modèle CSOM est conçu pour le développement pour Project Online et fonctionne également avec une installation locale Project Server.

Les bases de données Project Server sont combinées en une seule base de données ; vous pouvez donc accéder aux vues et tables de rapports en ligne via un service OData. Le modèle objet client et le service OData incluent une interface REST. Project Workflows server peuvent être créés à l’aide de SharePoint Designer 2013. Project Professionnel 2013 peut s’intégrer aux données de création de rapports Project Server, aux listes de tâches SharePoint et à d’autres contenus externes à l’aide du modèle d’extensibilité des compléments Office pour les volets office. Project Standard 2013 peut utiliser des compléments du volet Office pour s’intégrer au contenu externe général.
  
Pour obtenir des diagrammes et plus d’informations sur les principales modifications apportées à Project Server 2013, consultez [l’architecture Project Server 2013](project-server-2013-architecture.md).
  
> [!NOTE]
> Project Server 2013 est basé sur la plateforme SharePoint Server 2013 et Project 2013 inclut pratiquement la même infrastructure que les autres applications Office 2013. Pour obtenir de la documentation sur le modèle pour les compléments SharePoint, les flux de travail basés sur SharePoint, les composants WebPart, le développement avec d’autres fonctionnalités SharePoint et la documentation des compléments Office, consultez [SharePoint compléments](/sharepoint/dev/sp-add-ins/sharepoint-add-ins), [Office compléments](/office/dev/add-ins/overview/office-add-ins) et [SharePoint  Vue d’ensemble du développement 2013](https://msdn.microsoft.com/library/jj164084%28office.15%29.aspx).
  
## <a name="major-new-features-in-project-2013"></a>Principales nouvelles fonctionnalités de Project 2013

<a name="pj15_WhatsNew_MajorNewFeatures"> </a>

Les nouvelles fonctionnalités de Project Standard 2013 et Project Professionnel 2013 incluent une interface utilisateur améliorée qui correspond à d’autres applications Office 2013 et prend en charge l’interface utilisateur de style moderne dans Windows 8, l’intégration à Office  Objets d’art pour les rapports, les rapports d’avancement et les nouvelles fonctionnalités de programmabilité pour les rapports. Project Professionnel 2013 permet un partage et une synchronisation plus étendus de projets sur SharePoint Server 2013, ainsi que les compléments du volet Office qui sont également implémentés dans d’autres applications Office 2013 telles que Word, Excel et Outlook.
  
Il existe de nombreuses nouvelles fonctionnalités dans Project Server 2013. Certains n’ont pas d’histoire de programmabilité majeure, comme la nouvelle chronologie dans Project Web App. Ces fonctionnalités seront documentées dans l’aide du produit et les documents destinés aux utilisateurs finaux sur Microsoft Office Online, ainsi que dans les rubriques destinées aux administrateurs et professionnels de l’informatique sur Microsoft TechNet. D’autres nouvelles fonctionnalités, telles que les feuilles de temps améliorées, facilitent l’interaction des développeurs tiers avec les feuilles de temps et les états via l’interface Project Server (PSI).
  
L’ajout de Project Online et du Office Store (<https://office.microsoft.com/store>) pour les compléments Project sont des modifications importantes, où Project Server est accessible via Microsoft Azure. L’accès cloud à Project Server utilise un modèle objet côté client (CSOM) pour le développement de compléments avec Microsoft .NET Framework, Microsoft Silverlight, Windows Phone et des applications web qui utilisent JavaScript. Une exigence de Project Online est que les quatre bases de données Project Server des versions précédentes soient fusionnées dans une base de données.
  
Project Les performances et l’extensibilité de Server 2013 sont améliorées dans de nombreux domaines tels que l’état des tâches, les feuilles de temps et la gestion de projet. Project Workflows Server sont repensés avec la version 4 de Windows Workflow Foundation (WF4). L’utilisation de .NET Framework 4 et Windows Communication Foundation (WCF) avec l’interface PSI améliore la sécurité, les performances et l’extensibilité. Par exemple, vous pouvez modifier le protocole de transport des applications basées sur WCF à l’aide des fichiers de configuration, sans modifier le code d’application ou recompiler. Project Web App met en cache de nombreux appels PSI où les données ne changent pas considérablement.
  
> [!NOTE]
> Pour le développement avec Project Server 2013, vous pouvez utiliser Visual Studio avec les extensions d’outils Office et SharePoint, qui peuvent créer en mode natif des compléments pour les produits Office 2013. Project Server 2013 nécessite Visual Studio pour activer entièrement le développement de fonctionnalités telles que les pages de détails du projet et les applications WCF. Les extensions des outils de SharePoint dans Visual Studio peuvent déployer des composants WebPart et d’autres fonctionnalités SharePoint directement sur Project Web App et d’autres sites SharePoint.
>
> Visual Studio n’est plus nécessaire pour développer des workflows Project Server qui utilisent des champs personnalisés, des étapes, des phases et des types de projets d’entreprise qui peuvent être gérés dans Project Web App. Bien que vous puissiez utiliser Visual Studio pour développer des flux de travail, ils sont souvent plus faciles et plus rapides à créer à l’aide de SharePoint Designer. Visual Studio peut être utilisé pour les flux de travail qui nécessitent un accès au modèle objet client ou à d’autres API externes.
  
### <a name="project-add-ins"></a>Compléments Project

<a name="pj15_WhatsNew_Apps"> </a>

La distribution et la commercialisation de logiciels ont été révolutionnées par le concept du complément. Pour Project 2013, les compléments peuvent être disponibles à l’achat et au téléchargement à partir du magasin Office public ou distribués dans un catalogue privé sur SharePoint. Un complément est un programme interactif autonome qui effectue un petit nombre de tâches connexes. Un complément Project peut être un complément du volet Office pour les clients Project Standard 2013 ou Project Standard 2013, ou un complément pour Project Server 2013 ou Project Online.
  
Pour plus d’informations sur les compléments pour les clients du Bureau à distance Project, voir la section relative aux [compléments du volet de tâches dans Project](#pj15_WhatsNew_Agave). Pour obtenir un exemple Project Server 2013, consultez [Créer un complément SharePoint hébergé Project Server](create-a-sharepoint-hosted-project-server-add-in.md). En plus des articles du [SDK Office et SharePoint Compléments](https://msdn.microsoft.com/library/fp161507.aspx), le [blog Office](https://blogs.office.com/dev/) contient de nombreux billets qui sont également pertinents pour Project 2013 et Project Online.
  
Un complément pour Project Server 2013 peut fonctionner avec une installation locale et Project Online. Les compléments Project Server peuvent inclure des composants WebPart, des récepteurs d’événements à distance et une logique métier. L’accès au modèle objet Project Server dans un complément se fait par l’intermédiaire du modèle objet client, et pas de l’interface PSI. Le stockage de données peut être basé sur le cloud, par exemple avec des SQL Azure, externes comme par le biais de Microsoft Business Connectivity Services (BCS), internes à une base de données locale ou mixtes.
  
#### <a name="add-in-security"></a>Sécurité des compléments

En général, les actions effectuées par un complément sont effectuées pour le compte de l’utilisateur qui exécute le complément ; vous n’utilisez pas explicitement l’emprunt d’identité ni ne spécifiez qui peut exécuter le complément. Les actions ne peuvent pas dépasser le niveau d’autorisation de l’utilisateur qui exécute le complément.
  
Dans Office Outils de développement pour Visual Studio 2012, le fichier AppManifext.xml dispose d’un éditeur graphique dans lequel vous pouvez définir l’étendue de la demande d’autorisation. Par exemple, pour créer un complément qui permet aux chefs de projets de mettre à jour leurs projets, dans l’onglet **Autorisations** du volet Concepteur du fichier **AppManifest.xml**, sélectionnez **Projets multiples** pour la portée et **Écriture** pour l’autorisation. Si l’utilisateur du complément dispose des autorisations de chef de projets, il peut exécuter le complément pour les projets qu’il gère. Le code du fichier AppManifest.xml comprendrait les éléments suivants :
  
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
|**Compte-rendu** <br/> |**Lecture** (Nécessite l’autorisation de se connecter à Project Server.)  <br/> |
|**Flux de travail** <br/> |**Élever** (Nécessite l’autorisation d’exécuter des flux de travail. Le complément fonctionne avec des autorisations élevées afin de permettre des transitions d’une étape à une autre dans un flux de travail. Dans le complément, la logique métier contrôle les transitions d’étapes.)<br/> |

> [!NOTE]
> Project Server 2013 et Project Online n’utilisent pas le modèle d’authentification d’application uniquement dans SharePoint 2013 (voir les types de stratégie d’autorisation de complément [dans SharePoint 2013](https://msdn.microsoft.com/library/124879c7-a746-4c10-96a7-da76ad5327f0%28Office.15%29.aspx)).
  
Pour plus d’informations sur le développement, la distribution, l’hébergement et la gestion de compléments, consultez [SharePoint compléments et compléments](/sharepoint/dev/sp-add-ins/sharepoint-add-ins) Office, ainsi que des [rubriques connexes](/office/dev/add-ins/overview/office-add-ins) dans la documentation des développeurs SharePoint Server 2013 et Office 2013. Pour plus d’informations sur l’étendue de la demande d’autorisation pour d’autres compléments SharePoint, consultez [les autorisations de complément dans SharePoint 2013](https://msdn.microsoft.com/library/5f7a8440-3c09-4cf8-83ec-c236bfa2d6c4%28Office.15%29.aspx).
  
### <a name="integrating-with-sharepoint-server"></a>Intégration à SharePoint Server

<a name="pj15_WhatsNew_IntegrationWSS"> </a>

De nombreuses fonctionnalités de Project Web App nécessitent la nouvelle infrastructure dans SharePoint Server 2013, telles que l’authentification OAuth et basée sur les revendications, Project autorisations et autorisations de serveur via des groupes SharePoint, la synchronisation de projets avec des listes de tâches SharePoint et Project  Flux de travail déclaratifs du serveur. L’application de service du projet peut être associée à une collection de sites dans une batterie de serveurs SharePoint. La synchronisation du projet peut être réalisée avec une liste de tâches SharePoint, où SharePoint gère le projet. Un projet d’entreprise peut également être synchronisé avec une liste de tâches SharePoint, où Project Server maintient un contrôle total. Pour obtenir des diagrammes architecturaux et une explication de la synchronisation de projet, consultez [l’architecture Project Server 2013](project-server-2013-architecture.md).
  
Il existe de nombreuses nouvelles fonctionnalités dans SharePoint Server 2013. Pour plus d’informations, consultez [SharePoint pour les développeurs](https://msdn.microsoft.com/sharepoint).
  
### <a name="integrating-with-workflows"></a>Intégration aux flux de travail

<a name="pj15_WhatsNew_Workflow"> </a>

Les flux de travail représentent une fonctionnalité essentielle de la gestion de portefeuille de projets. Un cycle de vie du projet peut inclure des processus de longue durée qui couvrent de nombreuses phases. Les phases de gouvernance comprennent les propositions de projet, les analyses de l’impact de l’entreprise, ainsi que la sélection, la création, la planification, la gestion et le suivi des projets.
  
les flux de travail Project Server 2013 reposent sur la plateforme de flux de travail SharePoint 2013, qui utilise WF4. Contrairement aux versions précédentes, les flux de travail déclaratifs pour Project Server 2013 peuvent être créés à l’aide de SharePoint Designer 2013 et sont accessibles à la fois en local et en ligne. Project Workflows Server utilisent le modèle de sécurité de flux de travail SharePoint avec OAuth et peuvent être installés sur un site Project Web App. La figure 1 montre que SharePoint Designer 2013 peut ajouter des étapes à un flux de travail de site pour la gestion de la demande, où les étapes sont définies dans Project Web App.
  
**Figure 1. Utilisation de SharePoint Designer pour ajouter une étape à un flux de travail pour Project Web App**

![Ajout d’une étape à un flux de travail dans SPD](media/pj15_CreateWorkflowSPD_AddStageInSPD.gif "Ajout d’une étape à un flux de travail dans SPD")

Vous créez un flux de travail déclaratif en ajoutant des étapes de flux de travail, des actions, des conditions et d’autres éléments dans un outil de conception, qui peut être SharePoint Designer 2013 ou Visual Studio 2012. L’outil de conception enregistre ensuite le flux de travail en tant que code XAML qui est interprété au moment de l’exécution. Les workflows déclaratifs peuvent s’exécuter dans Project Server 2013 local ou dans Project Online. En utilisant Visual Studio 2012, vous pouvez également créer des actions et des formulaires personnalisés pour un contrôle supplémentaire, et enregistrer des modèles de flux de travail à réutiliser avec plusieurs instances Project Web App. SharePoint Designer 2013 peut utiliser des actions personnalisées créées dans Visual Studio 2012.
  
Un flux de travail Project Server 2013 agit comme une application, où un administrateur, qui dispose d’autorisations de conception pour Project Web App, peut publier un flux de travail déclaratif et l’associer à un type de projet d’entreprise (EPT). L’EPT doit être destiné à un projet d’entreprise, où Project Server conserve un contrôle total. Une liste de tâches SharePoint ne peut pas utiliser un flux de travail Project Server.
  
OAuth permet aux chefs de projets qui disposent d’autorisations de création de projets d’appeler le flux de travail sans utiliser l’emprunt d’identité. Les appels du flux de travail à Project Server, par exemple pour lire une valeur de champ personnalisé afin de décider quelle branche à suivre, sont réalisés au nom du chef de projets. Pour éviter que le chef de projets ne crée un flux de travail qui passe automatiquement à l’étape suivante, l’appel pour passer à l’étape suivante de flux de travail s’exécute comme l’auteur du flux de travail (l’administrateur). En revanche, les utilisateurs des flux de travail Project Server 2010 hérités effectuent des appels empruntés par le biais du compte d’utilisateur proxy de flux de travail pour accéder à l’administrateur tout au long du flux de travail.
  
Bien que Project Server 2013 en local puisse utiliser des flux de travail compilés basés sur WF3.5, nous vous recommandons de mettre à niveau les workflows hérités vers des flux de travail déclaratifs basés sur WF4. La nouvelle technologie est plus robuste et évolutive. Les analystes d’entreprise et le personnel de PMO peuvent créer ou mettre à jour des conceptions de flux de travail à l’aide de Visio 2013 et implémenter des flux de travail Project Server sans coder à l’aide de SharePoint Designer 2013.
  
Pour plus d’informations sur la création d’un flux de travail déclaratif pour Project Web App, consultez [Prise en main du développement de flux de travail Project Server](getting-started-developing-project-server-workflows.md). Pour obtenir une comparaison des fonctionnalités SharePoint Designer et Visual Studio pour les flux de travail, consultez [Développer des flux de travail SharePoint 2013 à l’aide de Visual Studio](https://msdn.microsoft.com/library/office/jj163199.aspx).
  
### <a name="client-side-object-model"></a>Modèle objet côté client

<a name="pj15_WhatsNew_CSOM"> </a>

L’accès par programme à Project Online nécessite un modèle CSOM basé sur le modèle CSOM SharePoint. Project Online’authentification sera auprès d’OAuth à l’aide d’un ID en direct Windows, et non de l’authentification Project Server Forms ou Authentification Windows.
  
Voici les principes et fonctionnalités du modèle CSOM dans Project Server 2013 :
  
- Le modèle objet client est conçu pour faciliter l’utilisation. Par exemple, les méthodes et les propriétés utilisent ou fournissent directement des données par nom, plutôt que d’exiger plusieurs GUID ou paramètres _changeXml_, ou de transmettre des jeux de données.
- Le modèle objet client Project Server implémente un sous-ensemble de la fonctionnalité de l’interface PSI, en se basant sur les exigences les plus courantes des solutions tierces.
- Le modèle objet client appelle l’interface PSI en interne, mais cela est pris en compte différemment. Par exemple, les mises à jour pour toutes les modifications d’état sont effectuées via la méthode **StatusAssignmentCollection.SubmitAllStatusUpdates**, et non via la méthode PSI **Statusing.SubmitStatus** pour l’utilisateur ou la méthode **SubmitStatusForResource** pour d’autres ressources.
- Le modèle objet client est accessible par un service WCF (Client.svc), plutôt que par les 22 services publics de l’interface PSI.
- L’initialisation du modèle CSOM Project Server se fait directement par le biais de la classe [ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) avec l’URL Project Web App, et non à l’aide d’une référence WCF ou d’un assembly proxy.
- Le modèle objet client implémente plusieurs interfaces et bibliothèques clientes, qui sont prises en charge par l’infrastructure CSOM SharePoint interne. Les interfaces et bibliothèques clientes sont les suivantes :

  - Bibliothèque cliente Microsoft .NET dans l’assembly Microsoft.ProjectServer.Client.dll

  - Bibliothèque Silverlight dans l’assembly Microsoft.ProjectServer.Client.Silverlight.dll

  - Bibliothèque Windows Phone 8 dans l’assembly Microsoft.ProjectServer.Client.Phone.dll

  - Bibliothèque JavaScript pour les applications web dans le fichier PS.js ou le fichier PS.debug.js

  - Points de terminaison REST pour l’accès avec le protocole OData

  - Prise en charge native pour les requêtes LINQ avec filtrage afin de limiter la quantité de données renvoyées

- Le modèle CSOM peut être utilisé à la fois pour les solutions Project Online et pour les solutions locales, indépendamment de l’interface PSI et d’autres assemblys Project Server tels que Microsoft.Office.Project.Server.Library.dll.
- Des fonctionnalités supplémentaires du modèle CSOM Project Server 2013 peuvent être prises en compte pour les mises à jour cumulatives et les service packs, en fonction des demandes des partenaires Project Server et de la communauté des développeurs.

> [!NOTE]
> Le modèle objet client représente l’interface privilégiée pour les développeurs tiers de Project Server. Nous vous recommandons d’utiliser le modèle objet client pour développer de nouvelles applications, si celui-ci inclut les fonctionnalités dont votre application a besoin.
  
Pour plus d’informations sur le développement avec le modèle CSOM, consultez le [modèle objet côté client (CSOM) pour Project 2013](client-side-object-model-csom-for-project-2013.md). Pour plus d’informations sur l’interface REST dans SharePoint applications, consultez _Programmation à l’aide du service REST SharePoint_ dans la documentation du développeur SharePoint 2013.
  
### <a name="changes-in-the-reporting-database"></a>Changements dans la base de données de rapports

<a name="pj15_WhatsNew_RDBChanges"> </a>

Les quatre bases de données de Project Server 2010 sont combinées en une seule base de données Project dans Project Server 2013. Le nom par défaut de la base de données Project est ProjectService. Les tables et vues de création de rapports conservent leurs noms précédents, et les tables et vues des bases de données Brouillon, Publié et Archive ont les préfixes `draft`, `pub`et `ver` dans la base de données ProjectService. Par exemple, la table de projets publiés s’intitule pub.MSP_PROJECTS.
  
> [!IMPORTANT]
> L’accès direct n’est pas pris en charge pour le brouillon (`draft` préfixe), les tables et les vues publiées (`pub`) et archivées (`ver`). Les rapports doivent utiliser uniquement les tables et les vues de création de rapports, qui ont le préfixe `dbo`. Par exemple, le dbo. MSP_EpmProject table inclut la liste des projets dans l’instance Project Web App.
>
> Rien ne vous empêche d’utiliser activement l’accès direct à la base de données par programme pour mettre à jour les données dans l’une des tables et vues dans la base de données Project. Vous devez être conscient que le cache Project Professionel, les tables des données brouillon et publiées, ainsi que les tables de rapport reposent tous sur un protocole de synchronisation de cache qui peut être perturbé par la modification directe de données. Toutefois, si vous endommagez vos bases de données Project Server ou les caches côté client Project Professionnel suite à un accès direct pour modifier les données, notez que le support technique ne sera pas en mesure de vous aider.
  
Project Server 2013 introduit un service OData pour l’accès en ligne et local. Les tables et vues de création de rapports en ligne sont exposées uniquement par l’interface OData ; pour une utilisation locale, vous pouvez utiliser l’interface OData ou accéder directement aux tables et vues de création de rapports dans la base de données ProjectService dans la batterie de serveurs SharePoint. Project Online ne prend pas en charge une base de données mutualisée. Autrement dit, plusieurs instances de Project Web App chacune ont leur propre base de données Project. Le service OData exécute en interne SQL requêtes sur les tables et les vues de création de rapports, et fournit une charge utile XML ou JSON. Pour une présentation du service OData pour la création de rapports dans Project Server 2013 et pour la référence de schéma **ProjectData**, consultez [ProjectData - Project référence du service OData](https://msdn.microsoft.com/library/office/jj163015.aspx).
  
Pour obtenir des informations générales sur les requêtes OData, consultez [les conventions OData : URI](https://www.odata.org/documentation/). Par exemple, vous pouvez voir tous les projets dans une instance locale de Project Web App où le nom du projet commence par « Test » à l’aide de la requête suivante dans un navigateur. Cliquez avec le bouton droit sur la page du navigateur, puis cliquez sur **Afficher la source**.
  
```html
https://ServerName /ProjectServerName /_api/ProjectData/Projects?$filter=startswith(ProjectName, 'Test') eq true
```

Pour importer des données de projet dans PowerPivot dans Excel 2013, dans le ruban DATA, sélectionnez **À partir du flux de données OData** dans le menu déroulant **D’autres sources**. Dans la boîte de dialogue **Assistant Connexion de données** , tapez <https://ServerName/ProjectServerName/_api/ProjectData/> l’emplacement du flux de données, choisissez **Suivant**, puis sélectionnez la table **Projets** dans la page **Sélectionner des tables** de l’Assistant. Nommez et enregistrez le fichier .odc, puis choisissez **Terminer**. Dans la boîte de dialogue **Importation de données**, choisissez **Rapport de tableau croisé dynamique**. Dans la feuille de calcul Excel, choisissez des champs pour les lignes et colonnes du tableau croisé dynamique que vous souhaitez afficher.
  
Les utilisateurs locaux Project Server, qui disposent des autorisations appropriées, peuvent accéder directement aux tables et vues de création de rapports via Microsoft SQL Server pour créer des rapports, comme ils le font dans Project Server 2010. Dans Project Server 2013, les utilisateurs peuvent également accéder aux tables de rapports locales via l’interface OData. Vous pouvez récupérer des données Project Server en ligne ou en local via des points de terminaison REST pour le service OData. Par exemple, la table dbo.MSP_PROJECT et la vue dbo.MSP_EpmProject_UserView peuvent être utilisées pour les rapports. Toutes les tables ou vues qui ont un , ou `ver` un préfixe sont destinées à une `draft``pub`utilisation interne par Project Server uniquement et ne sont pas destinées à l’utilisation de rapports. Par exemple, la table draft.MSP_TASKS et la vue pub.MSP_PROJECTS_WORKING_VIEW ne sont pas documentées et sont destinées à une utilisation interne uniquement.
  
> [!NOTE]
> Vous pouvez étendre la création de rapports en local en ajoutant des tables, vues, champs et procédures stockées dans une base de données distincte. Vous ne devez pas modifier les tables et vues de création de rapports existantes dans la base de données Project Server.
  
Les tables de création de rapports, les vues et les champs de la base de données Project sont documentés dans un fichier d’aide HTML dans une mise à jour ultérieure du téléchargement du Kit de développement logiciel (SDK) Project 2013. Pour obtenir de la documentation sur le schéma XML OData pour le service **ProjectData**, consultez [ProjectData - Project référence du service OData](https://msdn.microsoft.com/library/office/jj163015.aspx). Dans la plupart des cas, les requêtes des tables de création de rapports et des vues créées pour Project Server 2010 fonctionnent avec la base de données Project dans Project Server 2013. Les utilisateurs locaux peuvent accéder aux cubes OLAP Project Server dans SQL Server Analysis Services, comme ils le font actuellement. Dans Project Online, les cubes OLAP ne sont pas disponibles.
  
### <a name="task-pane-add-ins-in-project"></a>Compléments du volet de tâches dans Project

<a name="pj15_WhatsNew_Agave"> </a>

Project Standard 2013 et Project Professionnel 2013 prennent en charge les compléments du volet Office, qui peuvent être utilisés pour intégrer et afficher du contenu externe dans une page web. Le volet Office affiche le contenu de la page web qui a accès via JavaScript aux tâches, ressources, vues et données générales du projet. Le modèle objet JavaScript pour Project peut obtenir des informations sur une tâche ou une ressource sélectionnée, et peut obtenir des données dans une cellule sélectionnée dans la grille pour des vues telles que le diagramme de Gantt. Les compléments du volet de tâches pour Project peuvent également implémenter des gestionnaires d’événements pour des événements modifiés de sélection de tâche, de ressource ou de vue.
  
La figure 2 illustre le complément du volet de tâches **Hello ProjectData** qui interroge le service **ProjectData**, puis compare les données du projet actuel avec les moyennes de tous les projets. Le Project téléchargement du Kit de développement logiciel (SDK) 2013 inclut le code source complet du complément.
  
**Figure 2. Un complément du volet de tâches dans Project Professionel peut accéder à des données dans Project Server**

![Comparaison du projet actuel avec tous les projets](media/pj15_RestQueryApp_CompareProject.gif "Comparaison du projet actuel avec tous les projets")
  
> [!NOTE]
> Project Standard 2013 ne peut pas s’intégrer directement à Project Server 2013 via des compléments du volet Office.
  
Les compléments du volet Office dans Project Professionnel peuvent gérer les composants WebPart créés pour Project Server 2013, afin que les développeurs puissent créer une extension une fois qu’elle s’exécute avec Project Web App et Project Professionnel. Les compléments du volet Office général développés pour d’autres produits Office 2013 peuvent également être utilisés avec Project Standard 2013 et Project Professionnel 2013. Pour plus d’informations, voir [Task pane add-ins for Project](task-pane-add-ins-for-project.md).
  
### <a name="project-server-event-receivers"></a>Récepteurs d’événements Project Server

<a name="pj15_WhatsNew_Events"> </a>

Il peut y avoir plusieurs serveurs Project Web App (également appelés serveurs web frontaux ou WFE) dans une batterie de serveurs SharePoint qui inclut l’application de service Project principale. Les récepteurs d’événements peuvent également être appelés gestionnaires d’événements. Les gestionnaires d’événements locaux peuvent être implémentés avec le code de confiance totale et déployés sur l’ensemble des WFE pour une installation Project Server locale. Les récepteurs d’événements à distance peuvent être implémentés dans les services web sur des serveurs locaux ou à distance et accessibles par l’intermédiaire de plusieurs WFE et installations de Project Server. Project Online ne pouvez utiliser que des récepteurs d’événements distants.
  
les gestionnaires d’événements Project Server sont gérés par SharePoint pour chaque instance Project Web App, plutôt que par une page de Project Web App Paramètres spécifique. Dans l’application d’administration centrale SharePoint, choisissez Paramètres **d’application générale**, **choisissez Gérer** sous **PWA Paramètres**, puis choisissez l’instance dans la liste déroulante **Project Web App Instance** sur le PWA Paramètres  Page. Pour ajouter un gestionnaire d’événements local ou un récepteur d’événements à distance, choisissez **Gestionnaires d’événements côté serveur**.
  
Pour une installation locale de Project Server, vous pouvez créer un récepteur d’événements distant en tant que fonctionnalité de SharePoint qui utilise la classe [Microsoft.ProjectServer.Client.EventHandlerCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx) dans le modèle CSOM, puis gérer par programmation le récepteur d’événements à l’aide de méthodes de la classe [EventHandlerCollection](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCollection.aspx). Pour les récepteurs d’événements à distance, les pré-événements sont synchrones, les post-événements sont asynchrones et il existe un délai si le récepteur d’événements à distance ne renvoie rien.
  
> [!NOTE]
> L’Administration centrale de SharePoint est disponible uniquement pour les installations locales. Pour Project Online et SharePoint Online, vous pouvez ajouter ou supprimer des récepteurs d’événements distants à l’aide d’un package d’application CSOM.
  
Dans la page Gestionnaires d’événements côté serveur, le processus d’ajout d’un gestionnaire d’événements local pour une installation locale Project Server est presque le même que celui décrit dans le gestionnaire [d’événements Create a Project Server et consigne une rubrique d’événement](https://msdn.microsoft.com/library/gg615466.aspx) pour Project Server 2010. La différence est que la page Nouveau gestionnaire d’événements comporte des options supplémentaires. Par exemple, choisissez **Project Création** dans la liste **des événements**, puis choisissez **NOUVEAU GESTIONNAIRE D’ÉVÉNEMENTS**. Dans la page Nouveau gestionnaire d’événements, les deux seuls champs requis sont **Nom** et **Ordre** (voir la figure 3). Si vous ajoutez un gestionnaire d’événements de confiance totale local, ajoutez le champ **Nom de l’assembly** et le champ **Nom** de classe ; laissez **l’URL du point de terminaison** vide. Si vous ajoutez un récepteur d’événements distant, ajoutez **l’URL** du point de terminaison et laissez le nom de **l’assembly** et le **nom de classe** vides.
  
> [!CAUTION]
> Si vous spécifiez _à la fois_ le nom de l’assembly/nom de classe et l’URL du point de terminaison, Project Server appelle uniquement le gestionnaire d’événements local (local). Le récepteur d’événements à distance est ignoré.
>
> Si vous créez deux gestionnaires d’événements pour le même événement, où un gestionnaire d’événements est local et l’autre est un récepteur d’événements à distance, et que la valeur **Ordre** est identique pour les deux, Project Server ignore le récepteur d’événements à distance.
  
**Figure 3. Ajout d’un gestionnaire d’événements local ou d’un récepteur d’événements à distance**

![Configuration d’un gestionnaire d’événements ou d’un récepteur d’événements](media/pj15_EventHandlers_NewEventHandler.gif "Configuration d’un gestionnaire d’événements ou d’un récepteur d’événements")

Si vous avez besoin d’accéder aux jeux de données PSI pour un gestionnaire d’événements local, vous pouvez copier l’assembly Microsoft.Office.Project.Schema.dll à partir de [Windows]\Microsoft.NET\assembly\GAC\_MSIL\Microsoft.Office. Project. Répertoire Schema\v4.0_15.0.0.0__71e9bce111e9429c.

Au lieu de l’interface PSI, nous vous recommandons d’utiliser les classes d’événements dans l’espace **de noms Microsoft.ProjectServer.Client** ; le développement avec le modèle CSOM ne nécessite pas de manipulation de jeux de données. Pour développer des récepteurs d’événements distants pour Project Online, vous devez utiliser la classe [Event](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.Event.aspx) et la classe [EventHandlerCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx) dans le modèle CSOM.
  
Avant de déployer un gestionnaire d’événements Project Server, installez et testez le gestionnaire d’événements dans le cadre d’une installation test de Project Server. Pour une installation locale Project Server, si le gestionnaire d’événements local que vous ajoutez devient inopérant, le service d’événements Project Server 2013 ne parvient pas à charger les autres gestionnaires d’événements personnalisés valides. Dans ce cas, vous devez supprimer le gestionnaire d’événements à l’origine du problème et redémarrer le service d’événements.
  
> [!NOTE]
> Pour une installation de Project Server locale, nous vous recommandons de migrer vers les récepteurs d’événements à distance à l’aide du modèle objet client pour développer les récepteurs d’événements. Étant donné que les récepteurs d’événements à distance ne disposent pas de code tiers en cours d’exécution au sein du service d’événements Project Server, les récepteurs d’événements à distance sont plus stables. Les administrateurs locaux n’ont plus la responsabilité de gérer le service d’événements Project Server.
  
Pour obtenir des informations générales sur les événements, consultez [Gestion des événements dans les applications pour SharePoint](https://msdn.microsoft.com/library/jj220048%28office.15%29.aspx).
  
## <a name="deprecated-features"></a>Fonctionnalités déconseillées

<a name="pj15_WhatsNew_Deprecated"> </a>

> [!NOTE]
> Pour plus d’informations sur les fonctionnalités et LES API qui sont dépréciées ou supprimées dans Project Server 2016 préversion, consultez [Ce qui est déconseillé ou supprimé dans Project Server 2016 préversion](/project/what-s-deprecated-or-removed-in-project-server-2016).
  
Les fonctionnalités déconseillées sont toujours disponibles dans Project 2013 pour certaines solutions, mais ne doivent pas être utilisées pour le nouveau développement. La plupart des fonctionnalités et pratiques suivantes ne fonctionnent pas avec Project Online ou avec l’installation locale par défaut de Project Server 2013 en mode d’autorisation SharePoint. Les solutions existantes qui utilisent ces fonctionnalités peuvent ne pas fonctionner pour une mise à niveau de Project Server 2010 vers Project Server 2013. Bien que les solutions qui utilisent des fonctionnalités déconseillées puissent continuer à fonctionner dans certains cas, elles ne sont pas entièrement prises en charge pour toutes les installations Project 2013.
  
Si vos solutions utilisent des fonctionnalités déconseillées, elles doivent être testées avant le déploiement et vous devez les modifier pour utiliser les fonctionnalités prises en charge dès que cela est possible. Pour plus d’informations sur la configuration de la sécurité locale Project Server 2013 pour Project mode d’autorisation, consultez la section _SharePoint Mode d’autorisation_ dans [Nouveautés pour les professionnels de l’informatique dans Project Server 2013](/project/what-s-new-for-it-pros-in-project-server-2016).
  
- **Les scénarios** [d’extension PSI des extensions](/previous-versions/office/developer/office-2010/ff843378(v=office.14)) sont déconseillés et ne seront pas pris en charge dans les versions ultérieures. Ces scénarios locaux Project Server 2013 ont permis l’intégration à l’aide de services wcF (Windows Communication Foundation) personnalisés.
  
- **Project PSI** La [classe Project](./project-psi-reference-overview.md) de l’interface PSI est déconseillée. Pour tous les nouveaux développements, utilisez le [modèle objet Project](client-side-object-model-csom-for-project-2013.md). Project Les applications Server 2013 qui utilisent l’interface PSI Project continueront de fonctionner, mais Project Online applications devront remplacer toutes les méthodes PSI de classe Project par leurs méthodes CSOM équivalentes.
  
- **INTERFACE PSI du plan de ressources** [L’interface PSI du plan de ressources](/previous-versions/office/project-class/gg240019(v=office.15)) est déconseillée. Il continuera d’être pris en charge pour le développement Project 2013, mais ne sera pas pris en charge dans les versions ultérieures.
  
- **Interface ASMX pour l’interface PSI** L’interface PSI inclut des interfaces en double pour le développement d’extensions Project Server locales. L’interface des services web ASMX a été introduite avec la première implémentation de l’interface PSI dans Office Project Server 2007. Project Server 2010 a ajouté l’interface des services WCF, où le modèle objet duplique essentiellement les services web ASMX. Bien que Project Server 2013 continue de prendre en charge ASMX et WCF, les nouvelles solutions qui nécessitent l’interface PSI doivent utiliser les services WCF. Si possible, les nouvelles solutions doivent être écrites en utilisant le modèle objet client.
  
  Les services web ASMX de l’interface PSI sont déconseillés dans Project Server 2013. Pour qu’elles fonctionnent dans les futures versions de Project Server, les solutions utilisant les services web ASMX doivent être réécrites afin d’utiliser soit les services WCF, soit le modèle objet client. Pour plus d’informations, consultez la section _Mise à niveau des applications avec les API serveur Project_ dans [Project Programmabilité du serveur](project-server-programmability.md).
  
- **Fournisseur de liens d’objet (OLP)** Dans les versions précédentes de Project Server, le service **ObjectLinkProvider** dans l’interface PSI (voir [WebSvcObjectLinkProvider](/previous-versions/office/ms481347(v=office.14)) permet de gérer les liens d’objets web entre les tâches de projet d’entreprise et les listes de SharePoint spécialisées dans le site du projet pour les problèmes, les risques, les livrables et les documents. Dans Project Server 2013, le protocole OLP est déconseillé.
  
  Vous pouvez utiliser la classe **[RelatedItemManager](/previous-versions/office/sharepoint-server/jj168020(v=office.15))** dans le SharePoint CSOM pour créer, lire et supprimer des liens d’objets web entre les éléments de la liste des tâches et les autres listes d’un site de projet. Par exemple, pour ajouter un lien à partir d’un élément de tâche à un problème, vous pouvez utiliser la méthode **[AddSingleLink](/previous-versions/office/sharepoint-server/jj166451(v=office.15))** ou l’une des deux méthodes similaires, **AddSingleLinkFromUrl** ou **AddSingleLinkToUrl**. La classe **RelatedItemManager** inclut également des méthodes pour supprimer une liaison d’objet web et pour lire les éléments associés. Pour la classe équivalente dans le modèle objet JSOM (modèle objet JavaScript), consultez [SP. Objet RelatedItemManager (sp.js)](/previous-versions/office/sharepoint-visio/jj838582(v=office.15)).
  
  Nous vous recommandons d’utiliser le modèle CSOM SharePoint pour créer des applications de type OLP pour une installation locale de Project Server 2013 et pour Project Online. [L’espace de noms Microsoft.SharePoint](/previous-versions/office/sharepoint-server/ms464984(v=office.15)) n’inclut pas de classe **RelatedItemManager** ****.
  
- **Autorisations personnalisées** Les autorisations de sécurité personnalisées pour accéder à des fonctionnalités ou extensions de serveur Project spécifiques ont été prises en charge dans Office Project Server 2007, où un article du Kit de développement logiciel (SDK) expliquait comment les créer en modifiant directement la base de données publiée. Dans Project Server 2010, les autorisations personnalisées fonctionnent toujours, mais sont déconseillées. Dans Project Server 2013, les autorisations personnalisées ne fonctionnent pas avec le mode d’autorisation SharePoint par défaut pour les installations locales. Pour le mode d’autorisation Project, les autorisations personnalisées sont prises en charge. Avec Project Online, l’accès direct à la base de données n’est pas possible.
  
- **Imitation** L’emprunt d’identité dans les applications PSI, où l’utilisateur d’une application peut assumer les autorisations de sécurité d’un autre utilisateur Project Server, est déconseillé dans Project Server 2013. Comme indiqué précédemment, une installation locale Project Server 2013 par défaut utilise SharePoint mode d’autorisation, qui n’autorise pas l’emprunt d’identité dans les groupes de sécurité Project Server. Pour plus d’informations, consultez [Authentification, autorisation et sécurité dans SharePoint 2013](/sharepoint/dev/general-development/authentication-authorization-and-security-in-sharepoint).
  
  Les applications de gestion des états sont des extensions par défaut qui ont peut-être déjà utilisé l’emprunt d’identité dans les versions précédentes de Project Server. Project Server 2010 a introduit la méthode **ReadStatusForResource** et la méthode **SubmitStatusForResource** dans l’interface PSI, ainsi que l’autorisation globale **StatusBrokerPermission**, ce qui a éliminé la nécessité d’emprunter l’identité pour lire et mettre à jour l’état pour le compte d’un autre utilisateur. Le modèle CSOM dans Project Server 2013 utilise l’interface PSI sous-jacente pour activer en toute transparence les extensions d’état et peut être utilisé pour les installations Project Online ou locales.
  
- **Génération de rapports d’extensions de base de données** L’ajout de tables et de vues personnalisées à la base de données de rapports est une pratique courante avec les versions précédentes de Project Server. Étant donné que Project Server 2013 combine les quatre bases de données des versions précédentes en une seule base de données, les mises à niveau ne transfèrent pas les tables personnalisées, les vues ou les SPROC aux tables de création de rapports de la base de données Project Server 2013.
  
  Nous vous recommandons d’utiliser SQL Azure ou une base de données SQL Server distincte pour les tables et vues de création de rapports personnalisées, où vous pouvez gérer les sauvegardes et les mises à jour de base de données. Pour Project Online, cela est obligatoire.
  
- **Rapports** Les tables et vues de création de rapports locales dans la base de données Project Server, ainsi que les cubes OLAP, _ne sont pas_ dépréciées et restent entièrement prises en charge. Toutefois, les tables et vues de création de rapports (la base de données de rapports dans les versions précédentes Project Server) ne sont pas accessibles dans Project Online. De même, les cubes OLAP sont disponibles uniquement avec les installations locales de Project Server 2013. Pour générer des rapports d’applications avec Project Online, vous pouvez utiliser le service **ProjectData**, via des requêtes REST avec le protocole OData.
  
- **Project Guide** Le guide de Project est une fonctionnalité standard des applications de bureau Office Project 2007, où le contenu HTML et JavaScript dans un volet Office fournit des conseils interactifs pour la création et la gestion de projets. Dans Project 2010, le guide de Project n’est pas disponible dans une installation par défaut, mais peut être activé via VBA ou un complément VSTO. Le Project téléchargement du Kit de développement logiciel (SDK) 2010 inclut les fichiers Project Guide modifiés.
  
  Modèle objet VBA et **Microsoft.Office. Le modèle objet Interop.MSProject** dans Project 2013 inclut toujours les 22 membres de la classe **Application** et la classe **Project** qui peut gérer le guide de Project. Toutefois, Project applications du volet Office 2013 peuvent entrer en conflit avec les actions d’un volet office Project Guide et le contenu du guide Project ne peut pas être facilement distribué ou vendu dans le Office Store. Nous vous recommandons vivement de développer Project solutions de volet Office avec des compléments Office, et non du contenu personnalisé Project Guide. Pour plus d’informations sur le Guide Project, consultez la [documentation du SDK Project 2010](https://msdn.microsoft.com/library/ms512767.aspx).
  
## <a name="comparing-project-server-on-premises-with-project-online"></a>Comparaison de Project Server local avec Project Online

<a name="pj15_WhatsNew_Comparing"> </a>

Pour vous aider à déterminer s’il faut utiliser Project Serveur local ou Project Online, et les types d’extensions que vous pouvez développer dans les deux cas, le tableau 2 compare les fonctionnalités extensibles d’une installation locale de Project Server 2013 à Project Online. Le tableau 2 ne comprend pas les différences en matière de déploiement, d’administration ou d’utilisation. Pour plus d’informations sur Project Online et Project Server 2013, consultez [Project 2013 pour les développeurs](https://developer.microsoft.com/project/docs) et [les Project Online](https://developer.microsoft.com/project).
  
**Tableau 2. Extensibilité de Project Server local et de Project Online**

| Fonctionnalité |Project Server local | Project Online |
|:-----|:-----|:-----|
|**Programmabilité** <br/> |Applications basées sur le modèle objet client ; modèle de programmation cohérent  <br/>- Bibliothèques clientes .NET, Silverlight Windows Phone  <br/>- Bibliothèque JavaScript pour les pages personnalisées, les composants WebPart et les extensions de ruban  <br/>- Protocoles OData et REST<br/><br/> Applications basées sur l’interface PSI ; modèle de programmation complexe, pouvant également créer des applications pour l’administration, l’analyse de portefeuille, les notifications, la sécurité en mode Project, le système de file d’attente, ainsi que d’autres domaines<br/><br/>Extensions de l’interface PSI  <br/><br/>Autorisations personnalisés avec la sécurité en mode Project (déconseillé)  <br/><br/>Emprunt d’identité avec l’interface PSI (déconseillé)  <br/><br/>Code de confiance totale ; installation d’extensions dans une batterie de serveurs SharePoint  <br/> |Applications basées sur le modèle objet client ; modèle de programmation cohérent  <br/>- Bibliothèques clientes .NET, Silverlight Windows Phone<br/>- Bibliothèque JavaScript pour les pages personnalisées, les composants WebPart et les extensions de ruban<br/>- Protocoles OData et REST<br/><br/>Possibilité d’utiliser l’interface PSI, mais elle n’est pas prise en charge : aucune connexion OAuth et service-à-service<br/><br/>Aucune extension de l’API CSOM<br/><br/>Aucune autorisation personnalisée<br/><br/>Aucun emprunt d’identité<br/><br/>Aucun code de confiance totale  <br/> |
|**Bases de données personnalisées** <br/> |- SQL Azure  <br/>- SQL Server (la modification des tables et des vues de création de rapports dans la base de données Project Server n’est pas prise en charge)  <br/> |- SQL Azure  <br/>- SQL Server (la modification des tables et des vues de création de rapports dans la base de données Project Server n’est pas prise en charge)  <br/> |
|**Compte-rendu** <br/> |- **Service ProjectData** ; Protocoles OData et REST  <br/>- Création de rapports de tables et de vues dans la base de données Project Server<br/>- Base de données OLAP  <br/> |- **Service ProjectData** ; Protocoles OData et REST  <br/> |
|**Gestionnaires d’événements** <br/> |- Récepteurs d’événements distants, accessibles via des points de terminaison WCF<br/>- Gestionnaires d’événements de confiance totale, installés dans SharePoint batterie de serveurs  <br/> | - Récepteurs d’événements distants, accessibles via des points de terminaison WCF  <br/> |
|**Flux de travail** <br/> |Workflows déclaratifs, créés avec SharePoint Designer 2013<br/>- Utiliser uniquement sur une instance de Project Web App spécifique<br/>- Peut importer une conception de flux de travail à partir de Visio 2013<br/>- Peut importer et utiliser des actions personnalisées<br/><br/> Flux de travail déclaratifs, créés avec Visual Studio 2012<br/>- Créer une application qui peut inclure des flux de travail<br/>- Créer un package de solution SharePoint (.wsp) qui peut inclure des flux de travail<br/>- Créer des modèles de flux de travail à réutiliser<br/>- Créer et utiliser des actions personnalisées  <br/><br/>Possibilité d’utiliser des flux de travail compilés et hérités créés avec WF3.5 (mise à niveau recommandée vers un flux de travail WF4 déclaratif)  <br/> |Workflows déclaratifs, créés avec SharePoint Designer 2013<br/>- Utiliser uniquement sur une instance de Project Web App spécifique<br/>- Peut importer une conception de flux de travail à partir de Visio 2013<br/>- Peut importer et utiliser des actions personnalisées  <br/><br/>Flux de travail déclaratifs, créés avec Visual Studio 2012<br/>- Créer une application qui peut inclure des flux de travail  <br/>- Créer un package de solution SharePoint (.wsp) qui peut inclure des flux de travail<br/>- Créer des modèles de flux de travail à réutiliser <br/>- Créer et utiliser des actions personnalisées  <br/> |
|**Distribution** <br/> |- Office Store (pour les applications basées sur CSOM)<br/>- Catalogue d’applications privées sur SharePoint<br/>- Partage de fichiers intranet  <br/> |- Office Store<br/>- Catalogue d’applications privées sur SharePoint  <br/> |

## <a name="conclusion"></a>Conclusion

<a name="pj15_WhatsNew_Conclusion"> </a>

Project Server 2013 offre une multitude de nouvelles fonctionnalités et scénarios de développement que les partenaires et les clients peuvent utiliser pour adapter et étendre les fonctionnalités et l’utilité de Project Server dans les grandes entreprises et dans les petites organisations. Vous pouvez utiliser l’infrastructure pour Office 2013 et SharePoint 2013 afin de créer et de distribuer des applications pour Project 2013 qui peuvent considérablement étendre la commercialisation et l’utilisation d’applications personnalisées. Certaines fonctionnalités et pratiques d’extensibilité des versions précédentes sont déconseillées dans Project 2013, en particulier les services web ASMX de l’interface PSI et les fonctionnalités qui impliquent l’emprunt d’identité ou des modifications directes de base de données, qui ne peuvent pas être utilisées avec Project Online.
  
L’introduction du modèle CSOM permet d’accéder par programmation à Project Online pour un large éventail d’appareils et à l’aide de JavaScript dans les applications web. Le modèle objet client fournit un modèle de programmation plus cohérent par rapport à l’interface PSI. Les données de Project Server peuvent être consultées de nombreuses autres façons que dans les versions précédentes, y compris à travers le service OData en ligne et par le biais de points de terminaison REST pour les données de création de rapports dans la base de données Project. Les rapports existants fonctionnent toujours de la même manière qu’en local et les nouveaux rapports ont plus de flexibilité.
  
Office compléments offrent une nouvelle voie pour vendre des solutions et intégrer Project Standard 2013 au contenu web et à d’autres produits Office 2013. Vous pouvez également créer de nouvelles façons d’intégrer Project Professionnel 2013 aux données et aux listes SharePoint Project Server via le volet Office Office compléments.
  
Pour plus d’informations sur le développement d’applications et l’utilisation des fonctionnalités de programmabilité et du modèle CSOM de SharePoint Server 2013, consultez [SharePoint pour les développeurs](/sharepoint/dev/) et [Office pour les développeurs](https://developer.microsoft.com/office/docs).
  
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
