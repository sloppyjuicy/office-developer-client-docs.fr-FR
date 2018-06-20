---
title: Mises à jour pour les développeurs dans Project
manager: soliver
ms.date: 09/29/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b2b22cd-6e28-43a8-9092-b411da8bfb53
description: Nouvelles fonctionnalités incluent un modèle objet côté client (CSOM), les interfaces REST, un service OData pour la création de rapports, des récepteurs d’événements distants, flux de travail déclaratifs et compléments de volet de tâches pour les clients Project.
ms.openlocfilehash: facd52c5ba2473de41f2a6bede431af0f55ba4ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787938"
---
# <a name="updates-for-developers-in-project"></a>Mises à jour pour les développeurs dans Project

Fonctionnalités d’extensibilité dans Project Server 2013 fonctionnent avec des compléments pour Project Online et installations locales. Nouvelles fonctionnalités incluent un modèle objet côté client (CSOM), les interfaces REST, un service OData pour la création de rapports, des récepteurs d’événements distants, flux de travail déclaratifs et compléments de volet de tâches pour les clients Project. Découvrez également les fonctionnalités déconseillées qui ne doivent pas être utilisées pour le développement de nouveau.
  
Project Server 2013 s’appuie sur l’infrastructure introduit avec Microsoft Office Project Server 2007 et étendu par Project Server 2010. Project Server 2013 ajoute un modèle objet côté client (CSOM) qui est refactoriser simplifié à partir de l’Interface Project Server (PSI) et contient une bibliothèque JavaScript et des bibliothèques de .NET Framework 4 pour les applications Windows, Windows Phone 8 et Microsoft Silverlight. Le modèle est conçu pour le développement pour Project Online et fonctionne également avec une installation de Project Server sur site. 

Les bases de données Project Server sont regroupées dans une base de données ; Vous pouvez accéder en ligne tables de création de rapports et des vues via un service OData. Le modèle CSOM et le service OData incluent une interface Representational State Transfer (REST). Flux de travail Project Server peut être créés à l’aide de SharePoint Designer 2013. Project Professionnel 2013 peut s’intégrer avec le rapport des données, les listes de tâches SharePoint et les autres contenus externes en utilisant le modèle d’extensibilité des compléments Office des volets Office Project Server. Project Standard 2013 pouvez utiliser des compléments de volet de tâches pour intégrer le contenu externe généraux.
  
Pour plus d’informations sur les modifications majeures dans Project Server 2013 et des diagrammes, voir [architecture de Project Server 2013](project-server-2013-architecture.md).
  
