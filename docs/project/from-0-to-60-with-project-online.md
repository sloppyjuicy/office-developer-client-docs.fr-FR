---
title: De 0 à 60 avec Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: 'Un développeur peut personnaliser un site Project Online (SharePoint hébergé) à l’aide d’applications autonomes et/ou compléments Project. Un large éventail d’applications est possible que la plage à partir de répondre aux besoins des personnes impliquées dans un projet pour les fonctions d’assistance PMO, telles qu’une des options suivantes :'
ms.openlocfilehash: 00f79b05b886bfd2c54c118245e22f10bb5451bf
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392584"
---
# <a name="from-0-to-60-with-project-online"></a>De 0 à 60 avec Project Online

Un développeur peut personnaliser un site Project Online (SharePoint hébergé) à l’aide d’applications autonomes et/ou compléments Project. Un large éventail d’applications est possible que la plage à partir de répondre aux besoins des personnes impliquées dans un projet pour les fonctions d’assistance PMO, telles qu’une des options suivantes :
  
- Saisie de données feuilles de présence optimisée pour les travailleurs
- Approbation de feuilles de présence efficace de contrôleurs
- Supervision des autorisations (acquisition et état) nécessaires pour un projet
- État/vérification des projets en cours
- Rapport des problèmes
- Modifier le rapport d’état de gestion
    
Project Online inclut la prise en charge de l’API pour prendre en charge les scénarios suivants :
  
- Pour un complément Project (SharePoint) hébergée :
    
  - Code (JavaScript, HTML, CSS) qui est hébergée dans SharePoint Online
  - Ressources qui sont téléchargés vers le navigateur et exécutées sur SharePoint Online.  
  - Logique métier qui se trouve dans JavaScript   
  - Accédez aux données est/stocké dans Project Online ou SharePoint telle que (mais n’est pas limité à) :  
  - Champs personnalisés  
  - Lists
    
- Pour un projet (SharePoint) hébergé par le fournisseur complément :
    
  - Code qui existe sur un site externe pour le site Project Online 
  - Un site externe, qui peut être (mais n’est pas limité à) :  
  - Un autre site SharePoint  
  - / Service application Web créée sur une plate-forme  
  - Le site externe contient la logique métier  
  - Le navigateur est redirigé à partir de Project Online site externe avec des jetons d’accès à Project Online  
  - Le site externe permettre émettre des appels vers SharePoint et Project Online
    
- Pour un complément externe/autonomes :
    
  - Utilisateur exécute une application sur leur appareil
  - Application authentifie et appelle directement les API de projet en ligne
    

|Type d’application|Implémentation de l’API|Environnement cible|Exemples d’applications|
|:-----|:-----|:-----|:-----|
|Projet hébergé  <br/> |JSOM (modèle d’objet Java Script)  <br/> REST  <br/> |Browser  <br/> |Entrée de feuille de présence  <br/> Approbation des feuilles de présence  <br/> État du projet  <br/> Rapport des problèmes  <br/> |
|Projet fournisseur hébergé  <br/> |Bibliothèque cliente CSOM  <br/> |Site Web Azure / d’application  <br/> Environnement non Windows (feu, etc.).  <br/> |Validateur de feuille de temps externe  <br/> Projet importateur  <br/> |
|Externe/autonome  <br/> |REST  <br/> CSOM  <br/> |REST - n’importe quelle plateforme  <br/> CSOM - n’importe quelle plateforme .NET pris en charge  <br/> |Entrée de feuille de présence  <br/> Migration de projets vers un nouveau site  <br/> Modifier l’état de gestion.  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a>Que faut-il pour commencer à développer des applications pour Project Online ?

Les éléments nécessaires pour le développement d’applications Project Online sont un compte Project Online et données--informations relatives au projet qui incluent des affectations, tâches, ressources et des champs personnalisés et des projets de test. Un environnement de développement est également nécessaire, mais les détails de l’environnement de développement dépendent du type d’application et l’interface API nécessaires à l’application. Les sections suivantes décrivent les besoins en matière de développement pour les trois interfaces API.
  
La documentation de référence décrit le modèle objet commun pour tous les trois interfaces, ainsi qu’un mappage d’entité qui montre les relations entre les composants de modèle objet.
  
## <a name="project-hosted-add-in-development-environment"></a>Environnement de développement de projet hébergé

Un complément hébergé est un complément qui réside sur le serveur et qui est téléchargé sur un navigateur d’exécution. Compléments hébergés peuvent utiliser les interfaces JSOM ou REST et sont écrits en JavaScript. Project Online fournit des références à la bibliothèque JSOM d’exécution. En supposant que le développement est sur une plate-forme Windows, le suivi des ressources nécessaires :
  
- Visual Studio 2015 (recommandé) ou Visual Studio 2013
    
- Outils de développement Office pour Visual Studio
    
- Langage JavaScript
    
Visitez le site https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages pour un exemple d’application. 
  
