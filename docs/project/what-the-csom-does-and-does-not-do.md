---
title: Fonctionnalité du modèle CSOM
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6828485c-040b-4278-923f-4cc7c8fe0fb1
description: Le modèle objet côté client (CSOM) est un ensemble d’API pour Project Server 2013 qui sont destinées à la fois en ligne et sur site utiliser dans les applications qui peuvent être développées pour les tablettes PC et appareils mobiles. Cet article inclut certains scénarios courants d’utilisation du modèle CSOM et répertorie les limites de CSOM.
ms.openlocfilehash: ad9f9e0404cb0063a1c58c8e66a022372881a24f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399290"
---
# <a name="what-the-csom-does-and-does-not-do"></a>Fonctionnalité du modèle CSOM

Le modèle objet côté client (CSOM) est un ensemble d’API pour Project Server 2013 qui sont destinées à la fois en ligne et sur site utiliser dans les applications qui peuvent être développées pour les tablettes PC et appareils mobiles. Cet article inclut certains scénarios courants d’utilisation du modèle CSOM et répertorie les limites de CSOM.
  
|||
|:-----|:-----|
|||
   
Le modèle CSOM permet le développement d’applications pour Project Server 2013 et l’intégration de Project Server avec d’autres applications. Les applications peuvent être développées pour s’exécuter sur PC, les appareils mobiles tels que Windows Phone 7.5, tablettes telles que les périphériques Windows 8 et iOS et Android. Le modèle fournit des API qui traitent des fonctionnalités de douze plus fréquemment utilisées des services PSI dans Project Server. Les API de modèle sont organisées différemment et sont faciles à utiliser que les services PSI basées sur ASMX et basée sur WCF. Le modèle CSOM n’utilise pas de jeux de données ADO.NET et est accessible via le protocole OData. Vous pouvez développer avec le modèle à l’aide de bibliothèques de .NET Framework 4, JavaScript, ou les requêtes Representational State Transfer (REST).
  
Pour une vue d’ensemble des articles qui illustrent l’utilisation de JavaScript et .NET Framework 4 avec le modèle CSOM, voir [modèle d’objet côté Client (CSOM) pour Project Server](client-side-object-model-csom-for-project-2013.md). Pour plus d’informations sur les assemblys CSOM, classes et des membres, voir la référence d’espace de noms [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) . 
  
## <a name="usage-scenarios-for-the-csom"></a>Scénarios d’utilisation pour le modèle CSOM
<a name="pj15_WhatTheCSOM_UsageScenarios"> </a>

Voici des exemples de certains types d’applications prenant en charge le modèle CSOM. Le modèle peut être utilisée au lieu de la PSI pour de nombreux scénarios :
  
- **Développer les applications qui étendent Project Server** Le principal objectif de CSOM est le développement d’applications pour Project Server 2013, où les applications peuvent être créées pour une vaste gamme de périphériques tels que des PC, les appareils mobiles et tablettes. Les applications peuvent être distribuées au sein d’un catalogue d’applications privé ou dans l’Office Store public. 
    
- **Automatiser la création ou la gestion des entités dans Project Server** Le modèle CSOM peut effectuer des opérations CRUD pour les entités, telles que les projets, tâches, affectations, des ressources d’entreprise, des champs personnalisés, tables de choix, feuilles de temps, gestionnaires d’événements, phases du flux de travail et des étapes. Il existe souvent les cas où une application personnalisée peut gagner du temps en bloc et les tâches répétitives. 
    
- **Obtenir des données dans les tables de la base de données de projet publiés** Base de données direct d’accéder à la brouillon, publiée et archiver les tables n'est pas pris en charge, vous pouvez utiliser le modèle CSOM pour lire les données qui ne sont pas disponibles dans les tables ou les affichages de rapports. Par exemple, obtenir des informations sur les étapes de flux de travail, phases et activités. Pour lire les données dans les tableaux de création de rapports, vous pouvez utiliser des requêtes OData. 
    
- **Valider les données de feuille de temps et état** Utiliser le modèle CSOM dans les gestionnaires d’événements locaux ou des récepteurs d’événements distants pour les événements avant pour valider des données d’état ou de la feuille de temps affectation que les utilisateurs entrent, avant que les données sont enregistrées dans Project Web App. 
    
- **Créer des projets financiers** Créer des projets pour la capture de temps par le biais de la feuille de temps pour l’intégration avec un système d’analyse. Créer une hiérarchie de codes financiers qui reflètent la structure de répartition des coûts du système financier. Projets financières ne nécessitent pas de mises à jour de statut ou de planification. 
    
- **Intégrer avec les systèmes comptables** Capturer les coûts des ressources et les dépenses associées aux projets d’alimentation financières et de facturation et à des fins de comparaison budget. Synchroniser les tâches, les ressources et les affectations entre les systèmes. Capturer des données de feuille de temps dans un système à l’autre flux (les feuilles de temps est utilisée en fonction des besoins de votre organisation ou des projets individuels). 
    
