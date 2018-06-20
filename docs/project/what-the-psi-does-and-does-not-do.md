---
title: Ce que fait la PSI et ne fait pas
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: eac6be6a-9a20-4bc0-8da2-b2fd93aab04f
description: L’Interface de Project Server (PSI) peut aider à automatiser de nombreux processus côté serveur dans les installations locales de Project Server 2013. Toutefois, plusieurs fonctions nécessitent l’utilisation de Microsoft Project Professional 2013.
ms.openlocfilehash: 0afdcdf43c4748fff42f7b5bc74af6c4b59b0b07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787940"
---
# <a name="what-the-psi-does-and-does-not-do"></a>Ce que fait la PSI et ne fait pas

L’Interface de Project Server (PSI) peut aider à automatiser de nombreux processus côté serveur dans les installations locales de Project Server 2013. Toutefois, plusieurs fonctions nécessitent l’utilisation de Microsoft Project Professional 2013.
  
|||
|:-----|:-----|
|||
   
L’interface PSI est conçue pour compléter les fonctionnalités de Project Professional 2013, plutôt que de fournir un autre serveur pour toutes les fonctions de Project Professionnel. Les développeurs tiers peuvent utiliser PSI pour aider à créer des composants WebPart pour les installations locales de Project Web App et les espaces de travail de projet, créer des applications Windows personnalisées et les applications web qui interagissent avec les données de Project Server sur site, développer des flux de travail logique de gestion de portefeuille de projet, développer des gestionnaires d’événements locaux de confiance totale et intégration de Project Server avec d’autres applications. L’interface PSI ne peut pas être utilisée pour le développement d’applications pour l’Office Store, les appareils mobiles ou les tablettes ; Pour ce faire, vous pouvez utiliser le modèle objet côté client (CSOM).
  
> [!NOTE]
> L’interface PSI fournit une interface par programme plus étendue pour Project Server 2013 que celle offerte par le modèle CSOM. Mais, à moins que le modèle ne fournit pas les fonctionnalités dont vous avez besoin, nous vous recommandons d’utiliser le modèle CSOM à développer de nouvelles applications. Pour plus d’informations, voir [ce que le modèle et ne fait pas](what-the-csom-does-and-does-not-do.md). 
  
## <a name="usage-scenarios-for-the-psi"></a>Scénarios d’utilisation pour la PSI
<a name="pj14_WhatPSIDoes_UsageScenarios"> </a>

Voici des exemples de certaines applications qui prend en charge l’interface PSI pour les calculs et les projets côté serveur :
  
- **Automatiser la création ou la gestion des entités dans Project Server** Bien que Project Professional 2013 et Project Web App ensemble sont conçus pour gérer la création d’entités, telles que les projets et champs personnalisés des ressources d’entreprise et la gestion, il existe souvent les cas où une application personnalisée peut gagner du temps avec en bloc ou tâches répétitives. Plusieurs types de travaux CSOM ne fait pas, par exemple, avec les cubes OLAP, analyses de portefeuille project, pilotes d’entreprise, les notifications, fournisseurs d’objet de lien, sécurité et interopérabilité SharePoint peut automatiser la PSI. 
    
- **Obtenir des données dans la liste publiée ou tables d’archivage de la base de données de projet** Base de données direct d’accéder à la brouillon, publiée et archiver les tables n'est pas pris en charge, vous pouvez utiliser l’interface PSI pour lire des données qui ne sont pas disponibles dans les tables ou les affichages de rapports. Par exemple, obtenir des informations sur les versions de projets, les dates et les modifications qui sont stockées dans les tables d’archivage, puis remplir un contrôle de grille JS dans un composant WebPart avec les informations. 
    
- **Valider les données de feuille de temps et état** Utilisez l’interface PSI dans les gestionnaires d’événements avant locales pour valider des données d’état ou de la feuille de temps affectation que les utilisateurs entrent, avant que les données sont enregistrées dans Project Web App. 
    
