---
title: Fonctionnalités de l’interface PSI
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: eac6be6a-9a20-4bc0-8da2-b2fd93aab04f
description: L’interface PSI (Project Server Interface) peut vous aider à automatiser de nombreux processus côté serveur dans les installations sur site de Project Server 2013. Toutefois, plusieurs fonctions nécessitent l’utilisation de Microsoft Project Professional 2013.
ms.openlocfilehash: b93c3535ca6693a84d11370de17bc18375f168ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346528"
---
# <a name="what-the-psi-does-and-does-not-do"></a>Fonctionnalités de l’interface PSI

L’interface PSI (Project Server Interface) peut vous aider à automatiser de nombreux processus côté serveur dans les installations sur site de Project Server 2013. Toutefois, plusieurs fonctions nécessitent l’utilisation de Microsoft Project Professional 2013.
  
|||
|:-----|:-----|
|||
   
L’interface PSI est conçue pour compléter les fonctionnalités de Project Professionnel 2013, au lieu de fournir une alternative basée sur le serveur pour toutes les fonctions Project Professional. Les développeurs tiers peuvent utiliser l’interface PSI pour créer des WebParts pour les installations locales de Project Web App et des espaces de travail de projet, créer des applications Windows personnalisées et des applications web qui interagissent avec les données Project Server locales, développer une logique de flux de travail pour la gestion de portefeuille de projets, développer des gestionnaires d’événements locaux de confiance totale et intégrer Project Server à d’autres applications. L’interface PSI ne peut pas être utilisée pour le développement d’applications pour l’Office Store, les appareils mobiles ou les tablettes . Pour cela, vous pouvez utiliser le modèle objet côté client (CSOM).
  
> [!NOTE]
> L’interface PSI fournit une interface de programmation plus complète pour Project Server 2013 que le CSOM. Toutefois, sauf si le modèle CSOM ne fournit pas les fonctionnalités dont vous avez besoin, nous vous recommandons d’utiliser le modèle CSOM pour développer de nouvelles applications. Pour plus d’informations, voir ce que fait et ne fait pas le [CSOM.](what-the-csom-does-and-does-not-do.md) 
  
## <a name="usage-scenarios-for-the-psi"></a>Scénarios d’utilisation de l’interface PSI
<a name="pj14_WhatPSIDoes_UsageScenarios"> </a>

Voici quelques exemples d’applications que l’interface PSI prend en charge pour les calculs et les projets côté serveur :
  
- **Automatiser la création ou la gestion d’entités dans Project Server** Bien que Project Professionnel 2013 et Project Web App soient conçus ensemble pour gérer et créer des entités telles que des projets, des ressources d’entreprise et des champs personnalisés, il existe souvent des cas où une application personnalisée peut gagner du temps avec des travaux en bloc ou répétitifs. L’interface PSI peut automatiser plusieurs types de travaux que le modèle CSOM ne fait pas, par exemple, avec des cubes OLAP, des analyses de portefeuille de projets, des pilotes d’entreprise, des notifications, des fournisseurs de liens d’objets, la sécurité et l’interopérabilité de SharePoint. 
    
- **Obtenir des données dans les tables publiées ou archivées de la base de données Project** Étant donné que l’accès direct à la base de données aux tables provisoires, publiées et d’archivage n’est pas pris en charge, vous pouvez utiliser l’interface PSI pour lire les données qui ne sont pas disponibles dans les tables ou vues de rapports. Par exemple, obtenez des informations sur les versions, les dates et les modifications du projet qui sont stockées dans les tables d’archivage, puis remplir un contrôle Grille JS dans un élément Web Part avec les informations. 
    
- **Valider les données d’état et de feuille de temps** Utilisez l’interface PSI dans les handlers de pré-événements locaux pour valider l’état d’affectation ou les données de feuille de temps que les utilisateurs entrent, avant que les données ne sont enregistrées dans Project Web App. 
    
- **Maintenance projects** Create placeholder projects to use with resource plans. Reserve or book time against resources for maintenance work or base business. Maintenance projects generally do not have tasks. 
    
- **Créer des projets financiers** Créez des projets de capture du temps via la feuille de temps pour les intégrer à un système financier. Créez une hiérarchie de codes financiers qui traduit la structure de répartition des coûts du système financier. Les projets financiers ne nécessitent pas de planification ou de mise à jour de statut. 
    
- **Intégration avec les systèmes de comptabilité** Capturez les coûts de ressources et les frais associés aux projets pour alimenter les systèmes financiers et de facturation, et à des fins de comparaison budgétaire. Synchronize tasks, resources, and assignments between the systems. Capture timesheet data in one system to feed the other (which timesheet is used depends on the needs of the organization or of individual projects). 
    
