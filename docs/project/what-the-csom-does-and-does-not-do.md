---
title: Fonctionnalités du modèle CSOM
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 6828485c-040b-4278-923f-4cc7c8fe0fb1
description: Le modèle objet côté client (CSOM) est un ensemble d’API pour Project Server 2013 conçues pour une utilisation en ligne et locale dans les applications qui peuvent être développées pour les PC, les appareils mobiles et les tablettes. Cet article inclut des cas d’utilisation type du modèle CSOM et répertorie également les limites de ce modèle.
ms.localizationpriority: high
ms.openlocfilehash: ca926d445b2ea447c76282ea36c7df472988ca54
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372107"
---
# <a name="what-the-csom-does-and-does-not-do"></a>Fonctionnalités du modèle CSOM

Le modèle objet côté client (CSOM) est un ensemble d’API pour Project Server 2013 conçues pour une utilisation en ligne et locale dans les applications qui peuvent être développées pour les PC, les appareils mobiles et les tablettes. Cet article inclut des cas d’utilisation type du modèle CSOM et répertorie également les limites de ce modèle.
  
|||
|:-----|:-----|
|||

Le CSOM permet le développement des applications pour Project Server 2013 et l’intégration de Project Server à d’autres applications. Les applications peuvent être développées pour s’exécuter sur des PC, des appareils mobiles comme Windows Phone 7.5, des tablettes comme les appareils Windows 8, ainsi que des appareils iOS et Android. Le CSOM offre des API qui couvrent les fonctionnalités des 12 services PSI les plus couramment utilisés dans Project Server. Les API CSOM sont organisées différemment et sont plus faciles à utiliser que les services PSI basés sur WCF et sur ASMX. Le CSOM n’utilise pas de jeu de données ADO.NET et est accessible via le protocole OData. Le CSOM permet le développement des applications à l’aide des bibliothèques .NET Framework 4, de JavaScript ou des requêtes REST.
  
Pour une vue d’ensemble du CSOM et des articles qui montrent comment utiliser JavaScript et .NET Framework 4 avec le CSOM, consultez l’article [Modèle objet côté client (CSOM) pour Project Server](client-side-object-model-csom-for-project-2013.md). Pour plus d’informations sur les classes, les membres et les assemblys CSOM, consultez la référence de l’espace de noms [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx).
  
## <a name="usage-scenarios-for-the-csom"></a>Scénarios d’utilisation du CSOM

<a name="pj15_WhatTheCSOM_UsageScenarios"> </a>

Voici des exemples de certains types d’applications pris en charge par le CSOM. Le CSOM peut être utilisé à la place de l’interface PSI dans de nombreux cas :
  
- **Développer des applications qui étendent Project Server** L’objectif principal du CSOM est le développement d’applications pour Project Server 2013, où les applications peuvent être créées pour un large éventail d’appareils incluant des PC, des appareils mobiles et des tablettes. Les applications peuvent être distribuées au sein d’un catalogue d’applications privé ou d’un Office Store public.

- **Automatiser la création ou la gestion des entités dans Project Server** Le CSOM peut effectuer des opérations CRUD pour les entités comme des projets, des tâches, des affectations, des ressources d’entreprise, des champs personnalisés, des tables de choix, des feuilles de temps, des  gestionnaires d’événements, des phases de flux de travail et des étapes. Il existe souvent des cas où une application personnalisée peut faire économiser du temps avec des tâches répétitives ou en bloc.

- **Obtenir des données dans les tables publiées de la base de données Project** Étant donné que l’accès direct à la base de données vers les tables provisoires, publiées et archivées n’est pas pris en charge, vous pouvez utiliser le CSOM pour lire les données qui ne sont pas disponibles dans les vues ou les tables de création de rapports. Vous pouvez, par exemple, obtenir des informations relatives aux étapes, aux phases et aux activités de flux de travail. Pour lire les données dans les tables de création de rapports, vous pouvez utiliser des requêtes OData.

- **Valider les données de feuille de temps et de statut** Utilisez le CSOM dans les gestionnaires d’événements locaux ou les récepteurs d’événements distants pour les pré-événements afin de valider les données de feuille de temps et de statut d’affectation saisies par les utilisateurs avant l’enregistrement des données dans Project Web App.

- **Créer des projets financiers** Créez des projets pour la capture de temps via la feuille de temps pour l’intégration à un système financier. Créez une hiérarchie de codes financiers qui reflètent la structure de répartition des coûts du système financier. Les projets financiers ne nécessitent pas de mise à jour de planification ou d’état.

- **Intégrer aux systèmes de comptabilité** Capturez les coûts et les dépenses de ressources associés aux projets pour alimenter les systèmes financiers et de facturation et à des fins de comparaison de budget. Synchronisez les tâches, les ressources et les affectations entre les systèmes. Capturez des données de feuille de temps dans un système pour alimenter l’autre (la feuille de temps utilisée dépend des besoins de l’organisation ou des projets individuels).