- **Projets de maintenance** Créer des projets à utiliser avec les plans de ressources espace réservé. Temps réserve ou d’un livre par rapport aux ressources pour les travaux de maintenance ou commerciale de base. Projets de maintenance n’ont généralement pas de tâches. 
    
- **Créer des projets financiers** Créer des projets pour la capture de temps par le biais de la feuille de temps pour l’intégration avec un système d’analyse. Créer une hiérarchie de codes financiers qui reflètent la structure de répartition des coûts du système financier. Projets financières ne nécessitent pas de mises à jour de statut ou de planification. 
    
- **Intégrer avec les systèmes comptables** Capturer les coûts des ressources et les dépenses associées aux projets d’alimentation financières et de facturation et à des fins de comparaison budget. Synchroniser les tâches, les ressources et les affectations entre les systèmes. Capturer des données de feuille de temps dans un système à l’autre flux (les feuilles de temps est utilisée en fonction des besoins de votre organisation ou des projets individuels). 
    
- **Automatisation des mises à jour à partir des membres de l’équipe** Pour les projets qui ne sont pas gérées activement, mettre à jour automatiquement les projets sur le serveur avec l’avancement et d’autres modifications à partir de membres de l’équipe. Projets peuvent être mis à jour et republiés sans un responsable de projet révision des résultats ou la réalisation d’ajustements dans le plan. 
    
- **Données d’évaluation de Project Server dans les gestionnaires d’événements locaux de confiance totale** Un gestionnaire d’événements local pour l’événement avant **ProjectCreating** pouvez utiliser des données de Project Server à partir de l’interface PSI pour aider à déterminer s’il faut annuler un événement. Par exemple, avant de créer un projet, comparez la proposition de projet avec des projets existants. 
    
- **Créer des activités de flux de travail personnalisé pour la gestion de la demande** Utilisez l’interface PSI dans les activités de flux de travail locale, la confiance totale pour modifier et mettre à jour les propositions de projet basées sur des modèles de projet d’entreprise. Champs personnalisés de projet permet de baliser le projet avec les informations nécessaires pour le processus d’initiation et d’approbation. Ajouter des tâches pour identifier les phases du projet pour les principaux jalons et livrables. Lors de l’approbation des propositions de projet, un flux de travail peut modifier les propositions dans des projets à grande échelle qui sont gérés avec Project Professional. 
    
