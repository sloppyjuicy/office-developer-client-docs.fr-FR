---
title: De 0 à 60 avec Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: "Un développeur d'applications peut personnaliser un site Project Online (SharePoint hébergé) à l'aide d'applications autonomes et/ou de compléments de projet. Il est possible d'effectuer une multitude d'applications entre les besoins des utilisateurs impliqués dans un projet et les fonctions de prise en charge de PMO, tels que les suivants:"
ms.openlocfilehash: 00f79b05b886bfd2c54c118245e22f10bb5451bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344407"
---
# <a name="from-0-to-60-with-project-online"></a>De 0 à 60 avec Project Online

Un développeur d'applications peut personnaliser un site Project Online (SharePoint hébergé) à l'aide d'applications autonomes et/ou de compléments de projet. Il est possible d'effectuer une multitude d'applications entre les besoins des utilisateurs impliqués dans un projet et les fonctions de prise en charge de PMO, tels que les suivants:
  
- Entrée de données de la fiche de pointage rationalisée pour les travailleurs
- Approbation de la fiche de pointage efficace pour les superviseurs
- Supervision des autorisations (approvisionnement et état) nécessaires pour un projet
- État/contrôle d'intégrité des projets actifs
- Rapport des problèmes
- Modifier le rapport d'état de gestion
    
Project Online inclut une prise en charge des API pour les scénarios suivants:
  