> [!NOTE]
> Project Server 2013 repose sur la plateforme SharePoint Server 2013 et Project 2013 présente l’essentiel de la même infrastructure que les autres applications Office 2013. Pour la documentation du modèle pour SharePoint Add-ins, flux de travail basées sur SharePoint, des composants WebPart, développement avec d’autres fonctionnalités SharePoint et de la documentation des compléments Office, voir [Office et SharePoint Add-ins](http://msdn.microsoft.com/library/fp161507%28office.15%29.aspx) et [développement SharePoint 2013 vue d’ensemble](http://msdn.microsoft.com/library/jj164084%28office.15%29.aspx). 
  
## <a name="major-new-features-in-project-2013"></a>Principales nouvelles fonctionnalités de Project 2013
<a name="pj15_WhatsNew_MajorNewFeatures"> </a>

Nouvelles fonctionnalités de Project Standard 2013 et Project Professional 2013 incluent qui correspond aux autres applications Office 2013 et prend en charge l’interface utilisateur de style moderne dans Windows 8, l’intégration avec les objets Office Art pour des rapports d’avancement, l’interface utilisateur améliorée les rapports et les nouvelles fonctionnalités de la programmabilité de rapports. Project Professional 2013 permet aux plus étendues partage et synchronisation de projets dans SharePoint Server 2013, ainsi que les tâche volet compléments qui sont également implémentées dans d’autres applications Office 2013, telles que Word, Excel et Outlook.
  
Il existe plusieurs nouvelles fonctionnalités dans Project Server 2013. Certains n’ont pas d’un article de la programmabilité principaux, tels que la chronologie de nouveau dans Project Web App. Ces fonctionnalités seront documentées dans la documentation d’aide et de l’utilisateur final sur Microsoft Office Online et dans les rubriques destinés aux administrateurs et les professionnels de l’informatique sur Microsoft TechNet. Autres nouvelles fonctionnalités, telles que des feuilles de temps améliorées, rendent plus facile pour les développeurs tiers interagir avec des feuilles de temps et état via l’Interface Project Server (PSI).
  
L’ajout de Project Online et l’Office Store (http://office.microsoft.com/store) pour les compléments de projet sont des modifications, où Project Server est accessible via Microsoft Azure. Nuage l’accès à Project Server utilise un modèle objet côté client (CSOM) pour le développement de compléments Microsoft .NET Framework, Microsoft Silverlight, Windows Phone, et les applications web qui utilisent JavaScript. Une exigence de Project Online est que les quatre bases de données Project Server des versions précédentes sont fusionnés dans une base de données.
  
L’évolutivité et les performances de project Server 2013 est améliorée dans de nombreux domaines tels que la gestion de projets, des feuilles de temps et état de la tâche. Flux de travail Project Server ont été repensées avec la version 4 de Windows Workflow Foundation (WF4). Utilisation du .NET Framework 4 et Windows Communication Foundation (WCF) avec l’interface PSI améliore la sécurité, de performances et d’évolutivité. Par exemple, vous pouvez modifier le protocole de transport des applications basées sur WCF à l’aide de fichiers de configuration, sans modifier le code d’application ou recompilation. Project Web App met en cache beaucoup d’appels PSI où données ne changent pas vraiment.
  
> [!NOTE]
> Pour le développement avec Project Server 2013, vous pouvez utiliser Visual Studio avec les extensions d’outils Office et SharePoint, qui peuvent créer en mode natif des compléments pour les produits Office 2013. Project Server 2013 requiert Visual Studio afin d’activer entièrement le développement de fonctionnalités telles que les pages de détails de projet et des applications basées sur WCF. Les extensions d’outils SharePoint dans Visual Studio peuvent déployer des composants WebPart et autres fonctionnalités SharePoint directement dans Project Web App et autres sites SharePoint. 
>
> Visual Studio n’est plus requise pour développer des flux de travail Project Server qui utilisent des champs personnalisés, des phases, des phases et des types de projets d’entreprise qui peuvent être gérés dans Project Web App. Bien que vous pouvez utiliser Visual Studio pour développer des flux de travail, ils sont souvent plus facile et plus rapides à créer à l’aide de SharePoint Designer. Visual Studio peut être utilisé pour les flux de travail qui nécessite un accès à la CSOM ou d’autres API externe. 
  
### <a name="project-add-ins"></a>Compléments Project
<a name="pj15_WhatsNew_Apps"> </a>

Distribution et marketing du logiciel a été révolutionné avec le concept d’un complément. Pour Project 2013, les compléments peuvent être rendues disponibles pour l’achat et le téléchargement de l’Office Store public ou distribués dans un catalogue privé sur SharePoint. Un complément est généralement un programme autonome et interactif qui effectue un petit nombre de tâches connexes. Un complément Project peut être une tâche volet macro complémentaire pour les clients Project Standard 2013 Project Standard 2013, ou un complément pour Project Server 2013 ou Project Online.
  
Pour plus d’informations à propos des compléments pour les clients de bureau Project, voir [tâche volet des compléments dans le projet](#pj15_WhatsNew_Agave). Pour obtenir un exemple de Project Server 2013, voir [le complément Project créer un hébergée dans SharePoint Server](create-a-sharepoint-hosted-project-server-add-in.md). Outre les articles dans [Office et SharePoint Add-ins SDK](http://msdn.microsoft.com/library/fp161507.aspx), le [Blog Office](https://blogs.office.com/dev/) a nombreuses publications sont également pertinentes à Project 2013 et Project Online. 
  
Un complément pour Project Server 2013 peut fonctionner avec une installation sur site et de Project Online. Compléments Project Server peuvent inclure des composants WebPart, les récepteurs d’événements distants et la logique métier. Accès au modèle objet Project Server dans un complément est par le biais du modèle CSOM, pas l’interface PSI. Stockage des données peut être basées sur le nuage tels que SQL Azure, externes tels que par le biais de Microsoft Business Connectivity Services (BCS), interne avec une base de données locale, ou mixte.
  
#### <a name="add-in-security"></a>Ajout de sécurité

En règle générale, les actions effectuées par un complément sont effectuées au nom de l’utilisateur qui exécute le complément ; ne pas explicitement utiliser l’emprunt d’identité ou de spécifier les personnes autorisées à exécuter la macro complémentaire. Actions ne peut pas dépasser le niveau d’autorisation de l’utilisateur qui exécute la macro complémentaire. 
  
Dans les outils de développement Office pour Visual Studio 2012, le fichier AppManifext.xml possède un éditeur graphique dans laquelle vous pouvez définir l’étendue de demande d’autorisation. Par exemple, pour créer un complément qui permet aux responsables de projet mettre à jour leurs projets, sous l’onglet **autorisations** du volet Concepteur **AppManifest.xml** , sélectionnez **Plusieurs projets** pour l’étendue et **l’écriture** pour l’autorisation. Si l’utilisateur dispose des autorisations de gestionnaire de projet, il peut exécuter la macro complémentaire pour les projets dont il gère. Le code dans le fichier AppManifest.xml serait sont les suivantes : 
  
```XML
  <AppPermissionRequests>
    <AppPermissionRequest Scope="http://sharepoint/projectserver/projects" Right="Write" />
  </AppPermissionRequests>
```

**Le tableau 1. Étendues des demandes d’autorisation pour les compléments Project Server**

|Portée|Autorisations|
|:-----|:-----|
|**Project Server** <br/> |**Gérer les** (Requiert des autorisations d’administrateur de Project Server).  <br/> |
|**Plusieurs projets** <br/> |**Lecture**, **écriture** (requiert des autorisations de gestionnaire de projet pour certaines opérations ; autorisations de membre de l’équipe de projet pour basic lire des opérations, telles que les affectations de tâches.)  <br/> |
|**Projet unique** <br/> |**Lecture**, **écriture** (requiert au moins des autorisations de membre d’équipe de projet ; l’accès à des données dans un projet dépend des autres niveaux d’autorisation.)  <br/> |
|**Ressources d’entreprise** <br/> |**Lecture**, **écriture** (requiert des autorisations de gestionnaire de ressources).  <br/> |
|**État** <br/> |**SubmitStatus** (Requiert l’autorisation pour envoyer l’état de vos projets.)  <br/> |
|**Création de rapports** <br/> |**En lecture** (Requiert l’autorisation d’ouvrir une session sur Project Server.)  <br/> |
|**Flux de travail** <br/> |**Élever** (Requiert l’autorisation d’exécuter des flux de travail. Le complément s’exécute avec des autorisations élevées pour activer les transitions pour chaque étape dans un flux de travail. Logique métier dans le complément de contrôle transitions étape).  <br/> |
   
> [!NOTE]
> Project Server 2013 et Project Online n’utilisent pas le modèle d’authentification d’application uniquement dans SharePoint 2013 (voir le [complément de types de stratégie d’autorisation dans SharePoint 2013](http://msdn.microsoft.com/library/124879c7-a746-4c10-96a7-da76ad5327f0%28Office.15%29.aspx)). 
  
Pour plus d’informations sur le développement, distribuer, l’hébergement et la gestion des compléments, voir les rubriques connexes dans la documentation du développeur SharePoint Server 2013 et Office 2013 et [des compléments Office](http://msdn.microsoft.com/library/1e123201-6e70-45c1-a48c-d5b955896ddb%28Office.15%29.aspx)et [SharePoint Add-ins](http://msdn.microsoft.com/library/cd1eda9e-8e54-4223-93a9-a6ea0d18df70%28Office.15%29.aspx) . Pour plus d’informations sur l’étendue de demande d’autorisation pour les autres compléments SharePoint, voir [Add-in permissions in SharePoint 2013](http://msdn.microsoft.com/library/5f7a8440-3c09-4cf8-83ec-c236bfa2d6c4%28Office.15%29.aspx).
  
### <a name="integrating-with-sharepoint-server"></a>Intégration à SharePoint Server
<a name="pj15_WhatsNew_IntegrationWSS"> </a>

De nombreuses fonctionnalités dans Project Web App nécessitent la nouvelle infrastructure dans SharePoint Server 2013 telles que OAuth et l’authentification basée sur les revendications, d’autorisation Project Server et les autorisations par le biais des groupes SharePoint, la synchronisation des projets avec les tâches SharePoint listes et des flux de travail déclaratifs Project Server. L’Application de Service Project peut être associée à n’importe quelle collection de sites dans une batterie de serveurs SharePoint. Synchronisation de projet peut être une liste de tâches SharePoint, où SharePoint tient à jour le projet. Un projet d’entreprise peut également être synchronisé avec une liste de tâches SharePoint, où Project Server gère le contrôle total. Pour les schémas d’architecture et une explication de la synchronisation de project, voir [architecture de Project Server 2013](project-server-2013-architecture.md).
  
Il existe plusieurs nouvelles fonctionnalités dans SharePoint Server 2013. Pour plus d’informations, voir [SharePoint pour les développeurs](http://msdn.microsoft.com/en-US/sharepoint).
  
### <a name="integrating-with-workflows"></a>Intégration aux flux de travail
<a name="pj15_WhatsNew_Workflow"> </a>

Les flux de travail représentent une fonctionnalité essentielle de la gestion de portefeuille de projets. Un cycle de vie du projet peut inclure des processus de longue durée qui couvrent de nombreuses phases. Les phases de gouvernance comprennent les propositions de projet, les analyses de l’impact de l’entreprise, ainsi que la sélection, la création, la planification, la gestion et le suivi des projets.
  
Flux de travail Project Server 2013 reposant sur la plateforme de flux de travail SharePoint 2013, qui utilise WF4. À la différence dans les versions précédentes, le flux de travail déclaratif pour Project Server 2013 peut être créé à l’aide de SharePoint Designer 2013 et est accessible pour locale et une utilisation en ligne. Flux de travail Project Server utilisent le modèle de sécurité de flux de travail SharePoint avec OAuth et peut être installé sur un site Project Web App. La figure 1 montre que SharePoint Designer 2013 peuvent ajouter des étapes à un flux de travail pour la gestion de la demande, où les étapes sont définies dans Project Web App.
  
**La figure 1. Utilisation de SharePoint Designer pour ajouter une étape à un flux de travail pour Project Web App**

![Ajout d’une étape à un flux de travail dans SPD] (media/pj15_CreateWorkflowSPD_AddStageInSPD.gif "Ajout d’une étape à un flux de travail dans SPD")

<br/>

Vous créez un flux de travail déclaratif en ajoutant des étapes de flux de travail, actions, conditions et autres éléments dans un outil de conception, qui peut être SharePoint Designer 2013 ou Visual Studio 2012. L’outil de création puis enregistre le flux de travail en tant que code XAML, qui est interprété au moment de l’exécution. Flux de travail déclaratifs permettre s’exécuter dans Project Server 2013 sur site ou dans Project Online. À l’aide de Visual Studio 2012, vous pouvez également générer des actions personnalisées et des formulaires pour un contrôle supplémentaire et enregistrer des modèles de flux de travail pour les réutiliser avec plusieurs instances de Project Web App. SharePoint Designer 2013 peut consommer des actions personnalisées qui sont créées dans Visual Studio 2012.
  
Un flux de travail Project Server 2013 agit comme une application, où un administrateur — disposant des autorisations de conception pour Project Web App — peuvent publier un flux de travail déclaratif et l’associer à un type de projet d’entreprise (TPE). TPE doit correspondre à un projet d’entreprise, où Project Server gère le contrôle total. Une liste de tâches SharePoint ne peut pas utiliser un flux de travail Project Server. 
  
OAuth permet aux responsables de projet qui disposent d’autorisations de création de projet pour appeler le flux de travail sans l’aide de l’emprunt d’identité. Appels de flux de travail à Project Server, par exemple pour lire une valeur de champ personnalisé pour décider quelle branche à suivre, sont effectuées pour le compte du responsable de projet. Pour empêcher le responsable de projet de création d’un flux de travail passe automatiquement à l’étape suivante, l’appel pour passer à la prochaine étape du flux de travail s’exécute en tant que l’auteur du flux de travail (l’administrateur). En revanche, les utilisateurs des flux de travail Project Server 2010 hérité émettre d’appels empruntées via le compte d’utilisateur Proxy du flux de travail pour obtenir l’accès d’administrateur au sein de l’ensemble du flux.
  
Bien que Project Server 2013 local peut utiliser compilée WF3.5-flux de travail, nous vous recommandons de mettre à niveau les workflows hérités au flux de travail déclaratifs selon WF4. La technologie la plus récente est plus évolutif et fiable. Les analystes d’entreprise et le personnel PMO peut créer ou mettre à jour des modèles de flux de travail à l’aide de Visio 2013 et implémenter des flux de travail Project Server sans codage à l’aide de SharePoint Designer 2013.
  
Pour plus d’informations sur la création d’un flux de travail déclaratif pour Project Web App, voir [mise en route du développement de flux de travail Project Server](getting-started-developing-project-server-workflows.md). Pour une comparaison des fonctionnalités de Visual Studio pour les flux de travail SharePoint Designer, voir [Develop SharePoint 2013 workflows using Visual Studio](http://msdn.microsoft.com/en-us/library/office/jj163199.aspx).
  
### <a name="client-side-object-model"></a>Modèle objet côté client
<a name="pj15_WhatsNew_CSOM"> </a>

L’accès par programme à Project Online nécessite un modèle qui repose sur SharePoint CSOM. Authentification du projet en ligne seront avec OAuth à l’aide d’un identifiant Windows Live ID, pas Project Server formulaires ou l’authentification Windows.
  
Les principes et les fonctionnalités de CSOM dans Project Server 2013 sont les suivantes :
  
- Le modèle est conçu pour faciliter l’utilisation. Par exemple, méthodes et propriétés directement utilisent ou fournissent des données par nom, plutôt que nécessitant de GUID, paramètre _changeXml_ ou en passant autour de jeux de données. 
    
- Le modèle objet client Project Server implémente un sous-ensemble de la fonctionnalité de l’interface PSI, en se basant sur les exigences les plus courantes des solutions tierces.
    
- Le modèle CSOM appelle la PSI en interne, mais est prises en charge différemment. Par exemple, les mises à jour pour toutes les modifications d’état sont effectuées par le biais de la méthode **StatusAssignmentCollection.SubmitAllStatusUpdates** , non par la méthode **Statusing.SubmitStatus** PSI pour l’utilisateur ou la méthode **SubmitStatusForResource** pour d’autres ressources. 
    
- Le modèle objet client est accessible par un service WCF (Client.svc), plutôt que par les 22 services publics de l’interface PSI.
    
- Initialisation de l’ordinateur Project Server CSOM n’est directement par le biais de la classe [ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) avec l’URL Project Web App, pas à l’aide d’un assembly de référence ou proxy WCF. 
    
- Le modèle objet client implémente plusieurs interfaces et bibliothèques clientes, qui sont prises en charge par l’infrastructure CSOM SharePoint interne. Les interfaces et bibliothèques clientes sont les suivantes :
    
  - Bibliothèque cliente Microsoft .NET dans l’assembly Microsoft.ProjectServer.Client.dll
    
  - Bibliothèque Silverlight dans l’assembly Microsoft.ProjectServer.Client.Silverlight.dll
    
  - Bibliothèque Windows Phone 8 dans l’assembly Microsoft.ProjectServer.Client.Phone.dll
    
  - Bibliothèque JavaScript pour les applications web dans le fichier PS.js ou PS.debug.js
    
  - Points de terminaison REST pour l’accès avec le protocole OData
    
  - Prise en charge native pour les requêtes LINQ avec filtrage afin de limiter la quantité de données renvoyées
    
- Le modèle peut être utilisée à la fois pour les solutions Project Online et pour les solutions locales, indépendamment de la PSI et d’autres assemblys Project Server tels que Microsoft.Office.Project.Server.Library.dll.
    
- Des fonctionnalités supplémentaires de Project Server 2013 CSOM peuvent être considéré comme pour les mises à jour cumulatives et les service packs, en fonction de demandes par les partenaires de Project Server et de la Communauté des développeurs.
    
> [!NOTE]
> Le modèle objet client représente l’interface privilégiée pour les développeurs tiers de Project Server. Nous vous recommandons d’utiliser le modèle objet client pour développer de nouvelles applications, si celui-ci inclut les fonctionnalités dont votre application a besoin. 
  
Pour plus d’informations sur le développement avec le modèle CSOM, voir [modèle d’objet côté Client (CSOM) pour Project 2013](client-side-object-model-csom-for-project-2013.md). Pour plus d’informations sur l’interface REST dans les applications SharePoint, voir *programmation à l’aide du service REST SharePoint* dans la documentation du développeur SharePoint 2013. 
  
### <a name="changes-in-the-reporting-database"></a>Changements dans la base de données de rapports
<a name="pj15_WhatsNew_RDBChanges"> </a>

Les quatre bases de données dans Project Server 2010 sont combinées en une seule base de données de projet dans Project Server 2013. Le nom par défaut de la base de données de projet est ProjectService. Création de rapports tables et vues conservent leur nom précédent, et tables et vues des bases de données brouillon, publié et Archive ont les préfixes `draft`, `pub`, et `ver` dans la base de données ProjectService. Par exemple, la table des projets publiés est la composition. MSP_PROJECTS. 
  
> [!IMPORTANT]
> Direct access n’est pas pris en charge pour le brouillon (`draft` préfixe), publié (`pub`) et d’archivage (`ver`) tables et les vues. Rapports doivent utiliser uniquement les tables et vues, dont la création de rapports le `dbo` préfixe. Par exemple, la table dbo. Table MSP_EpmProject inclut la liste des projets dans l’instance de Project Web App. 
>
> Rien ne vous empêche d’utiliser activement l’accès direct à la base de données par programme pour mettre à jour les données dans l’une des tables et vues dans la base de données Project. Vous devez être conscient que le cache Project Professionel, les tables des données brouillon et publiées, ainsi que les tables de rapport reposent tous sur un protocole de synchronisation de cache qui peut être perturbé par la modification directe de données. Toutefois, si vous endommagez vos bases de données Project Server ou les caches côté client Project Professionnel suite à un accès direct pour modifier les données, notez que le support technique ne sera pas en mesure de vous aider. 
  
Project Server 2013 présente un service OData pour en ligne et accès locaux. Les tables de création de rapports en ligne et les affichages sont exposées uniquement par l’interface OData ; pour une utilisation locale, vous pouvez utiliser l’interface OData ou accéder directement à la création de rapports tables et affichages dans la base de données ProjectService dans la batterie de serveurs SharePoint. Project Online ne prend pas en charge une base de données une architecture mutualisée. Autrement dit, plusieurs instances de Project Web App chaque ont leur propre base de données de projet. Le service OData exécute des requêtes SQL sur les tables et les affichages de rapports en interne et fournit une charge utile JSON ou XML. Pour une présentation du service OData pour la création de rapports dans Project Server 2013 et la référence du schéma **ProjectData** , voir [ProjectData - référence de service OData Project](https://msdn.microsoft.com/en-us/library/office/jj163015.aspx).
  
Pour obtenir des informations générales sur les requêtes OData, voir [OData : conventions d’URI](http://www.odata.org/developers/protocols/uri-conventions#FilterSystemQueryOption). Par exemple, vous pouvez voir tous les projets dans une instance locale de Project Web App, où le nom du projet commence par « Test » à l’aide de la requête suivante dans un navigateur. Avec le bouton droit dans la page du navigateur, puis cliquez sur **Afficher la source**.
  
```html
http://ServerName /ProjectServerName /_api/ProjectData/Projects?$filter=startswith(ProjectName, 'Test') eq true
```

Pour importer les données de projet dans PowerPivot dans Excel 2013, dans le ruban données, sélectionnez le **flux de données OData à partir de** dans le menu déroulant **à partir d’autres Sources** . Dans la boîte de dialogue **Assistant connexion de données** , tapez http://ServerName/ProjectServerName/_api/ProjectData/ dans les données de flux d’emplacement, cliquez sur **suivant**et puis sélectionnez la table de **projets** dans la page **Sélectionner les Tables** de l’Assistant. Nom et enregistrez le fichier .odc, puis cliquez sur **Terminer**. Dans la boîte de dialogue **Importer des données** , choisissez le **Rapport de tableau croisé dynamique**. Dans la feuille de calcul Excel, choisissez champs pour les lignes de tableau croisé dynamique et les colonnes que vous souhaitez afficher.
  
Utilisateurs de Project Server sur site, qui disposent des autorisations correctes, peuvent accéder directement à la création de rapports tables et vues par le biais de Microsoft SQL Server pour créer des rapports, comme ils le font dans Project Server 2010. Dans Project Server 2013, les utilisateurs peuvent également des tables de création de rapports access locale via l’interface OData. Vous pouvez récupérer des données de Project Server en ligne ou sur site par le biais de points de terminaison REST pour le service OData. Par exemple, la table dbo. Table MSP_PROJECT et le propriétaire. Affichage MSP_EpmProject_UserView utilisable pour les rapports. Les tables ou les vues qui ont une `draft`, `pub`, ou `ver` préfixe pour une utilisation interne par Project Server uniquement et ne sont pas pour les rapports d’utilisation. Par exemple, le projet. Table MSP_TASKS et la publication. Affichage MSP_PROJECTS_WORKING_VIEW ne sont pas documentés et sont à usage interne uniquement. 
  
> [!NOTE]
> Vous pouvez étendre la création de rapports en local en ajoutant des tables, vues, champs et procédures stockées dans une base de données distincte. Vous ne devez pas modifier les tables et vues de création de rapports existantes dans la base de données Project Server. 
  
Les tables, les vues et les champs dans la base de données Project rapports seront documentées dans un fichier d’aide HTML dans une mise à jour ultérieur du téléchargement du Kit de développement Project 2013. Pour la documentation du schéma XML OData pour le service **ProjectData** , voir [ProjectData - référence de service OData Project](https://msdn.microsoft.com/en-us/library/office/jj163015.aspx). Dans la plupart des cas, les requêtes de création de rapports tables et des vues qui ont été créés pour Project Server 2010 fonctionnera avec la base de données de projet dans Project Server 2013. Les utilisateurs locaux peuvent accéder les cubes OLAP Project Server dans SQL Server Analysis Services, comme ils le font actuellement. Les cubes OLAP dans Project Online, ne sont pas disponibles.
  
### <a name="task-pane-add-ins-in-project"></a>Compléments du volet de tâches dans Project
<a name="pj15_WhatsNew_Agave"> </a>

Project Standard 2013 et Project Professional 2013 prend en charge la tâche volet compléments, qui peuvent être utilisés pour intégrer et afficher le contenu externe dans une page Web. Le volet Office affiche le contenu de page Web qui dispose d’un accès par le biais de JavaScript pour les tâches, ressources, des vues et données générales du projet. Le modèle objet JavaScript pour Project permettre obtenir des informations sur une tâche sélectionnée ou une ressource et peut obtenir des données dans une cellule sélectionnée dans la grille pour les affichages tels que le diagramme de Gantt. Tâche volet des compléments pour Project peuvent également implémenter des gestionnaires d’événements pour une tâche, une ressource ou afficher les événements de changement de sélection. 
  
La figure 2 montre **l’Application Hello ProjectData** tâche volet complément qui interroge le service **ProjectData** , puis compare les données dans le projet actuel avec la moyenne de tous les projets. Le téléchargement du Kit de développement Project 2013 inclut le code source complet pour le complément. 
  
**La figure 2. Un complément volet de tâches dans Project Professional peut accéder aux données dans Project Server**

![Comparaison du projet actuel avec tous les projets] (media/pj15_RestQueryApp_CompareProject.gif "Comparaison du projet actuel avec tous les projets")
  
> [!NOTE]
> Project Standard 2013 ne peut pas s’intégrer avec Project Server 2013 directement par le biais de compléments de volet de tâches. 
  
Compléments Office volet dans Project Professionnel peuvent prendre en charge les composants WebPart qui sont conçus pour Project Server 2013, afin que les développeurs peuvent créer une extension une fois qui s’exécute avec Project Web App et Project Professional. Tâche volet compléments qui sont développées pour d’autres produits Office 2013 peuvent également servir avec Project Standard 2013 et Project Professional 2013. Pour plus d’informations, voir [tâche volet des compléments pour Project](task-pane-add-ins-for-project.md).
  
### <a name="project-server-event-receivers"></a>Récepteurs d’événements Project Server
<a name="pj15_WhatsNew_Events"> </a>

Il peut y avoir plusieurs serveurs de Project Web App (également appelées serveurs web frontaux ou WFE) dans une batterie de serveurs SharePoint qui inclut l’Application de Service de projet principal. Récepteurs d’événements peuvent également être appelées gestionnaires d’événements. Gestionnaires d’événements locaux peuvent être implémentées avec du code de confiance totale et déployées sur tous les WFE pour une installation de Project Server locale. Récepteurs d’événements distants peuvent être implémentées dans les services web sur des serveurs locaux ou distants et accessible par WFE plusieurs et plusieurs installations de Project Server. Project Online peut utiliser des récepteurs d’événements distants uniquement.
  
Gestionnaires d’événements Project Server sont gérés par SharePoint pour chaque instance de Project Web App, plutôt que par une page spécifique de paramètres de Project Web App. Dans l’application Administration centrale de SharePoint, sélectionnez **Paramètres généraux de l’Application**, sélectionnez **Gérer** sous **Paramètres PWA**, puis l’instance dans la liste déroulante **Instance Project Web App** sur les paramètres PWA page. Pour ajouter un gestionnaire d’événements local ou d’un récepteur d’événements distants, choisissez les **Gestionnaires d’événements côté serveur**.
  
Pour une installation locale de Project Server, vous pouvez créer un récepteur d’événements distants dans une fonctionnalité SharePoint qui utilise la classe [Microsoft.ProjectServer.Client.EventHandlerCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx) dans le modèle CSOM et gérer par programme le récepteur d’événements à l’aide des méthodes dans la classe [EventHandlerCollection](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCollection.aspx) . Pour les récepteurs d’événements distants, des événements sont synchrones, après les événements sont asynchrones et il existe un délai d’expiration pour les cas où le récepteur d’événements distants ne retourne pas. 
  
> [!NOTE]
> Administration centrale de SharePoint est disponible uniquement pour les installations locales. Pour Project Online et SharePoint Online, vous pouvez ajouter ou supprimer des récepteurs d’événements distants à l’aide d’un package d’application basé sur le modèle. 
  
Dans la page gestionnaires d’événements côté serveur, le processus pour ajouter un gestionnaire d’événements locaux pour une installation de Project Server sur site est presque identique à la procédure décrite dans la rubrique [créer un gestionnaire d’événements Project Server et enregistrer un événement](http://msdn.microsoft.com/en-us/library/gg615466.aspx) pour Project Server 2010. La différence est que la page nouveau gestionnaire d’événements a des options supplémentaires. Par exemple, choisissez **Création de projet** dans la liste des **événements** , puis cliquez sur **Nouveau gestionnaire d’événements**. Sur la page Gestionnaire d’événement, les deux seuls champs obligatoires sont **le nom** et la **commande** (voir Figure 3). Si vous ajoutez un gestionnaire d’événements locaux de confiance totale, ajoutez le champ **Nom de l’Assembly** et le champ **Nom de la classe** ; **Url du point de terminaison** laissez vide. Si vous ajoutez un récepteur d’événements distants, ajoutez **Les Url de point de terminaison**et renseignez le **Nom de l’Assembly** et le **Nom de classe** . 
  
> [!CAUTION]
> Si vous spécifiez *à la fois* le nom d’assembly/nom de la classe et l’URL du point de terminaison, Project Server appelle uniquement l’ordinateur local (localement) Gestionnaire d’événements. Récepteur d’événements distants est ignoré. 
> 
> Si vous créez deux gestionnaires d’événements pour l’événement même, où un gestionnaire d’événements est local 1 est un récepteur d’événements distants et la valeur de **l’ordre** est le même pour les deux, Project Server ignore le récepteur d’événements distants. 
  
**La figure 3. Ajout d’un gestionnaire d’événements local ou d’un récepteur d’événements distants**

![Configuration d’un gestionnaire d’événements ou d’un récepteur d’événements] (media/pj15_EventHandlers_NewEventHandler.gif "Configuration d’un gestionnaire d’événements ou d’un récepteur d’événements")
    
Si vous souhaitez accéder aux groupes de données PSI pour un gestionnaire d’événements local, vous pouvez copier l’assembly Microsoft.Office.Project.Schema.dll à partir de la [Windows]\Microsoft.NET\assembly\GAC\_MSIL\Microsoft.Office.Project.Schema\v4.0_15.0.0.0__ répertoire 71e9bce111e9429c. 

Au lieu de l’interface PSI, nous vous conseillons d’utiliser les classes d’événements dans l’espace de noms **Microsoft.ProjectServer.Client** ; développement avec le modèle CSOM ne nécessite pas de manipulation de jeux de données. Pour développer des récepteurs d’événements distants pour Project Online, vous devez utiliser la classe [d’événements](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.Event.aspx) et de la classe [EventHandlerCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.EventHandlerCreationInformation.aspx) dans le modèle CSOM. 
  
Avant de déployer un gestionnaire d’événements Project Server, installez et testez le Gestionnaire d’événements sur une installation de test de Project Server. Pour une installation de Project Server sur site, si le Gestionnaire d’événements local que vous ajoutez devient inopérant, le Service d’événements Project Server 2013 ne parvient pas à charger les autres gestionnaires d’événements personnalisé valide. Dans ce cas, vous devez supprimer le Gestionnaire d’événements de problème et redémarrez le service d’événements.
  
> [!NOTE]
> Pour une installation de Project Server locale, nous vous recommandons de migrer vers les récepteurs d’événements à distance à l’aide du modèle objet client pour développer les récepteurs d’événements. Étant donné que les récepteurs d’événements à distance ne disposent pas de code tiers en cours d’exécution au sein du service d’événements Project Server, les récepteurs d’événements à distance sont plus stables. Les administrateurs locaux n’ont plus la responsabilité de gérer le service d’événements Project Server. 
  
Pour obtenir des informations générales sur les événements, voir [Gestion des événements dans les applications pour SharePoint](http://msdn.microsoft.com/en-us/library/jj220048%28office.15%29.aspx). 
  
## <a name="deprecated-features"></a>Fonctionnalités déconseillées
<a name="pj15_WhatsNew_Deprecated"> </a>

> [!NOTE]
> Pour plus d’informations sur les fonctionnalités et API qui est déconseillées ou supprimées dans Project Server Preview 2016, voir [ce qui a déconseillées ou supprimées dans Project Server 2016 Preview](https://technet.microsoft.com/library/mt422816%28v=office.16%29.aspx). 
  
Fonctionnalités déconseillées sont toujours disponibles dans Project 2013 pour certaines solutions, mais ne doivent pas être utilisées pour le développement de nouveau. La plupart des fonctionnalités et des pratiques suivantes ne fonctionne pas avec Project Online, ou l’installation locale par défaut de Project Server 2013 en mode d’autorisation SharePoint. Les solutions existantes qui utilisent ces fonctionnalités ne fonctionnent pas pour une mise à niveau de Project Server 2010 vers Project Server 2013. Bien que déconseillé des solutions qui utilisent fonctionnalités peuvent continuer à travailler dans certains cas, ils ne sont pas entièrement pris en charge pour toutes les installations de Project 2013.
  
Si vos solutions utilisent les fonctionnalités déconseillées, ils doivent être testées entièrement avant le déploiement et vous devez modifier les à utiliser pris en charge des fonctionnalités au plus tôt est pratique. Pour plus d’informations sur la configuration de la sécurité de Project Server 2013 sur site pour le mode d’autorisation Project, consultez la section *Mode d’autorisation SharePoint* dans [Nouveautés pour les professionnels de l’informatique dans Project Server 2013](http://technet.microsoft.com/en-us/library/ff631142%28office.15%29.aspx).
  
- **Extensions** [Scénarios d’extension PSI](https://msdn.microsoft.com/library/office/ff843378%28v=office.14%29.aspx) sont désapprouvées et ne sera pas prise en charge dans les versions ultérieures. Ces scénarios de Project Server 2013 local activé l’intégration à l’aide des services Windows Communication Foundation (WCF) personnalisés. 
  
- **Projet PSI** La [classe Project](https://msdn.microsoft.com/library/office/websvcproject.project_di_pj14mref.aspx%28Office.15%29.aspx) de la PSI est déconseillée. Pour tout nouveau développement, utilisez le [Modèle de projet](https://msdn.microsoft.com/library/office/microsoft.projectserver.client_di_pj14mref.aspx%28Office.15%29.aspx). Project Server 2013 applications qui utilisent la PSI Project continueront de fonctionner, mais les applications Project Online vous devrez remplacer toutes les méthodes PSI classe Project avec leurs équivalents méthodes CSOM.
  
- **Plan de ressources PSI** La [Ressource planifier PSI](https://msdn.microsoft.com/library/office/websvcresourceplan_di_pj14mref.aspx) est déconseillée. Il continuera à être pris en charge pour le développement de Project 2013, mais ne sera pas prise en charge dans les versions ultérieures. 
  
- **Interface ASMX pour l’interface PSI** L’interface PSI inclut des interfaces en double pour développer des extensions de Project Server sur site. L’interface de services web ASMX a été introduit avec la première implémentation de l’interface PSI dans Office Project Server 2007. Project Server 2010 Ajout de l’interface de services WCF, où le modèle objet duplique essentiellement des services web ASMX. Bien que Project Server 2013 continue de prendre en charge ASMX et WCF, les nouvelles solutions qui nécessitent la PSI doivent utiliser les services WCF. Si possible, les nouvelles solutions doivent être écrites à l’aide du modèle CSOM. 
  
  Services web ASMX de la PSI sont déconseillées dans Project Server 2013. Pour fonctionner dans les futures versions de Project Server, les solutions qui utilisent les services web ASMX doivent être réécrites pour utiliser les services WCF ou le modèle CSOM. Pour plus d’informations, consultez la section *applications de mise à niveau avec les API de Project Server* de [programmabilité de Project Server](project-server-programmability.md).
  
- **Fournisseur de liaison d’objet (OLP)** Dans les versions précédentes de Project Server, le service **ObjectLinkProvider** dans l’interface PSI (voir [WebSvcObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.aspx) ) permet de gérer les liaisons entre les tâches de projet d’entreprise et des listes SharePoint spécialisés dans le site de projet de l’objet web pour les problèmes, risques, des livrables et des documents. Dans Project Server 2013, OLP est déconseillée. 
  
  Vous pouvez utiliser la classe **[RelatedItemManager](http://msdn.microsoft.com/en-us/library/microsoft.sharepoint.client.relateditemmanager.aspx)** dans le CSOM SharePoint pour créer, lire ou supprimer des liaisons d’objet web entre les éléments de la liste de tâches et d’autres listes dans un site de projet. Par exemple, pour ajouter un lien à partir d’un élément de tâche à un problème, vous pouvez utiliser la méthode **[AddSingleLink](http://msdn.microsoft.com/en-us/library/office/microsoft.sharepoint.client.relateditemmanager.addsinglelink.aspx)** ou une des deux méthodes similaires, **AddSingleLinkFromUrl** ou **AddSingleLinkToUrl**. La classe **RelatedItemManager** inclut également des méthodes pour supprimer un lien d’objet web et la lecture des éléments associés. La classe équivalente dans le JSOM (modèle objet JavaScript), consultez la rubrique [SP RelatedItemManager object (sp.js)](http://msdn.microsoft.com/en-us/library/jj838582.aspx).
  
  Nous recommandons d’utiliser le CSOM SharePoint pour créer des applications de type OLP pour une installation locale de Project Server 2013 et Project Online. L’espace de noms [Microsoft.SharePoint](http://msdn.microsoft.com/en-us/library/microsoft.sharepoint.aspx) n’inclut pas un **RelatedItemManager** *** classe. 
  
- **Autorisations personnalisées** Autorisations de sécurité personnalisé pour accéder aux fonctionnalités spécifiques de Project Server ou les extensions ont été pris en charge dans Office Project Server 2007, où un article SDK explique comment les créer en modifiant directement la base de données publiée. Dans Project Server 2010, des autorisations personnalisées fonctionnent toujours mais sont déconseillées. Dans Project Server 2013, les autorisations personnalisées ne fonctionnent pas avec le mode d’autorisation SharePoint par défaut pour les installations locales. Pour le mode d’autorisation Project, des autorisations personnalisées sont prises en charge. Avec Project Online, l’accès direct de la base de données n’est pas possible. 
  
- **Emprunt d’identité** Emprunt d’identité dans les applications PSI, où l’utilisateur d’une application peut prendre les autorisations de sécurité d’un autre utilisateur de Project Server, est déconseillé dans Project Server 2013. Comme indiqué précédemment, une valeur par défaut local installation Project Server 2013 utilise le mode d’autorisation SharePoint, qui n’autorise pas l’emprunt d’identité dans les groupes de sécurité Project Server. Pour plus d’informations, voir [authentification, autorisation et sécurité dans SharePoint 2013](http://msdn.microsoft.com/en-us/library/ms457529%28office.15%29.aspx).
  
  Applications d’état sont des extensions standard que vous avez peut-être utilisé l’emprunt d’identité dans les versions précédentes de Project Server. Project Server 2010 introduit la méthode **ReadStatusForResource** et la méthode **SubmitStatusForResource** dans l’interface PSI, ainsi que de l’autorisation globale **StatusBrokerPermission** , lequel supprimait la nécessité d’emprunt d’identité lire et mettre à jour de statut pour un autre utilisateur. Le modèle CSOM dans Project Server 2013 utilise l’interface PSI sous-jacentes pour activer en toute transparence des extensions d’état et peut être utilisé pour Project Online ou installations locales. 
  
- **Extensions de base de données de rapport** Ajout de tables personnalisées et les vues pour la base de données de création de rapports est courant avec les versions précédentes de Project Server. Étant donné que Project Server 2013 combine les quatre bases de données de versions précédentes dans une base de données, mises à niveau ne transférez pas tableaux personnalisés, des vues ou procédures stockées dans les tables de création de rapports dans la base de données Project Server 2013. 
  
  Nous vous recommandons d’utiliser une base de données SQL Server distinct ou SQL Azure pour des tableaux de création de rapports personnalisés et les affichages, où vous pouvez gérer des sauvegardes de base de données et les mises à jour. Pour Project Online, cela est nécessaire.
  
- **Création de rapports** Les rapports des tables locales et les vues dans la base de données Project Server et les cubes OLAP, sont *pas* déconseillée et restent entièrement pris en charge. Toutefois, les tables et les vues (la création de rapports de base de données dans les versions précédentes de Project Server) création de rapports ne sont pas accessibles dans Project Online. De même, les cubes OLAP sont disponibles uniquement avec les installations locales de Project Server 2013. Pour les rapports d’applications avec Project Online, vous pouvez utiliser le service **ProjectData** , par le biais de requêtes REST au protocole OData. 
  
- **Guide de projets** Le Guide de projets est une fonctionnalité standard dans les applications de bureau Office Project 2007, où le contenu HTML et JavaScript dans un volet Office fournit un guide interactif pour la création et la gestion de projets. Dans Project 2010, le Guide de projets n’est pas disponible dans une installation par défaut, mais peut être activé via VBA ou un complément VSTO. Le téléchargement du SDK Project 2010 comprend les fichiers du Guide de projets modifiés. 
  
  Le modèle d’objet VBA et le modèle d’objet **Microsoft.Office.Interop.MSProject** dans Project 2013 toujours incluent les membres de la classe **d’Application** et la classe **Project** qui peut gérer le Guide de projets 22. Toutefois, les applications du volet Office peuvent entrer en conflit avec les actions dans un volet Guide de projets et le contenu du Guide de projets de Project 2013 ne peut pas être facilement distribué ou vendu dans l’Office Store. Il est vivement recommandé que vous développez des solutions de volet de tâches Project avec les compléments Office, contenu de Guide de projets non personnalisé. Pour plus d’informations sur le Guide de projets, voir la [Documentation du SDK Project 2010](http://msdn.microsoft.com/en-us/library/ms512767.aspx).
  
## <a name="comparing-project-server-on-premises-with-project-online"></a>Comparaison de Project Server local avec Project Online
<a name="pj15_WhatsNew_Comparing"> </a>

Pour vous aider à décider s’il faut utiliser Project Server locaux ou Project Online et les types d’extensions que vous pouvez développer dans les deux cas, le tableau 2 compare les fonctionnalités d’une installation locale de Project Server 2013 avec Project Online extensibles. Le tableau 2 n’inclut pas les différences dans le déploiement, l’administration ou l’utilisation. Pour plus d’informations sur Project Online et Project Server 2013, voir [Project 2013 pour les développeurs](http://msdn.microsoft.com/en-US/office/fp161502) et [Project Online](http://www.microsoft.com/project/).
  
**Le tableau 2. Extensibilité de Project Server localement et Project Online**

| Fonctionnalité |Project Server local | Project Online |
|:-----|:-----|:-----|
|**Programmabilité** <br/> |Applications basées sur le modèle objet client ; modèle de programmation cohérent  <br/>-.NET, Silverlight, les bibliothèques clientes Windows Phone  <br/>-Bibliothèque JavaScript les pages personnalisées, les composants WebPart et les extensions du ruban  <br/>-Protocoles OData et REST<br/><br/> Applications basées sur l’interface PSI ; modèle de programmation complexe, pouvant également créer des applications pour l’administration, l’analyse de portefeuille, les notifications, la sécurité en mode Project, le système de file d’attente, ainsi que d’autres domaines<br/><br/>Extensions de l’interface PSI  <br/><br/>Autorisations personnalisés avec la sécurité en mode Project (déconseillé)  <br/><br/>Emprunt d’identité avec l’interface PSI (déconseillé)  <br/><br/>Code de confiance totale ; installation d’extensions dans une batterie de serveurs SharePoint  <br/> |Applications basées sur le modèle objet client ; modèle de programmation cohérent  <br/>-.NET, Silverlight, les bibliothèques clientes Windows Phone<br/>-Bibliothèque JavaScript les pages personnalisées, les composants WebPart et les extensions du ruban<br/>-Protocoles OData et REST<br/><br/>Possibilité d’utiliser l’interface PSI, mais elle n’est pas prise en charge : aucune connexion OAuth et service-à-service<br/><br/>Aucune extension de l’API CSOM<br/><br/>Aucune autorisation personnalisée<br/><br/>Aucun emprunt d’identité<br/><br/>Aucun code de confiance totale  <br/> |
|**Bases de données personnalisées** <br/> |-SQL Azure  <br/>-SQL Server (modification des tables et les vues dans la base de données n’est pas prise en charge de Project Server)  <br/> |-SQL Azure  <br/>-SQL Server (modification des tables et les vues dans la base de données n’est pas prise en charge de Project Server)  <br/> |
|**Création de rapports** <br/> |- Service **ProjectData** ; Protocoles OData et REST  <br/>-Rapports de tables et les vues dans la base de données Project Server<br/>: Base de données OLAP  <br/> |- Service **ProjectData** ; Protocoles OData et REST  <br/> |
|**Gestionnaires d’événements** <br/> |-Récepteurs d’événements distants, accessibles par le biais de points de terminaison WCF<br/>-Gestionnaires d’événements confiance totale, installés dans la batterie de serveurs SharePoint  <br/> | -Récepteurs d’événements distants, accessibles par le biais de points de terminaison WCF  <br/> |
|**Flux de travail** <br/> |Flux de travail déclaratifs, créé avec SharePoint Designer 2013<br/>-Utiliser uniquement sur une instance spécifique de Project Web App<br/>-Peut importer un modèle de flux de travail à partir de Visio 2013<br/>-Peuvent importer et utiliser des actions personnalisées<br/><br/> Flux de travail déclaratifs créés avec Visual Studio 2012<br/>-Permet de créer une application qui peut inclure des flux de travail<br/>-Créer un package de solution (.wsp) SharePoint qui peut inclure des flux de travail<br/>-Créer des modèles de flux de travail pour réutilisation<br/>-Permet de créer et utiliser des actions personnalisées  <br/><br/>Possibilité d’utiliser des flux de travail compilés et hérités créés avec WF3.5 (mise à niveau recommandée vers un flux de travail WF4 déclaratif)  <br/> |Flux de travail déclaratifs, créé avec SharePoint Designer 2013<br/>-Utiliser uniquement sur une instance spécifique de Project Web App<br/>-Peut importer un modèle de flux de travail à partir de Visio 2013<br/>-Peuvent importer et utiliser des actions personnalisées  <br/><br/>Flux de travail déclaratifs créés avec Visual Studio 2012<br/>-Permet de créer une application qui peut inclure des flux de travail  <br/>-Créer un package de solution (.wsp) SharePoint qui peut inclure des flux de travail<br/>-Créer des modèles de flux de travail pour réutilisation <br/>-Permet de créer et utiliser des actions personnalisées  <br/> |
|**Distribution** <br/> |-Office Store (pour les applications basées sur le modèle)<br/>-Catalogue d’applications privé sur SharePoint<br/>-Partage de fichiers intranet  <br/> |-Office Store<br/>-Catalogue d’applications privé sur SharePoint  <br/> |

   
## <a name="conclusion"></a>Conclusion
<a name="pj15_WhatsNew_Conclusion"> </a>

Project Server 2013 offre un large éventail de nouvelles fonctionnalités de développement et de scénarios que les partenaires et clients peuvent utiliser pour adapter et étendre les fonctionnalités et l’utilité de Project Server dans les grandes entreprises et dans les petites entreprises. Vous pouvez utiliser l’infrastructure pour Office 2013 et SharePoint 2013 pour aider à créer et distribuer des applications pour Project 2013 qui peuvent étendent considérablement la négociabilité et l’utilisation des applications personnalisées. Certaines fonctionnalités d’extensibilité et les pratiques de versions précédentes sont déconseillées dans Project 2013, notamment les services web ASMX des fonctionnalités qui impliquent l’emprunt d’identité ou des modifications de la base de données direct, qui ne peut pas être utilisées avec Project Online et PSI.
  
L’introduction de CSOM permet l’accès par programme à Project Online pour un large éventail de périphériques et à l’aide de JavaScript dans les applications web. Le modèle fournit un modèle de programmation plus cohérent par rapport à l’interface PSI. Données Project Server est accessible de différentes façons plus que dans les versions précédentes, y compris par le biais du service OData en ligne et points de terminaison REST pour les données de rapports dans la base de données de projet. Rapports existants fonctionnent toujours de la même manière pour une utilisation locale ; nouveaux rapports ont une plus grande flexibilité.
  
Compléments Office fournissent une nouvelle avenue pour la vente des solutions et Project Standard 2013 intégrer de contenu web et d’autres produits Office 2013. Vous pouvez également créer des nouvelles façons d’intégrer Project Professional 2013 avec les données de Project Server et des listes SharePoint via le volet Office Add-ins.
  
Pour plus d’informations sur le développement d’applications et en utilisant les fonctions de programmabilité et le modèle de SharePoint Server 2013, voir [SharePoint pour les développeurs](http://msdn.microsoft.com/en-US/sharepoint) et [Office pour les développeurs](http://msdn.microsoft.com/en-US/office).
  
## <a name="see-also"></a>Voir aussi

- [Architecture de Project Server 2013](project-server-2013-architecture.md)  
- [Tâches de programmation du projet](project-programming-tasks.md) 
- [Modèle objet côté client (CSOM) pour Project 2013](client-side-object-model-csom-for-project-2013.md) 
- [ProjectData – Référence de service Project OData](https://msdn.microsoft.com/en-us/library/office/jj163015.aspx)  
- [Compléments du volet Office pour Project](task-pane-add-ins-for-project.md)   
- [OData : Conventions d’URI](http://www.odata.org/documentation/uri-conventions#FilterSystemQueryOption)    
- [Pour les développeurs SharePoint](http://msdn.microsoft.com/en-US/sharepoint)    
- [Office pour les développeurs](http://msdn.microsoft.com/en-US/office)   
- [Gestion des événements dans les applications pour SharePoint](http://msdn.microsoft.com/en-us/library/jj220048%28office.15%29.aspx)   
- [Office Store](http://office.microsoft.com/en-us/store/)   
- [Project Online](http://www.microsoft.com/project/)
    