- **Extensions de créer la PSI** (**Déconseillées.** Les extensions sont déconseillées dans Project Server 2013 et ne seront pas prise en charge dans les versions futures.) L’interface PSI peut être étendue avec des services personnalisés à l’aide de l’interface Windows Communication Foundation (WCF). Extensions PSI s’exécutent sur l’ordinateur Project Server et peuvent utiliser la même infrastructure de sécurité qui utilisent les services PSI intégrés. Extensions peuvent interroger des tables dans les création de rapports, utilisez les tables de base de données distincte, consolider les appels PSI pour enregistrer la bande passante et intégrer des applications tierces et d’autres composants côté serveur. Pour plus d’informations, voir [Développement d’Extensions PSI](http://msdn.microsoft.com/library/1b484623-94fb-47c9-84c1-3e68a9133042%28Office.15%29.aspx).
    
- **Emprunt d’identité utilisés dans les applications de confiance totale, locales** Les appels vers l’interface WCF de la PSI peuvent être empruntées, afin qu’une application suppose que les autorisations de sécurité de l’utilisateur représenté. Emprunt d’identité doit être utilisé avec modération et avec soin. Lecture et mise à jour des informations d’état pour d’autres utilisateurs ne nécessitent pas l’emprunt d’identité. Nouvelles applications qui nécessitent l’emprunt d’identité doivent utiliser le modèle CSOM et le protocole OAuth au lieu de la PSI. Pour plus d’informations sur l’emprunt d’identité avec l’interface PSI, voir [Utiliser l’emprunt d’identité avec WCF](http://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx).
    
> [!NOTE]
> Dans certains cas, la PSI peut être utilisée dans les applications clientes avec CSOM et Project Online. Si vous utilisez un service web PSI basées sur ASMX, l’application doit inclure une méthode pour authentifier l’objet [Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) dans le modèle et une méthode pour authentifier la ** System.Web.Services.Protocols.SoapHttpClientProtocol** objet client. Pour obtenir un exemple qui utilise un service web avec SharePoint CSOM, voir [Authentification à distance en matière d’authentification SharePoint Online Using Claims-Based](http://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx). > Fait de contraintes autorisations au niveau de l’application, l’interface PSI ne peut être utilisée dans les applications qui sont conçues pour la distribution dans l’Office Store public. Dans ce cas, vous pouvez utiliser uniquement le modèle CSOM. 
  
## <a name="what-the-psi-does-not-do"></a>Ce que l’interface PSI ne fait pas
<a name="pj14_WhatPSIDoes_DoesNotDo"> </a>

Bien qu’il existe de nombreuses possibilités de l’interface PSI, il existe certaines choses que PSI ne fait pas. Voici deux choses PSI ne peut pas faire, mais ne le modèle CSOM.
  
### <a name="project-online-and-remote-event-receivers"></a>Project Online et les récepteurs d’événements distants

La limitation de la PSI principale est avec Project Online. Applications qui utilisent la PSI nécessitent un accès confiance totale à une installation locale de Project Server. Par exemple, l’interface PSI ne peut être utilisée dans les récepteurs d’événements distants, où le récepteur d’événements est installé en tant que service sur Microsoft Azure.
  
### <a name="workflows-and-claims-authentication"></a>Flux de travail et authentification par revendications

Une définition de flux de travail qui utilise la version de Windows Workflow Foundation 4 (WF4) requiert une authentification basée sur les revendications, dont la PSI ne prend pas en charge directement. Cela signifie que vous ne pouvez pas utiliser l’interface PSI pour créer un projet dans Project Server 2013 ayant un type de projet d’entreprise (TPE) à une définition de flux de travail WF4.
  
Vous pouvez utiliser l’interface PSI pour créer des projets avec TPE qui n’ont aucun flux de travail ou utilise une définition de WF3.5 héritée (la version de flux de travail dans Project Server 2010). Pour créer un projet avec un TPE qui dispose d’une définition de WF4, utilisez le modèle CSOM.
  
 **Actions qui nécessitent de Project Professionnel :**
  
La liste suivante, voici ce que le modèle CSOM ni la PSI.
  
#### <a name="local-data"></a>Données locales

- Manipulation de données dans des projets locaux (fichiers .mpp). Par exemple, définition des tables des taux de coûts ou des profils de disponibilité des ressources locales. 
    
- Définition ou modification des calendriers de base locaux ou les calendriers des ressources, y compris les exceptions de calendrier.
    
- Définition des champs personnalisés locaux. (La PSI ne prend en charge la modification des valeurs de champ personnalisé local sur les tâches, ressources et affectations.)
    
#### <a name="enterprise-data"></a>Données d’entreprise

- Extraction ou de modifier le modèle global d’entreprise. Données globales de l’entreprise dans Project Server 2013 sont un ensemble de tables de données binaires dans la base de données Project, pas un modèle de projet comme dans Office Project Server 2007 et versions antérieures.
    
- Définition ou modification des calendriers d’entreprise. Les méthodes de [calendrier](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx) gérer les exceptions de calendrier uniquement. 
    
#### <a name="master-projects-and-cross-project-links"></a>Projets maîtres et des liaisons entre projets

- Création de projets maîtres et insertion de sous-projets.
    
- Planification d’un chemin critique entre un projet principal. 
    
- Création de liaisons entre projets.
    
#### <a name="resources"></a>Ressources

- Demande ou effectuer l’audit des ressources.
    
- Modification de la ressource sur une affectation. (Vous pouvez utiliser l’interface PSI pour supprimer l’affectation et de créer un nouveau.)
    
- Suppression ou remplacement d’une ressource qui a un travail réel accepté (les chiffres réels).
    
- Modification d’un type de ressource entre le travail, matériel et coût.
    
- Création ou modification des calendriers des ressources.
    
- Lorsque vous ajoutez une ressource à une tâche, la PSI ne redistribue pas automatiquement le fonctionnement Project Professionnel. Il incombe au développeur de choisir et de définir explicitement la répartition du travail sur les affectations.
    
#### <a name="cost-resources"></a>Ressources de coûts

- Modification, création ou la suppression des ressources de coûts et les affectations en utilisant les méthodes de [projet](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx) . Les méthodes de [ressources](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) peuvent créer des ressources de coûts, mais ne peut pas les modifier. 
    
#### <a name="work-contours"></a>Profils de travail

- Modification des données chronologiques.
    
    > [!NOTE]
    > La méthode [UpdateStatus](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.UpdateStatus.aspx) dans le service Web **d’état** peut modifier les chiffres réels de chronologie des affectations une fois que le responsable de projet met à jour et publie les données d’affectation. 
  
- Définition ou modification de l’affectation contour type (par exemple, à deux dimensions, charge croissante ou à charge décroissante).
    
#### <a name="baselines-and-earned-value"></a>Lignes de base et la valeur acquise

- Enregistrement d’une planification ou modification des données de base. 
    
- Si une date d’avancement.
    
- Variation de calcul et la valeur acquise. 
    
#### <a name="interactive-scheduling"></a>Planification interactive

- Prise en charge la planification interactive. (Étant donné que Project Server gère les interactions de manière asynchrone, planification interactive doit être effectuée avec Project Professional.)
    
    > [!NOTE]
    > Pour éviter de modifier le comportement de programmation, les méthodes PSI sont reportés à partir de Project Server 2010 agissent de la même manière dans Project Server 2013. Par exemple, [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) présente les limitations même toujours et utilise le moteur de planification côté serveur plus ancien. La nouvelle méthode [QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) supprime de nombreux de ces restrictions et utilise le nouveau Project Server 2013 côté serveur moteur de planification, qui est le même moteur de planification dans Project Professional 2013. 
  
#### <a name="wbs"></a>WBS

- Définition d’un masque de code de travail breakdown structure (WBS). 
    
#### <a name="tasks"></a>Tâches

- Modification du type de tâche (travail fixe, durée ou les unités).
    
- Modification si une tâche est pilotée par l’effort.
    
- Modifier l’allocation des coûts fixes.
    
- Modification du contenu du champ [TASK_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NOTES.aspx) . L’interface PSI peut lire uniquement une partie du texte des notes de tâche, qui sont des données binaires .rtf. Toutefois, vous pouvez modifier les remarques sur les affectations ( [ASSN_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.AssignmentRow.ASSN_NOTES.aspx) ), qui sont des données de texte. La base de données de création de rapports n’inclut pas les notes de tâche ou une affectation. 
    
- Création ou modification des tâches périodiques.
    
- Attribution ou modification de calendrier des tâches sur les tâches existantes.
    
- Création d’une tâche avec un calendrier des tâches.
    
- Modification de la valeur du champ [TASK_IGNORES_RES_CAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IGNORES_RES_CAL.aspx) (tâche ignore le calendrier des ressources). 
    
- Modification de l’état actif d’une tâche à l’aide de [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) , si des modifications sont effectuées dans le même appel. Pour plus d’informations, voir la section *Planification de projet sur le serveur* de [la programmabilité de Project Server](project-server-programmability.md).
    
#### <a name="summary-tasks"></a>Tâches récapitulatives

- Création ou modification des affectations sur des tâches récapitulatives.
    
    > [!NOTE]
    > Nous vous recommandons de ne pas émettre d’affectations sur des tâches récapitulatives à l’aide de Project Professional ou tout autre moyen. Pour plus d’informations, voir la section *Planification de projet sur le serveur* de [la programmabilité de Project Server](project-server-programmability.md). 
  
- Modification des champs de tâche récapitulative sont reportées normalement à partir de la tâche subordonnée. Projets côté serveur reporter toujours des informations de synthèse, au lieu de la définition des informations sur la tâche récapitulative et leur intégration aux tâches subordonnées. Vous pouvez modifier uniquement les champs suivants sur les tâches récapitulatives :
    
  - Interdépendances des tâches
    
  - Champs personnalisés non-formule
    
  - [TASK_NAME](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NAME.aspx)
    
  - [TASK_OUTLINE_LEVEL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_OUTLINE_LEVEL.aspx)
    
  - [TASK_IS_MARKED](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IS_MARKED.aspx)
    
  - [TASK_CONSTRAINT_TYPE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_CONSTRAINT_TYPE.aspx)
    
  - [TASK_CONSTRAINT_DATE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_CONSTRAINT_DATE.aspx)
    
  - [TASK_PRIORITY](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_PRIORITY.aspx)
    
  - [TASK_DEADLINE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_DEADLINE.aspx)
    
  - [TASK_FIXED_COST](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST.aspx)
    
  - [TASK_FIXED_COST_ACCRUAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST_ACCRUAL.aspx) (la valeur uniquement lors de la création de la tâche) 
    
  - [COLONNES TASK_WBS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_WBS.aspx)
    
Pour la tâche récapitulative du projet, les limitations PSI sont les mêmes que pour Project Professionnel. La PSI peut modifier les attributions de budget, y compris les budgets des coûts.
  
#### <a name="project-level-calculation-options"></a>Options de calcul au niveau du projet

- Modification d’un type de projet entre la planification de démarrer (SFS) et planification de fin doté. (La PSI peut créer un projet sous forme de SFS ou relier, mais une fois créé peut être modifié dans Project Professionnel uniquement.)
    
- Modification du calendrier de base du projet ([CAL_UID](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.CAL_UID.aspx) ) après la création de projet. 
    
- Modification des options pour les calculs. Vous pouvez utiliser l’interface PSI pour définir les options de calcul suivantes lorsque le projet est créé, mais en modifiant les options nécessite Project Professional. (En mode Backstage, choisissez **Options**, puis cliquez sur l’onglet **prévisions** de la boîte de dialogue **Options de projet** .) 
    
  - [PROJ_OPT_CALC_ACT_COSTS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_CALC_ACT_COSTS.aspx)
    
  - [PROJ_OPT_CRITICAL_SLACK_LIMIT](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_CRITICAL_SLACK_LIMIT.aspx)
    
  - [PROJ_OPT_HONOR_CONSTRAINTS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_HONOR_CONSTRAINTS.aspx)
    
  - [PROJ_OPT_MOVE_ACTUAL_IF_LATER](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_ACTUAL_IF_LATER.aspx)
    
  - [PROJ_OPT_MOVE_ACTUAL_TO_STATUS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_ACTUAL_TO_STATUS.aspx)
    
  - [PROJ_OPT_MOVE_REMAINING_IF_EARLIER](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_REMAINING_IF_EARLIER.aspx)
    
  - [PROJ_OPT_MOVE_REMAINING_TO_STATUS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_REMAINING_TO_STATUS.aspx)
    
  - [PROJ_OPT_MULT_CRITICAL_PATHS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MULT_CRITICAL_PATHS.aspx)
    
  - [PROJ_OPT_SPLIT_IN_PROGRESS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_SPLIT_IN_PROGRESS.aspx)
    
  - [PROJ_OPT_SPREAD_ACT_COSTS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_SPREAD_ACT_COSTS.aspx)
    
  - [PROJ_OPT_SPREAD_PCT_COMP](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_SPREAD_PCT_COMP.aspx)
    
  - [PROJ_OPT_TASK_UPDATES_RES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_TASK_UPDATES_RES.aspx)
    
## <a name="see-also"></a>Voir aussi
<a name="pj14_WhatPSIDoes_AR"> </a>

- [Ce que fait le modèle CSOM et ne fait pas](what-the-csom-does-and-does-not-do.md)
    
- [Programmabilité Project Server](project-server-programmability.md)
    
- [Authentification à distance dans SharePoint Online à l’aide de l’authentification basée sur les revendications](http://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx)
    
- [Compléments Office](http://msdn.microsoft.com/library/1e123201-6e70-45c1-a48c-d5b955896ddb%28Office.15%29.aspx)
    

