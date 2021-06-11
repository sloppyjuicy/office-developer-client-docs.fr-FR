---
title: De 0 à 60 avec Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: 'Un développeur d’applications peut personnaliser un site Project Online (hébergé SharePoint) à l’aide d’applications autonomes et/ou de Project de sites. Un grand nombre d’applications sont possibles, qu’il s’agit de répondre aux besoins de ceux impliqués dans un projet ou de fonctions de prise en charge PMO, telles que l’une des suivantes :'
ms.openlocfilehash: 00f79b05b886bfd2c54c118245e22f10bb5451bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344407"
---
# <a name="from-0-to-60-with-project-online"></a>De 0 à 60 avec Project Online

Un développeur d’applications peut personnaliser un site Project Online (hébergé SharePoint) à l’aide d’applications autonomes et/ou de Project de sites. Un grand nombre d’applications sont possibles, qu’il s’agit de répondre aux besoins de ceux impliqués dans un projet ou de fonctions de prise en charge PMO, telles que l’une des suivantes :
  
- Entrée simplifiée des données de carte de temps pour les employés
- Approbation de carte de temps efficace pour les superviseurs
- Supervision des autorisations (approvisionnement et état) nécessaires pour un projet
- Vérification de l’état/de l’état des projets actifs
- Rapport des problèmes
- Rapport d’état de la gestion des changements
    
Project Online la prise en charge de l’API pour prendre en charge les scénarios suivants :
  
- Pour un Project (SharePoint) hébergé :
    
  - Code (JavaScript, HTML, CSS) hébergé dans SharePoint Online
  - Ressources téléchargées dans le navigateur et exécutées sur SharePoint Online.  
  - Logique métier en JavaScript   
  - Accéder aux données qui sont dans/stockées dans Project Online ou SharePoint par exemple (mais n’est pas limité à) :  
  - Champs personnalisés  
  - Listes
    
- Pour un Project (SharePoint) hébergé par un fournisseur :
    
  - Code qui existe sur un site externe au site Project Online site 
  - Un site externe, qui peut être (mais n’est pas limité à) :  
  - Autre site SharePoint site  
  - Application web/service créé sur n’importe quelle plateforme  
  - Le site externe contient une logique métier  
  - Le navigateur est redirigé de Project Online vers un site externe avec des jetons d’accès Project Online  
  - Le site externe peut effectuer des appels vers SharePoint et Project Online
    
- Pour un add-in externe/autonome :
    
  - Un utilisateur exécute une application sur son appareil
  - L’application s’authentifier et appelle Project Online API directement
    

|Type d’application|Implémentation d’API|Environnement cible|Exemples d’applications|
|:-----|:-----|:-----|:-----|
|Project hébergé  <br/> |JSOM (Java Script Object Model)  <br/> REST  <br/> |Navigateur  <br/> |Entrée de carte de temps  <br/> Approbation de carte de temps  <br/> État du projet  <br/> Rapport des problèmes  <br/> |
|Project Fournisseur hébergé  <br/> |Bibliothèque cliente CSOM  <br/> |Site web/application Azure  <br/> Environnement non Windows (LAMP, etc.)  <br/> |Validateur de feuille de temps externe  <br/> Project Importer  <br/> |
|Externe/Autonome  <br/> |REST  <br/> CSOM  <br/> |REST - n’importe quelle plateforme  <br/> CSOM : toute plateforme prise en charge par .NET  <br/> |Entrée de carte de temps  <br/> Migration de projets vers un nouveau site  <br/> État de gestion des changements.  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a>Que faut-il pour commencer à développer des applications pour Project Online ?

Les éléments courants nécessaires au développement d’applications Project Online sont un compte Project Online et des données de test , des projets et des informations relatives aux projets qui incluent des affectations, des tâches, des ressources et des champs personnalisés. Un environnement de développement est également nécessaire, mais les spécificités de l’environnement de développement dépendent du type d’application et de l’interface API nécessaires pour l’application. Les sections suivantes décrivent les besoins de développement pour les trois interfaces API.
  
La documentation de référence décrit le modèle objet commun aux trois interfaces, ainsi qu’une carte d’entité qui illustre les relations entre les composants du modèle objet.
  
## <a name="project-hosted-add-in-development-environment"></a>Project environnement de développement de add-in hébergé

Un add-in hébergé est un module qui réside sur le serveur et qui est téléchargé dans un navigateur pour exécution. Les add-ins hébergés peuvent utiliser les interfaces JSOM ou REST et sont écrits en JavaScript. Project Online fournit des références à la bibliothèque JSOM pour l’exécution. En supposant que le développement se trouve sur une plateforme Windows, les ressources nécessaires suivent :
  
- Visual Studio 2015 (de préférence) ou Visual Studio 2013
    
- Office de développement pour Visual Studio
    
