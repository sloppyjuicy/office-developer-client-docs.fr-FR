---
title: Fonctionnalités de l’interface PSI
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: eac6be6a-9a20-4bc0-8da2-b2fd93aab04f
description: L'interface PSI (Project Server Interface) peut vous aider à automatiser de nombreux processus côté serveur dans les installations locales de Project Server 2013. Toutefois, plusieurs fonctions requièrent l'utilisation de Microsoft Project Professionnel 2013.
ms.openlocfilehash: b93c3535ca6693a84d11370de17bc18375f168ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346528"
---
# <a name="what-the-psi-does-and-does-not-do"></a>Fonctionnalités de l’interface PSI

L'interface PSI (Project Server Interface) peut vous aider à automatiser de nombreux processus côté serveur dans les installations locales de Project Server 2013. Toutefois, plusieurs fonctions requièrent l'utilisation de Microsoft Project Professionnel 2013.
  
|||
|:-----|:-----|
|||
   
Le PSI est conçu pour compléter les fonctionnalités de Project Professional 2013, au lieu de fournir une alternative serveur pour toutes les fonctions Project professionnel. Les développeurs tiers peuvent utiliser le PSI pour créer des composants WebPart pour les installations locales de Project Web App et des espaces de travail de projet, créer des applications Windows personnalisées et des applications Web qui interagissent avec des données Project Server locales, développer un flux de travail logique pour la gestion de portefeuille de projets, développer des gestionnaires d'événements de confiance totale et intégrer Project Server à d'autres applications. Le programme PSI ne peut pas être utilisé pour le développement d'applications pour l'Office Store, les appareils mobiles ou les tablettes; pour cela, vous pouvez utiliser le modèle objet côté client (CSOM).
  
> [!NOTE]
> La PSI fournit une interface de programmation plus complète pour Project Server 2013 que le CSOM fournit. Toutefois, sauf si le CSOM ne fournit pas les fonctionnalités dont vous avez besoin, nous vous recommandons d'utiliser le CSOM pour développer de nouvelles applications. Pour plus d'informations, consultez la rubrique relative à [la fonction CSOM](what-the-csom-does-and-does-not-do.md). 
  
## <a name="usage-scenarios-for-the-psi"></a>Scénarios d'utilisation pour la PSI
<a name="pj14_WhatPSIDoes_UsageScenarios"> </a>

Voici quelques exemples d'applications prises en charge par le programme PSI pour les projets et les calculs côté serveur:
  
- **Automatiser la création ou la gestion des entités dans Project Server** Bien que Project Professional 2013 et Project Web App soient conçus pour gérer la gestion et la création d'entités telles que des projets, des ressources d'entreprise et des champs personnalisés, il existe souvent des situations dans lesquelles une application personnalisée peut gagner du temps en bloc ou tâches répétitives. La PSI peut automatiser plusieurs types de travaux que le CSOM ne fait pas, par exemple, avec les cubes OLAP, les analyses de portefeuille de projets, les axes stratégiques, les notifications, les fournisseurs de liens d'objets, la sécurité et l'interopérabilité SharePoint. 
    
- **Obtenir des données dans les tables publiées ou d'archive de la base de données Project** Étant donné que l'accès direct à la base de données aux tables brouillon, publié et d'archivage n'est pas pris en charge, vous pouvez utiliser le PSI pour lire les données non disponibles dans les tables ou les vues de création de rapports. Par exemple, obtenir des informations sur les versions, les dates et les modifications d'un projet qui sont stockées dans les tables d'archivage, puis remplir un contrôle de Grille JS dans un composant WebPart avec les informations. 
    
- **Valider les données d'État et de feuille de temps** Utilisez la PSI dans les gestionnaires de pré-événements locaux pour valider l'état des affectations ou les données de feuille de temps entrées par les utilisateurs, avant d'enregistrer les données dans Project Web App. 
    
- **Maintenance projects** Create placeholder projects to use with resource plans. Reserve or book time against resources for maintenance work or base business. Maintenance projects generally do not have tasks. 
    
- **Créer des projets financiers** Créez des projets de capture du temps via la feuille de temps pour les intégrer à un système financier. Créez une hiérarchie de codes financiers qui traduit la structure de répartition des coûts du système financier. Les projets financiers ne nécessitent pas de planification ou de mise à jour de statut. 
    
- **Intégration avec les systèmes de comptabilité ** Capturez les coûts de ressources et les frais associés aux projets pour alimenter les systèmes financiers et de facturation, et à des fins de comparaison budgétaire. Synchronize tasks, resources, and assignments between the systems. Capture timesheet data in one system to feed the other (which timesheet is used depends on the needs of the organization or of individual projects). 
    