- **Mises à jour automatiques par les membres de l’équipe** Pour les projets qui ne sont pas gérés activement, mettez-les à jour automatiquement sur le serveur concernant la progression et d’autres modifications apportées par les membres de l’équipe du projet. Les projets peuvent être mis à jour et republiés sans examen des résultats ni ajustements de plan par un responsable de projet. 
    
- **Évaluer les données Project Server dans les serveurs d’événements de confiance totale locaux** Un responsable d’événements local pour le pré-événement **ProjectCreating** peut utiliser les données Project Server de l’interface PSI pour déterminer s’il faut annuler un événement. Par exemple, avant de créer un projet, comparez la proposition de projet avec des projets existants. 
    
- **Créer des activités de flux de travail personnalisées pour la gestion de la demande** Utilisez l’interface PSI dans les activités de flux de travail de confiance totale locales pour modifier et mettre à jour des propositions de projet basées sur des modèles de projet d’entreprise. Utilisez des champs personnalisés de projet pour marquer le projet avec les informations nécessaires au processus d’initiation et d’approbation. Add tasks to identify project phases for key milestones or deliverables. Lorsque les propositions de projet sont approuvées, un flux de travail peut les transformer en projets à grande échelle gérés avec Project Professionnel. 
    
- **Créer des extensions PSI** **(supprimé.** Les extensions sont dépréciées dans Project Server 2013 et ne seront pas pris en charge dans les prochaines version.) L’interface PSI peut être étendue avec des services personnalisés à l’aide de l’interface Windows Communication Foundation (WCF). Les extensions PSI s’exécutent sur l’ordinateur Project Server et peuvent utiliser la même infrastructure de sécurité que les services PSI intégrés. Les extensions peuvent interroger les tables de rapports, utiliser des tables de base de données distinctes, consolider les appels PSI pour économiser la bande passante et s’intégrer à des applications tierces et à d’autres composants côté serveur. Pour plus d’informations, voir [Développement d’extensions PSI.](https://msdn.microsoft.com/library/1b484623-94fb-47c9-84c1-3e68a9133042%28Office.15%29.aspx)
    
- **Utiliser l’emprunt d’identité dans les applications locales de confiance totale** Les appels à l’interface WCF de l’interface PSI peuvent être emprunts d’identité, de sorte qu’une application assume les autorisations de sécurité de l’utilisateur dont l’identité est usurpée. L’emprunt d’identité doit être utilisé avec parcimonie et précaution. La lecture et la mise à jour des informations d’état pour d’autres utilisateurs ne nécessitent pas l’emprunt d’identité. Les nouvelles applications qui nécessitent l’emprunt d’identité doivent utiliser le CSOM et le protocole OAuth au lieu de l’interface PSI. Pour plus d’informations sur l’emprunt d’identité avec l’interface PSI, voir [Utiliser l’emprunt d’identité avec WCF](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx).
    
> [!NOTE]
> Dans certains cas, l’interface PSI peut être utilisée dans les applications clientes avec le CSOM et Project Online. Si vous utilisez un service web PSI BASÉ sur ASMX, l’application doit inclure une méthode pour authentifier l’objet [Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) dans le CSOM et une méthode pour authentifier l’objet client **System.Web.Services.Protocols.SoapHttpClientProtocol.** Pour obtenir un exemple qui utilise un service web avec le modèle CSOM SharePoint, voir Authentification à distance dans [SharePoint Online](https://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx)à l’aide de l’authentification basée sur les revendications . > en raison des autorisations limitées au niveau de l’application, l’interface PSI ne peut pas être utilisée dans les applications conçues pour la distribution dans l’Office Store public. Dans ce cas, vous pouvez utiliser uniquement le CSOM. 
  
## <a name="what-the-psi-does-not-do"></a>Ce que l’interface PSI ne fait pas
<a name="pj14_WhatPSIDoes_DoesNotDo"> </a>

Bien qu’il existe de nombreuses choses que l’interface PSI peut faire, il existe certaines choses que l’interface PSI ne fait pas. Voici deux choses que l’interface PSI ne peut pas faire, mais le CSOM peut faire.
  
### <a name="project-online-and-remote-event-receivers"></a>Project Online et récepteurs d’événements distants

La limitation principale de l’interface PSI est avec Project Online. Les applications qui utilisent l’interface PSI nécessitent un accès de confiance totale à une installation sur site de Project Server. Par exemple, l’interface PSI ne peut pas être utilisée dans les récepteurs d’événements distants, où le récepteur d’événements est installé en tant que service sur Microsoft Azure.
  
### <a name="workflows-and-claims-authentication"></a>Flux de travail et authentification basée sur les revendications

Une définition de flux de travail qui utilise Windows Workflow Foundation version 4 (WF4) nécessite une authentification basée sur les revendications, que l’interface PSI ne prend pas directement en charge. Cela signifie que vous ne pouvez pas utiliser l’interface PSI pour créer un projet dans Project Server 2013 ayant un type de projet d’entreprise (EPT) avec une définition de flux de travail WF4.
  
Vous pouvez utiliser l’interface PSI pour créer des projets avec des epts qui n’ont pas de flux de travail ou qui utilisent une définition WF3.5 héritée (la version du flux de travail dans Project Server 2010). Pour créer un projet avec un EPT ayant une définition WF4, utilisez le CSOM.
  
 **Actions qui nécessitent Project Professionnel :**
  
La liste suivante est ce que ni l’interface PSI ni le CSOM ne peuvent faire.
  
#### <a name="local-data"></a>Données locales

- Manipulation des données dans les projets locaux (fichiers .mpp). Par exemple, la définition de tables de taux de coûts ou de contours de disponibilité pour les ressources locales. 
    
- Définition ou modification des calendriers de base locaux ou des calendriers de ressources, y compris les exceptions de calendrier.
    
- Définition de champs personnalisés locaux. (L’interface PSI prend en charge la modification des valeurs de champs personnalisés locaux sur les tâches, les ressources et les affectations.)
    
#### <a name="enterprise-data"></a>Données d’entreprise

- Vérification ou modification du modèle global d’entreprise. Les données globales d’entreprise dans Project Server 2013 sont un ensemble de tables de données binaires dans la base de données Project, et non un modèle de projet comme dans Office Project Server 2007 et les versions antérieures.
    
- Définition ou modification des calendriers d’entreprise. Les [méthodes Calendar](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx) gèrent uniquement les exceptions de calendrier. 
    
#### <a name="master-projects-and-cross-project-links"></a>Projets maîtres et liens entre projets

- Création de projets maîtres et insertion de sous-projets.
    
- Planification d’un chemin critique dans un projet maître. 
    
- Création de liens entre projets.
    
#### <a name="resources"></a>Ressources

- Demander ou effectuer un ni deux niveaux de ressources.
    
- Modification de la ressource sur une affectation. (Vous pouvez utiliser l’interface PSI pour supprimer l’affectation et en créer une nouvelle.)
    
- Suppression ou remplacement d’une ressource dont le travail réel est accepté (chiffres réels).
    
- Modification d’un type de ressource entre le travail, le matériel et le coût.
    
- Création ou modification de calendriers de ressources.
    
- Lors de l’ajout d’une ressource à une tâche, l’interface PSI ne redistribue pas automatiquement le travail de la même manière que Project Professional. C’est au développeur de choisir et de définir explicitement la répartition du travail sur les affectations.
    
#### <a name="cost-resources"></a>Ressources de coûts

- Modification, création ou suppression de ressources et d’affectations de coûts à l’aide des [méthodes Project.](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx) Les [méthodes Resource](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) peuvent créer des ressources de coût, mais ne peuvent pas les modifier. 
    
#### <a name="work-contours"></a>Profils de travail

- Modification des données timephased.
    
    > [!NOTE]
    > La [méthode UpdateStatus](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.UpdateStatus.aspx) dans le service **Web** d’état peut modifier les chiffres réels selon le temps sur les affectations une fois que le responsable de projet a mis à jour et publié les données d’affectation. 
  
- Définition ou modification du type de contour d’affectation (par exemple, plat, chargé à l’arrière ou frontal).
    
#### <a name="baselines-and-earned-value"></a>Lignes de base et valeur acquise

- Enregistrement d’une ligne de base ou modification des données de référence. 
    
- Définition d’une date d’avancement.
    
- Calcul de la variance et de la valeur acquise. 
    
#### <a name="interactive-scheduling"></a>Planification interactive

- Prise en charge de la planification interactive. (Étant donné que Project Server gère les interactions de manière asynchrone, la planification interactive doit être effectuée avec Project Professionnel.)
    
    > [!NOTE]
    > Pour éviter de modifier le comportement par programme, les méthodes PSI qui sont présentés à partir de Project Server 2010 agissent de la même manière dans Project Server 2013. Par exemple, [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) présente toujours les mêmes limitations et utilise l’ancien moteur de planification côté serveur. La nouvelle méthode [QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) supprime un grand nombre de ces limitations et utilise le nouveau moteur de planification côté serveur Project Server 2013, qui est le même moteur de planification que dans Project Professionnel 2013. 
  
#### <a name="wbs"></a>WBS

- Définition d’un masque de code de structure de répartition du travail (WBS). 
    
#### <a name="tasks"></a>Tâches

- Modification du type de tâche (travail fixe, durée ou unités).
    
- Déterminer si une tâche est pilotée par l’effort.
    
- Modification de la comptabilité d’exercice des coûts fixes des tâches.
    
- Modification du contenu du [TASK_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NOTES.aspx) champ. L’interface PSI peut lire uniquement la partie texte des notes de tâche, qui sont des données binaires .rtf. Toutefois, vous pouvez modifier les notes [d’affectation (ASSN_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.AssignmentRow.ASSN_NOTES.aspx) ), qui sont des données texte. La base de données de rapports n’inclut pas les notes de tâche ou d’affectation. 
    
- Création ou modification de tâches périodiques.
    
- Affectation ou modification du calendrier des tâches sur les tâches existantes.
    
- Création d’une tâche avec un calendrier des tâches.
    
- Modification de la valeur du [champ TASK_IGNORES_RES_CAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IGNORES_RES_CAL.aspx) (la tâche ignore le calendrier des ressources). 
    
- Modification de l’état actif d’une tâche à l’aide de [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) , si des modifications supplémentaires sont apportées dans le même appel. Pour plus d’informations, voir la section *Planification de projet sur le* serveur dans la [programmabilité de Project Server.](project-server-programmability.md)
    
#### <a name="summary-tasks"></a>Tâches récapitulatives

- Création ou modification d’affectations sur des tâches récapitulatifs.
    
    > [!NOTE]
    > Nous vous recommandons de ne pas effectuer d’affectations sur des tâches récapitulatifs à l’aide de Project Professionnel ou d’une autre façon. Pour plus d’informations, voir la section *Planification de projet sur le* serveur dans la [programmabilité de Project Server.](project-server-programmability.md) 
  
- Modification des champs de tâche récapitulatifs qui sont normalement inscrits à partir de la sous-tâche. Les projets côté serveur relaient toujours des informations récapitulatifs, au lieu de définir des informations sur la tâche récapitulatif et de les faire descendre dans les tâches secondaires. Vous pouvez modifier uniquement les champs suivants sur les tâches récapitulatifs :
    
  - Interdépendances des tâches
    
  - Champs personnalisés non formule
    
  - [TASK_NAME](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NAME.aspx)
    
  - [TASK_OUTLINE_LEVEL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_OUTLINE_LEVEL.aspx)
    
  - [TASK_IS_MARKED](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IS_MARKED.aspx)
    
  - [TASK_CONSTRAINT_TYPE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_CONSTRAINT_TYPE.aspx)
    
  - [TASK_CONSTRAINT_DATE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_CONSTRAINT_DATE.aspx)
    
  - [TASK_PRIORITY](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_PRIORITY.aspx)
    
  - [TASK_DEADLINE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_DEADLINE.aspx)
    
  - [TASK_FIXED_COST](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST.aspx)
    
  - [TASK_FIXED_COST_ACCRUAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST_ACCRUAL.aspx) (définir la valeur uniquement lors de la création de la tâche) 
    
  - [TASK_WBS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_WBS.aspx)
    
Pour la tâche récapitulatif du projet, les limitations PSI sont les mêmes que pour Project Professionnel. L’interface PSI peut modifier les affectations budgétaires, y compris les budgets de coûts.
  
#### <a name="project-level-calculation-options"></a>Options de calcul au niveau du projet

- Modification d’un type de projet entre Planification à partir du début (SFS) et Planification à partir de la fin (SFF). (L’interface PSI peut créer un projet en tant que SFS ou SFF, mais une fois créé, il ne peut être modifié que dans Project Professionnel.)
    
- Modification du calendrier de base[du projet (CAL_UID](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.CAL_UID.aspx) ) après la création du projet. 
    
- Modification des options de calcul. Vous pouvez utiliser l’interface PSI pour définir les options de calcul suivantes lors de la création du projet, mais la modification des options nécessite Project Professionnel. (En affichage Backstage, choisissez **Options,** puis sélectionnez **l’onglet** Planification dans la boîte de dialogue **Options** de projet.) 
    
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

- [Fonctionnalité du modèle CSOM](what-the-csom-does-and-does-not-do.md)  
- [Programmabilité de Project Server](project-server-programmability.md)   
- [Authentification à distance dans SharePoint Online à l’aide de l’authentification basée sur les revendications](https://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx)  
- [Compléments Office](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins) 
    