- **Automatiser les mises à jour des membres de l’équipe** Pour les projets qui ne sont pas gérés activement, mettez automatiquement à jour les projets sur le serveur avec la progression et d’autres modifications des membres de l’équipe de projet. Les projets peuvent être mis à jour et republiés sans qu’un responsable de projet examine les résultats ou n’apporte des ajustements au plan.

    > [!NOTE]
    > Le CSOM prend en charge l’envoi des mises à jour de statut, mais ne prend actuellement pas en charge les approbations de statut.
  
- **Évaluer les données de Project Server dans les récepteurs d’événements distants** Un récepteur d’événements distant pour un pré-événement **ProjectCreating** peut utiliser les données de Project Server depuis le CSOM pour vous aider à déterminer si l’événement doit être annulé. Par exemple, avant de créer un projet, comparez la proposition de projet avec des projets existants.

- **Prise en charge des flux de travail Project Server déclaratifs** Le CSOM active les flux de travail Project Server qui sont créés dans SharePoint Designer 2013. Le CSOM prend en charge les définitions de flux de travail qui utilisent Windows Workflow Foundation version 4 (WF4). (L’interface PSI ne prend pas en charge les flux de travail WF4.)

- **Créer des flux de travail Project Server complexes** Lorsque vous développez des flux de travail avec Visual Studio 2012, vous pouvez utiliser le CSOM pour des actions complexes au sein des étapes de flux de travail, ou créer des actions de flux de travail personnalisés.

## <a name="what-the-csom-does-not-do"></a>Fonctionnalités non prises en charge par le CSOM

<a name="pj15_WhatTheCSOM_DoesNotDo"> </a>

Le CSOM ne constitue pas un remplacement complet de l’interface PSI. Étant donné que le CSOM utilise en interne les services PSI, le CSOM présente la plupart des limitations fonctionnelles de l’interface PSI. En plus des limitations du PSI, comme le fait de ne pas pouvoir accéder aux données dans les projets locaux (fichiers .mpp), le CSOM n’inclut pas les fonctionnalités d’administration habituellement gérées dans Project Web App. Par exemple, la création de groupes de sécurité personnalisés peut être gérée dans la page Paramètres de site - Autorisations pour Project Web App.
  
Pour obtenir la liste des actions que ni l’interface PSI ni le modèle CSOM ne gèrent, consultez la section *Ce que l’interface PSI ne fait pas* dans [Ce que fait et ne fait pas l’interface PSI](what-the-psi-does-and-does-not-do.md).
  
### <a name="psi-services-that-the-csom-does-not-cover"></a>Services PSI non couverts par le CSOM

<a name="pj15_WhatTheCSOM_PSIServices"> </a>

Le CSOM n’inclut pas les fonctionnalités des services PSI suivants :
  