- **Mises à jour automatiques par les membres de l’équipe** Pour les projets qui ne sont pas gérés activement, mettez-les à jour automatiquement sur le serveur concernant la progression et d’autres modifications apportées par les membres de l’équipe du projet. Les projets peuvent être mis à jour et republiés sans examen des résultats ni ajustements de plan par un responsable de projet. 
    
- **Évaluer les données Project Server dans les gestionnaires d'événements de confiance totale locaux** Un gestionnaire d'événements local pour l'événement préalable **ProjectCreating** peut utiliser des données Project Server à partir de la PSI pour vous aider à déterminer s'il faut annuler un événement. Par exemple, avant de créer un projet, comparez la proposition de projet avec des projets existants. 
    
- **Créer des activités de flux de travail personnalisées pour la gestion de la demande** Utilisez la PSI dans les activités de flux de travail de confiance totale et locale pour modifier et mettre à jour des propositions de projet basées sur des modèles de projet d'entreprise. Utilisez les champs personnalisés de Project pour marquer le projet avec les informations nécessaires au processus d'initiation et d'approbation. Add tasks to identify project phases for key milestones or deliverables. Lorsque des propositions de projet sont approuvées, un flux de travail peut modifier les propositions en projets à pleine envergure qui sont gérés avec Project professionnel. 
    
- **Créer des extensions PSI** (**Déconseillé.** Les extensions sont déconseillées dans Project Server 2013 et ne seront pas prises en charge dans les versions ultérieures.) La PSI peut être étendue avec des services personnalisés à l'aide de l'interface Windows Communication Foundation (WCF). Les extensions PSI s'exécutent sur l'ordinateur Project Server et peuvent utiliser la même infrastructure de sécurité que celle utilisée par les services PSI intégrés. Les extensions peuvent interroger les tables de création de rapports, utiliser des tables de base de données distinctes, consolider les appels PSI pour économiser de la bande passante et s'intégrer avec des applications tierces et d'autres composants côté serveur. Pour plus d'informations, consultez la rubrique [developING PSI extensions](https://msdn.microsoft.com/library/1b484623-94fb-47c9-84c1-3e68a9133042%28Office.15%29.aspx).
    
- **Utiliser l'emprunt d'identité dans les applications locales de confiance totale** Les appels vers l'interface WCF de la PSI peuvent être empruntés, de sorte qu'une application assume les autorisations de sécurité de l'utilisateur emprunté. L'emprunt d'identité doit être utilisé avec parcimonie et avec précaution. La lecture et la mise à jour des informations d'État pour d'autres utilisateurs ne nécessitent pas l'emprunt d'identité. Les nouvelles applications qui requièrent l'emprunt d'identité doivent utiliser le CSOM et le protocole OAuth au lieu de la PSI. Pour plus d'informations sur l'emprunt d'identité avec l'interface PSI, consultez la rubrique [utiliser l'emprunt d'identité avec WCF](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx).
    
