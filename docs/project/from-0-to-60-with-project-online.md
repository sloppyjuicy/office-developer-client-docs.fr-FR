---
title: De 0 à 60 avec Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: 'Un développeur d’applications peut personnaliser un site Project Online (SharePoint hébergé) à l’aide d’applications autonomes et/ou de compléments Project. Il est possible que de nombreuses applications répondent aux besoins des personnes impliquées dans un projet jusqu’aux fonctions de support PMO, comme l’une des suivantes :'
ms.openlocfilehash: aa872bd50c711076c4eaad17ed7aac8c0aef61f1
ms.sourcegitcommit: a6d13fdae7eb2e503236c1b629a59b36a4fb76f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2022
ms.locfileid: "66083463"
---
# <a name="from-0-to-60-with-project-online"></a>De 0 à 60 avec Project Online

Un développeur d’applications peut personnaliser un site Project Online (SharePoint hébergé) à l’aide d’applications autonomes et/ou de compléments Project. Il est possible que de nombreuses applications répondent aux besoins des personnes impliquées dans un projet jusqu’aux fonctions de support PMO, comme l’une des suivantes :
  
- Entrée de données de carte de temps rationalisée pour les workers
- Approbation de carte de temps efficace pour les superviseurs
- Surveillance des permis (approvisionnement et état) nécessaires à un projet
- État/Contrôle d’intégrité des projets actifs
- Rapport sur les problèmes
- Rapport d’état de gestion des modifications
    
Project Online inclut la prise en charge des API pour prendre en charge les scénarios suivants :
  
- Pour un complément hébergé Project (SharePoint) :
    
  - Code (JavaScript, HTML, CSS) hébergé dans SharePoint Online
  - Ressources téléchargées dans le navigateur et exécutées sur SharePoint Online.  
  - Logique métier en JavaScript   
  - Accéder aux données qui sont dans/stockées dans Project Online ou SharePoint telles que (mais qui ne sont pas limitées à) :  
  - Champs personnalisés  
  - Listes
    
- Pour un complément hébergé par un fournisseur Project (SharePoint) :
    
  - Code qui existe sur un site externe au site Project Online 
  - Un site externe, qui peut être (mais qui n’est pas limité à) :  
  - Un autre site SharePoint  
  - Web App/Service basé sur n’importe quelle plateforme  
  - Le site externe contient une logique métier  
  - Le navigateur est redirigé de Project Online vers un site externe avec des jetons d’accès à Project Online  
  - Le site externe peut effectuer des appels à SharePoint et Project Online
    
- Pour un complément externe/autonome :
    
  - L’utilisateur exécute une application sur son appareil
  - L’application s’authentifie et appelle directement Project Online API
    

|Type d’application|Implémentation de l’API|Environnement cible|Exemples d’application|
|:-----|:-----|:-----|:-----|
|Project hébergé  <br/> |JSOM (Java Script Object Model)  <br/> REST  <br/> |Navigateur  <br/> |Entrée de carte de temps  <br/> Approbation de la carte de temps  <br/> État du projet  <br/> Rapport sur les problèmes  <br/> |
|fournisseur Project hébergé  <br/> |Bibliothèque de client CSOM  <br/> |Site web/application Azure  <br/> Environnement non Windows (LAMP, etc.)  <br/> |Validateur de feuille de temps externe  <br/> importateur Project  <br/> |
|Externe/autonome  <br/> |REST  <br/> CSOM  <br/> |REST - n’importe quelle plateforme  <br/> CSOM : n’importe quelle plateforme .NET prise en charge  <br/> |Entrée de carte de temps  <br/> Migration de projets vers un nouveau site  <br/> État de gestion des modifications. |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a>Que faut-il pour commencer à développer des applications pour Project Online ?

Les éléments courants nécessaires au développement d’applications Project Online sont un compte Project Online et des données de test ( projets et informations relatives au projet) qui incluent des affectations, des tâches, des ressources et des champs personnalisés. Un environnement de développement est également nécessaire, mais les spécificités de l’environnement de développement dépendent du type d’application et de l’interface API nécessaire pour l’application. Les sections suivantes décrivent les besoins de développement pour les trois interfaces API.
  
La documentation de référence décrit le modèle objet commun aux trois interfaces, ainsi qu’une carte d’entités qui montre les relations entre les composants du modèle objet.
  
## <a name="project-hosted-add-in-development-environment"></a>Project environnement de développement de complément hébergé

Un complément hébergé est un complément qui réside sur le serveur et qui est téléchargé dans un navigateur pour l’exécution du runtime. Les compléments hébergés peuvent utiliser les interfaces JSOM ou REST et sont écrits en JavaScript. Project Online fournit des références à la bibliothèque JSOM pour l’exécution du runtime. En supposant que le développement se trouve sur une plateforme Windows, les ressources nécessaires suivent :
  