- Pour un complément hébergé par un projet (SharePoint):
    
  - Code (JavaScript, HTML, CSS) hébergé dans SharePoint Online
  - Les ressources qui sont téléchargées vers le navigateur et exécutées sur SharePoint Online.  
  - Logique métier en JavaScript   
  - Accédez aux données stockées dans Project Online ou dans SharePoint, par exemple (sans s'y limiter):  
  - Champs personnalisés  
  - Listes
    
- Pour un complément Project (SharePoint) hébergé par un fournisseur:
    
  - Code qui existe sur un site externe au site Project Online 
  - Un site externe, qui peut être (sans s'y limiter):  
  - Un autre site SharePoint  
  - Application/service Web bâti sur n'importe quelle plateforme  
  - Le site externe contient une logique métier  
  - Le navigateur est redirigé de Project Online vers le site externe avec des jetons d'accès à Project Online  
  - Le site externe peut effectuer des appels vers SharePoint et Project Online
    
- Pour un complément externe/autonome:
    
  - L'utilisateur exécute une application sur son appareil
  - L'application authentifie et appelle directement les API Project Online
    

|Type d’application|Implémentation de l'API|Environnement cible|Exemples d'applications|
|:-----|:-----|:-----|:-----|
|Projet hébergé  <br/> |JSOM (modèle objet de script Java)  <br/> REST  <br/> |Navigateur  <br/> |Entrée de la ligne de présence  <br/> Approbation de la fiche de pointage  <br/> État du projet  <br/> Rapport des problèmes  <br/> |
|Fournisseur de projets hébergé  <br/> |Bibliothèque cliente CSOM  <br/> |Site Web/application Azure  <br/> Environnement non-Windows (lampe, etc.)  <br/> |Validateur de feuille de temps externe  <br/> Importateur de projet  <br/> |
|Externe/autonome  <br/> |REST  <br/> CSOM  <br/> |REST: n'importe quelle plateforme  <br/> CSOM: toute plateforme prise en charge par .NET  <br/> |Entrée de la ligne de présence  <br/> Migration de projets vers un nouveau site  <br/> Modifier l'état de gestion.  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a>Que faut-il prendre pour commencer à développer des applications pour Project Online?

Les éléments communs nécessaires au développement d'applications Project Online sont un compte Project Online et des données de test: des projets et des informations relatives au projet qui incluent des affectations, des tâches, des ressources et des champs personnalisés. Un environnement de développement est également nécessaire, mais des caractéristiques de l'environnement de développement dépendent du type d'application et de l'interface API nécessaires pour l'application. Les sections suivantes décrivent les besoins de développement pour les trois interfaces API.
  
La documentation de référence décrit le modèle objet qui est commun aux trois interfaces, ainsi qu'un mappage d'entité qui affiche les relations entre les composants de modèle objet.
  
## <a name="project-hosted-add-in-development-environment"></a>Environnement de développement de complément hébergé par le projet

Un complément hébergé est un complément qui réside sur le serveur et téléchargé dans un navigateur pour l'exécution de l'exécution. Les compléments hébergés peuvent utiliser les interfaces JSOM ou REST et sont écrits en JavaScript. Project Online fournit des références à la bibliothèque JSOM pour l'exécution de l'exécution. En supposant que le développement se trouve sur une plateforme Windows, les ressources nécessaires sont les suivantes:
  
- Visual Studio 2015 (recommandé) ou Visual Studio 2013
    
- Outils de développement Office pour Visual Studio
    
- Langage JavaScript
    
Consultez https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages l'exemple d'application. 
  
Vous pouvez télécharger et exécuter l'exemple en quelques étapes simples:
  
1. Télécharger et ouvrir l'exemple d'application
    
2. Mettre à jour la propriété SiteURL dans la fenêtre Propriétés
    
   Project Online examine à la fois l'étendue de l'application du complément et les autorisations de l'utilisateur pour régir l'accès aux informations sur l'hôte Project online. Si l'accès est explicitement refusé dans l'un ou l'autre de ces paramètres, ou les deux, Project Online refuse l'accès aux informations. Dans le cas contraire, l'accès est accordé.
    
3. Activez [chargement](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) sur votre site.  
    
4. Créez le projet.
    
5. Exécutez le projet.
    
## <a name="project-provider-hosted-add-in-development-environment"></a>Environnement de développement de complément hébergé par un fournisseur de projets

Les compléments hébergés par le fournisseur sont des applications écrites et résidant sur n'importe quelle plateforme Web. Ils peuvent se connecter et effectuer des opérations de données à l'aide de l'API REST (ou CSOM pour les plateformes Microsoft). Toute langue et tout environnement qui prend en charge l'interface REST peuvent être utilisés pour le développement. 
  
Un exemple de l'environnement de développement Windows pour ce type d'application inclut les éléments suivants:
  
-  Visual Studio 2015 (recommandé) ou Visual Studio 2013 
    
- Outils de développement Microsoft Office pour Visual Studio (fourni avec Visual Studio 2015 Professional et Enterprise Edition)
    
- .NET Framework 4,0 ou version ultérieure
    
- [Package CSOM SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (pour les appels CSOM) 
    
- Langage de programmation, tel que C# 
    
Visitez https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations les exemples de scripts de travail. 
  
Vous pouvez exécuter l'exemple en quelques étapes:
  
1. Télécharger et ouvrir l'exemple d'application
    
2. Mettre à jour la propriété SiteURL dans la fenêtre Propriétés
    
   Project Online examine à la fois l'étendue de l'application du complément et les autorisations de l'utilisateur pour régir l'accès aux informations sur l'hôte Project online. Si l'accès est explicitement refusé dans l'un ou l'autre de ces paramètres, ou les deux, Project Online refuse l'accès aux informations. Dans le cas contraire, l'accès est accordé.
    
3. Activez [chargement](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) sur votre site. 
    
4. Créez le projet.
    
5. Exécutez le projet.
    
## <a name="externalstandalone-application-development-environment"></a>Environnement de développement d'application externe/autonome

Une application autonome peut appeler Project Online à l'aide du modèle objet côté client (CSOM) ou REST pour communiquer avec Project Online pour créer, récupérer, mettre à jour et supprimer des informations résidant sur le serveur. Il s'agit d'une application cliente autonome qui dépend du niveau d'accès utilisateur à exécuter. 
  
Un exemple de l'environnement de développement Windows pour ce type d'application inclut les éléments suivants:
  
- Visual Studio 2015 (recommandé) ou Visual Studio 2013 
    
- Outils de développement Microsoft Office pour Visual Studio (fourni avec Visual Studio 2015 Professional et Enterprise Edition)
    
- .NET Framework 4,0 ou version ultérieure
    
- [Package CSOM SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (pour les appels CSOM) 
    
- Langage de programmation, tel que C# 
    
Consultez https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields l'exemple d'application. 
  
Vous pouvez exécuter l'exemple en quelques étapes:
  
1. Télécharger l'exemple d'application
    
2. Effectuez quelques modifications pour accéder à votre site Project Online: le nom du site, le compte d'utilisateur et le mot de passe.
    
   Assurez-vous que l'utilisateur a accès à tous les projets. Project Online utilise les autorisations des utilisateurs pour régir l'accès aux informations dans le magasin de données.
    
3. Ajoutez l'assembly SharePoint aux références à l'aide de la console du gestionnaire de package NuGet, accessible à partir du menu outils en tapant ce qui suit dans la console NuGet: 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. Créez le projet.
    
5. Exécutez le projet.
    
## <a name="next-steps"></a>Étapes suivantes

Chaque exemple d'application contient un article expliquant les points forts de l'utilisation de l'API de projet individuelle. Les articles figurent dans la liste suivante, ainsi que quelques articles qui décrivent les relations entre les entités, les informations sur le système de requêtes et l'accès aux champs personnalisés. 
  
- [Développement d'une application Project Online à l'aide du modèle objet côté client](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [Développement d'un complément Project Online à l'aide du modèle objet JavaScript (JSOM)](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [Accès aux champs personnalisés d’entreprise Project Online](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a>Voir aussi

Pour obtenir de la documentation et des exemples relatifs à Microsoft Project Online et au développement d’applications à l’aide de CSOM, consultez le [Portail de développement Project](https://developer.microsoft.com/en-us/project).
    