- Langage JavaScript
    
Visitez https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages un exemple d’application. 
  
Vous pouvez télécharger et exécuter l’exemple en quelques étapes simples :
  
1. Télécharger et ouvrir l’exemple d’application
    
2. Mettre à jour siteURL dans la fenêtre Propriétés
    
   Project Online examine à la fois l’étendue de l’application du module complémentaire et les autorisations de l’utilisateur pour régir l’accès aux informations sur l Project Online hôte. Si l’accès est explicitement refusé dans l’un des paramètres ou les deux, Project Online refuse l’accès aux informations. Sinon, l’accès est accordé.
    
3. Activez [le chargement de version secondaire](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) sur votre site.  
    
4. Créez le projet.
    
5. Exécutez le projet.
    
## <a name="project-provider-hosted-add-in-development-environment"></a>Project environnement de développement de add-in hébergé par un fournisseur

Les applications hébergées par un fournisseur sont des applications écrites et résidant sur n’importe quelle plateforme web. Ils peuvent se connecter et effectuer des opérations de données à l’aide de l’API REST (ou CSOM pour les plateformes Microsoft). Tout langage et environnement qui prend en charge l’interface REST peut être utilisé pour le développement. 
  
Un exemple de l’environnement Windows de développement pour ce type d’application comprend les éléments suivants :
  
-  Visual Studio 2015 (de préférence) ou Visual Studio 2013 
    
- Microsoft Office Outils de développement Visual Studio (fournis avec Visual Studio 2015 Professional et Enterprise éditions)
    
- .NET Framework 4.0 ou plus
    
- [Package CSOM SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (pour les appels CSOM) 
    
- Langage de programmation, tel que C # 
    
Consultez https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations les exemples de scripts de travail. 
  
Vous pouvez exécuter l’exemple en quelques étapes :
  
1. Télécharger et ouvrir l’exemple d’application
    
2. Mettre à jour siteURL dans la fenêtre Propriétés
    
   Project Online examine à la fois l’étendue de l’application du module complémentaire et les autorisations de l’utilisateur pour régir l’accès aux informations sur l Project Online hôte. Si l’accès est explicitement refusé dans l’un des paramètres ou les deux, Project Online refuse l’accès aux informations. Sinon, l’accès est accordé.
    
3. Activez [le chargement de version secondaire](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) sur votre site. 
    
4. Créez le projet.
    
5. Exécutez le projet.
    
## <a name="externalstandalone-application-development-environment"></a>Environnement de développement d’applications externes/autonomes

Une application autonome peut appeler Project Online à l’aide du modèle objet côté client (CSOM) ou REST pour communiquer avec Project Online afin de créer, récupérer, mettre à jour et supprimer des informations résidant sur le serveur. Il s’agit d’une application cliente autonome qui dépend du niveau d’accès utilisateur à exécuter. 
  
Un exemple de l’environnement Windows de développement pour ce type d’application comprend les éléments suivants :
  
- Visual Studio 2015 (de préférence) ou Visual Studio 2013 
    
- Microsoft Office Outils de développement Visual Studio (fournis avec Visual Studio 2015 Professional et Enterprise éditions)
    
- .NET Framework 4.0 ou plus
    
- [Package CSOM SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (pour les appels CSOM) 
    
- Langage de programmation, tel que C # 
    
Visitez https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields un exemple d’application. 
  
Vous pouvez exécuter l’exemple en quelques étapes :
  
1. Télécharger l’exemple d’application
    
2. A apporté quelques modifications pour accéder à votre site Project Online site : le nom du site, le compte d’utilisateur et le mot de passe.
    
   Assurez-vous que l’utilisateur a accès à tous les projets. Project Online utilise les autorisations utilisateur pour régir l’accès aux informations dans le magasin de données.
    
3. Ajoutez l’assembly SharePoint aux références à l’aide de la console Nuget Gestionnaire de package, disponible dans le menu Outils en tapant ce qui suit dans la console Nuget : 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. Créez le projet.
    
5. Exécutez le projet.
    
## <a name="next-steps"></a>Étapes suivantes

Chaque exemple d’application dispose d’un article expliquant les points forts de l’utilisation de l’API Project individuelle. Les articles apparaissent dans la liste suivante, ainsi que quelques articles qui décrivent les relations d’entité, les informations sur le système de requête et l’accès aux champs personnalisés. 
  
- [Développement d’une application Project Online’aide du modèle objet côté client](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [Développement d’Project Online à l’aide du modèle objet JavaScript (JSOM)](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [Accès aux champs personnalisés d’entreprise Project Online](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a>Voir aussi

Pour obtenir de la documentation et des exemples relatifs à Microsoft Project Online et au développement d’applications à l’aide de CSOM, consultez le [Portail de développement Project](https://developer.microsoft.com/en-us/project).
    