- Visual Studio 2015 (par défaut) ou Visual Studio 2013
    
- outils de développement Office pour Visual Studio
    
- Langage JavaScript
    
Visitez https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages un exemple d’application. 
  
Vous pouvez télécharger et exécuter l’exemple en quelques étapes simples :
  
1. Télécharger et ouvrir l’exemple d’application
    
2. Mettre à jour SiteURL dans le Fenêtre Propriétés
    
   Project Online examine à la fois l’étendue de l’application du complément et les autorisations utilisateur pour régir l’accès aux informations sur l’hôte Project Online. Si l’accès est explicitement refusé dans l’un ou les deux paramètres, Project Online refuse l’accès aux informations. Sinon, l’accès est accordé.
    
3. Activez [le chargement indépendant](/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) sur votre site.  
    
4. Créez le projet.
    
5. Exécutez le projet.
    
## <a name="project-provider-hosted-add-in-development-environment"></a>Project environnement de développement de complément hébergé par un fournisseur

Les compléments hébergés par le fournisseur sont des applications écrites et résidant sur n’importe quelle plateforme web. Ils peuvent se connecter et effectuer des opérations de données à l’aide de l’API REST (ou CSOM pour les plateformes Microsoft). Tout langage et environnement qui prend en charge l’interface REST peut être utilisé pour le développement. 
  
Voici un exemple de l’environnement de développement Windows pour ce type d’application :
  
-  Visual Studio 2015 (par défaut) ou Visual Studio 2013 
    
- outils de développement Microsoft Office pour Visual Studio (fournis avec les éditions Professional et Enterprise Visual Studio 2015)
    
- .NET Framework 4.0 ou version ultérieure
    
- [Package CSOM SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (pour les appels CSOM) 
    
- Un langage de programmation, tel que C # 
    
Visitez https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations les exemples de scripts de travail. 
  
Vous pouvez exécuter l’exemple en quelques étapes :
  
1. Télécharger et ouvrir l’exemple d’application
    
2. Mettre à jour SiteURL dans le Fenêtre Propriétés
    
   Project Online examine à la fois l’étendue de l’application du complément et les autorisations utilisateur pour régir l’accès aux informations sur l’hôte Project Online. Si l’accès est explicitement refusé dans l’un ou les deux paramètres, Project Online refuse l’accès aux informations. Sinon, l’accès est accordé.
    
3. Activez [le chargement indépendant](/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) sur votre site. 
    
4. Créez le projet.
    
5. Exécutez le projet.
    
## <a name="externalstandalone-application-development-environment"></a>Environnement de développement d’applications externe/autonome

Une application autonome peut appeler Project Online à l’aide du modèle objet côté client (CSOM) ou REST pour communiquer avec Project Online pour créer, récupérer, mettre à jour et supprimer des informations résidant sur le serveur. Il s’agit d’une application cliente autonome qui dépend du niveau d’accès utilisateur à exécuter. 
  
Voici un exemple de l’environnement de développement Windows pour ce type d’application :
  
- Visual Studio 2015 (par défaut) ou Visual Studio 2013 
    
- outils de développement Microsoft Office pour Visual Studio (fournis avec les éditions Professional et Enterprise Visual Studio 2015)
    
- .NET Framework 4.0 ou version ultérieure
    
- [Package CSOM SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (pour les appels CSOM) 
    
- Un langage de programmation, tel que C # 
    
Visitez https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields un exemple d’application. 
  
Vous pouvez exécuter l’exemple en quelques étapes :
  
1. Télécharger l’exemple d’application
    
2. Apportez quelques modifications pour accéder à votre site Project Online : le nom du site, le compte d’utilisateur et le mot de passe.
    
   Vérifiez que l’utilisateur a accès à tous les projets. Project Online utilise des autorisations utilisateur pour régir l’accès aux informations dans le magasin de données.
    
3. Ajoutez l’assembly SharePoint aux références à l’aide de la console Gestionnaire de package Nuget, disponible dans le menu Outils en tapant ce qui suit dans la console Nuget : 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. Créez le projet.
    
5. Exécutez le projet.
    
## <a name="next-steps"></a>Prochaines étapes

Chaque exemple d’application comporte un article pour expliquer les points forts de l’utilisation de l’API Project individuelle. Les articles apparaissent dans la liste suivante, ainsi que quelques articles qui décrivent les relations d’entité, les informations sur le système de requête et l’accès aux champs personnalisés. 
  
- [Développement d’une application Project Online à l’aide du modèle objet côté client](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [Développement d’un complément Project Online à l’aide du modèle objet JavaScript (JSOM)](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [Accès aux champs personnalisés d’entreprise Project Online](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a>Voir aussi

Pour obtenir de la documentation et des exemples relatifs à Microsoft Project Online et au développement d’applications à l’aide de CSOM, consultez le [Portail de développement Project](https://developer.microsoft.com/project).
    