> [!NOTE]
> Dans certains cas, la PSI peut être utilisée dans les applications clientes avec le CSOM et Project online. Si vous utilisez un service Web PSI basé sur ASMX, l'application doit inclure une méthode pour authentifier l'objet [Microsoft. ProjectServer. client. ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) dans le CSOM et une méthode pour authentifier le ** Objet client System. Web. services. Protocols. SoapHttpClientProtocol** . Pour obtenir un exemple d'utilisation d'un service Web avec SharePoint CSOM, consultez la rubrique [authentification à distance dans SharePoint Online à l'aide de l'authentification basée sur les revendications](https://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx). > en raison des autorisations au niveau de l'application restreintes, la PSI ne peut pas être utilisée dans les applications qui sont conçues pour être distribuées dans l'Office Store public. Dans ce cas, vous pouvez utiliser uniquement l'CSOM. 
  
## <a name="what-the-psi-does-not-do"></a>Ce que fait la PSI
<a name="pj14_WhatPSIDoes_DoesNotDo"> </a>

Bien qu'il y ait de nombreuses choses que la PSI peut faire, il existe certaines choses que la PSI ne fait pas. Voici deux choses que la PSI ne peut pas faire, mais que le CSOM peut faire.
  
### <a name="project-online-and-remote-event-receivers"></a>Récepteurs d'événements distants et Project Online

La limite principale de la PSI est de Project online. Les applications qui utilisent l'interface PSI nécessitent un accès de confiance totale à une installation locale de Project Server. Par exemple, la PSI ne peut pas être utilisée dans les récepteurs d'événements distants, où le récepteur d'événements est installé en tant que service sur Microsoft Azure.
  
### <a name="workflows-and-claims-authentication"></a>Flux de travail et authentification basée sur les revendications

Une définition de flux de travail qui utilise Windows Workflow Foundation version 4 (WF4) nécessite une authentification basée sur les revendications, que la PSI ne prend pas directement en charge. Cela signifie que vous ne pouvez pas utiliser le PSI pour créer un projet dans Project Server 2013 qui a un type de projet d'entreprise (EPT) avec une définition de flux de travail WF4.
  
Vous pouvez utiliser le PSI pour créer des projets avec TPE qui n'ont pas de flux de travail ou qui utilisent une définition WF 3.5 héritée (la version de flux de travail dans Project Server 2010). Pour créer un projet avec une EPT qui a une définition WF4, utilisez l'CSOM.
  
 **Actions nécessitant Project professionnel:**
  
La liste suivante répertorie les éléments que ni la PSI ni la CSOM ne peut faire.
  
#### <a name="local-data"></a>Données locales

- La manipulation des données dans les projets locaux (fichiers. mpp). Par exemple, la définition des tables des taux de coûts ou des profils de disponibilité pour les ressources locales. 
    
- Définition ou modification des calendriers de base locaux ou des calendriers de ressources, y compris les exceptions de calendrier.
    
- Définition de champs personnalisés locaux. (Le PSI prend en charge la modification des valeurs des champs personnalisés locaux sur les tâches, les ressources et les affectations.)
    
#### <a name="enterprise-data"></a>Données d’entreprise

- Extraction ou modification du modèle global d'entreprise. Les données globales d'entreprise dans Project Server 2013 sont un ensemble de tables de données binaires dans la base de données Project, et non un modèle de projet comme dans Office Project Server 2007 et les versions antérieures.
    
- Définition ou modification des calendriers d'entreprise. Les méthodes de [calendrier](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx) gèrent uniquement les exceptions de calendrier. 
    
#### <a name="master-projects-and-cross-project-links"></a>Projets maîtres et liaisons entre projets

- Création de projets principaux et insertion de sous-projets.
    
- Planification d'un chemin critique sur un projet maître. 
    
- Création de liaisons entre projets.
    
#### <a name="resources"></a>Ressources

- Demande ou exécution de l'audit des ressources.
    
- Modification de la ressource sur une affectation. (Vous pouvez utiliser le PSI pour supprimer l'affectation et en créer une autre.)
    
- Suppression ou remplacement d'une ressource dont le travail réel est accepté (chiffres réels).
    
- Modification d'un type de ressource entre le travail, la matière et le coût.
    
- Création ou modification des calendriers des ressources.
    
- Lors de l'ajout d'une ressource à une tâche, la PSI ne redistribue pas automatiquement le travail de la manière dont Project Professionnel procède. Il revient au développeur de choisir et de définir explicitement la répartition du travail sur les affectations.
    
#### <a name="cost-resources"></a>Ressources de coûts

- Modification, création ou suppression des ressources et des affectations de coûts à l'aide des méthodes de [projet](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx) . Les méthodes de [ressource](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) peuvent créer des ressources de coûts mais ne peuvent pas les modifier. 
    
#### <a name="work-contours"></a>Profils de travail

- Modification des données chronologiques.
    
    > [!NOTE]
    > La méthode [UpdateStatus](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.UpdateStatus.aspx) dans le service Web d' **État** peut modifier les chiffres réels chronologiques des affectations une fois que le responsable de projet a mis à jour et publié les données d'affectation. 
  
- Définition ou modification du type de contour de l'affectation (par exemple, plat, charge croissante ou chargement frontal).
    
#### <a name="baselines-and-earned-value"></a>Planifications et valeur acquise

- Enregistrement d'une ligne de base ou modification des données de planification. 
    
- Définition d'une date d'avancement.
    
- Calcul de l'écart et de la valeur acquise. 
    
#### <a name="interactive-scheduling"></a>Planification interactive

- Prise en charge de la planification interactive. (Dans la mesure où Project Server gère les interactions de manière asynchrone, la planification interactive doit être réalisée avec Project professionnel.)
    
    > [!NOTE]
    > Pour éviter de modifier le comportement par programmation, les méthodes PSI qui sont reportées à partir de Project Server 2010 agissent de la même manière dans Project Server 2013. Par exemple, [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) présente toujours les mêmes limites et utilise l'ancien moteur de planification côté serveur. La nouvelle méthode [QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) supprime un grand nombre de ces limitations et utilise le nouveau moteur de planification côté serveur de project Server 2013, qui est le même moteur de planification que dans project professionnel 2013. 
  
#### <a name="wbs"></a>WBS

- Définition d'un masque de code de structure de répartition du travail (WBS). 
    
#### <a name="tasks"></a>Tâches

- Modification du type de tâche (travail fixe, durée ou unités).
    
- Modification de la façon dont une tâche est pilotée par l'effort.
    
- Modification de la tâche de régularisation des coûts fixes.
    
- Modification du contenu du champ [TASK_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NOTES.aspx) . La PSI ne peut lire que la partie texte des notes de tâche, qui sont des données binaires. rtf. Toutefois, vous pouvez modifier des notes d'affectation ( [ASSN_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.AssignmentRow.ASSN_NOTES.aspx) ), qui sont des données textuelles. La base de données de création de rapports n'inclut pas de remarques sur les tâches ou les affectations. 
    
- Création ou modification de tâches périodiques.
    
- Affectation ou modification du calendrier des tâches sur les tâches existantes.
    
- Création d'une nouvelle tâche avec un calendrier des tâches.
    
- Modification de la valeur du champ [TASK_IGNORES_RES_CAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IGNORES_RES_CAL.aspx) (la tâche ignore le calendrier des ressources). 
    
- Modification de l'état actif d'une tâche à l'aide de [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) , si des modifications supplémentaires sont apportées dans le même appel. Pour plus d'informations, reportez-vous à la section *planification de projet sur le serveur* dans programmabilité de [Project Server](project-server-programmability.md).
    
#### <a name="summary-tasks"></a>Tâches récapitulatives

- Création ou modification des affectations sur les tâches récapitulatives.
    
    > [!NOTE]
    > Nous vous recommandons de ne pas effectuer des affectations sur les tâches récapitulatives à l'aide de Project Professionnel ou de toute autre manière. Pour plus d'informations, reportez-vous à la section *planification de projet sur le serveur* dans programmabilité de [Project Server](project-server-programmability.md). 
  
- Modification des champs de tâche récapitulative qui sont normalement reportés à partir de la sous-tâche. Les projets côté serveur cumulent toujours les informations récapitulatives, au lieu de définir des informations sur la tâche récapitulative et de les pousser vers les tâches subordonnées. Vous pouvez modifier uniquement les champs suivants dans les tâches récapitulatives:
    
  - Interdépendances des tâches
    
  - Champs personnalisés autres que des formules
    
  - [NOM_TÂCHE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NAME.aspx)
    
  - [TASK_OUTLINE_LEVEL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_OUTLINE_LEVEL.aspx)
    
  - [TASK_IS_MARKED](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IS_MARKED.aspx)
    
  - [TASK_CONSTRAINT_TYPE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_CONSTRAINT_TYPE.aspx)
    
  - [TASK_CONSTRAINT_DATE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_CONSTRAINT_DATE.aspx)
    
  - [TASK_PRIORITY](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_PRIORITY.aspx)
    
  - [TASK_DEADLINE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_DEADLINE.aspx)
    
  - [TASK_FIXED_COST](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST.aspx)
    
  - [TASK_FIXED_COST_ACCRUAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST_ACCRUAL.aspx) (définir la valeur uniquement lors de la création de la tâche) 
    
  - [TASK_WBS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_WBS.aspx)
    
Pour la tâche récapitulative du projet, les limitations PSI sont les mêmes que pour Project professionnel. Le PSI peut modifier les affectations budgétaires, y compris les budgets de coûts.
  
#### <a name="project-level-calculation-options"></a>Options de calcul au niveau du projet

- Modification d'un type de projet entre planifier de démarrage (SFS) et planifier à partir de la fin (SFF). (Le PSI peut créer un projet en tant que SFS ou SFF, mais une fois créé, il peut être modifié uniquement dans Project professionnel.)
    
- Modification du calendrier de base de projet ([CAL_UID](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.CAL_UID.aspx) ) après la création du projet. 
    
- Modification des options de calcul. Vous pouvez utiliser le PSI pour définir les options de calcul suivantes lors de la création du projet, mais la modification des options nécessite Project professionnel. (En mode Backstage, choisissez **options**, puis choisissez l'onglet **planification** dans la boîte de dialogue **options de projet** .) 
    
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
    