Vous pouvez télécharger et exécuter l’exemple en plusieurs étapes :
  
1. Télécharger et ouvrir l’exemple d’application
    
2. Mise à jour SiteURL dans la fenêtre Propriétés
    
   Project Online examine à la fois la portée d’application de la macro complémentaire et les autorisations utilisateur déterminent l’accès aux informations sur l’hôte de Project Online. Si l’accès est refusé explicitement dans un ou les deux paramètres, Project Online refuse l’accès aux informations. Dans le cas contraire, l’accès est accordé.
    
3. Activer le [chargement de version test](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) sur votre site.  
    
4. Générez le projet.
    
5. Exécutez le projet.
    
## <a name="project-provider-hosted-add-in-development-environment"></a>Environnement hébergé par le fournisseur de développement du projet

Les compléments fournisseur hébergé sont les applications écrites et résidant sur n’importe quelle plateforme web. Ils peuvent se connecter et effectuer des opérations de données utilisant le REST (ou CSOM pour les plateformes Microsoft) API. N’importe quel langage et un environnement qui prend en charge l’interface REST peuvent être utilisés pour le développement. 
  
Un exemple de l’environnement de développement Windows pour ce type d’application comprend les éléments suivants :
  
-  Visual Studio 2015 (recommandé) ou Visual Studio 2013 
    
- Outils de développement Microsoft Office pour Visual Studio (fourni avec Visual Studio 2015 Professional et Enterprise Edition)
    
- .NET framework 4.0 ou version ultérieure
    
- [Package SharePointOnline CSOM](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (pour les appels CSOM) 
    
- Un langage de programmation, tels que Visual C# 
    
Visitez le site https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations pour l’utilisation des exemples de scripts. 
  
Vous pouvez exécuter l’exemple en quelques étapes :
  
1. Télécharger et ouvrir l’exemple d’application
    
2. Mise à jour SiteURL dans la fenêtre Propriétés
    
   Project Online examine à la fois la portée d’application de la macro complémentaire et les autorisations utilisateur déterminent l’accès aux informations sur l’hôte de Project Online. Si l’accès est refusé explicitement dans un ou les deux paramètres, Project Online refuse l’accès aux informations. Dans le cas contraire, l’accès est accordé.
    
3. Activer le [chargement de version test](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) sur votre site. 
    
4. Générez le projet.
    
5. Exécutez le projet.
    
## <a name="externalstandalone-application-development-environment"></a>Environnement de développement d’application externe/autonome

Une application autonome peut appeler Project Online à l’aide du modèle d’objet côté Client (CSOM) ou le reste de communiquer avec Project Online pour créer, extraire, mettre à jour et supprimer des informations résidant sur le serveur. Il s’agit d’une application cliente autonome qui varie selon le niveau d’accès utilisateur à exécuter. 
  
Un exemple de l’environnement de développement Windows pour ce type d’application comprend les éléments suivants :
  
- Visual Studio 2015 (recommandé) ou Visual Studio 2013 
    
- Outils de développement Microsoft Office pour Visual Studio (fourni avec Visual Studio 2015 Professional et Enterprise Edition)
    
- .NET framework 4.0 ou version ultérieure
    
- [Package SharePointOnline CSOM](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (pour les appels CSOM) 
    
- Un langage de programmation, tels que Visual C# 
    
Visitez le site https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields pour un exemple d’application. 
  
Vous pouvez exécuter l’exemple en quelques étapes :
  
1. Télécharger l’exemple d’application
    
2. Apporter quelques modifications pour accéder à votre site Project Online : le nom du site, le compte d’utilisateur et le mot de passe.
    
   Assurez-vous que l’utilisateur a accès à tous les projets. Project Online utilise des autorisations utilisateur pour déterminent l’accès à des informations dans le magasin de données.
    
3. Les références à l’aide de la Console du Gestionnaire de Package Nuget, disponibles dans le menu Outils en tapant ce qui suit dans la console de Nuget, ajoutez l’assembly de SharePoint : 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. Générez le projet.
    
5. Exécutez le projet.
    
## <a name="next-steps"></a>Étapes suivantes

Chaque exemple d’application possède un article afin d’expliquer la mise en surbrillance de l’utilisation de l’API de projet individuels. Les articles s’affichent dans la liste suivante, ainsi que de quelques articles qui décrivent les relations entre les entités, des informations sur le système de requête et l’accès aux champs personnalisés. 
  
- [Développement d’une Application en ligne de projet à l’aide du modèle objet côté Client](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [Développement d’un complément Project Online à l’aide du modèle objet JavaScript (JSOM)](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [Accès aux champs personnalisés d’entreprise Project Online](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a>Voir aussi

Pour la documentation et des exemples relatifs à Project Online et développement d’applications à l’aide de CSOM, voir le [Portail de développement Project](https://developer.microsoft.com/en-us/project).
    