- **Automatisation des mises à jour à partir des membres de l’équipe** Pour les projets qui ne sont pas gérées activement, mettre à jour automatiquement les projets sur le serveur avec l’avancement et d’autres modifications à partir de membres de l’équipe. Projets peuvent être mis à jour et republiés sans un responsable de projet révision des résultats ou la réalisation d’ajustements dans le plan. 
    
    > [!NOTE]
    > Le modèle CSOM prend en charge les mises à jour de statut envoi, mais ne prend actuellement pas en charge approbations d’état. 
  
- **Données évaluer Project Server dans les récepteurs d’événements distants** Un récepteur d’événements distants pour un pré-événement **ProjectCreating** pouvez utiliser des données de Project Server à partir du modèle CSOM afin de déterminer s’il faut annuler l’événement. Par exemple, avant de créer un projet, comparez la proposition de projet avec des projets existants. 
    
- **Flux de travail Project Server déclaratifs prise en charge** Le modèle CSOM permet de flux de travail Project Server qui est créés dans SharePoint Designer 2013. Le modèle CSOM prend en charge les définitions de flux de travail qui utilisent Windows Workflow Foundation version 4 (WF4). (La PSI ne gère pas les flux de travail WF4.) 
    
- **Créer des workflows complexes Project Server** Lorsque vous développez des flux de travail avec Visual Studio 2012, vous pouvez utiliser le modèle CSOM pour les actions complexes au sein des étapes de flux de travail ou créer des actions de flux de travail personnalisé. 
    
## <a name="what-the-csom-does-not-do"></a>Ce que le modèle CSOM ne fait pas
<a name="pj15_WhatTheCSOM_DoesNotDo"> </a>

Le modèle n’est pas un remplacement complet pour l’interface PSI. Étant donné que le modèle CSOM utilise en interne des services PSI, le modèle CSOM a nombreuses limitations fonctionnelles même ayant la PSI. En plus des limitations de la PSI, par exemple n’avoir aucun accès aux données dans des projets locaux (fichiers .mpp), le modèle n’inclut pas les fonctionnalités d’administration qui gère les généralement Project Web App. Par exemple, la création de groupes de sécurité personnalisés peut être géré dans la page Paramètres du Site - autorisations Project Web App. 
  
Pour obtenir la liste des actions qui prennent en charge l’interface PSI ni le modèle CSOM, consultez la section *quel la PSI ne fait pas* dans [ce que la PSI fait et ne fait pas](what-the-psi-does-and-does-not-do.md).
  
### <a name="psi-services-that-the-csom-does-not-cover"></a>Services PSI qui n’aborde pas la CSOM
<a name="pj15_WhatTheCSOM_PSIServices"> </a>

Le modèle n’inclut pas les fonctionnalités des services PSI suivants :
  