- **Service d’administration** Pour gérer les opérations et les paramètres d’administration dans Project Server et pour les sites de projets connexes, comme la création de périodes fiscales et la définition des paramètres de la feuille de temps, utilisez les méthodes PSI dans la classe [WebSvcAdmin.Admin](https://msdn.microsoft.com/library/WebSvcAdmin.Admin.aspx). Project Web App lui-même utilise des méthodes d'**administration** dans plusieurs des pages qui sont liées à la page des paramètres du serveur (https://*ServerName* / *ProjectServerName*/_layouts/15/pwa/Admin/Admin.aspx).

- **Service d’archivage** Pour enregistrer et gérer des entités comme les projets, les ressources et les champs personnalisés dans les tables archivées, utilisez les méthodes PSI dans la classe [Archive](https://msdn.microsoft.com/library/WebSvcArchive.Archive.aspx).

- **Service CubeAdmin** Pour créer et gérer les cubes OLAP pour les installations sur site, utilisez les méthodes PSI de la classe [WebSvcCubeAdmin.CubeAdmin](https://msdn.microsoft.com/library/WebSvcCubeAdmin.CubeAdmin.aspx), ou utilisez la page de gestion des bases de données OLAP (https:// *ServerName* / *ProjectServerName* /_layouts/15/pwa/CubeAdmin/CubeAnalysisAdmin.aspx) dans Project Web App.

    > [!NOTE]
    > Microsoft Project Online ne prend pas en charge les cubes OLAP.
  
- **Service de pilote** Pour créer et gérer les axes stratégiques pour les analyses de portefeuilles de projets, utilisez les méthodes PSI dans la classe [WebSvcDriver.Driver](https://msdn.microsoft.com/library/WebSvcDriver.Driver.aspx).

- **Service LoginForms et service LoginWindows** L’authentification dans le CSOM s’effectue durant l’initialisation de l’objet **ProjectContext** avec l’authentification OAuth ou Windows. Pour créer des applications pour une authentification multi-niveau, où une application locale de confiance totale peut utiliser l’authentification par formulaire et l’authentification Windows, utilisez les méthodes PSI dans la classe [WebSvcLoginForms.LoginForms](https://msdn.microsoft.com/library/WebSvcLoginForms.LoginForms.aspx) et la classe [WebSvcLoginWindows.LoginWindows](https://msdn.microsoft.com/library/WebSvcLoginWindows.LoginWindows.aspx).

- **Service de notification** Pour créer et gérer des alertes et des rappels, utilisez les méthodes PSI dans la classe [WebSvcNotifications.Notifications](https://msdn.microsoft.com/library/WebSvcNotifications.Notifications.aspx).

- **Service ObjectLinkProvider** Pour créer et gérer des objets web et des liens vers des documents et des éléments de liste SharePoint, utilisez les méthodes PSI dans la classe [WebSvcObjectLinkProvider.ObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.ObjectLinkProvider.aspx).

- **Service PortfolioAnalyses** Pour créer et gérer des analyses de portefeuille de projets, y compris les solutions du planificateur et les solutions de l’optimiseur, utilisez les méthodes PSI dans la classe [WebSvcPortfolioAnalyses.PortfolioAnalyses](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.aspx).

- **Service QueueSystem** Le CSOM peut obtenir des informations de base sur les travaux en file d’attente de Project Server et inclut la méthode [ProjectContext.WaitForQueue](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WaitForQueue.aspx). Pour une gestion plus approfondie du système de mise en file d’attente de Project Server, utilisez les méthodes PSI dans la classe [WebSvcQueueSystem.QueueSystem](https://msdn.microsoft.com/library/WebSvcQueueSystem.QueueSystem.aspx).

- **Service de sécurité** Pour créer et gérer des groupes de sécurité, des modèles et des catégories Project Server, et vérifier les autorisations pour l’utilisateur actuel, utilisez les méthodes PSI dans la classe [WebSvcSecurity.Security](https://msdn.microsoft.com/library/WebSvcSecurity.Security.aspx).

- **Service WssInterop** Pour obtenir des informations et gérer les sites de projets, utilisez les méthodes PSI dans la classe [WebSvcWssInterop.WssInterop](https://msdn.microsoft.com/library/WebSvcWssInterop.WssInterop.aspx).

    > [!NOTE]
    > Vous pouvez utiliser le CSOM dans SharePoint Server 2013. Les sites de projets sont des sites SharePoint.
  
Le CSOM n’active pas les extensions comme celles de l’interface PSI. Par exemple, si vous créez une extension PSI pour une utilisation locale, le CSOM ne peut pas être modifié pour utiliser l’extension PSI. Vous pouvez implémenter des scénarios d’extension d’autres manières :
  
- Agrégez les appels CSOM au sein d’un composant local ou d’un composant qui s’exécute sur Microsoft Azure.

- Utilisez les requêtes OData des données de création de rapports au lieu d’accéder directement aux tables de création de rapports dans la base de données Project Server.

- Intégrez les appels CSOM aux applications tierces via l’authentification OAuth à partir de Microsoft Project Online ou à des composants côté serveur pour une utilisation locale.

- Les applications qui utilisent le CSOM peuvent également utiliser des bases de données personnalisées en local ou avec SQL Azure.

### <a name="request-limits-of-the-csom"></a>Limites des requêtes du CSOM

<a name="pj15_WhatTheCSOM_RequestLimits"> </a>

Le CSOM dans Project Server 2013 repose sur l’implémentation CSOM dans SharePoint Server 2013 et hérite des limites de taille maximale d’une requête. SharePoint est limité à 2 Mo pour une requête d’opération et à 50 Mo pour la taille d’un objet binaire soumis. La taille de la requête est limitée pour protéger le serveur des files d’attente excessivement longues des opérations et des retards de traitement des objets binaires volumineux.
  
Par exemple, si vous utilisez le CSOM pour créer un projet et que vous modifiez le projet pour ajouter 252 tâches avec une quantité minimale d’informations comme un nom court, le GUID de la tâche et une durée de 1 jour, la quantité totale des données dans la requête **DraftProject.Update** est inférieure à 2 Mo. Toutefois, si vous essayez d’ajouter 253 tâches à un projet vide, la limite de 2 Mo est dépassée et vous recevez l’exception suivante : **Microsoft.SharePoint.Client.ServerException : la requête utilise une quantité excessive de ressources**
  
Pour capturer les données dans une requête CSOM sur HTTP ou HTTPS, vous pouvez utiliser un outil de débogage web tel que [Fiddler](https://www.fiddler2.com) (<https://www.fiddler2.com>). Pour obtenir un exemple de code qui implémente un test de taille de requête et inclut une solution qui divise une requête volumineuse en groupes plus petits, consultez [DraftProject.Update](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.DraftProject.Update.aspx).
  
## <a name="see-also"></a>Voir aussi

<a name="pj15_WhatTheCSOM_AR"> </a>

- [Modèle objet côté client (CSOM) pour Project Server](client-side-object-model-csom-for-project-2013.md)
- [Fonctionnalités de l’interface PSI](what-the-psi-does-and-does-not-do.md)
- [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)