- **Service d’administration** Pour gérer les paramètres d’administration et opérations dans Project Server et pour les sites de projet associés, tels que la création des périodes fiscales et de définir des paramètres de feuille de temps, utilisez les méthodes PSI dans la classe [WebSvcAdmin.Admin](https://msdn.microsoft.com/library/WebSvcAdmin.Admin.aspx) . Project Web App lui-même utilise les méthodes **Admin** dans la plupart des pages qui sont liées à la page Paramètres du serveur (https:// *nom_serveur*  /  *ProjectServerName* /_layouts/15/pwa/Admin/Admin.aspx). 
    
- **Service d’archivage** Pour enregistrer et gérer les entités telles que les projets, ressources et des champs personnalisés dans les tables d’archivage, utilisez les méthodes PSI dans la classe de [l’Archive](https://msdn.microsoft.com/library/WebSvcArchive.Archive.aspx) . 
    
- **Service CubeAdmin** Pour créer et gérer des cubes OLAP pour les installations locales, utilisez les méthodes PSI dans la classe [WebSvcCubeAdmin.CubeAdmin](https://msdn.microsoft.com/library/WebSvcCubeAdmin.CubeAdmin.aspx) , ou utilisez la page Gestion de base de données OLAP (https:// *nom_serveur*  /  *ProjectServerName* /_layouts/15/pwa / CubeAdmin/CubeAnalysisAdmin.aspx) dans Project Web App. 
    
    > [!NOTE]
    > Project Online ne prend pas en charge les cubes OLAP. 
  
- **Service de pilote** Pour créer et gérer les pilotes d’entreprise pour les analyses de portefeuille de projet, utilisez les méthodes PSI dans la classe [WebSvcDriver.Driver](https://msdn.microsoft.com/library/WebSvcDriver.Driver.aspx) . 
    
- **Services LoginForms et LoginWindows** Authentification dans le modèle est effectuée lors de l’initialisation de l’objet **ProjectContext** , avec l’authentification OAuth ou Windows. Pour créer des applications pour authentification multiple, où une application de confiance totale locale peut utiliser l’authentification par formulaires et l’authentification Windows, utilisez les méthodes PSI dans la classe [WebSvcLoginForms.LoginForms](https://msdn.microsoft.com/library/WebSvcLoginForms.LoginForms.aspx) et le [ WebSvcLoginWindows.LoginWindows](https://msdn.microsoft.com/library/WebSvcLoginWindows.LoginWindows.aspx) classe. 
    
- **Service de notification** Pour créer et gérer les alertes et rappels, utilisez les méthodes PSI dans la classe [WebSvcNotifications.Notifications](https://msdn.microsoft.com/library/WebSvcNotifications.Notifications.aspx) . 
    
- **Service ObjectLinkProvider** Pour créer et gérer les objets web et des liens vers des documents et éléments de liste SharePoint, utilisez les méthodes PSI dans la classe [WebSvcObjectLinkProvider.ObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.ObjectLinkProvider.aspx) . 
    
- **Service PortfolioAnalyses** Pour créer et gérer les analyses de portefeuille project, y compris les solutions planificateur et l’optimiseur, utilisez les méthodes PSI dans la classe [WebSvcPortfolioAnalyses.PortfolioAnalyses](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.aspx) . 
    
- **Service QueueSystem** CSOM permettre obtenir des informations de base sur les travaux de file d’attente de Project Server, ainsi que la méthode [ProjectContext.WaitForQueue](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WaitForQueue.aspx) . Pour la gestion approfondie du système de mise en attente de Project Server, utilisez les méthodes PSI dans la classe [WebSvcQueueSystem.QueueSystem](https://msdn.microsoft.com/library/WebSvcQueueSystem.QueueSystem.aspx) . 
    
- **Service de sécurité** Pour créer et gérer les catégories, les modèles et groupes de sécurité Project Server et pour vérifier les autorisations de l’utilisateur actuel, utilisez les méthodes PSI dans la classe [WebSvcSecurity.Security](https://msdn.microsoft.com/library/WebSvcSecurity.Security.aspx) . 
    
- **Service WssInterop** Pour obtenir des informations sur et gérer des sites de projet, utilisez les méthodes PSI dans la classe [WebSvcWssInterop.WssInterop](https://msdn.microsoft.com/library/WebSvcWssInterop.WssInterop.aspx) . 
    
    > [!NOTE]
    > Vous pouvez utiliser le modèle CSOM dans SharePoint Server 2013. Sites de projet sont des sites SharePoint. 
  
Le modèle CSOM n’active pas les extensions telles que l’interface PSI peut avoir. Par exemple, si vous créez une extension PSI pour une utilisation locale, le modèle CSOM ne sont pas modifiables pour utiliser l’extension PSI. Vous pouvez implémenter des scénarios d’extension d’autres manières :
  
- Appels CSOM agrégations au sein d’un composant local ou d’un composant qui s’exécute sur Microsoft Azure.
    
- Utiliser des requêtes OData des données de création de rapports, au lieu d’accéder directement à des tables de création de rapports dans la base de données Project Server.
    
- Intégrer les appels CSOM avec les applications tierces par le biais de l’authentification OAuth à partir de Project Online ou avec des composants côté serveur pour une utilisation locale.
    
- Les applications qui utilisent le modèle CSOM peuvent également utiliser des bases de données personnalisées locale ou avec SQL Azure.
    
### <a name="request-limits-of-the-csom"></a>Limites des demandes de CSOM
<a name="pj15_WhatTheCSOM_RequestLimits"> </a>

Le modèle CSOM dans Project Server 2013 repose sur l’implémentation du modèle dans SharePoint Server 2013 et hérite les limites de la taille maximale d’une demande. SharePoint a une limite de 2 Mo pour une demande d’opérations et une limite de 50 Mo pour la taille d’un objet binaire soumis. La taille de la demande est limitée à protéger le serveur de files d’attente trop longues des opérations et de traitement des retards pour les objets binaires volumineux.
  
Par exemple, si vous utilisez le modèle pour créer un projet, puis modifiez le projet pour ajouter des 252 tâches avec un minimum d’informations telles que nom court, le GUID de tâche et une durée de 1 d, la quantité totale de données dans la demande de **DraftProject.Update** est inférieur à 2 MO. Mais, si vous essayez d’ajouter 253 ces tâches à un projet vide, la limite de 2 Mo est dépassée et vous recevez l’exception suivante : **Microsoft.SharePoint.Client.ServerException : la demande utilise trop de ressources**
  
Pour capturer les données dans une demande CSOM via HTTP ou HTTPS, vous pouvez utiliser un outil tel que [Fiddler](https://www.fiddler2.com) de débogage site web (https://www.fiddler2.com). Pour obtenir un exemple de code qui implémente un test pour la taille de la demande et inclut une solution qui divise une demande importante en plus petits groupes, voir [DraftProject.Update](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.DraftProject.Update.aspx) . 
  
## <a name="see-also"></a>Voir aussi
<a name="pj15_WhatTheCSOM_AR"> </a>

- [Modèle objet côté client (CSOM) pour Project Server](client-side-object-model-csom-for-project-2013.md)
    
- [Fonctionnalités de l’interface PSI](what-the-psi-does-and-does-not-do.md)
    
- [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)
    

