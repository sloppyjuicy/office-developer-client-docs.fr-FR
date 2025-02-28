---
title: Codes d’erreur de Project Server
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- error codes
- errors
- Project Server errors
- PSErrorID
- PSI errors
keywords:
- PSI, codes d’erreur, codes d’erreur, Project Server, PSErrorID, interface Project Server, codes d’erreur, Project Server, codes d’erreur
ms.assetid: db78a09c-ebef-47cc-8623-40abe117aa08
description: Cette rubrique présente des tableaux de codes d’erreur pour l’interface Project Server (PSI) dans Project Server 2013. Les tableaux sont organisés par domaine fonctionnel et par plage de codes d’erreur.
ms.localizationpriority: high
ms.openlocfilehash: a46844582254317a61720dcefa583323cb5a7ea7
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62461425"
---
# <a name="project-server-error-codes"></a>Codes d’erreur de Project Server

Cette rubrique présente des tableaux de codes d’erreur pour l’interface Project Server (PSI) dans Project Server 2013. Les tableaux sont organisés par domaine fonctionnel et par plage de codes d’erreur.
   
Les processus Project Server 2013 et les méthodes PSI ont des numéros de code d’erreur qui sont généralement organisés par domaine fonctionnel. L’énumération [Microsoft.Office.Project.Server.Library.PSErrorID](https://msdn.microsoft.com/library/microsoft.office.project.server.library.pserrorid_di_pj14mref(v=office.14).aspx) est dupliquée dans [WebSvcProject.PSErrorID](https://msdn.microsoft.com/library/office/websvcproject.pserrorid_di_pj14mref.aspx) ; elles répertorient les codes d’erreur dans l’ordre alphabétique, par leur nom. Cette rubrique répertorie les codes d’erreur dans des tableaux organisés par classe PSI ou domaine fonctionnel et par numéro d’identification (ID) d’erreur. 
  
> [!NOTE]
>  De nombreux codes d’erreur sont généraux et peuvent avoir plusieurs causes possibles. Pour plus d’informations sur les erreurs, vous pouvez procéder comme suit : 
> - Pour les applications basées sur ASMX, utilisez **System.Web.Services.Protocols.SoapException** avec l’objet **PSClientError** pour afficher la liste ou la hiérarchie des erreurs dans un appel de méthode PSI. Voir [Exemple de code d’erreur pour ASMX](#pj15_ErrorCodes_ASMXExample). 
> - Pour les applications basées sur WCF, vous pouvez utiliser **System.ServiceModel.FaultException** pour obtenir un objet **PSClientError** et pour obtenir des informations supplémentaires sur l’erreur. Voir [Exemple de code d’erreur pour WCF](#pj15_ErrorCodes_WCFExample). 
> - Utilisez le journal des événements d’application sur l’ordinateur Project Server.
> - Utilisez les journaux du suivi du service de journalisation unifiée (ULS). Pour obtenir une explication, reportez-vous à la section relative à la *vérification des erreurs* dans la [prise en main du développement pour Project 2010](https://msdn.microsoft.com/library/gg607685.aspx). 
> - Pour plus d’informations sur l’utilisation des journaux du service ULS, consultez l’article [Project Server 2010 : Que faire face aux événements inattendus](https://blogs.msdn.com/b/brismith/archive/2010/03/24/project-server-2010-what-to-expect-when-you-get-the-unexpected.aspx) sur le blog du support technique de Project et recherchez des informations concernant la lecture des journaux du service ULS sur le blog. 
> - Pour vous aider à rechercher ou examiner des problèmes spécifiques dans les données ULS, utilisez la [visionneuse ULS](https://www.codeproject.com/Articles/458052/ULS-Log-Viewer). 
> - Utilisez Microsoft SQL Server Profiler pour intercepter ou surveiller des erreurs de base de données. Pour plus d’informations, consultez [SQL Server Profiler](https://msdn.microsoft.com/library/3ad5f33d-559e-41a4-bde6-bb98792f7f1a.aspx). 
> - De nombreux codes d’erreur sont utilisés uniquement en interne. Par exemple, les services web **ExchangeSync** et **PWA** n’étant pas pris en charge pour le développement tiers, vous ne verrez probablement pas de codes d’erreur associés aux méthodes dans ces domaines, telles que les méthodes **Rules** et **StatusReports**. Cependant, les tableaux présents dans cet article comprennent tous les codes d’erreur Project Server par souci d’exhaustivité. 
  
## <a name="table-1-error-code-functional-areas-and-related-number-ranges"></a>Tableau 1. Domaines fonctionnels de code d’erreur et plages de numéros associées

|Domaine fonctionnel Project Server|Plage de numéros de codes|
|:-----|:-----|
|[Tableau 3 : Codes d’erreur généraux](#pj15_ErrorCodes_General) <br/> |0 - 99 ; 500 - 999 ; 9131 ; 10000 - 10099 ; 20000 - 20099 ; 26000 - 26099  <br/> |
|[Tableau 4 : Cache actif](#pj15_ErrorCodes_ActiveCache) <br/> |12000 - 12099  <br/> |
|[Tableau 5 : Synchronisation Active Directory](#pj15_ErrorCodes_ActiveDirectory) <br/> |27000 - 27999  <br/> |
|[Tableau 6. Service web d’administration](#pj15_ErrorCodes_Admin) <br/> |16600 - 16699 ; 19011, 19012, et 19032 ; 20003 ; et 25000 - 25099  <br/> |
|[Tableau 7 : Archivage (sauvegarde et restauration)](#pj15_ErrorCodes_Archive) <br/> |25000 - 25999 ; et 29000 - 29099  <br/> |
|[Tableau 8 : Affectations](#pj15_ErrorCodes_Assignments) <br/> |120 - 199  <br/> |
|[Tableau 9 : Calendrier](#pj15_ErrorCodes_Calendar) <br/> |77 ; et 13000 - 13999  <br/> |
|[Tableau 10 : Service de construction du cube (SCC)](#pj15_ErrorCodes_CBS) <br/> |17000 - 17999  <br/> |
|[Tableau 11 : Archivage - extraction](#pj15_ErrorCodes_CICO) <br/> |10100 - 10199  <br/> |
|[Tableau 12 : Champs personnalisés](#pj15_ErrorCodes_CustomFields) <br/> |11500 - 11999  <br/> |
|[Tableau 13 : Tables de choix](#pj15_ErrorCodes_LookupTables) <br/> |11000 - 11499  <br/> |
|[Tableau 14 : Divers](#pj15_ErrorCodes_Miscellaneous) <br/> |11000 - 11499  <br/> |
|[Tableau 15. Notifications](#pj15_ErrorCodes_Notifications) <br/> |16000 - 16599  <br/> |
|[Tableau 16 : Optimiseur](#pj15_ErrorCodes_Optimizer) (analyse de portefeuille de projets)  <br/> |29000 - 29999  <br/> |
|[Tableau 17 : Planificateur](#pj15_ErrorCodes_Planner) (analyse de portefeuille de projets)  <br/> |28000 - 28999  <br/> |
|[Tableau 18 : Projets](#pj15_ErrorCodes_Projects) <br/> |100 - 499 ; 1000 - 1199 ; 9100 - 9199 ; et 23000 - 23999  <br/> |
|[Tableau 19 : Service de données de création de rapports](#pj15_ErrorCodes_RDS) (RDS)  <br/> |24000 - 24999  <br/> |
|[Tableau 20 : Ressources](#pj15_ErrorCodes_Resources) <br/> |2000 - 2999  <br/> |
|[Tableau 21 : Plans de ressources](#pj15_ErrorCodes_ResourcePlans) <br/> |30000 - 30999  <br/> |
|[Tableau 22 : Règles](#pj15_ErrorCodes_Rules) <br/> |21000 - 21099  <br/> |
|[Tableau 23 : Sécurité](#pj15_ErrorCodes_Security) <br/> |19000 - 19099  <br/> |
|[Tableau 24 : Événements du serveur](#pj15_ErrorCodes_Events) <br/> |19033 ; et 22000 - 22999  <br/> |
|[Tableau 25 : Gestion des états](#pj15_ErrorCodes_Statusing) <br/> |3100 - 3199  <br/> |
|[Tableau 26 : Rapports d’état](#pj15_ErrorCodes_StatusReports) <br/> |12100 - 12299  <br/> |
|[Tableau 27 : Tâches](#pj15_ErrorCodes_Tasks) <br/> |7000 - 7099  <br/> |
|[Tableau 28 : Feuilles de temps](#pj15_ErrorCodes_Timesheets) <br/> |3200 – 3299  <br/> |
|[Tableau 29 : Délégation d’utilisateur](#pj15_ErrorCodes_UserDelegation) <br/> |43000 - 43500  <br/> |
|[Tableau 30 : Flux de travail](#pj15_ErrorCodes_Workflow) <br/> |35000 - 35999 : flux de travail  <br/> |
|[Tableau 31 : WSSInterop et ObjectLinkProvider (intégration SharePoint)](#pj15_ErrorCodes_WSS) <br/> |16400 - 16499 : intégration SharePoint et espaces de travail de projet  <br/> 18000 - 18099 : fournisseur de liaison d’objet et importation de projet SharePoint  <br/> |
   
## <a name="table-2-error-code-table-by-number-range"></a>Tableau 2. Tableau de codes d’erreur par plage de numéros

|Plage de codes d’erreur|Tableau de codes d’erreur|
|:-----|:-----|
|0 - 99  <br/> |[Tableau 3 : Codes d’erreur généraux](#pj15_ErrorCodes_General), sauf 77 qui figure dans [Tableau 9 : Calendrier](#pj15_ErrorCodes_Calendar) <br/> |
|100 - 119  <br/> |[Tableau 18 : Projets](#pj15_ErrorCodes_Projects) <br/> |
|120 - 199  <br/> |[Tableau 8 : Affectations](#pj15_ErrorCodes_Assignments) <br/> |
|500 - 999  <br/> |[Tableau 3 : Codes d’erreur généraux](#pj15_ErrorCodes_General) <br/> |
|1000 - 1199  <br/> |[Tableau 18 : Projets](#pj15_ErrorCodes_Projects) <br/> |
|2000 - 2999  <br/> |[Tableau 20 : Ressources](#pj15_ErrorCodes_Resources) <br/> |
|3100 - 3199  <br/> |[Tableau 25 : Gestion des états](#pj15_ErrorCodes_Statusing) <br/> |
|3200 – 3299  <br/> |[Tableau 28 : Feuilles de temps](#pj15_ErrorCodes_Timesheets) <br/> |
|7000 - 7099  <br/> |[Tableau 27 : Tâches](#pj15_ErrorCodes_Tasks) <br/> |
|9100 - 9199  <br/> |[Tableau 18 : Projets](#pj15_ErrorCodes_Projects), sauf 9131 qui figure dans [Tableau 3 : Codes d’erreur généraux](#pj15_ErrorCodes_General) <br/> |
|10000 - 10099  <br/> |[Tableau 3 : Codes d’erreur généraux](#pj15_ErrorCodes_General) <br/> |
|10100 - 10199  <br/> |[Tableau 11 : Archivage - extraction](#pj15_ErrorCodes_CICO) <br/> |
|11000 - 11499  <br/> |[Tableau 13 : Tables de choix](#pj15_ErrorCodes_LookupTables) <br/> |
|11500 - 11999  <br/> |[Tableau 12 : Champs personnalisés](#pj15_ErrorCodes_CustomFields) <br/> |
|12000 - 12099  <br/> |[Tableau 4 : Cache actif](#pj15_ErrorCodes_ActiveCache) <br/> |
|12100 - 12299  <br/> |[Tableau 26 : Rapports d’état](#pj15_ErrorCodes_StatusReports) <br/> |
|13000 - 13999  <br/> |[Tableau 9 : Calendrier](#pj15_ErrorCodes_Calendar) <br/> |
|16000 - 16399  <br/> |[Tableau 15. Notifications](#pj15_ErrorCodes_Notifications) <br/> |
|16400 - 16499  <br/> |[Tableau 31 : WssInterop et ObjectLinkProvider (intégration SharePoint)](#pj15_ErrorCodes_WSS) <br/> |
|16600 - 16699  <br/> |[Tableau 6. Service web d’administration](#pj15_ErrorCodes_Admin) <br/> |
|17000 - 17999  <br/> |[Tableau 10 : Service de construction du cube (SCC)](#pj15_ErrorCodes_CBS) <br/> |
|18000 - 18099  <br/> |[Tableau 31 : Intégration SharePoint](#pj15_ErrorCodes_WSS) <br/> |
|19000 - 19099  <br/> |[Tableau 23 : Sécurité](#pj15_ErrorCodes_Security), sauf 19011, 19012 et 19032 qui sont des codes relatifs à la sécurité figurant dans [Tableau 6 : Service web d’administration](#pj15_ErrorCodes_Admin) <br/> |
|20000 - 20099  <br/> |[Tableau 3 : Codes d’erreur généraux](#pj15_ErrorCodes_General), sauf 20003 qui figure dans [Tableau 6 : Service web d’administration](#pj15_ErrorCodes_Admin) <br/> |
|21000 - 21099  <br/> |[Tableau 22 : Règles](#pj15_ErrorCodes_Rules) <br/> |
|22000 - 22999  <br/> |[Tableau 24 : Événements du serveur](#pj15_ErrorCodes_Events) <br/> |
|23000 - 23999  <br/> |[Tableau 18 : Projets](#pj15_ErrorCodes_Projects) <br/> |
|24000 - 24999  <br/> |[Tableau 19 : Service de données de création de rapports](#pj15_ErrorCodes_RDS) (RDS)  <br/> |
|25000 - 25999  <br/> |[Tableau 7 : Archivage (sauvegarde et restauration)](#pj15_ErrorCodes_Archive), sauf 25004, 25006 qui figurent dans [Tableau 6 : Service web d’administration](#pj15_ErrorCodes_Admin) <br/> |
|26000 - 26099  <br/> |[Tableau 3 : Codes d’erreur généraux](#pj15_ErrorCodes_General) <br/> |
|27000 - 27999  <br/> |[Tableau 5 : Synchronisation Active Directory](#pj15_ErrorCodes_ActiveDirectory) <br/> |
|28000 - 28999  <br/> |[Tableau 17 : Planificateur](#pj15_ErrorCodes_Planner) (analyse de portefeuille de projets)  <br/> |
|29000 - 29999  <br/> |[Tableau 16 : Optimiseur](#pj15_ErrorCodes_Optimizer) (analyse de portefeuille de projets), sauf 29021 qui figure dans [Tableau 7 : Archive](#pj15_ErrorCodes_Archive) <br/> |
|30000 - 30999  <br/> |[Tableau 21 : Plans de ressources](#pj15_ErrorCodes_ResourcePlans) <br/> |
|31000 - 31999  <br/> 32000 - 32100  <br/> |[Tableau 14 : Divers](#pj15_ErrorCodes_Miscellaneous) (Audit ; pas utilisé)  <br/> Pages de détails de projet  <br/> |
|35000 - 35999  <br/> 40000 - 40499  <br/> |[Tableau 30 : Flux de travail](#pj15_ErrorCodes_Workflow) <br/> |
|40500 - 40999  <br/> 42000 - 42999  <br/> |[Tableau 14 : Divers](#pj15_ErrorCodes_Miscellaneous) (**ExchangeSync** ; utilisation interne)  <br/> Chronologie Project Web App  <br/> |
|43000 - 43500  <br/> |[Tableau 29 : Délégation d’utilisateur](#pj15_ErrorCodes_UserDelegation) <br/> |
|50000 - 51999  <br/> |[Tableau 14 : Divers](#pj15_ErrorCodes_Miscellaneous) (erreurs de base de données)  <br/> |

<a name="pj15_ErrorCodes_General"></a>

## <a name="table-3-general-error-codes"></a>Tableau 3 : Codes d’erreur généraux

|Code d’erreur général|Description|
|:-----|:-----|
|NoError = 0 ; Success = 0  <br/> |Aucune erreur ou réussite.  <br/> |
|GeneralRequestInvalidParameter = 6  <br/> |L’un des nœuds ou des paramètres de la demande n’est pas valide ou n’est pas valide dans le contexte de la demande.  <br/> |
|GeneralInvalidValue = 11  <br/> |Valeur de la demande non valide ; par exemple, la valeur 0 pour un GUID.  <br/> |
|GeneralStartDateGTorEQFinishDate = 26  <br/> |Plage de dates spécifiée non valide.  <br/> |
|GeneralQueueOperationInProcess = 29  <br/> |Erreur générique pour une opération en cours de traitement dans la file d’attente.  <br/> |
|GeneralUnhandledException = 42  <br/> |Une exception non gérée s’est produite.  <br/> |
|GeneralDuplicateGUIDSpecified = 66  <br/> |GUID en double dans la demande.  <br/> |
|GeneralDateNotValid = 69  <br/> |Les dates doivent se situer entre le 01/01/1984 et le 12/12/2049.  <br/> |
|GeneralCostInvalid = 70  <br/> |Paramètre de coût non valide.  <br/> |
|GeneralWorkInvalid = 71  <br/> |Paramètre de travail non valide.  <br/> |
|GeneralDurationInvalid = 72  <br/> |Paramètre de durée non valide.  <br/> |
|GeneralUnitsInvalid = 73  <br/> |Unité spécifiée non valide.  <br/> |
|GeneralOnlyInsertsAllowed = 74  <br/> |Seules les insertions sont autorisées.  <br/> |
|GeneralOnlyUpdatesAllowed = 75  <br/> |Seules les mises à jour sont autorisées.  <br/> |
|GeneralSessionInvalid = 76  <br/> |Paramètre de session non valide.  <br/> |
|GeneralDependencyUidInvalid = 78  <br/> |GUID de dépendance non valide.  <br/> |
|GeneralNumberInvalid = 79  <br/> |Nombre non valide.  <br/> |
|GeneralInvalidDataStore = 80  <br/> |La base de données spécifiée n’existe pas. Utiliser une base de données dans [DataStoreEnum](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.DataStoreEnum.aspx).  <br/> |
|GeneralDurationOrWorkFormatInvalid = 513  <br/> |Durée ou format du travail non valide.  <br/> |
|GeneralRateFormatInvalid = 518  <br/> |Format de taux non valide.  <br/> |
|GeneralQueueException = 9131  <br/> |Exception : erreur générale du service de mise en file d’attente.  <br/> |
|GeneralItemDoesNotExist = 10000  <br/> |Un élément spécifié n’existe pas.  <br/> |
|GeneralLCIDInvalid = 10001  <br/> |Identificateur de paramètres régionaux (ID de langue) non valide.  <br/> |
|GeneralRowDoesNotExist = 10002  <br/> |La ligne spécifiée dans un **DataTable** n’existe pas.  <br/> |
|GeneralInvalidColumnValue = 20000  <br/> |Une valeur de colonne dans un **DataTable** n’est pas valide.  <br/> |
|GeneralInvalidDataRowState = 20001  <br/> |Un état **DataRow** n’est pas valide.  <br/> |
|GeneralDuplicatedNames = 20004  <br/> |Nom en double. Les noms doivent être uniques.  <br/> |
|GeneralReadOnlyColumn = 20005  <br/> |La colonne est en lecture seule.  <br/> |
|GeneralReadOnlyRow = 20006  <br/> |La ligne est en lecture seule.  <br/> |
|GeneralNotNullColumn = 20007  <br/> |La colonne ne peut pas être NULL.  <br/> |
|GeneralObjectAlreadyExists = 20008  <br/> |L’objet existe déjà.  <br/> |
|GeneralInvalidObject = 20009  <br/> |Objet non valide.  <br/> |
|GeneralSecurityAccessDenied = 20010  <br/> |Accès refusé en raison d’autorisations de sécurité.  <br/> |
|GeneralInvalidOperation = 20011  <br/> |Opération non valide.  <br/> |
|GeneralInvalidCharacters = 20012  <br/> |Certains caractères ne sont pas valides. La tabulation et les caractères suivants ne sont pas valides dans un nom de projet : `\ / " : ; < > | , . ' ? * #` <br/> |
|GeneralNameTooLong = 20013  <br/> |Le nom est trop long.  <br/> |
|GeneralNameCannotBeBlank = 20014  <br/> |Le nom ne peut pas être vide. N’utilisez pas de chaîne NULL ou vide.  <br/> |
|GeneralInvalidOperationOnReadOnlyValue = 20016  <br/> |Opération non valide tentée sur une valeur en lecture seule.  <br/> |
|GeneralInvalidDateOverlap = 20018  <br/> |La demande contient des dates qui se chevauchent.  <br/> |
|GeneralParameterCannotBeNull = 20020  <br/> |Le paramètre ne peut pas être NULL.  <br/> |
|GeneralDescTooLong = 20021  <br/> |La description est trop longue.  <br/> |
|GeneralCategoryPermissionDenied = 20022  <br/> |Autorisation de catégorie refusée.  <br/> |
|GeneralNotLicensed = 20024  <br/> |L’utilisateur ne dispose pas de licence pour Project Server.  <br/> |
|GeneralGlobalPermissionDenied = 20023  <br/> |Autorisation globale refusée.  <br/> |
|GeneralActionCanceledByEventHandler = 22000  <br/> |Le gestionnaire d’événements a annulé l’opération.  <br/> |
|GeneralActionCanceledBecauseServerEventServiceNotFound = 22001  <br/> |Le service d’événements Project Server est introuvable.  <br/> |
|GeneralActionCanceledBecauseServerEventServiceProblem = 22002  <br/> |Le service d’événements Project Server a rencontré un problème.  <br/> |
|GeneralQueueJobFailed = 26000  <br/> |Échec du travail en file d’attente.  <br/> |
|GeneralQueueInvalidJobUID = 26001  <br/> |GUID de travail non valide pour la file d’attente.  <br/> |
|GeneralQueueInvalidTrackingUID = 26002  <br/> |GUID de suivi non valide pour la file d’attente.  <br/> |
|GeneralQueueInvalidJobInfoUID = 26003  <br/> |GUID d’informations sur le travail non valide pour la file d’attente.  <br/> |
|GeneralQueueInvalidCorrelationUID = 26004  <br/> |GUID de corrélation de file d’attente non valide.  <br/> |
|GeneralQueueCorrelationBlocked = 26005  <br/> |La corrélation de file d’attente est bloquée.  <br/> |
|GeneralQueueInvalidMessageType = 26006  <br/> |Type de message de file d’attente non valide.  <br/> |
|GeneralQueueInvalidJobState = 26007  <br/> |État du travail en file d’attente non valide.  <br/> |
|GeneralQueueInvalidGroupState = 26008  <br/> |État du groupe en file d’attente non valide.  <br/> |
|GeneralQueueInvalidGroupPriority = 26009  <br/> |Priorité du groupe en file d’attente non valide.  <br/> |
|GeneralQueueInvalidCorrelationPriority = 26010  <br/> |Priorité de la corrélation en file d’attente non valide.  <br/> |
|GeneralQueueInvalidQueueID = 26011  <br/> |Numéro d’identification de file d’attente non valide.  <br/> |
|GeneralQueueInvalidAdminAction = 26012  <br/> |L’action **Admin** n’est pas valide pour la file d’attente.  <br/> |
|GeneralQueueInvalidStatType = 26013  <br/> |Type d’état de file d’attente non valide.  <br/> |
|GeneralQueueInvalidBlockPolicy = 26014  <br/> |Stratégie de blocage de file d’attente non valide.  <br/> |
|GeneralQueueCannotRetryJob = 26015  <br/> |La file d’attente ne peut pas recommencer le travail.  <br/> |
|GeneralQueueInvalidSetting = 26016  <br/> |Paramètre non valide pour la file d’attente.  <br/> |
|GeneralQueueInvalidRendezvousUID = 26017  <br/> |GUID Rendezvous de file d’attente non valide.  <br/> |
|GeneralDalErrorGettingConnectionStrings = 26018  <br/> |Erreur lors de l’obtention des chaînes de connexion pour la couche d’accès aux données.  <br/> |
|GeneralDalErrorConnectingToDatabase = 26019  <br/> |Erreur dans la couche d’accès aux données lors de la connexion à la base de données.  <br/> |
|GeneralDalInvalidArgumentCountCreatingFilter = 26020  <br/> |Nombre d’arguments non valide pour la création d’un filtre.  <br/> |
|GeneralDataTableCannotBeNull = 26024  <br/> |Un **DataTable** ne peut pas être **null**.  <br/> |
|GeneralDatasetConstraints = 26025  <br/> |Erreur dans les contraintes **DataSet**.  <br/> |
|GeneralInvalidDataSetStructure = 26027  <br/> |La structure **DataSet** n’est pas valide.  <br/> |
|GeneralDalNoRowsUpdated = 26028  <br/> |Aucune ligne mise à jour dans la couche d’accès aux données.  <br/> |
|GeneralDataTableCannotBeEmpty = 26029  <br/> |La valeur **DataTable** ne peut pas être vide.  <br/> |
|GeneralWSSContentDBNotWritable = 26030  <br/> |Impossible d’écrire dans la base de données de contenu SharePoint. La base de données de contenu est peut-être en lecture seule ou il existe un blocage au niveau de la collection de sites.  <br/> |
|GeneralSPValidateFormDigestError = 26031  <br/> |Erreur lors de la validation de chiffrement de formulaire dans un rappel Project Web App, généralement causée par le dépassement du délai d’attente.  <br/> |
|GeneralDelegationActiveForCurrentUser = 26032  <br/> |L’utilisateur actuel possède une délégation active. Cette erreur est générée par des méthodes web dans le service **WinProj** pour Project Professionnel.<br/> |

<a name="pj15_ErrorCodes_ActiveCache"></a>

## <a name="table-4-active-cache"></a>Tableau 4 : Cache actif

|Code d’erreur relatif au cache actif|Description|
|:-----|:-----|
|ActiveCacheInvalidDataFormat = 12000  <br/> |Format de données non valide.  <br/> |
|ActiveCacheUnsupportedDataFormatVersion = 12001  <br/> |Version du format de données non pris en charge.  <br/> |
|ActiveCacheInvalidQueuedMessageType = 12003  <br/> |Type de message en file d’attente non valide.  <br/> |
|ActiveCacheNullQueuedMessage = 12004  <br/> |Le message en file d’attente est NULL.  <br/> |
|ActiveCacheQueuedMessageExecutionError = 12005  <br/> |Erreur d’exécution pour le message en file d’attente.  <br/> |
|ActiveCacheInvalidDataSize = 12006  <br/> |Taille de données non valide.  <br/> |
|ActiveCacheQueueJobAlreadyStarted = 12007  <br/> |Travail en file d’attente déjà démarré.  <br/> |
|ActiveCacheInvalidQueuedMessageFormat = 12008  <br/> |Format du message dans la file d’attente non valide.  <br/> |
|ActiveCacheUnsupportedQueuedMessageVersion = 12009  <br/> |Version du message dans la file d’attente non valide.  <br/> |
|ActiveCacheUnsupportedQueueDataType = 12011  <br/> |Type de données dans la file d’attente non pris en charge.  <br/> |
|ActiveCacheInvalidVersionStampForSave = 12012  <br/> |Marquage de version pour l’opération d’enregistrement non valide.  <br/> |
|ActiveCacheProjectTypeMismatch = 12013  <br/> |Le type de projet ne correspond pas au type attendu.  <br/> |
|ActiveCacheDataValidationFailed = 12014  <br/> |Échec de la validation des données.  <br/> |
|ActiveCacheUnsupportedProjectProfessionalVersion = 12015  <br/> |Version de Project Professionnal non prise en charge.  <br/> |
|ActiveCacheGeneralSQLException = 12016  <br/> |Il y a une erreur SQL générale.  <br/> |

<a name="pj15_ErrorCodes_ActiveDirectory"></a>

## <a name="table-5-active-directory-synchronization"></a>Tableau 5. Synchronisation Active Directory

|Code d’erreur relatif à la synchronisation Active Directory|Description|
|:-----|:-----|
|AdSyncUpdateTimerJobFailed = 27002  <br/> |Échec de la synchronisation du travail du minuteur de mise à jour avec les services d’annuaire Active Directory.  <br/> |
|AdSyncDeleteTimerJobFailed = 27003  <br/> |Échec de la synchronisation du travail du minuteur de suppression avec Active Directory.  <br/> |
|AdSyncAdConnectFail = 27006  <br/> |Connexion à Active Directory impossible.  <br/> |
|AdMaximumGroupsCountExceeded = 27007  <br/> |Nombre maximal de groupes dépassé.  <br/> |
|SRAInvalidVersion = 27300  <br/> |Version SRA non valide.  <br/> |
|SRADelayedUpgradeFailed = 27301  <br/> |Échec de l’opération de mise à jour asynchrone SRA.  <br/> |
|(27000 - 27999)  <br/> |D’autres erreurs de synchronisation pour Active Directory ne sont pas énumérées dans Project Server.  <br/> |

<a name="pj15_ErrorCodes_Admin"></a>

## <a name="table-6-admin-web-service"></a>Tableau 6. Service web d’administration

|Code d’erreur relatif au service web d’administration|Description|
|:-----|:-----|
|AdminViewNameAlreadyExists = 16600  <br/> |Le nom de vue existe déjà. Les noms doivent être uniques.  <br/> |
|AdminViewInvalidDividerPosition = 16601  <br/> |Position du séparateur non valide.  <br/> |
|AdminViewDataWasTampered = 16602  <br/> |Les données ont été modifiées.  <br/> |
|AdminViewMaxDisplayedFieldsNumberExceeded = 16603  <br/> |L’affichage dépasse le nombre maximal de champs.  <br/> |
|AdminViewCannotDeleteDefaultView = 16604  <br/> |Impossible de supprimer la vue par défaut.  <br/> |
|AdminViewCannotCopyDefaultView = 16605  <br/> |Impossible de copier la vue par défaut.  <br/> |
|AdminLocalCustomFieldInvalid = 19011  <br/> |Champ personnalisé local non valide.  <br/> |
|AdminEnterpriseCustomFieldInvalid = 19012  <br/> |Champ personnalisé d’entreprise non valide.  <br/> |
|AdminNTAccountNotFound = 19032  <br/> |Le compte Windows (NTLM) est introuvable.  <br/> |
|AdminUnableToMerge = 20003  <br/> |Impossible de fusionner les données.  <br/> |
|AdminDeleteArchivedProjectsFailed = 25004  <br/> |Échec de l’opération de suppression pour les projets archivés.  <br/> |
|AdminUpdateArchiveScheduleFailed = 25006  <br/> |Échec de la mise à jour de la planification de l’archivage.  <br/> |
|AdminArchiveScheduleFailed = 28018  <br/> |Échec de la planification de l’archivage.  <br/> |
|AdminReadArchivedProjectsListFailed = 28019  <br/> |Échec de la lecture de la liste des projets archivés.  <br/> |
|AdminReadArchiveScheduleFailed = 28020  <br/> |Échec de la lecture de la planification de l’archivage.  <br/> |
|AdminUserAccountNameNull = 28021  <br/> |Le nom du compte d’utilisateur est NULL.  <br/> |
|AdminIsWindowsUserNull = 28022  <br/> |Le compte d’utilisateur Windows (NTLM) semble être NULL.  <br/> |
|AdminInvalidTimePeriodState = 28023  <br/> |État de la période non valide.  <br/> |
|AdminGlobalUpdateFailed = 28024  <br/> |La mise à jour de l’entreprise globale a échoué durant l’appel à **SetServerCurrency**.  <br/> |
|AdminGlobalCheckedOut = 28025  <br/> |Le modèle global d’entreprise est déjà extrait durant l’appel à **SetServerCurrency**.  <br/> |
|AdminInvalidDatabaseTimeout = 28026  <br/> |Dépassement du délai d’attente causé par une base de données non valide.  <br/> |
|AdminInvalidDatabaseTimeoutType = 28027  <br/> |Dépassement du délai d’attente causé par un type de base de données non valide.  <br/> |
|AdminInvalidEntityType = 28028  <br/> |Le type d’entité n’est pas valide. Voir [EntityCollection](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.EntityCollection.aspx).  <br/> |
|AdminInvalidCompatibilityModeChange = 28029  <br/> |Modification du mode de compatibilité non valide.  <br/> |
|AdminInvalidCompatibilityMode = 28030  <br/> |Mode de compatibilité non valide.  <br/> |
|AdminInvalidProjectProfessionalVersions = 28031  <br/> |Ensemble de versions de Project Professional non valide.  <br/> |
|AdminInvalidProjectProfessionalVersion = 28032  <br/> |Version de Project Professional non valide.  <br/> |
|AdminTooManyProjectProfessionalVersions = 28033  <br/> |Trop de versions de Project Professional sont spécifiées.  <br/> |
|AdminDuplicateProjectProfessionalMajorVersions = 28034  <br/> |Versions principales de Project Professional en double. Vous ne pouvez spécifier qu’une seule version pour chaque version principale, à partir de Project Professional 2007.  <br/> |
|AdminInvalidServerFlags = 28035  <br/> |Un ou plusieurs indicateurs non valides dans les paramètres de Project Server.  <br/> |
|AdminNullProjectProfessionalVersions = 28036  <br/> |Une ou plusieurs versions de Project Professionnel sont null.  <br/> |

<a name="pj15_ErrorCodes_Archive"></a>

## <a name="table-7-archive-web-service"></a>Tableau 7. Service web d’archivage

|Code d’erreur relatif au service web d’archivage (sauvegarde et restauration)|Description|
|:-----|:-----|
|ArchiveProjectFailure = 25000  <br/> |Échec de l’opération d’archivage du projet.  <br/> |
|ArchiveProjectsFailed = 25001  <br/> |Impossible d’enregistrer les projets de la base de données d’archivage.  <br/> |
|ArchiveProjectFailed = 25002  <br/> |Impossible d’enregistrer l’archive du projet.  <br/> |
|RestoreProjectFailed = 25003  <br/> |Impossible de restaurer le projet.  <br/> |
|ArchiveResourcesFailed = 25007  <br/> |Impossible d’enregistrer l’archive des ressources.  <br/> |
|ArchiveCustomFieldsFailed = 25008  <br/> |Impossible d’enregistrer l’archive des champs personnalisés.  <br/> |
|RestoreCustomFieldsFailed = 25009  <br/> |Impossible de restaurer les champs personnalisés.  <br/> |
|ArchiveSystemSettingsFailed = 25010  <br/> |Impossible d’enregistrer l’archive des paramètres système.  <br/> |
|RestoreSystemSettingsFailed = 25011  <br/> |Impossible de restaurer les paramètres système.  <br/> |
|ArchiveCategoriesFailed = 25012  <br/> |Impossible d’enregistrer l’archive des catégories de sécurité.  <br/> |
|RestoreCategoriesFailed = 25013  <br/> |Impossible de restaurer les catégories de sécurité.  <br/> |
|ArchiveViewsFailed = 25014  <br/> |Impossible d’enregistrer l’archive des vues.  <br/> |
|RestoreViewsFailed = 25015  <br/> |Impossible de restaurer les vues.  <br/> |
|ArchiveGlobalProjectFailed = 25016  <br/> |Impossible d’enregistrer l’archive globale d’entreprise.  <br/> |
|RestoreGlobalProjectFailed = 25017  <br/> |Impossible de restaurer le modèle global d’entreprise.  <br/> |
|ArchiveInvalidRetentionPolicyValue = 25018  <br/> |Valeur de stratégie de rétention d’archivage non valide.  <br/> |
|ArchiveCustomFieldsFailure = 25019  <br/> |Impossible de lire l’archive des champs personnalisés.  <br/> |
|ArchiveGlobalProjectFailure = 25020  <br/> |Impossible de lire l’archive globale d’entreprise.  <br/> |
|ArchiveResourcesFailure = 25021  <br/> |Impossible de lire l’archive des ressources.  <br/> |
|ArchiveSystemSettingsFailure = 25022  <br/> |Impossible de lire l’archive des paramètres système.  <br/> |
|ArchiveViewsFailure = 25023  <br/> |Impossible de lire l’archive des vues.  <br/> |
|ArchiveCategoriesFailure = 25024  <br/> |Impossible de lire l’archive des catégories de sécurité.  <br/> |
|ResourcePlanPublishFailure = 25025  <br/> |Impossible de publier le plan de charge des ressources.  <br/> |
|RestoreCategoriesFailure = 25026  <br/> |Impossible de restaurer les catégories de sécurité à partir de l’archive.  <br/> |
|RestoreCustomFieldsFailure = 25027  <br/> |Impossible de restaurer les champs personnalisés à partir de l’archive.  <br/> |
|RestoreGlobalProjectFailure = 25028  <br/> |Impossible de restaurer le modèle global d’entreprise à partir de l’archive.  <br/> |
|RestoreProjectFailure = 25029  <br/> |Impossible de restaurer le projet à partir de l’archive.  <br/> |
|RestoreResourcesFailure = 25030  <br/> |Impossible de restaurer les ressources à partir de l’archive.  <br/> |
|RestoreSystemSettingsFailure = 25031  <br/> |Impossible de restaurer les paramètres système à partir de l’archive.  <br/> |
|RestoreViewsFailure = 25032  <br/> |Impossible de restaurer les vues à partir de l’archive.  <br/> |
|ArchiveReadProjectArchiveRetentionSettingFailed = 25033  <br/> |Impossible de lire les paramètres de rétention d’archivage du projet.  <br/> |
|RestoreResourcesFailed = 29021  <br/> |Impossible de restaurer les ressources.  <br/> |

<a name="pj15_ErrorCodes_Assignments"></a>

## <a name="table-8-assignment"></a>Tableau 8. Affectation

|Code d’erreur d’affectation|Description|
|:-----|:-----|
|AssignmentNotFound = 120  <br/> |Affectation introuvable.  <br/> |
|AssignmentWrongTrackingMethod = 122  <br/> |Méthode de suivi de l’affectation incorrecte.  <br/> |
|AssignmentWorkTypeInvalid = 127  <br/> |Type de travail d’affectation non valide.  <br/> |
|AssignmentRateTableInvalid = 130  <br/> |Table des taux pour l’affectation non valide.  <br/> |
|AssignmentAlreadyExists = 131  <br/> |L’affectation existe déjà.  <br/> |
|AssignmentDuplicateSpecified = 132  <br/> |Affectation en double.  <br/> |
|AssignmentUidInvalid = 133  <br/> |GUID de l’affectation non valide.  <br/> |
|AssignmentDelayInvalid = 134  <br/> |Retard d’affectation non valide.  <br/> |
|AssignmentCannotEditSummaryTask = 135  <br/> |Impossible de modifier une tâche récapitulative pour les affectations.  <br/> |
|AssignmentInvalid = 136  <br/> |Affectation non valide.  <br/> |
|AssignmentFieldsInvalidForBudget = 137  <br/> |Champs d’affectation non valides pour le budget.  <br/> |
|AssignmentAlreadyAssignedToResource = 138  <br/> |La ressource dispose déjà d’une affectation.  <br/> |
|AssignmentInvalidOwner = 139  <br/> |Le propriétaire de l’affectation n’est pas valide.  <br/> |

<a name="pj15_ErrorCodes_Calendar"></a>

## <a name="table-9-calendar"></a>Tableau 9. Calendrier

|Code d’erreur de calendrier|Description|
|:-----|:-----|
|CalendarUidInvalid = 77  <br/> |GUID de calendrier non valide.  <br/> |
|CalendarOnlyOneShiftIsNull = 13000  <br/> |Un seul déplacement est NULL.  <br/> |
|CalendarRecurrenceDaysShouldBeNull = 13001  <br/> |Les jours de périodicité doivent être NULL.  <br/> |
|CalendarRecurrenceMonthDayShouldBeNull = 13002  <br/> |Le jour et le mois de périodicité doivent être NULL.  <br/> |
|CalendarRecurrenceMonthShouldBeNull = 13003  <br/> |Le mois de périodicité doit être NULL.  <br/> |
|CalendarRecurrenceMonthShouldNotBeNull = 13004  <br/> |Le mois de périodicité ne doit pas être NULL.  <br/> |
|CalendarRecurrencePositionShouldBeNull = 13005  <br/> |La position de périodicité doit être NULL.  <br/> |
|CalendarRecurrencePositionShouldNotBeNull = 13006  <br/> |La position de périodicité ne doit pas être NULL.  <br/> |
|CalendarRecurrenceDaysShouldNotBeNull = 13007  <br/> |Les jours de périodicité ne doivent pas être NULL.  <br/> |
|CalendarInvalidRecurrenceFrequency = 13008  <br/> |Fréquence de périodicité non valide.  <br/> |
|CalendarInvalidRecurrenceType = 13009  <br/> |Type de périodicité non valide.  <br/> |
|CalendarInvalidRecurrenceDays = 13010  <br/> |Jours de périodicité non valides.  <br/> |
|CalendarInvalidCombinationOfMonthDayAndPosition = 13011  <br/> |Combinaison du jour, du mois et de la position non valide.  <br/> |
|CalendarInvalidRecurrencePosition = 13012  <br/> |Position de périodicité non valide.  <br/> |
|CalendarCannotModifyExceptionsForCalendarBeingDeleted = 13013  <br/> |Impossible de modifier les exceptions de calendrier lorsqu’un calendrier est en cours de suppression.  <br/> |
|CalendarExceptionConflict = 13014  <br/> |Conflit dans les exceptions de calendrier.  <br/> |
|CalendarBadDateValue = 13015  <br/> |Date non valide.  <br/> |
|CalendarNotFound = 13021  <br/> |Le calendrier est introuvable.  <br/> |
|CalendarAlreadyExists = 13022  <br/> |Le calendrier existe déjà.  <br/> |
|CalendarNameShouldNotBeNull = 13023  <br/> |Le nom du calendrier est NULL.  <br/> |
|CalendarInternalError = 13025  <br/> |Erreur interne dans le fonctionnement du calendrier.  <br/> |
|CalendarNameTooLong = 13027  <br/> |Le nom du calendrier est trop long.  <br/> |
|CalendarInvalidCalendarName = 13028  <br/> |Nom du calendrier non valide.  <br/> |
|CalendarStandardCalendarNotFound = 13031  <br/> |Le calendrier standard est introuvable.  <br/> |
|CalendarInvalidShifts = 13032  <br/> |Déplacements non valides.  <br/> |
|CalendarCannotDeleteCalendarUsedByProject = 13033  <br/> |Impossible de supprimer un calendrier en cours d’utilisation dans un projet.  <br/> |
|CalCalendarUniqueIdToDuplicateShouldBeNull = 13035  <br/> |Le GUID doit être NULL pour dupliquer un calendrier.  <br/> |
|CalendarInvalidBaseCalendarUniqueId = 13037  <br/> |GUID de calendrier de base non valide.  <br/> |
|CalendarInvalidUniqueIdToDuplicate = 13038  <br/> |GUID non valide pour la duplication d’un calendrier.  <br/> |
|CalendarUnusedCalendarException = 13039  <br/> |L’exception de calendrier n’a pas de calendrier correspondant. Cela se produit lorsque la méthode **UpdateResources** est utilisée lorsqu’il existe une entrée dans la table **ResourceDataSet.CalendarExceptions**, mais pas d’élément **BaseCalendarUniqueId** pour cette ressource dans la table **Resources**.<br/> |
|CalendarCannotDeleteStandardCalendar = 13040  <br/> |Impossible de supprimer le calendrier standard.  <br/> |
|CalendarCannotRenameStandardCalendar = 13041  <br/> |Impossible de renommer le calendrier standard.  <br/> |
|CalendarCannotDeleteCalendarUsedByEnterpriseResource = 13042  <br/> |Le calendrier est en cours d’utilisation par une ressource d’entreprise et ne peut pas être supprimé.  <br/> |
|CalendarFilterInvalid = 13043  <br/> |Le filtre n’est pas valide pour un calendrier.  <br/> |

<a name="pj15_ErrorCodes_CBS"></a>

## <a name="table-10-cubeadmin-and-cube-build-service"></a>Tableau 10. CubeAdmin et Service de construction du cube

|Code d’erreur CubeAdmin et Service de construction du cube (SCC)|Description|
|:-----|:-----|
|CBSGeneralFailure = 17001  <br/> |Échec du service de construction du cube (SCC). Il s’agit d’un code d’erreur générale pouvant provenir de plusieurs causes différentes.  <br/> |
|CBSDsoNotInstalled = 17002  <br/> |Le SCC nécessite l’installation du composant Objets d’aide à la prise de décision (DSO) pour Analysis Services.  <br/> |
|CBSASConnectionFailure = 17003  <br/> |Échec de la connexion du SCC au serveur Analysis Services.  <br/> |
|CBSOlapProcessingFailure = 17004  <br/> |Échec du traitement du cube OLAP.  <br/> |
|CBSMetadataProcessingFailure = 17005  <br/> |Échec du traitement des métadonnées de cube.  <br/> |
|CBSASServerLockTimeOut = 17006  <br/> |Le verrouillage du serveur Analysis Services a expiré.  <br/> |
|CBSOlapDatabaseSetupFailure = 17007  <br/> |Échec de la configuration de la base de données du cube OLAP.  <br/> |
|CBSASEntityLimitation = 17008  <br/> |Le nombre d’entités pouvant être utilisées par Analysis Services a été dépassé.  <br/> |
|CBSRequestInvalidArguments = 17009  <br/> |Un ou plusieurs arguments de la demande du SCC ne sont pas valides.  <br/> |
|CBSQueueingRequestFailed = 17010  <br/> |Échec de l’envoi du travail vers la file d’attente par le SCC.  <br/> |
|CBSUpdateCubeCalculatedMeasureDefintionError = 17011  <br/> |Erreur dans un membre calculé du cube.  <br/> |
|CBSAttemptToOverwrite = 17013  <br/> |Impossible de remplacer des données dans le cube.  <br/> |
|CBSCustomFieldCannotBeAddedAsDimension = 17014  <br/> |Le champ personnalisé ne peut pas être une dimension de cube.  <br/> |
|CBSCustomFieldFailedToBeAddedAsDimension = 17015  <br/> |Échec de l’ajout du champ personnalisé en tant que dimension dans le cube.  <br/> |
|CBSCustomFieldCannotBeAddedAsMeasure = 17016  <br/> |Le champ personnalisé ne peut pas être une mesure de cube.  <br/> |
|CBSCustomFieldFailedToBeAddedAsMeasure = 17017  <br/> |Échec de l’ajout du champ personnalisé en tant que mesure dans le cube.  <br/> |
|CBSDsoTranslatorNotFound = 17018  <br/> |Le traducteur d’objets d’aide à la prise de décision est introuvable.  <br/> |
|CBSUpdateOlapDBOperationFailure = 17019  <br/> |Échec de la mise à jour de la base de données OLAP.  <br/> |
|CBSOlapDBInvalidArguments = 17020  <br/> |Un ou plusieurs arguments ne sont pas valides pour la base de données OLAP.  <br/> |
|CBSOlapDatabaseReadSettingListFailed = 17021  <br/> |Échec de la lecture de la liste des paramètres de la base de données OLAP.  <br/> |
|CBSOlapDatabaseReadSettingFailed = 17022  <br/> |Échec de la lecture du paramètre de la base de données OLAP.  <br/> |
|CBSDeleteOlapDatabaseSetting = 17023  <br/> |Erreur lors de la suppression du paramètre de la base de données OLAP.  <br/> |
|CBSSetDefaultOlapDatabase = 17024  <br/> |Erreur lors de la définition de la base de données OLAP par défaut.  <br/> |
|CBSSetOlapDatabaseEnabled = 17025  <br/> |Erreur lors de l’activation de la base de données OLAP.  <br/> |
|CBSGetDefaultOlapDatabase = 17026  <br/> |Erreur lors de l’obtention de la base de données OLAP par défaut.  <br/> |
|CBSCustomFieldFailedToBeAddedAsDimensionOrMeasure = 17027  <br/> |Impossible d’ajouter un champ personnalisé en tant que dimension ou mesure.  <br/> |
|CBSOlapDatabaseAssocFieldsSettings = 17028  <br/> |Erreur dans les paramètres de champs associés à la base de données OLAP.  <br/> |
|CBSUpdateOlapDBOperationDuplicateOrFailure = 17029  <br/> |Échec de l’opération de mise à jour de la base de données OLAP ou opération en double.  <br/> |
|CBSErrorReadingDefaultDatabase = 17030  <br/> |Erreur lors de la lecture de la base de données OLAP par défaut.  <br/> |
|CBSCreateOlapDBOperationFailure = 17031  <br/> |Échec de la création de l’opération de base de données OLAP.  <br/> |
|CBSSetCubeFieldsSettingsFromListForGroupMeasureFailed = 17032  <br/> |Échec de la définition de la liste pour les paramètres de mesure de groupe des champs de cube.  <br/> |
|CBSErrorReadingCubeDepartments = 17033  <br/> |Erreur lors de la lecture des services dans le cube OLAP.  <br/> |
|CBSErrorMaxOlapDatabaseCountReached = 17034  <br/> |Nombre maximal de bases de données OLAP atteint.  <br/> |
|CBSErrorReadingCubeFieldsSettings = 17035  <br/> |Erreur de lecture des paramètres des champs du cube.  <br/> |

<a name="pj15_ErrorCodes_CICO"></a>

## <a name="table-11-check-in-and-check-out"></a>Tableau 11. Archivage et extraction

|Code d’erreur d’archivage - extraction|Description|
|:-----|:-----|
|CICOCheckedOutToOtherUser = 10100  <br/> |Extrait pour un autre utilisateur.  <br/> |
|CICOAlreadyCheckedOutToYou = 10101  <br/> |Déjà extrait pour vous.  <br/> |
|CICONotCheckedOut = 10102  <br/> |Non extrait.  <br/> |
|CICOCheckedOutInOtherSession = 10103  <br/> |Extrait dans une autre session.  <br/> |
|CICOInvalidSessionGuid = 10104  <br/> |GUID de session non valide.  <br/> |
|CICOAlreadyCheckedOutInSameSession = 10105  <br/> |Déjà extrait dans la même session.  <br/> |
|CICOCannotCheckOutVisibilityModeProjectWithMppInDocLib = 10106  <br/> |Impossible d’extraire le projet en mode Visibilité avec un fichier mpp dans la bibliothèque de documents.  <br/> |

<a name="pj15_ErrorCodes_CustomFields"></a>

## <a name="table-12-custom-field"></a>Tableau 12. Champ personnalisé

|Code d’erreur de champ personnalisé|Description|
|:-----|:-----|
|CustomFieldInvalidPropertyType = 11500  <br/> |Type de propriété non valide.  <br/> |
|CustomFieldInvalidScope = 11503  <br/> |Portée du champ personnalisé non valide.  <br/> |
|CustomFieldScopesMustBeIdentical = 11504  <br/> |Les portées doivent être identiques.  <br/> |
|CustomFieldInvalidEntityUID = 11505  <br/> |GUID d’entité de champ personnalisé non valide.  <br/> |
|CustomFieldHasInvalidPropertiesForNonLookupTableCF = 11506  <br/> |Propriétés non valides pour un champ personnalisé sans table de choix.  <br/> |
|CustomFieldNonExistentWeightsTableUID = 11507  <br/> |Le GUID de table de pondérations n’existe pas.  <br/> |
|CustomFieldInvalidName = 11508  <br/> |Nom du champ personnalisé non valide.  <br/> |
|CustomFieldInvalidDefault = 11510  <br/> |Valeur par défaut pour le champ personnalisé non valide.  <br/> |
|CustomFieldInvalidLookupTableUID = 11511  <br/> |GUID de table de choix non valide.  <br/> |
|CustomFieldTypeDoesNotMatchLookupTableMask = 11512.  <br/> |Le type de champ personnalisé ne correspond pas au masque de la table de choix.  <br/> |
|CustomFieldCannotHaveNonLeafNodeDefault = 11513  <br/> |La valeur par défaut du champ personnalisé doit être un nœud terminal.  <br/> |
|CustomFieldMatchingOnlyAvailableForResources = 11514  <br/> |Le champ personnalisé correspondant est disponible uniquement pour les ressources.  <br/> |
|CustomFieldUIDCannotMatchLookupTableUID = 11516  <br/> |Le GUID ne correspond à aucun GUID de table de choix.  <br/> |
|CustomFieldUIDAlreadyExists = 11517  <br/> |Le GUID de champ personnalisé existe déjà.  <br/> |
|CustomFieldIDAlreadyExists = 11518  <br/> |Le numéro d’identification de champ personnalisé existe déjà.  <br/> |
|CustomFieldNameAlreadyExists = 11519  <br/> |Le nom du champ personnalisé existe déjà.  <br/> |
|CustomFieldInvalidEntity = 11520  <br/> |Entité non valide pour le champ personnalisé.  <br/> |
|CustomFieldMaskDoesNotMatchEntityType = 11521  <br/> |Le masque de code ne correspond pas au type d’entité.  <br/> |
|CustomFieldLowerOrderBitsOutOfRange = 11522  <br/> |Les bits les moins significatifs sont en dehors des limites.  <br/> |
|CustomFieldInvalidMaxValues = 11523  <br/> |Une ou plusieurs valeurs maximales ne sont pas valides.  <br/> |
|CustomFieldCannotModifyCertainValuesOnceDefined = 11524  <br/> |Certaines valeurs ne peuvent pas être modifiées une fois qu’elles ont été définies.  <br/> |
|CustomFieldNonExistentPID = 11526  <br/> |Le numéro d’identification de propriété de champ personnalisé n’existe pas.  <br/> |
|CustomFieldCannotChangeBuiltInFields = 11527  <br/> |Impossible de modifier les champs prédéfinis de Project Server, tels que les champs Type de coût, État et RBS.  <br/> |
|CustomFieldSecondaryUidCannotEqualUid = 11528  <br/> |Le GUID secondaire ne peut pas être égal au GUID principal.  <br/> |
|CustomFieldCannotHaveSecondaryUIDorIDForThisEntityType = 11529  <br/> |Le champ personnalisé ne peut pas disposer d’un GUID secondaire ou d’un GUID pour ce type d’entité.  <br/> |
|CustomFieldNameMatchesIntrinsicField = 11530  <br/> |Le nom du champ personnalisé correspond à un champ intrinsèque.  <br/> |
|CustomFieldInvalidAggregationType = 11531  <br/> |Type d’agrégation non valide.  <br/> |
|CustomFieldProjectFormulaFieldsMustUseFormulaAggregation = 11532  <br/> |Les champs de formule du projet doivent utiliser l’agrégation de formule.  <br/> |
|CustomFieldMustSpecifyEitherIDorUID = 11700  <br/> |Le numéro d’identification ou le GUID du champ personnalisé doit être spécifié.  <br/> |
|CustomFieldInvalidID = 11701  <br/> |Numéro d’identification de champ personnalisé non valide.  <br/> |
|CustomFieldInvalidUID = 11702  <br/> |GUID de champ personnalisé non valide.  <br/> |
|CustomFieldInvalidType = 11703  <br/> |Type de champ personnalisé non valide.  <br/> |
|CustomFieldInvalidTypeColumnFilledIn = 11704  <br/> |La valeur de la colonne du type de champ personnalisé n’est pas valide. Voir l’exemple dans [Exemple de code d’erreur pour WCF](#pj15_ErrorCodes_WCFExample).  <br/> |
|CustomFieldCodeValueDoesNotMatchLookupTable = 11706  <br/> |La valeur de code ne correspond pas à la table de choix.  <br/> |
|CustomFieldCodeValueIsNotLeafNode = 11707  <br/> |La valeur de code n’est pas un nœud terminal de la table de choix.  <br/> |
|CustomFieldRowAlreadyExists = 11708  <br/> |La ligne de champ personnalisé existe déjà.  <br/> |
|CustomFieldRowDoesNotMatchCorrespondingDefinitionInDB = 11710  <br/> |La ligne de champ personnalisé ne correspond pas à la définition de la base de données.  <br/> |
|CustomFieldCodeValueAlreadyUsed = 11711  <br/> |La valeur de code est déjà utilisée.  <br/> |
|CustomFieldMaxValuesExceeded = 11712  <br/> |Valeurs maximales des champs personnalisés dépassées.  <br/> |
|CustomFieldRequiredValueNotProvided = 11713  <br/> |Une valeur de champ personnalisé requise n’est pas fournie. Voir l’exemple dans [Exemple de code d’erreur pour WCF](#pj15_ErrorCodes_WCFExample).  <br/> |
|CustomFieldCannotChangeLookupTable = 11715  <br/> |Impossible de modifier la table de choix du champ personnalisé.  <br/> |
|CustomFieldFilterInvalid = 11716  <br/> |Filtre de champ personnalisé non valide.  <br/> |
|CustomFieldRolldownInvalidOnFormulaFields = 11717  <br/> |Impossible de réaliser une généralisation sur un champ personnalisé de formule.  <br/> |
|CustomFieldFormulaFieldCannotBeRequired = 11718  <br/> |Le champ de formule ne peut pas être obligatoire.  <br/> |
|CustomFieldFormulaFieldCannotBeWorkflowControlled = 11719  <br/> |Le champ de formule ne peut pas être contrôlé par un flux de travail.  <br/> |
|CustomFieldCannotSetValueOnFormulaFields = 11720  <br/> |Impossible de définir une valeur sur les champs de formule.  <br/> |
|CustomFieldNewPerRequestLimitExcedeed = 11721  <br/> |Limite de demande dépassée pour les nouveaux champs personnalisés. La limite est [NEW_CF_PER_REQUEST_LIMIT](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.CustomField.NEW_CF_PER_REQUEST_LIMIT.aspx) dans une demande.  <br/> |
|CustomFieldNameIsReservedName = 11722  <br/> |Le nom d’un champ personnalisé ne peut pas être un nom réservé.  <br/> |
|CustomFieldNameInvalidForOlapMeasure = 11723  <br/> |Nom du champ personnalisé non valide pour une mesure de cube OLAP.  <br/> |
|CustomFieldNameInvalidForOlapDimension = 11724  <br/> |Nom du champ personnalisé non valide pour une dimension de cube OLAP.  <br/> |
|CustomFieldSettingsInvalidForOlapMeasure = 11725  <br/> |Paramètres de champ personnalisé non valides pour une mesure de cube OLAP.  <br/> |
|CustomFieldSettingsInvalidForOlapDimension = 11726  <br/> |Paramètres de champ personnalisé non valides pour une dimension de cube OLAP.  <br/> |
|CustomFieldCannotAddRelativeImportanceField = 11727  <br/> |Impossible d’ajouter un champ d’importance relative.  <br/> |
|CustomFieldCannotAddProjectImpactField = 11728  <br/> |Impossible d’ajouter un champ d’impact de projet.  <br/> |
|CustomFieldInvalidDepartmentUid = 11731  <br/> |GUID de service dans le champ personnalisé non valide.  <br/> |
|CustomFieldCannotModifyDepartmentUidOnBuiltinFields = 11732  <br/> |Impossible de modifier le GUID de service pour des champs personnalisés prédéfinis.  <br/> |
|CustomFieldCannotHaveBothLookupTableAndMultilineText = 11733  <br/> |Un champ personnalisé ne peut pas inclure une table de choix et du texte multiligne.  <br/> |
|CustomFieldCannotHaveBothFormulaAndMultilineText = 11734  <br/> |Un champ personnalisé ne peut pas inclure une formule et du texte multiligne.  <br/> |
|CustomFieldDescriptionExceedsLimit = 11735  <br/> |La description du champ personnalisé est trop longue. La longueur maximale de la propriété **MD_PROP_DESCRIPTION** est 1 000 caractères.<br/> |
|CustomFieldOnlyTextFieldsCanHaveMultilineText = 11736  <br/> |Seuls les champs personnalisés de texte peuvent contenir du texte multiligne.  <br/> |
|CustomFieldOnlyProjectFieldsCanHaveMultilineText = 11737  <br/> |Seuls les champs personnalisés de projet peuvent contenir du texte multiligne.  <br/> |
|CustomFieldCannotChangeWorkflowControlledBehaviorForNonProjectCustomFields = 11738  <br/> |Un champ personnalisé ne peut pas modifier le comportement des champs personnalisés hors projet contrôlés par un flux de travail.  <br/> |
|CustomFieldIsWorkflowControlledAndCannotBeChanged = 11739  <br/> |Le champ personnalisé est contrôlé par un flux de travail et ne peut pas être modifié.  <br/> |
|CustomFieldCannotHaveRequiredFlagWhenWorkflowControlledFlagIsSet = 11740  <br/> |Le champ personnalisé ne peut pas être obligatoire lorsqu’il est contrôlé par un flux de travail.  <br/> |
|CustomFieldFormulaCreatesCircularReference = 11742  <br/> |La formule de champ personnalisé crée une référence circulaire.  <br/> |
|CustomFieldFormulaContainsInvalidFieldReference = 11743  <br/> |La formule de champ personnalisé contient une référence de champ qui n’est pas valide.  <br/> |
|CustomFieldFormulaContainsErrors = 11744  <br/> |La formule de champ personnalisé contient une ou plusieurs erreurs.  <br/> |
|CustomFieldLocalCustomFieldNotDefined = 11745  <br/> |Le champ personnalisé local n’est pas défini.  <br/> |
|CustomFieldGraphicalIndicatorContainsErrors = 11746  <br/> |L’indicateur graphique de champ personnalisé contient des erreurs.  <br/> |
|CustomFieldGraphicalIndicatorContainsInvalidFieldReference = 11747  <br/> |L’indicateur graphique de champ personnalisé contient une référence de champ qui n’est pas valide.  <br/> |
|CustomFieldGraphicalIndicatorTypeMismatch = 11748  <br/> |Incompatibilité de type pour l’indicateur graphique de champ personnalisé.  <br/> |
|CustomFieldFormulaFieldCannotReferenceWorkflowControlledField = 11749  <br/> |Un champ de formule ne peut pas faire référence à un champ contrôlé par un flux de travail.  <br/> |
|CustomFieldWorkflowCustomFieldBeingReferencedByFormula = 11750  <br/> |Une formule tente de référencer un champ personnalisé de flux de travail.  <br/> |

<a name="pj15_ErrorCodes_LookupTables"></a>

## <a name="table-13-lookup-table"></a>Tableau 13. Table de choix

|Code d’erreur de table de choix|Description|
|:-----|:-----|
|LookupTableMaskNotDefined = 11000  <br/> |Masque de code de table de choix non défini.  <br/> |
|LookupTableMaskHasTooManyValues = 11001  <br/> |Le masque de code de table de choix contient un trop grand nombre de valeurs.  <br/> |
|LookupTableMaskHasGaps = 11002  <br/> |Le masque de code de table de choix comporte des espaces.  <br/> |
|LookupTableMaskSequenceTypeLimitedToOneLevelDeep = 11003  <br/> |Le type de séquence de masque de code est limité à un seul niveau.  <br/> |
|LookupTableMaskSequenceTypeInvalid = 11004  <br/> |Type de séquence de masque de code non valide.  <br/> |
|LookupTableMaskSequenceRequiresAnyLength = 11005  <br/> |La longueur de la séquence de masque de code doit être _Any_.  <br/> |
|LookupTableMaskSeparatorTooLong = 11006  <br/> |Le séparateur de masque de code comporte un trop grand nombre de caractères.  <br/> |
|LookupTableMaskLevelMustBeBlankAcrossLCIDs = 11007  <br/> |Le niveau du masque de code doit être vide pour les identificateurs de paramètres régionaux (ID de langue).  <br/> |
|LookupTableMaskSeparatorInvalid = 11008  <br/> |Caractère de séparation du masque de code non valide.  <br/> |
|LookupTableMaskBlankSeparatorInvalidAfterAnyLengthSequence = 11009  <br/> |Un caractère de séparation vide n’est pas valide après une longueur de séquence de type _Any_.  <br/> |
|LookupTableMaskSequenceLengthInvalid = 11010  <br/> |Longueur de séquence du masque de code non valide.  <br/> |
|LookupTableMaskLevelMustBeOneOrMore = 11011  <br/> |Le masque de code doit être de niveau 1 ou supérieur.  <br/> |
|LookupTableItemDoesNotFitMask = 11050  <br/> |L’élément de table de choix ne correspond pas à la définition du masque de code.  <br/> |
|LookupTableItemContainsSeparator = 11051  <br/> |L’élément de table de choix contient un caractère de séparation.  <br/> |
|LookupTableItemFullValueTooLong = 11052  <br/> |La valeur complète de l’élément de table de choix est trop longue.  <br/> |
|LookupTableDuplicateSiblingsDisallowed = 11053  <br/> |Les frères en double ne sont pas autorisés dans la table de choix.  <br/> |
|LookupTableSortOrderIndexInvalid = 11054  <br/> |Index d’ordre de tri de la table de choix non valide.  <br/> |
|LookupTableSortOrderIndexDuplicate = 11055  <br/> |Index d’ordre de tri de la table de choix en double.  <br/> |
|LookupTableSortOrderTypeInvalid = 11056  <br/> |Type d’ordre de tri de la table de choix non valide.  <br/> |
|LookupTableSortOrderMustComeAfterParentSortOrder = 11057  <br/> |L’ordre de tri doit passer après l’ordre de tri parent.  <br/> |
|LookupTableSortOrderMustComeBeforeParentNextSiblingSortOrder = 11058  <br/> |L’ordre de tri doit passer avant le parent de l’ordre de tri frère suivant.  <br/> |
|LookupTableInvalidCookieLength = 11060  <br/> |Longueur du cookie pour une table de choix non valide.  <br/> |
|LookupTableMustHaveValuesForPrimaryLCIDorJustOneValue = 11061  <br/> |La table de choix doit comporter des valeurs pour l’identificateur de paramètres régionaux (ID de langue) principal ou une seule valeur. Lorsque vous créez une table de choix multilingue, par exemple, ajoutez une seule valeur de masque pour chaque niveau ou ajoutez d’abord la valeur du LCID principal.  <br/> |
|LookupTableLCIDNotSupportedInLookupTableLanguages = 11062  <br/> |L’identificateur de paramètres régionaux (ID de langue) ne figure pas dans les langues de la table de choix.  <br/> |
|LookupTableInvalidDescriptionLength = 11063  <br/> |Longueur de la description d’un élément de table de choix non valide.  <br/> |
|LookupTableCannotChangeBuiltInTables = 11064  <br/> |Impossible de modifier les tables de choix prédéfinies.  <br/> |
|LookupTableCannotChangeTypeOnceCreated = 11065  <br/> |Impossible de modifier le type de table de choix après sa création.  <br/> |
|LookupTableCannotDeleteLTWithDependantCustomField = 11066  <br/> |Impossible de supprimer une table de choix utilisée dans un champ personnalisé.  <br/> |
|LookupTableAllLevelsNotFilled = 11067  <br/> |Tous les niveaux de table de choix doivent être remplis.  <br/> |
|LookupTableDuplicateName = 11068  <br/> |Les noms de table de choix doivent être uniques.  <br/> |
|LookupTableInvalidName = 11069  <br/> |Nom de la table de choix non valide.  <br/> |
|LookupTableDuplicateSiblingPhoneticsDisallowed = 11071  <br/> |Une table de choix ne peut pas contenir d’éléments phonétiques frères en double.  <br/> |
|LookupTableItemInvalidLookupTable = 11073  <br/> |Élément de la table de choix non valide.  <br/> |
|LookupTableInvalidPhoneticsLength = 11074  <br/> |Longueur du champ phonétique non valide.  <br/> |
|LookupTableAlreadyExists = 11076  <br/> |La table de choix existe déjà.  <br/> |
|LookupTableInvalidUID = 11078  <br/> |GUID de la table de choix non valide.  <br/> |
|LookupTableFilterInvalid = 11079  <br/> |Filtre de la table de choix non valide.  <br/> |
|LookupTableLanguageParameterInvalidWithXmlFilter = 11080  <br/> |Un paramètre de langue n’est pas valide avec le paramètre _xmlFilter_ de la table de choix.  <br/> |
|LookupTableInvalidParentStructUid = 11081  <br/> |GUID d’une structure parent de table de choix non valide.  <br/> |
|LookupTableItemContainsListSeparator = 11082  <br/> |L’élément de table de choix contient un séparateur de listes.  <br/> |
   
Les codes d’erreur du tableau 14 comprennent des éléments relatifs aux erreurs de pages de détails de projet (PDP), de synchronisation Exchange, de chronologie Project Web App et de base de données. De nombreux codes d’erreur divers du tableau 14 sont utilisés en interne.
  
> [!NOTE]
> Les codes d’erreur d’audit ne sont pas utilisés dans Project Server 2013. 

<a name="pj15_ErrorCodes_Miscellaneous"></a>

## <a name="table-14-miscellaneous-error-codes"></a>Tableau 14. Codes d’erreur divers

|Code d’erreur divers|Description|
|:-----|:-----|
|AuditingUpdateFailure = 31000  <br/> |Non utilisé.  <br/> |
|AuditingCannotDeleteFeature = 31001  <br/> |Non utilisé.  <br/> |
|AuditingCannotAddFeature = 31002  <br/> |Non utilisé.  <br/> |
|AuditingFeatureIsNoLongerAudited = 31003  <br/> |Non utilisé.  <br/> |
|AuditingItemIsNotYetAvailable = 31004  <br/> |Non utilisé.  <br/> |
|AuditingInvalidFeatureUid = 31005  <br/> |Non utilisé.  <br/> |
|AuditingInvalidStoreForSelectedFeature = 31006  <br/> |Non utilisé.  <br/> |
|AuditingInvalidStore = 31007  <br/> |Non utilisé.  <br/> |
|AuditingVersionNameTooLong = 31008  <br/> |Non utilisé.  <br/> |
|AuditingBeginVersionFailure = 31009  <br/> |Non utilisé.  <br/> |
|AuditingEndVersionFailure = 31010  <br/> |Non utilisé.  <br/> |
|ProjectDetailPagesStrategicImpactRatingRequired = 32000  <br/> |Une évaluation d’impact stratégique est obligatoire pour la page de détails de projet.  <br/> |
|ProjectDetailPagesMissingPDPLinks = 32001  <br/> |Liens manquants vers les pages de détails de projet.  <br/> |
|ProjectDetailPagesUnavailableWorker = 32002  <br/> |Échec du chargement de l’exploration de projets. Aucun processus de travail n’est disponible.  <br/> |
|ProjectDetailPagesFailedToLoadProjectInWorker = 32003  <br/> |Échec du chargement du processus de travail.  <br/> |
|AppPermissionInvalidAppPermissionId = 32300  <br/> |Problème lié à l’ID d’autorisation de l’application.  <br/> |
|InvariantValidationPSIFailed = 40000  <br/> |Renvoyé par les méthodes **PWA** si des méthodes privées renvoient **ValidationMethodFailed**. Utilisation interne.<br/> |
|ValidationMethodFailed = 40001  <br/> |Renvoyé par les méthodes privées **PWA** lorsqu’elles détectent des incohérences de base de données. Utilisation interne.<br/> |
|GeneralExchangeSyncError = 40500  <br/> |Erreur générale lors de la synchronisation avec Microsoft Exchange. Usage interne.  <br/> |
|ExchangeSyncRootFolderCreationFailed = 40501  <br/> |Échec de la création du dossier racine lors de la synchronisation avec Microsoft Exchange.  <br/> |
|ExchangeSyncTaskFolderCreationFailed = 40502  <br/> |Échec de la création du dossier de tâches.  <br/> |
|ExchangeSyncCouldNotGetRootFolder = 40503  <br/> |Impossible d’obtenir le dossier racine.  <br/> |
|ExchangeSyncCouldNotLoadTaskObject = 40504  <br/> |Impossible de charger l’objet de tâche.  <br/> |
|ExchangeSyncNewExchangeTaskCreationFailed = 40505  <br/> |Échec de la création d’une tâche lors de la synchronisation avec Exchange.  <br/> |
|ExchangeSyncFailedToUpdateCacheForUser = 40506  <br/> |Échec de la mise à jour du cache de synchronisation Exchange pour l’utilisateur.  <br/> |
|ExchangeSyncFailedToUpdateExchangeTask = 40507  <br/> |Échec de la mise à jour de la tâche dans Microsoft Exchange.  <br/> |
|ExchangeSyncSubscriptionUpdateFailed = 40508  <br/> |Échec de la mise à jour de l’abonnement à la synchronisation Exchange.  <br/> |
|ExchangeSyncEWSUrlFailed = 40509  <br/> |Échec de l’URL du service web Microsoft Exchange.  <br/> |
|ExchangeSyncExchangeUrlRefreshFailed = 40510  <br/> |Échec de l’actualisation de l’URL Exchange.  <br/> |
|ExchangeSyncExchangeSubscriptionUpdateForUserFailed = 40511  <br/> |Échec de la mise à jour de l’abonnement Exchange pour l’utilisateur.  <br/> |
|ExchangeSyncGeneralProcessingFailure = 40512  <br/> |Échec de traitement général lors la synchronisation avec Microsoft Exchange.  <br/> |
|ExchangeSyncDeletionOfTasksInExchangeFailure = 40513  <br/> |Échec de la suppression des tâches lors de la synchronisation Exchange.  <br/> |
|ExchangeSyncAttemptedSyncOfInvalidConfiguredResource = 40514  <br/> |Tentative de synchronisation d’une ressource avec une configuration non valide.  <br/> |
|ExchangeSyncRetrievalOfEWSUrlCausedException = 40515  <br/> |Une exception s’est produite lors de la récupération du service web Exchange.  <br/> |
|TimelineViewDataDoesNotExist = 42000  <br/> |Les données n’existent pas pour l’affichage de la chronologie dans Project Web App.  <br/> |
|DatabaseUndefinedError = 50000  <br/> |La base de données n’est pas définie.  <br/> |
|DatabaseCannotInsertDuplicateKeyError = 50001  <br/> |La base de données ne peut pas insérer une clé dupliquée.  <br/> |

<a name="pj15_ErrorCodes_Notifications"></a>

## <a name="table-15-notification"></a>Tableau 15. Notification

|Code d’erreur de notification|Description|
|:-----|:-----|
|NotificationReminderUnknown = 16050  <br/> |Notification de rappel inconnue.  <br/> |
|NotificationReminderParentNotSubscribed = 16051  <br/> |Il n’existe aucun abonnement au parent de la notification de rappel.  <br/> |
|NotificationReminderParentNotFound = 16052  <br/> |Parent de la notification de rappel introuvable.  <br/> |
|NotificationReminderChildStillSubscribed = 16053  <br/> |Il existe encore un abonnement à l’enfant de la notification de rappel.  <br/> |
|NotificationReminderChildNotFound = 16054  <br/> |Enfant de la notification de rappel introuvable.  <br/> |
|NotificationEMailDeliveryFailed = 16080  <br/> |Échec de la remise du message électronique de notification.  <br/> |
|NotificationQueueMessageFailed = 16082  <br/> |Échec du message de file d’attente de notification.  <br/> |
|NotificationXSLTTransformationError = 16084  <br/> |Erreur lors de la transformation XSLT de la notification.  <br/> |
   
Tous les codes d’erreur dans le tableau 16 concernent l’optimiseur, qui est un composant utilisé dans les analyses de portefeuille de projets.

<a name="pj15_ErrorCodes_Optimizer"></a>

## <a name="table-16-optimizer-project-portfolio-analysis"></a>Tableau 16. Optimiseur (analyse de portefeuille de projets)

|Code d’erreur d’optimiseur|Description|
|:-----|:-----|
|OptimizerDepInvalidDepType = 29000  <br/> |La valeur de l’optimiseur **DEPENDENCY_TYPE** dans [OptimizerDependencyDataSet.OptimizerDependenciesRow](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.OptimizerDependencyDataSet.OptimizerDependenciesRow.aspx) n’est pas valide. Voir [Optimizer.DependencyTypes](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.Optimizer.DependencyTypes.aspx).  <br/> |
|OptimizerDepInvalidEntityType = 29001  <br/> |Le type d’entité n’est pas valide. Voir la propriété [Entities](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.EntityCollection.Entities.aspx).  <br/> |
|OptimizerDepInvalidPosition = 29003  <br/> |La valeur [POSITION](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.OptimizerDependencyDataSet.OptimizerDependencyDetailsRow.POSITION.aspx) n’est pas valide.  <br/> |
|OptimizerDepDuplicateDependentProjects = 29004  <br/> |Il y a des projets en double dans [OptimizerDependencyDataSet.OptimizerDependencyDetailsDataTable](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.OptimizerDependencyDataSet.OptimizerDependencyDetailsDataTable.aspx).  <br/> |
|OptimizerDepInvalidDependency = 29005  <br/> |Dépendance de l’optimiseur non valide.  <br/> |
|OptimizerDepCircularDependency = 29006  <br/> |Présence d’une dépendance circulaire.  <br/> |
|OptimizerCannotDeleteDependency = 29007  <br/> |Impossible de supprimer la dépendance.  <br/> |
|OptimizerCannotCreateDependency = 29008  <br/> |Impossible de créer la dépendance.  <br/> |
|OptimizerCannotUpdateDependency = 29009  <br/> |Impossible de mettre à jour la dépendance.  <br/> |
|OptimizerCannotCreateMultipleDependencies = 29010  <br/> |Impossible de créer plusieurs dépendances.  <br/> |
|OptimizerCannotUpdateMultipleDependencies = 29011  <br/> |Impossible de mettre à jour plusieurs dépendances.  <br/> |
|OptimizerEngineMatrixNotFilled = 29100  <br/> |L’optimiseur ne dispose pas de suffisamment de données pour effectuer le calcul.  <br/> |
|OptimizerEngineCustomFieldIsNotAConstraint = 29101  <br/> |Le champ personnalisé n’est pas une contrainte pour l’optimiseur.  <br/> |
|OptimizerCouldNotCalculatePrioritiesFromCustomFields = 29102  <br/> |Impossible de calculer les priorités à partir des champs personnalisés spécifiés.  <br/> |
|OptimizerEngineBinaryInfeasibleSolution = 29103  <br/> |Le calcul de l’optimiseur aboutit à une solution irréalisable.  <br/> |
|OptimizerEngineBinaryNumericalError = 29104  <br/> |Erreur numérique dans le calcul de l’optimiseur.  <br/> |
|OptimizerEngineBinaryTimedOut = 29105  <br/> |Le calcul de l’optimiseur a expiré.  <br/> |
|OptimizerEngineBinaryMaxedIterations = 29106  <br/> |Le calcul de l’optimiseur a atteint le nombre maximal d’itérations.  <br/> |
|OptimizerEngineBinarySubOptimal = 29107  <br/> |Les résultats du calcul de l’optimiseur ne sont pas optimaux.  <br/> |
|OptimizerEngineBinaryInternalError = 29108  <br/> |Erreur interne dans le calcul de l’optimiseur.  <br/> |
|OptimizerInvalidRange = 29200  <br/> |Plage de dates non valide pour l’optimiseur.  <br/> |
|OptimizerNonNormalizedWeights = 29201  <br/> |Les valeurs **WEIGHT** dans [AnalysisDataSet.AnalysisPriorityDataDataTable](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.AnalysisDataSet.AnalysisPriorityDataDataTable.aspx) ne sont pas normalisées.  <br/> |
|OptimizerCannotEditPrioritization = 29300  <br/> |Impossible de modifier la définition des priorités des axes stratégiques.  <br/> |
|OptimizerCannotDeletePrioritization = 29301  <br/> |Impossible de supprimer la définition des priorités des axes stratégiques.  <br/> |
|OptimizerCannotCreatePrioritization = 29302  <br/> |Impossible de créer la définition des priorités des axes stratégiques.  <br/> |
|OptimizerCannotUpdatePrioritization = 29303  <br/> |Impossible de mettre à jour la définition des priorités des axes stratégiques.  <br/> |
|OptimizerCannotCalculateDriverPriorities = 29304  <br/> |Impossible de calculer les priorités des axes stratégiques.  <br/> |
|OptimizerCannotCreateMultiplePrioritizations = 29305  <br/> |Impossible de créer plusieurs définitions des priorités des axes stratégiques.  <br/> |
|OptimizerCannotUpdateMultiplePrioritizations = 29306  <br/> |Impossible de mettre à jour plusieurs définitions des priorités des axes stratégiques.  <br/> |
|OptimizerDriverRelationsNotFilled = 29307  <br/> |Les données de DriverRelationsRow sont incomplètes.  <br/> |
|OptimizerDriversNotFilled = 29308  <br/> |Il n’y a pas suffisamment d’informations dans les axes stratégiques de projet pour trouver une solution.  <br/> |
|OptimizerDriverRelationsInvalidInversedValue = 29309  <br/> |Il y a des valeurs inverses dans [DriverPrioritizationDataSet.DriverRelationsRow](https://msdn.microsoft.com/library/WebSvcDriver.DriverPrioritizationDataSet.DriverRelationsRow.aspx).  <br/> |
|OptimizerCannotCreatePrioritizationUsingInactiveDrivers = 29310  <br/> |Il y a un axe stratégique inactif dans [DriverPrioritizationDataSet.DriverRelationsRow](https://msdn.microsoft.com/library/WebSvcDriver.DriverPrioritizationDataSet.DriverRelationsRow.aspx). Vérifier les propriétés **DRIVER1_UID** et **DRIVER2_UID**.  <br/> |
|OptimizerCannotChangePrioritizationType = 29311  <br/> |Impossible de modifier le type de définition des priorités.  <br/> |
|OptimizerCannotSpecifyPriorityValuesForCalculatedPrioritizations = 29312  <br/> |Si une priorité est calculée, vous ne pouvez pas spécifier la valeur de la priorité.  <br/> |
|OptimizerCannotNormalizePriorityValues = 29313  <br/> |Les valeurs de priorité ne peuvent pas être normalisées.  <br/> |
|OptimizerTooManyDriversInPrioritization = 29314  <br/> |Il existe un trop grand nombre d’axes stratégiques dans la définition des priorités.  <br/> |
|OptimizerInvalidProjectImpactValue = 29400  <br/> |Valeur d’impact de projet non valide.  <br/> |
|OptimizerCannotDeleteDriver = 29401  <br/> |Impossible de supprimer l’axe stratégique de projet.  <br/> |
|OptimizerCannotCreateDriver = 29402  <br/> |Impossible de créer l’axe stratégique de projet.  <br/> |
|OptimizerCannotUpdateDriver = 29403  <br/> |Impossible de mettre à jour l’axe stratégique de projet.  <br/> |
|OptimizerCannotEditDriver = 29404  <br/> |Impossible de modifier l’axe stratégique de projet.  <br/> |
|OptimizerCannotCreateMultipleDrivers = 29405  <br/> |Impossible de créer plusieurs axes stratégiques.  <br/> |
|OptimizerCannotUpdateMultipleDrivers = 29406  <br/> |Impossible de mettre à jour plusieurs axes stratégiques.  <br/> |
|OptimizerInvalidRelativeImportanceValue = 29407  <br/> |Valeur d’importance relative non valide.  <br/> |
|OptimizerInvalidDriverUid = 29500  <br/> |GUID de l’axe stratégique non valide.  <br/> |
|OptimizerInvalidEntityType = 29501  <br/> |Type d’entité non valide pour l’optimiseur.  <br/> |
|OptimizerInvalidProjectUid = 29502  <br/> |GUID de projet non valide.  <br/> |
|OptimizerInvalidCustomFieldUid = 29503  <br/> |GUID de champ personnalisé non valide pour l’optimiseur.  <br/> |
|OptimizerInvalidHardConstraintUid = 29504  <br/> |GUID de contrainte impérative non valide.  <br/> |
|OptimizerInvalidAnalysisUid = 29505  <br/> |GUID d’analyse non valide.  <br/> |
|OptimizerDriverFilterInvalid = 29506  <br/> |Filtre d’axe stratégique non valide.  <br/> |
|OptimizerPrioritizationFilterInvalid = 29507  <br/> |Filtre de définition des priorités non valide.  <br/> |
|OptimizerCannotLoadOptimizationEngine = 29508  <br/> |Impossible de charger le moteur de calcul de l’optimiseur.  <br/> |
|OptimizerAnalysisFilterInvalid = 29509  <br/> |Filtre d’analyse non valide.  <br/> |
|OptimizerSolutionFilterInvalid = 29510  <br/> |Filtre de solution non valide pour l’optimiseur.  <br/> |
|OptimizerDependenciesFilterInvalid = 29511  <br/> |Filtre de dépendances non valide pour l’optimiseur.  <br/> |
|OptimizerInvalidSolutionUid = 29512  <br/> |GUID de solution non valide pour l’optimiseur.  <br/> |
|OptimizerInvalidViewUid = 29513  <br/> |GUID de vue non valide pour l’optimiseur.  <br/> |
|OptimizerInvalidAnalysisType = 29600  <br/> |Type d’analyse de portefeuille non valide.  <br/> |
|OptimizerInvalidPrioritizationType = 29601  <br/> |Type de définition des priorités non valide pour l’optimiseur.  <br/> |
|OptimizerCannotDeleteAnalysis = 29602  <br/> |Impossible de supprimer l’analyse de portefeuille.  <br/> |
|OptimizerCannotCreateAnalysis = 29603  <br/> |Impossible de créer l’analyse de portefeuille.  <br/> |
|OptimizerCannotUpdateAnalysis = 29604  <br/> |Impossible de mettre à jour l’analyse de portefeuille.  <br/> |
|OptimizerInvalidPrioritizationUid = 29607  <br/> |GUID de définition des priorités non valide.  <br/> |
|OptimizerCannotCreateMultipleAnalyses = 29608  <br/> |Impossible de créer plusieurs analyses de portefeuille.  <br/> |
|OptimizerCannotUpdateMultipleAnalyses = 29609  <br/> |Impossible de mettre à jour plusieurs analyses de portefeuille.  <br/> |
|OptimizerCannotCalculateProjectPriorities = 29610  <br/> |L’optimiseur ne peut pas calculer les priorités du projet.  <br/> |
|OptimizerCannotDeleteAnalysisProjectImpact = 29611  <br/> |Impossible de supprimer l’impact de projet dans l’analyse de portefeuille.  <br/> |
|OptimizerCannotChangeAnalysisProjects = 29612  <br/> |Impossible de modifier les projets dans l’analyse de portefeuille.  <br/> |
|OptimizerCannotChangePriorityData = 29613  <br/> |Impossible de modifier les données de priorité.  <br/> |
|OptimizerCannotEditAnalysis = 29614  <br/> |Impossible de modifier l’analyse de portefeuille.  <br/> |
|OptimizerInvalidPlannerData = 29615  <br/> |Données du planificateur non valides pour l’optimiseur.  <br/> |
|OptimizerCannotChangeImpactData = 29616  <br/> |Impossible de modifier les données d’impact de projet.  <br/> |
|OptimizerInvalidProjectsNumber = 29617  <br/> |Nombre de projets non valide.  <br/> |
|OptimizerCannotAddImpactCFUIDToCFAnalysis = 29618  <br/> |Impossible d’ajouter le GUID de champ personnalisé d’impact de projet ([PROJECT_IMPACT_CF_UID](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.AnalysisDataSet.AnalysisRow.PROJECT_IMPACT_CF_UID.aspx)) pour l’analyse de portefeuille.  <br/> |
|OptimizerInvalidDepartmentUid = 29619  <br/> |Le [DEPARTMENT_UID](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.AnalysisDataSet.AnalysisRow.DEPARTMENT_UID.aspx) n’est pas valide.  <br/> |
|OptimizerTooManyProjectsInAnalysis = 29620  <br/> |Trop de projets dans l’analyse.  <br/> |
|QueueAnalysisCannotDeleteAnalysis = 29680  <br/> |La méthode [QueueDeleteAnalyses](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueDeleteAnalyses.aspx) ne peut pas supprimer l’analyse.  <br/> |
|QueueAnalysisCannotCreateAnalysis = 29681  <br/> |La méthode [QueueCreateAnalysis](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueCreateAnalysis.aspx) ne peut pas créer l’analyse.  <br/> |
|QueueAnalysisCannotUpdateAnalysis = 29682  <br/> |La méthode [QueueUpdateAnalysis](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueUpdateAnalysis.aspx) ne peut pas mettre à jour l’analyse.  <br/> |
|AnalysisMismatchedJobList = 29690  <br/> |La liste des tâches d’analyse ne correspond pas.  <br/> |
|OptimizerInvalidForceInLookupTableUid = 29691  <br/> |Impossible d’inclure de force le GUID de la table de choix.  <br/> |
|OptimizerInvalidForceOutLookupTableUid = 29692  <br/> |Impossible d’exclure de force le GUID de la table de choix.  <br/> |
|OptimizerDuplicateForceLookupTableUids = 29693  <br/> |Il existe plusieurs GUID de table de choix forcés en double.  <br/> |
|OptimizerInvalidDecisionResult = 29701  <br/> |Résultat de la décision non valide.  <br/> |
|OptimizerInvalidForcedStatus = 29702  <br/> |État forcé non valide.  <br/> |
|OptimizerCannotDeleteSolution = 29703  <br/> |La méthode [QueueDeleteOptimizerSolutions](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueDeleteOptimizerSolutions.aspx) ne peut pas supprimer la solution de l’optimiseur.  <br/> |
|OptimizerCannotCreateSolution = 29704  <br/> |La méthode [QueueCreateOptimizerSolution](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueCreateOptimizerSolution.aspx) ne peut pas créer la solution de l’optimiseur.  <br/> |
|OptimizerCannotUpdateSolution = 29705  <br/> |La méthode [QueueUpdateAnalysis](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueUpdateAnalysis.aspx) ne peut pas mettre à jour la solution de l’optimiseur.  <br/> |
|OptimizerCannotCalculateSolutionStrategicAlignment = 29706  <br/> |L’optimiseur ne peut pas calculer la solution pour l’alignement stratégique.  <br/> |
|OptimizerCannotCreateMultipleSolutions = 29707  <br/> |L’optimiseur ne peut pas créer plusieurs solutions.  <br/> |
|OptimizerCannotUpdateMultipleSolutions = 29708  <br/> |L’optimiseur ne peut pas mettre à jour plusieurs solutions.  <br/> |
|OptimizerCannotAddPrioritizationToCFAnalysis = 29709  <br/> |L’optimiseur ne peut pas ajouter une définition des priorités à un champ personnalisé pour l’analyse.  <br/> |
|OptimizerTableIsReadOnly = 29710  <br/> |La table de l’optimiseur est en lecture seule.  <br/> |
|OptimizerSolutionCreateMessageFailed = 29711  <br/> |L’optimiseur n’a pas pu générer un message de type : « solution créée ».  <br/> |
|OptimizerSolutionDeleteMessageFailed = 29712  <br/> |L’optimiseur n’a pas pu générer un message de type : « solution supprimée ».  <br/> |
|OptimizerCannotCalculateEfficientFrontier = 29714  <br/> |L’optimiseur ne peut pas calculer la limite efficace pour l’analyse.  <br/> |
|OptimizerCannotUpdateSolutionProperties = 29715  <br/> |Impossible de mettre à jour les propriétés de la solution.  <br/> |
|OptimizerInvalidConstraintPosition = 29716  <br/> |Position de contrainte de l’optimiseur non valide.  <br/> |
|OptimizerInvalidHardConstraintPosition = 29717  <br/> |Position de contrainte impérative de l’optimiseur non valide.  <br/> |
|OptimizerInvalidConstraintLimit = 29718  <br/> |Limite de contrainte de l’optimiseur non valide.  <br/> |
|OptimizerInvalidConstraintValue = 29719  <br/> |Valeur de contrainte non valide.  <br/> |
|OptimizerInvalidSolutionProjectsSet = 29720  <br/> |Ensemble de projets de la solution non valide.  <br/> |
|OptimizerCannotCommitSolution = 29721  <br/> |La méthode [CommitOptimizerSolution](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.CommitOptimizerSolution.aspx) ne peut pas valider la solution.  <br/> |
|OptimizerInvalidInputData = 29723  <br/> |Données d’entrée non valides pour l’optimiseur.  <br/> |
|OptimizerInvalidConstraintSet = 29724  <br/> |Ensemble de contraintes de l’optimiseur non valide.  <br/> |
|OptimizerCannotUpdateAnalysisMetrics = 29725  <br/> |Impossible de mettre à jour les mesures d’analyse.  <br/> |
|OptimizerSolutionMismatchedJobList = 29726  <br/> |La liste des tâches de la solution ne correspond pas.  <br/> |
|OptimizerInvalidForceLookupTableValue = 29727  <br/> |Valeur de table de choix forcée non valide.  <br/> |
|OptimizerCannotCreateSolutionWhileAnalysisUpdateIsPending = 29728  <br/> |Impossible de créer une solution d’optimiseur lorsqu’une mise à jour d’analyse est en attente.  <br/> |
|OptimizerProjectSelectorAtLeastOne = 29800  <br/> |Au moins un projet doit être sélectionné pour l’optimiseur.  <br/> |
   
Les codes d’erreur dans le tableau 17 concernent le planificateur, qui est un composant utilisé dans les analyses de portefeuille de projets.

<a name="pj15_ErrorCodes_Planner"></a>

## <a name="table-17-planner-project-portfolio-analysis"></a>Tableau 17. Planificateur (analyse de portefeuille de projets)

|Code d’erreur du planificateur|Description|
|:-----|:-----|
|PlannerSolutionMessageDeleteFailed = 28000  <br/> |Erreur de file d’attente : échec du message de suppression de la solution du planificateur.  <br/> |
|PlannerSolutionMessageCreateFailed = 28001  <br/> |Erreur de file d’attente : échec du message de création de la solution du planificateur.  <br/> |
|PlannerInvalidRBSValueUid = 28002  <br/> |GUID non valide pour une valeur RBS (Resource Breakdown Structure) dans les données du planificateur.  <br/> |
|PlannerInvalidCustomFieldUid = 28003  <br/> |GUID non valide pour un champ personnalisé.  <br/> |
|PlannerHorizonInvalid = 28004  <br/> |Horizon temporel du planificateur non valide. Un horizon temporel correspond à la période spécifiée pour la planification de la capacité.  <br/> |
|PlannerHorizonTooBig = 28005  <br/> |L’horizon temporel se situe dans un futur trop lointain.  <br/> |
|PlannerInvalidBookingType = 28006  <br/> |Type de réservation des ressources non valide.  <br/> |
|PlannerInvalidTimeScale = 28007  <br/> |Échelle de temps non valide.  <br/> |
|PlannerInvalidProjectSNET = 28008  <br/> |Date de type « début au plus tôt le » non valide pour le projet.  <br/> |
|PlannerInvalidProjectFNLT = 28009  <br/> |Date de type « fin au plus tard le » non valide pour le projet.  <br/> |
|PlannerInvalidAnalysisStartDate = 28010  <br/> |La valeur [START_DATE](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionProjectRequirementsByRoleRow.START_DATE.aspx) pour le projet n’est pas valide.  <br/> |
|PlannerInvalidAnalysisDuration = 28011  <br/> |La valeur [DURATION](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionProjectsRow.DURATION.aspx) n’est pas valide pour l’analyse de portefeuille.  <br/> |
|PlannerInvalidHorizonStartDate = 28012  <br/> |Date de début de l’horizon temporel non valide.  <br/> |
|PlannerInvalidHorizonEndDate = 28013  <br/> |Date de fin de l’horizon temporel non valide.  <br/> |
|PlannerInvalidHorizonTimeScale = 28014  <br/> |Échelle de temps de l’horizon temporel non valide.  <br/> |
|PlannerInvalidAnalysisType = 28015  <br/> |Type d’analyse de portefeuille non valide.  <br/> |
|PlannerHorizonStartDateDoesNotMatchTimeScale = 28016  <br/> |La date de début de l’horizon temporel ne correspond pas à l’échelle de temps.  <br/> |
|PlannerHorizonEndDateDoesNotMatchTimeScale = 28017  <br/> |La date de fin de l’horizon temporel ne correspond pas à l’échelle de temps.  <br/> |
|PlannerAnalysisNoCapacityData = 28037  <br/> |Aucune donnée de capacité de ressources pour l’analyse de portefeuille.  <br/> |
|PlannerInvalidSolutionUid = 28100  <br/> |GUID d’analyse de solution non valide.  <br/> |
|PlannerInvalidOptimizerSolutionUid = 28101  <br/> |GUID de solution de l’optimiseur non valide.  <br/> |
|PlannerInvalidLookupTableValueUid = 28102  <br/> |GUID de valeur de table de choix non valide.  <br/> |
|PlannerInvalidEfficientFrontierUid = 28103  <br/> |La valeur [FRONTIER_UID](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionEfficientFrontierRow.FRONTIER_UID.aspx) n’est pas valide.  <br/> |
|PlannerInvalidProjectUid = 28104  <br/> |GUID de projet non valide.  <br/> |
|PlannerInvalidAllocationThreshold = 28105  <br/> |Seuil de répartition non valide.  <br/> |
|PlannerInvalidHiringType = 28109  <br/> |La valeur [HIRING_TYPE](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.HIRING_TYPE.aspx) n’est pas valide. Voir [Planner.PlannerHiringType](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.Planner.PlannerHiringType.aspx).  <br/> |
|PlannerInvalidConstraintType = 28110  <br/> |La valeur [CONSTRAINT_TYPE](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.CONSTRAINT_TYPE.aspx) n’est pas valide. Voir [Planner.ConstraintType](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.Planner.ConstraintType.aspx).  <br/> |
|PlannerInvalidConstraintValue = 28111  <br/> |La valeur [CONSTRAINT_VALUE](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.CONSTRAINT_VALUE.aspx) n’est pas valide.  <br/> |
|PlannerInvalidRateTable = 28112  <br/> |La valeur [RATE_TABLE](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.RATE_TABLE.aspx) n’est pas valide.  <br/> |
|PlannerInvalidSolutionForConstraint = 28113  <br/> |Solution du planificateur non valide pour la contrainte. Un trop grand nombre de projets sont inclus de force lors du premier passage du planificateur.  <br/> |
|PlannerInvalidSolutionForDependencies = 28114  <br/> |Solution du planificateur non valide. Il existe un trop grand nombre de projets pour pouvoir examiner les dépendances ou conflits stratégiques. Cette erreur se produit lors du deuxième passage.  <br/> |
|PlannerInvalidSolutionForScheduling = 28115  <br/> |Solution du planificateur non valide pour la planification en raison de la présence de dépendances circulaires.  <br/> |
|PlannerInvalidAnalysisUid = 28116  <br/> |La valeur [ANALYSIS_UID](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.ANALYSIS_UID.aspx) n’est pas valide.  <br/> |
|PlannerInvalidProjectStartDate = 28200  <br/> |Date de début du projet non valide.  <br/> |
|PlannerInvalidProjectEndDate = 28201  <br/> |Date de fin du projet non valide.  <br/> |
|PlannerInvalidProjectDuration = 28202  <br/> |Durée du projet non valide.  <br/> |
|PlannerInvalidProjectFNLTDate = 28203  <br/> |Date de type « fin au plus tard le » non valide pour le projet.  <br/> |
|PlannerInvalidProjectSNETDate = 28204  <br/> |Date de type « début au plus tôt le » non valide pour le projet.  <br/> |
|PlannerCannotCreateSolution = 28900  <br/> |Le planificateur ne peut pas créer la solution.  <br/> |
|PlannerCannotUpdateSolution = 28901  <br/> |Le planificateur ne peut pas mettre à jour la solution.  <br/> |
|PlannerCannotDeleteSolution = 28902  <br/> |Le planificateur ne peut pas supprimer la solution.  <br/> |
|PlannerCannotCreateMultipleSolutions = 28903  <br/> |Le planificateur ne peut pas créer plusieurs solutions.  <br/> |
|PlannerCannotUpdateMultipleSolutions = 28904  <br/> |Le planificateur ne peut pas mettre à jour plusieurs solutions.  <br/> |
|PlannerTableIsReadOnly = 28907  <br/> |Le **DataTable** est accessible en lecture seule.  <br/> |
|PlannerCannotCommitSolution = 28908  <br/> |Le planificateur ne peut pas valider la solution dans la base de données.  <br/> |
|PlannerFieldIsReadOnly = 28909  <br/> |Le champ est en lecture seule.  <br/> |
|PlannerProjectNotInParentSolution = 28910  <br/> |Le projet n’est pas dans la solution parent.  <br/> |
|PlannerProjectNotSelectedInParentSolution = 28911  <br/> |Le projet n’est pas sélectionné dans la solution parent.  <br/> |
|PlannerProjectNotInParentAnalysis = 28912  <br/> |Le projet n’est pas dans l’analyse de portefeuille parent.  <br/> |
|PlannerProjectBeyondHorizon = 28913  <br/> |Le projet s’étend au-delà de l’horizon temporel.  <br/> |
|PlannerResourceAllocationInternalError = 28915  <br/> |Erreur interne lors de l’affectation des ressources.  <br/> |
|PlannerResourceAllocationInfeasibleSolution = 28916  <br/> |L’affectation des ressources constitue une solution irréalisable.  <br/> |
|PlannerProjectEndDateViolatesDependency = 28917  <br/> |La date de fin du projet ne respecte pas une dépendance.  <br/> |
|PlannerInvalidProjectsSet = 28919  <br/> |Ensemble de projets non valide.  <br/> |
|PlannerInvalidInputData = 28920  <br/> |Le planificateur comporte des données d’entrée non valides.  <br/> |
|PlannerDecimalOverflowError = 28921  <br/> |Erreur de dépassement décimal dans le planificateur.  <br/> |
|PlannerSolutionMismatchedJobList = 28922  <br/> |La solution comporte une liste de tâches qui ne correspond pas.  <br/> |
|PlannerInvalidForceLookupTableValue = 28923  <br/> |Valeur forcée d’une table de choix non valide.  <br/> |
|PlannerNoHiredResource = 28924  <br/> |Il n’existe aucune ressource embauchée pour la proposition.  <br/> |

<a name="pj15_ErrorCodes_Projects"></a>

## <a name="table-18-project"></a>Tableau 18. Projet

|Code d’erreur de projet|Description|
|:-----|:-----|
|ProjectGlobalNotFound = 100  <br/> |Modèle global d’entreprise introuvable.  <br/> |
|ProjectGlobalCannotBeDeleted = 101  <br/> |Impossible de supprimer le modèle global d’entreprise.  <br/> |
|ProjectNotFound = 1000  <br/> |Projet introuvable.  <br/> |
|ProjectAlreadyExists = 1001  <br/> |Le projet existe déjà.  <br/> |
|ProjectCheckedoutToOtherUser = 1002  <br/> |Le projet est extrait pour un autre utilisateur.  <br/> |
|ProjectTypeInvalidForCreate = 1003  <br/> |Type de projet non valide pour l’opération de création.  <br/> |
|ProjectParametersInvalid = 1004  <br/> |Un ou plusieurs paramètres de projet ne sont pas valides.  <br/> |
|ProjectNotCheckedoutToUser = 1006  <br/> |Projet non extrait pour l’utilisateur.  <br/> |
|ProjectCheckedout = 1007  <br/> |Projet extrait.  <br/> |
|ProjectTypeInvalid = 1008  <br/> |Type de projet non valide.  <br/> |
|ProjectIDInvalid = 1009  <br/> |Numéro d’identification de projet non valide.  <br/> |
|ProjectNameTooLong = 1014  <br/> |Le nom du projet est trop long.  <br/> |
|ProjectManagerNameTooLong = 1015  <br/> |Le nom du responsable de projet est trop long.  <br/> |
|ProjectNameInvalid = 1016  <br/> |Nom du projet non valide.  <br/> |
|ProjectStartDateMissing = 1025  <br/> |Date de début du projet manquante.  <br/> |
|ProjectNameMissing = 1026  <br/> |Nom du projet manquant.  <br/> |
|ProjectVersionMissing = 1027  <br/> |Version du projet manquante.  <br/> |
|ProjectDoesNotExist = 1028  <br/> |Le projet n’existe pas.  <br/> |
|ProjectMultipleProjectsInvalid = 1029  <br/> |Plusieurs projets non valides.  <br/> |
|ProjectHasWriteLock = 1030  <br/> |Le projet comporte un verrou en écriture dans la base de données.  <br/> |
|ProjectHasPendingWriteLock = 1031  <br/> |Le projet comporte un verrou en écriture en attente.  <br/> |
|ProjectHasNoReadLock = 1032  <br/> |Le projet ne comporte pas de verrou en lecture.  <br/> |
|ProjectHasReadLock = 1033  <br/> |Le projet comporte un verrou en lecture.  <br/> |
|ProjectNameAlreadyExists = 1034  <br/> |Le nom du projet existe déjà.  <br/> |
|ProjectOptCriticalSlackLimitInvalid = 1035  <br/> |Limite de marge critique facultative non valide.  <br/> |
|ProjectOptCurrencyPositionInvalid = 1036  <br/> |Position de devise facultative non valide.  <br/> |
|ProjectOptCurrencyDigitsInvalid = 1037  <br/> |Chiffres de la devise facultatifs non valides.  <br/> |
|ProjectOptCurrencySymbolTooLong = 1038  <br/> |Le symbole monétaire facultatif est trop long.  <br/> |
|ProjectCannotDelete = 1039  <br/> |Impossible de supprimer le projet. Seuls les projets côté serveur standard ou de modèle peuvent être supprimés.  <br/> |
|ProjectCannotAdd = 1040  <br/> |Impossible d’utiliser la méthode **AddToProject** sur le projet côté serveur.  <br/> |
|ProjectOptCurrencySymbolInvalid = 1041  <br/> |Symbole monétaire facultatif non valide.  <br/> |
|ProjectHasNoWriteLock = 1042  <br/> |Le projet ne comporte pas de verrou en écriture.  <br/> |
|ProjectFilterInvalid = 1043  <br/> |Filtre de projet non valide.  <br/> |
|ProjectTooLarge = 1044  <br/> |La proposition de projet est trop volumineuse.  <br/> |
|ProjectOptCurrencyCodeNot3Chars = 1045  <br/> |Le code devise facultatif ne comporte pas trois caractères.  <br/> |
|ProjectOptCurrencyCodeInvalid = 1046  <br/> |Code devise non valide dans les options du projet.  <br/> |
|ProjectActualsAreProtected = 1047  <br/> |Les chiffres réels du projet sont protégés.  <br/> |
|ProjectTemplateNotFound = 1048  <br/> |Modèle de projet introuvable.  <br/> |
|ProjectCurrencyCodeInvalid = 1049  <br/> |Code devise non valide.  <br/> |
|ProjectCannotEditCostResource = 1050  <br/> |Impossible de modifier la ressource de type Coût.  <br/> |
|ProjectIsNotPublished = 1051  <br/> |Projet non publié.  <br/> |
|ProjectExceededLWPTaskLimit = 1052  <br/> |Limite de tâche dépassée pour une proposition de projet (projet simplifié).  <br/> |
|ProjectOptFinishDateInvalid = 1053  <br/> |Date de fin non valide dans les options de projet.  <br/> |
|ProjectExceededItemsLimit = 1054  <br/> |La limite d’éléments à traiter a été dépassée. L’application de service Project Server ne peut pas utiliser **ProjectDataSet** pour ajouter ou mettre à jour plus de 1 000 éléments au total dans toutes les tables. Pour traiter plus de 1 000 éléments, utilisez des appels multiples, par exemple, de **QueueUpdateProject**.<br/> |
|ProjectColumnNotReadOnly = 1055  <br/> |La colonne n’est pas en lecture seule.  <br/> |
|ProjectInvalidOwner = 1056  <br/> |Propriétaire du projet non valide.  <br/> |
|ProjectCantEditPctWrkCompForNonWrkRscs = 1057  <br/> |Impossible de modifier **PctWorkComplete** pour une tâche sans aucune affectation de travail réelle.  <br/> |
|ProjectCannotEditMaterialResource = 1058  <br/> |Impossible de modifier la ressource consommable.  <br/> |
|ProjectCannotEditFieldWhenTaskHasNoWorkAssignment = 1059  <br/> |Impossible de modifier le champ, car la tâche n’a aucune affectation de travail.  <br/> |
|ProjectSubProjectNotFound = 1070  <br/> |Aucun sous-projet n’a été trouvé.  <br/> |
|ProjectResourceNotFound = 1100  <br/> |Ressource introuvable.  <br/> |
|ProjectResourceAlreadyExists = 1101  <br/> |La ressource existe déjà.  <br/> |
|ProjectCannotReplaceResourceWithSelf = 1106  <br/> |Impossible de remplacer la ressource avec le même objet.  <br/> |
|ProjectCannotChangeLockedTrackingMethod = 1107  <br/> |Modification impossible, car la méthode de suivi est verrouillée.  <br/> |
|ProjectInvalidColumnForCompatibilityMode = 1108  <br/> |Colonne non valide pour le mode de compatibilité.  <br/> |
|ProjectUpdateInvalidUpdateSequenceNumber = 1151  <br/> |Numéro de séquence non valide dans la mise à jour du projet.  <br/> |
|ProjectUpdateDuplicateUpdateSequenceNumber = 1152  <br/> |Numéro de séquence en double dans la mise à jour du projet.  <br/> |
|ProjectUpdateNullUpdateSequenceNumber = 1153  <br/> |Numéro de séquence NULL dans la mise à jour du projet.  <br/> |
|ProjectUpdateNullUpdateColumnNames = 1154  <br/> |Noms de colonnes NULL dans la mise à jour du projet.  <br/> |
|ProjectUpdateInvalidProjectUID = 1155  <br/> |GUID de projet non valide dans la mise à jour du projet.  <br/> |
|ProjectUpdateInvalidColumnForUpdate = 1156  <br/> |Colonne non valide pour la mise à jour du projet.  <br/> |
|ProjectUpdateCannotEditColumn = 1157  <br/> |Impossible de modifier la colonne dans la mise à jour du projet.  <br/> |
|ProjectUpdateNoChangesToValidateAndSchedule = 1158  <br/> |La mise à jour du projet ne contient aucune modification pouvant être validée et planifiée.  <br/> |
|LinkNotFound = 1159  <br/> |Le lien est introuvable.  <br/> |
|ProjectUpdateInvalidColumnValue = 1160  <br/> |Valeur de colonne non valide dans la mise à jour du projet.  <br/> |
|ProjectCannotDeleteItem = 1161  <br/> |Impossible de supprimer l’élément de projet.  <br/> |
|ProjectUpdateCannotComputeOptIndex = 1162  <br/> |Impossible de calculer l’optimisation de l’index dans la mise à jour du projet.  <br/> |
|ProjectCannotUpdateDueToVisibilityMode = 1163  <br/> |Mise à jour impossible, car le projet est en mode Visibilité.  <br/> |
|ProjectNodeConsistencyException = 9132  <br/> |Exception : le nœud n’est pas cohérent.  <br/> |
|ProjectSchedulingEngineException = 9133  <br/> |Exception dans le moteur de planification.  <br/> |
|ProjectFormulaCalculationException = 9134  <br/> |Exception lors du calcul de la formule.  <br/> |
|ProjectUpdateDatabaseException = 9135  <br/> |Exception lors de la mise à jour de la base de données.  <br/> |
|ProjectDeleteException = 9136  <br/> |Exception lors de la suppression du projet.  <br/> |
|ProjectOperationException = 9137  <br/> |Exception dans une opération de projet.  <br/> |
|ProjectCannotComunicateWithPCS = 9138  <br/> |Échec de la communication avec le processus de travail PCS.  <br/> |
|ProjectPCSSessionInvalid = 9139  <br/> |Échec de l’ouverture du projet dans une session de moteur.  <br/> |
|ProjectPublishFailure = 23000  <br/> |Échec dans la file d’attente lors de la publication du projet.  <br/> |
|ProjectCurrencyConflict = 23001  <br/> |Conflit dans la devise spécifiée.  <br/> |
|ProjectPublishFailed = 23002  <br/> |Échec de la publication du projet lors de la mise en file d’attente.  <br/> |
|ProjectReversePublishFailed = 23003  <br/> |Échec de l’opération de publication du projet lors de la mise en file d’attente.  <br/> |
|ProjectReversePublishFailure = 23004  <br/> |Échec de l’annulation de la publication du projet lors du traitement de la file d’attente.  <br/> |
|ProjectArchiveRetentionDeleteFailure = 23005  <br/> |Échec de la suppression du projet en raison de la rétention d’archivage.  <br/> |
|ProjectDeleteFailure = 23006  <br/> |Échec de la suppression du projet.  <br/> |
|ProjectPublishEnqueueFailure = 23007  <br/> |Échec de la publication du projet lors de la mise en file d’attente.  <br/> |
|ProjectCheckinFailure = 23008  <br/> |Échec de l’archivage du projet lors du traitement de la file d’attente.  <br/> |
|ProjectCheckinFailed = 23009  <br/> |Échec de l’archivage du projet lors la mise en file d’attente.  <br/> |
|ProjectCheckoutFailed = 23010  <br/> |L’utilisateur ne dispose pas de l’autorisation d’extraction du projet.  <br/> |
|ProjectPublishSummaryEnqueueFailure = 23011  <br/> |Échec de la publication du récapitulatif lors de la mise en file d’attente.  <br/> |
|ProjectPublishSummaryFailed = 23012  <br/> |Échec de la publication du récapitulatif.  <br/> |
|ProjectUpdateScheduledProjectFailure = 26026  <br/> |Échec de la mise à jour de la planification du projet lors du traitement de la file d’attente.  <br/> |
|ProjectSyncProjectEnterpriseEntitiesFailure = 26033  <br/> |Échec de la synchronisation des entités d’entreprise de projet lors du traitement de la file d’attente.  <br/> |
|GeneralDalDatabaseIsReadOnly = 26034  <br/> |Échec du chargement de l’exploration de projets. La base de données est en lecture seule.  <br/> |
|GeneralDatabaseCommunicationError = 26035  <br/> |Il peut y avoir de nombreuses causes différentes, telles que des problèmes de réseau ou d’authentification.  <br/> |

<a name="pj15_ErrorCodes_RDS"></a>

## <a name="table-19-reporting-data-service-rds"></a>Tableau 19. Service de données de création de rapports (RDS)

|Code d’erreur RDS|Description|
|:-----|:-----|
|ReportingAttributeCubeSettingsChangedMessageFailed = 24000  <br/> |Échec du message de modification RDS pour un attribut de paramètres de cube.  <br/> |
|ReportingBaseCalendarChangeMessageFailed = 24001  <br/> |Échec du message de modification RDS pour un calendrier de base.  <br/> |
|ReportingCustomFieldMetadataChangeMessageFailed = 24002  <br/> |Échec du message de modification RDS pour des métadonnées de champ personnalisé.  <br/> |
|ReportingEntityUserViewChangedMessageFailed = 24003  <br/> |Échec du message de modification RDS pour un affichage utilisateur de l’entité.  <br/> |
|ReportingFiscalPeriodChangeMessageFailed = 24004  <br/> |Échec du message de modification RDS pour une période fiscale.  <br/> |
|ReportingLookupTableChangeMessageFailed = 24005  <br/> |Échec du message de modification RDS pour une table de choix.  <br/> |
|ReportingProjectChangeMessageFailed = 24006  <br/> |Échec du message de modification RDS pour un projet.  <br/> |
|ReportingResourceCapacityUpdateMessageFailed = 24007  <br/> |Échec du message de modification RDS pour la capacité des ressources.  <br/> |
|ReportingResourceChangeMessageFailed = 24008  <br/> |Échec du message de modification RDS pour une ressource.  <br/> |
|ReportingTimesheetAdjustMessageFailed = 24009  <br/> |Échec du message d’adaptation RDS pour une feuille de temps.  <br/> |
|ReportingTimesheetClassCreateMessageFailed = 24010  <br/> |Échec du message de création RDS pour une classe de feuille de temps.  <br/> |
|ReportingTimesheetDeleteMessageFailed = 24011  <br/> |Échec du message de suppression RDS pour une feuille de temps.  <br/> |
|ReportingTimesheetPeriodDeleteMessageFailed = 24012  <br/> |Échec du message de suppression RDS pour une période de feuille de temps.  <br/> |
|ReportingTimesheetPeriodMessageFailed = 24013  <br/> |Échec du message RDS pour une période de feuille de temps.  <br/> |
|ReportingTimesheetSaveMessageFailed = 24014  <br/> |Échec du message d’enregistrement RDS pour une feuille de temps.  <br/> |
|ReportingTimesheetStatusChangeMessageFailed = 24015  <br/> |Échec du message de modification RDS pour l’état de la feuille de temps.  <br/> |
|ReportingWSSSyncMessageFailed = 24016  <br/> |Échec du message RDS pour la synchronisation SharePoint.  <br/> |
|ReportingGetSPWebFailed = 24017  <br/> |Échec de l’obtention de la valeur web de SharePoint par le service RDS.  <br/> |
|ReportingWssSyncListFailed = 24018  <br/> |Échec de la synchronisation du service RDS avec la liste SharePoint.  <br/> |
|ReportingWssTransferLinksFailed = 24019  <br/> |Échec du transfert des liens SharePoint par le service RDS.  <br/> |
|ReportingQueueMessageSubmitFailed = 24020  <br/> |Échec de l’envoi par le service RDS d’un message à la file d’attente.  <br/> |
|ReportingWssSyncHRefFailed = 24021  <br/> |Échec de la synchronisation du service RDS avec la valeur HRef de SharePoint.  <br/> |
|ReportingSyncGlobalDataMessageFailed = 24022  <br/> |Échec du message RDS de synchronisation avec les données globales d’entreprise.  <br/> |
|ReportingRDBRefreshMessageFailed = 24023  <br/> |Échec du message RDS d’actualisation de la RDB.  <br/> |
|ReportingAttributeCubeDepartmentsChangedMessageFailed = 24024  <br/> |Le message RDS n’a pas pu modifier l’attribut de service pour le cube OLAP.  <br/> |
|ReportingTimesheetProjectAggregationMessageFailed = 24025  <br/> |Le message RDS n’a pas pu effectuer l’agrégation des projets pour les tables de feuille de temps dans la RDB.  <br/> |
|ReportingRdbBulkDataSyncMessageFailed = 24026  <br/> |Le message RDS n’a pas pu effectuer la synchronisation des données en bloc dans la RDB.  <br/> |
|ReportingWorkflowMetadataSyncMessageFailed = 24027  <br/> |Le message RDS n’a pas pu synchroniser les métadonnées des flux de travail.  <br/> |
|ReportingProjectWorkflowInformationSyncMessageFailed = 24028  <br/> |Le message RDS n’a pas pu synchroniser les informations sur les flux de travail de projet.  <br/> |
|ReportingEptSyncMessageFailed = 24029  <br/> |Le message RDS n’a pas pu synchroniser le modèle de projet d’entreprise.  <br/> |
|ReportingSummaryProjectPublishMessageFailed = 24030  <br/> |Le message RDS n’a pas pu publier le projet de synthèse.  <br/> |
|ReportingSolutionCommitedDecisionChangedMessageFailed = 24031  <br/> |Le message RDS n’a pas pu modifier la décision validée pour la solution.  <br/> |
|ReportingDelayedUpgradeFailed = 24032  <br/> |La mise à niveau RDB retardée a échoué.  <br/> |

<a name="pj15_ErrorCodes_Resources"></a>

## <a name="table-20-resource"></a>Tableau 20. Ressource

|Code d’erreur de ressource|Description|
|:-----|:-----|
|ResourceNotFound = 2000  <br/> |Ressource introuvable.  <br/> |
|ResourceAlreadyExists = 2001  <br/> |La ressource existe déjà.  <br/> |
|ResourceCheckedoutToOtherUser = 2002  <br/> |Ressource extraite pour un autre utilisateur.  <br/> |
|ResourceUIDInvalid = 2011  <br/> |GUID de ressource non valide.  <br/> |
|ResourceNameInvalid = 2016  <br/> |Nom de la ressource non valide.  <br/> |
|ResourceNameTooLong = 2017  <br/> |Le nom de la ressource est trop long.  <br/> |
|ResourceInitialsTooLong = 2018  <br/> |Les initiales de la ressource sont trop longues.  <br/> |
|ResourceCheckedout = 2025  <br/> |Ressource extraite.  <br/> |
|ResourceNTAccountInvalid = 2026  <br/> |Compte Windows (NTLM) de la ressource non valide.  <br/> |
|ResourceNameAlreadyInUse = 2027  <br/> |Nom de la ressource déjà utilisé. Les noms doivent être uniques.  <br/> |
|ResourceNTAccountAlreadyInUse = 2028  <br/> |Compte NTLM de la ressource déjà utilisé.  <br/> |
|ResourceAdGuidAlreadyInUse = 2029  <br/> |GUID de ressource déjà utilisé.  <br/> |
|ResourceHasActuals = 2031  <br/> |La ressource dispose de chiffres réels.  <br/> |
|ResourceNTAccountTooLong = 2035  <br/> |Le compte NTLM est trop long.  <br/> |
|ResourceEMailAddressTooLong = 2036  <br/> |L’adresse de messagerie de la ressource est trop longue.  <br/> |
|ResourceCodeTooLong = 2037  <br/> |Le code de la ressource est trop long.  <br/> |
|ResourceGroupTooLong = 2038  <br/> |Le groupe de la ressource est trop long.  <br/> |
|ResourceWorkGroupInvalid = 2039  <br/> |Groupe de travail de la ressource non valide.  <br/> |
|ResourceTypeInvalid = 2040  <br/> |Type de ressource non valide.  <br/> |
|ResourceNonWorkResourceWithEMailInvalid = 2044  <br/> |Une ressource non liée au travail ne peut pas disposer d’une adresse de messagerie.  <br/> |
|rsResourceNameHasTrailingOrLeadingWhitespace = 2046  <br/> |Le nom de la ressource comporte un espace de début ou de fin.  <br/> |
|ResourceCannotDeleteCallingUserAccount = 2047  <br/> |L’utilisateur ne peut pas supprimer son propre compte.  <br/> |
|ResourceInitialsInvalid = 2048  <br/> |Initiales de la ressource non valides.  <br/> |
|ResourceAccrueAtInvalid = 2049  <br/> |Valeur d’allocation non valide.  <br/> |
|ResourceNonMaterialResourceCannotHaveMaterialLabel = 2050  <br/> |Une ressource non consommable ne peut pas comporter d’étiquette Matériau.  <br/> |
|ResourceMaterialResourceCannotHaveCertainFields = 2051  <br/> |Une ressource consommable ne peut pas comporter certains champs.  <br/> |
|ResourceAvailFromAvailToOverlap = 2052  <br/> |Chevauchement des dates de type « disponible à partir de » et « disponible jusqu’à ».  <br/> |
|ResourceInvalidEmailLanguage = 2053  <br/> |Langue du courrier électronique non valide.  <br/> |
|ResourceBookingTypeInvalid = 2055  <br/> |Type de réservation non valide.  <br/> |
|ResourceCannotReplaceMaterialResourceWithNonMaterialResource = 2056  <br/> |Impossible de remplacer une ressource consommable par une ressource non consommable.  <br/> |
|ResourceCannotUpdateEnterpriseResource = 2057  <br/> |Impossible de mettre à jour la ressource d’entreprise.  <br/> |
|rsResourceCannotAddLocalWithSameNameAsEnterprise = 2058  <br/> |Impossible d’ajouter une ressource locale portant le même nom qu’une ressource d’entreprise.  <br/> |
|ResourceCannotSetRateOnCostResource = 2059  <br/> |Impossible de définir un taux sur une ressource de type Coût.  <br/> |
|ResourceCannotSetRateOnMaterialResource = 2060  <br/> |Impossible de définir un taux sur une ressource consommable.  <br/> |
|ResourceCannotSetCanLevelOnNonWorkResource = 2061  <br/> |Impossible de définir le niveau d’une ressource non liée au travail.  <br/> |
|ResourceCannotDeleteThisUser = 2062  <br/> |Impossible de supprimer cet utilisateur.  <br/> |
|ResourceCannotDeactivateSelf = 2063  <br/> |Une ressource ne peut pas se désactiver elle-même.  <br/> |
|ResourceAvailabilityDateRangesOverlap = 2064  <br/> |Chevauchement des plages de dates de disponibilité des ressources.  <br/> |
|ResourceAvailabilityOutsideTheHireAndTerminationDateRange = 2065  <br/> |La date de disponibilité de la ressource se situe en dehors de la plage de dates d’embauche et de fin de contrat.  <br/> |
|ResourceFilterInvalid = 2066  <br/> |Filtre non valide pour une ressource.  <br/> |
|ResourceSegmentWithThisEffectiveDateDoesNotExist = 2067  <br/> |Impossible de supprimer un taux de ressource qui n’a pas été enregistré.  <br/> |
|ResourceSegmentWithThisEffectiveDateAlready = 2068  <br/> |Un segment avec cette date d’effet existe déjà.  <br/> |
|ResourceUserHasItemCheckedOutToItStill = 2069  <br/> |L’utilisateur dispose d’un élément toujours extrait.  <br/> |
|ResourceInvalidHireDate = 2070  <br/> |Date d’embauche non valide.  <br/> |
|ResourceInvalidTerminationDate = 2071  <br/> |Date de fin de contrat non valide.  <br/> |
|ResourceCannotChangeExistingResourceType = 2072  <br/> |Impossible de modifier un type de ressource.  <br/> |
|ResourceCannotSetTimesheetManagerOnSpecifiedResource = 2073  <br/> |Impossible de définir le responsable de la feuille de temps pour la ressource spécifiée.  <br/> |
|ResourceInvalidTimesheetManager = 2074  <br/> |Responsable de la feuille de temps non valide.  <br/> |
|ResourceInvalidAssignmentOwner = 2075  <br/> |Propriétaire de l’affectation non valide.  <br/> |
|ResourceCannotCreateCostResource = 2076  <br/> |Impossible de créer une ressource de type Coût.  <br/> |
|ResourceInvalidRbsValue = 2077  <br/> |Valeur RBS non valide.  <br/> |
|ResourceCannotSetAssignmentOwnerOnSpecifiedResource = 2078  <br/> |Impossible de définir le propriétaire de l’affectation pour la ressource spécifiée.  <br/> |
|ResourceFieldsInvalidForBudget = 2079  <br/> |Un ou plusieurs champs de budget ne sont pas valides.  <br/> |
|ResourceHyperlinkInvalid = 2080  <br/> |Lien hypertexte de la ressource non valide.  <br/> |
|ResourceAuthorizationValidOnlyOnWorkResources = 2081  <br/> |L’autorisation est uniquement valide sur les ressources de travail.  <br/> |
|ResourceIsProjectOwner = 2082  <br/> |Impossible de supprimer la ressource, car cette dernière correspond au propriétaire du projet.  <br/> |
|ResourceIsTimesheetManager = 2083  <br/> |Impossible de supprimer la ressource, car cette dernière correspond au responsable de la feuille de temps.  <br/> |
|ResourceIsDefaultAssignmentOwner = 2084  <br/> |Impossible de supprimer la ressource, car cette dernière correspond au propriétaire de l’affectation par défaut.  <br/> |
|ResourceIsAssignmentOwner = 2085  <br/> |Impossible de supprimer la ressource, car cette dernière correspond au propriétaire de l’affectation.  <br/> |
|ResourceIsUsedInResourcePlan = 2086  <br/> |Impossible de supprimer la ressource, car cette dernière est utilisée dans le plan de charge des ressources.  <br/> |
|ResourceCannotDeleteEnterpriseResource = 2087  <br/> |Impossible de supprimer la ressource d’entreprise pour une raison inconnue.  <br/> |
|ResourceSetResourceAuthorizationFailed = 2088  <br/> |Échec de la définition de l’autorisation d’accès aux ressources.  <br/> |
|ResourceTooManyResourcesSpecifiedToDelete = 2089  <br/> |Impossible de supprimer le nombre de ressources spécifié.  <br/> |
|ResourceTooManyResourcesReturned = 2090  <br/> |La méthode ne peut pas gérer ce nombre de ressources.  <br/> |
|ResourceCannotDeleteWorkflowProxyUser = 2091  <br/> |Impossible de supprimer l’utilisateur proxy du flux de travail.  <br/> |
|ResourceInvalidEmailWithExchangeSync = 2092  <br/> |Adresse électronique non valide pour la synchronisation avec Microsoft Exchange Server.  <br/> |
|ResourceInvalidResourceTypeWithExchangeSync = 2093  <br/> |Type de ressource non valide pour la synchronisation avec Exchange Server.  <br/> |
|ResourceInvalidPrincipalNameWithExchangeSync = 2094  <br/> |Nom principal de la ressource non valide pour la synchronisation avec Exchange Server.  <br/> |
|ResourceInvalidAuthenticationTypeWithExchangeSync = 2095  <br/> |Type d’authentification de la ressource non valide pour la synchronisation avec Exchange Server.  <br/> |
|ResourceExchangeSyncFlagAndPrincipalNameMismatch = 2096  <br/> |Non-concordance entre l’indicateur de synchronisation Exchange Server et le nom de principal de la ressource.  <br/> |
|ResourceUnsupportedUserUpdateInSharePointSecurityMode = 2097  <br/> |La création d’un utilisateur n’est pas prise en charge en mode de sécurité SharePoint.  <br/> |

<a name="pj15_ErrorCodes_ResourcePlans"></a>

## <a name="table-21-resource-plan"></a>Tableau 21. Plan des ressources

|Code d’erreur de plan de ressources|Description|
|:-----|:-----|
|ResourcePlanProjectPublishIncomplete = 30000  <br/> |Échec de la publication du projet pour le plan de charge des ressources.  <br/> |
|ResourcePlanInvalidResourceType = 30001  <br/> |Type de ressource non valide dans le plan de charge des ressources.  <br/> |
|ResourcePlanInactiveResourcesDisallowed = 30002  <br/> |Les ressources inactives ne sont pas autorisés dans un plan de charge des ressources.  <br/> |
|ResourcePlanFilterInvalid = 30003  <br/> |Filtre de plan de charge des ressources non valide.  <br/> |
|ResourcePlanSaveFailure = 30004  <br/> |Impossible d’enregistrer le plan de charge des ressources.  <br/> |
|ResourcePlanCheckinFailure = 30005  <br/> |Échec de l’archivage du plan de charge des ressources.  <br/> |
|ResourcePlanDeleteFailure = 30006  <br/> |Échec de la suppression du plan de charge des ressources.  <br/> |
|ResourcePlanInvalidUtilizationType = 30007  <br/> |Type d’utilisation du plan de charge des ressources non valide.  <br/> |
|ResourcePlanInvalidTimescale = 30008  <br/> |Échelle de temps du plan de charge des ressources non valide.  <br/> |
|ResourcePlanMismatchedJobList = 30009  <br/> |Non-concordance dans la liste des postes du plan de charge des ressources.  <br/> |
|ResourcePlanAlreadyExists = 30010  <br/> |Le plan de charge des ressources existe déjà.  <br/> |
|ResourcePlanInvalidProjectUID = 30011  <br/> |GUID de projet non valide pour le plan de charge des ressources.  <br/> |
|ResourcePlanResourceAlreadyExists = 30012  <br/> |La ressource existe déjà dans le plan de ressources.  <br/> |
   
Les codes d’erreur du tableau 22 concernent les méthodes **Règles** du service web **PWA**. Ils sont utilisés en interne. 

<a name="pj15_ErrorCodes_Rules"></a>

## <a name="table-22-rules"></a>Tableau 22. Règles

|Code d’erreur de règles|Description|
|:-----|:-----|
|RulesNameTooLong = 21001  <br/> |Le nom de la règle d’approbation est trop long. Utilisation interne uniquement dans Project Web App.  <br/> |
|RulesDescriptionTooLong = 21002  <br/> |La description de la règle est trop longue. Utilisation interne uniquement dans Project Web App.  <br/> |
|RulesInvalidRuleType = 21003  <br/> |Le type de règle n’est pas valide. Utilisation interne uniquement dans Project Web App.  <br/> |
|RulesInvalidConditionType = 21004  <br/> |Le type de condition pour une règle n’est pas valide. Utilisation interne uniquement dans Project Web App.  <br/> |
|RulesInvalidOperatorType = 21005  <br/> |Le type d’opérateur pour une règle n’est pas valide. Utilisation interne uniquement dans Project Web App.  <br/> |
|RulesInvalidListItemType = 21007  <br/> |Le type d’élément de liste pour une règle n’est pas valide. Utilisation interne uniquement dans Project Web App.  <br/> |
|RulesNameInvalidCharacters = 21008  <br/> |Un ou plusieurs caractères ne sont pas valides dans le nom de la règle. Utilisation interne uniquement dans Project Web App.  <br/> |
|RulesDescriptionInvalidCharacters = 21009  <br/> |Un ou plusieurs caractères ne sont pas valides dans la description de la règle. Utilisation interne uniquement dans Project Web App.  <br/> |
|RulesInvalidValueType = 21010  <br/> |Le type de valeur dans la règle n’est pas valide. Utilisation interne uniquement dans Project Web App.  <br/> |

<a name="pj15_ErrorCodes_Security"></a>

## <a name="table-23-security"></a>Tableau 23. Sécurité

|Code d’erreur de sécurité|Description|
|:-----|:-----|
|SecurityGroupCouldNotBeCreated = 19001  <br/> |Impossible de créer le groupe de sécurité.  <br/> |
|SecurityFieldAccessIDInvalid = 19003  <br/> |Numéro d’identification de code d’accès au champ de sécurité non valide.  <br/> |
|SecurityCannotUpdateFacForNonExistentCategory = 19004  <br/> |La catégorie de sécurité n’existe pas. Impossible de mettre à jour le code d’accès au champ.  <br/> |
|SecurityDuplicateCategoryUid = 19005  <br/> |GUID de catégorie de sécurité en double.  <br/> |
|SecurityDuplicateGroupUid = 19006  <br/> |GUID de groupe de sécurité en double.  <br/> |
|SecurityDuplicateTemplateUid = 19007  <br/> |GUID de modèle de sécurité en double.  <br/> |
|SecurityInvalidTemplateUidRef = 19008  <br/> |GUID de modèle de sécurité non valide.  <br/> |
|SecurityInvalidGlobalPermission = 19009  <br/> |Autorisation de sécurité globale non valide.  <br/> |
|SecurityInvalidCategoryPermission = 19010  <br/> |Autorisation de catégorie de sécurité non valide.  <br/> |
|SecurityUpdatedGroupNotFound = 19013  <br/> |Groupe de sécurité mis à jour introuvable.  <br/> |
|SecurityUpdatedCategoryNotFound = 19014  <br/> |Catégorie de sécurité mise à jour introuvable.  <br/> |
|SecurityUpdatedTemplateNotFound = 19015  <br/> |Modèle de sécurité mis à jour introuvable.  <br/> |
|SecurityGroupMemberNotFound = 19016  <br/> |Membre du groupe de sécurité introuvable.  <br/> |
|SecurityUserNotFound = 19018  <br/> |Utilisateur de Project Server introuvable.  <br/> |
|SecurityNoCategoryRelationForPermission = 19019  <br/> |Relation de catégorie de sécurité introuvable pour l’autorisation.  <br/> |
|SecurityCannotDeleteDefaultGroup = 19020  <br/> |Impossible de supprimer le groupe de sécurité par défaut.  <br/> |
|SecurityCannotDeleteDefaultCategory = 19021  <br/> |Impossible de supprimer la catégorie de sécurité par défaut.  <br/> |
|SecurityCategoryCouldNotBeCreated = 19022  <br/> |Impossible de créer la catégorie de sécurité.  <br/> |
|SecurityNoCategoryForPermission = 19023  <br/> |Catégorie de sécurité introuvable pour l’autorisation.  <br/> |
|SecurityNoCategoryForObject = 19024  <br/> |Catégorie de sécurité introuvable pour l’objet.  <br/> |
|SecurityNoCategoryForRule = 19025  <br/> |Catégorie de sécurité introuvable pour la règle.  <br/> |
|SecurityNoGroupForPermission = 19026  <br/> |Groupe de sécurité introuvable pour l’autorisation.  <br/> |
|SecurityCannotSetPermissionForFieldGroup = 19027  <br/> |Impossible de définir l’autorisation pour le champ de groupe de sécurité.  <br/> |
|SecurityInvalidFieldGroup = 19028  <br/> |Champ de groupe de sécurité non valide.  <br/> |
|SecurityCannotSetOrgPermission = 19029  <br/> |Impossible de définir l’autorisation d’organisation de sécurité.  <br/> |
|SecurityInvalidOrgPermission = 19030  <br/> |Autorisation d’organisation de sécurité non valide.  <br/> |
|SecurityInvalidSecurityRule = 19031  <br/> |Règle de sécurité non valide.  <br/> |
|SecurityTemplateNotFound = 19034  <br/> |Modèle de sécurité introuvable.  <br/> |
|SecurityInvalidObjectType = 19035  <br/> |Type d’objet de sécurité non valide.  <br/> |
|SecurityDuplicateUid = 19036  <br/> |GUID d’objet de sécurité en double.  <br/> |
|SecurityObjectNotFound = 19037  <br/> |Objet de sécurité introuvable.  <br/> |
|SecurityInvalidCategoryUidRef = 19080  <br/> |GUID de catégorie de sécurité non valide.  <br/> |
|SecurityInvalidProjectUidRef = 19081  <br/> |GUID de projet non valide pour l’objet de sécurité.  <br/> |
|SecurityInvalidGroupUidRef = 19082  <br/> |GUID de groupe de sécurité non valide.  <br/> |
|SecurityInvalidUserUidRef = 19083  <br/> |GUID d’utilisateur non valide pour l’objet de sécurité.  <br/> |
|SecurityInvalidCategoryPermissionUidRef = 19084  <br/> |GUID d’autorisation non valide pour la catégorie de sécurité.  <br/> |
|SecurityInvalidGlobalPermissionUidRef = 19085  <br/> |GUID d’autorisation globale de sécurité non valide.  <br/> |
|SecurityInvalidResourceUidRef = 19086  <br/> |GUID de ressource non valide pour l’objet de sécurité.  <br/> |
|SecurityDeleteNotSupportedBySetMethod = 19087  <br/> |La méthode ne peut pas supprimer l’objet de sécurité.  <br/> |
|SecurityInvalidProjectCategoryPermissionUidRef = 19088  <br/> |GUID d’autorisation de catégorie de projet non valide.  <br/> |
|SecurityCannotModifyCoreProjectCategoryDataInUpdate = 19089  <br/> |La méthode de mise à jour de la sécurité ne peut pas modifier les données de catégorie du projet principal.  <br/> |
|SecurityProjectCategoryEntitiesDoNotAllowInPlaceChanges = 19090  <br/> |Impossible de modifier les entités de catégorie de sécurité dans une mise à jour.  <br/> |
|SecurityCategoryCannotAddRelationForDeletedCategory = 19091  <br/> |Impossible d’ajouter une relation pour une catégorie de sécurité supprimée.  <br/> |
|SecurityCategoryCannotAddPermissionForDeletedCategory = 19092  <br/> |Impossible d’ajouter une autorisation pour une catégorie de sécurité supprimée.  <br/> |
|SecurityCategoryCannotAddPermissionForDeletedRelation = 19093  <br/> |Impossible d’ajouter une autorisation pour une relation de catégorie de sécurité supprimée.  <br/> |
|SecurityCategoryCannotDeleteRelationForNewlyAddedCategory = 19094  <br/> |Impossible de supprimer la relation pour une catégorie de sécurité qui vient d’être ajoutée.  <br/> |
|SecurityCategoryCannotDeletePermissionForNewlyAddedCategory = 19095  <br/> |Impossible de supprimer l’autorisation pour une catégorie de sécurité qui vient d’être ajoutée.  <br/> |
|SecurityCategoryCannotDeletePermissionForNewlyAddedRelation = 19096  <br/> |Impossible de supprimer l’autorisation pour une relation qui vient d’être ajoutée dans une catégorie de sécurité.  <br/> |
|SecurityCategoryCannotHaveDuplicateUserOrGroupUidsForRelation = 19097  <br/> |Utilisateur ou UID de groupe en double non autorisé pour une relation de catégorie de sécurité.  <br/> |
|SecurityCategoryPermissionMustHaveMatchingRelation = 19098  <br/> |Une autorisation de catégorie doit être associée à une relation de catégorie de sécurité correspondante.  <br/> |
|SecurityCategoryProjectAlreadyHasSecurityProjectCategory = 19099  <br/> |La liste des catégories sélectionnées possède déjà une catégorie de sécurité de projet.  <br/> |

<a name="pj15_ErrorCodes_Events"></a>

## <a name="table-24-project-server-event"></a>Tableau 24. Événement Project Server

|Code d’erreur d’événement Project Server|Description|
|:-----|:-----|
|ServerEventInvalidEventId = 19033  <br/> |Numéro d’identification d’événement Project Server non valide.  <br/> |
|ServerEventServiceNotFound = 22003  <br/> |Service d’événement Project Server introuvable. Cette erreur n’est pas utilisée dans le code de Project Server, mais elle correspond à un événement du service de journalisation unifiée (ULS) brut.  <br/> |
|ServerEventRemoteCouldNotReachProxy = 22005  <br/> |La Project Web App distante n’a pas pu atteindre le gestionnaire d’événements Project Server de proxy. Cette erreur n’est pas utilisée dans le code Project Server mais elle mappe à un événement ULS brut.  <br/> |
|ServerEventManagerCouldNotReachRemote = 22006  <br/> |Le gestionnaire d’événements Project Server n’a pas pu atteindre la Project Web App distante. Cette erreur n’est pas utilisée dans le code Project Server mais elle mappe à un événement ULS brut.  <br/> |
|ServerEventHandlerNotSigned = 22007  <br/> |Gestionnaire d’événements Project Server non signé.  <br/> |
|ServerEventHandlerMalformedAssemblyName = 22008  <br/> |Nom d’assembly non valide pour le gestionnaire d’événements Project Server.  <br/> |
|ServerEventHandlerOrderInvalid = 22009  <br/> |Ordre non valide pour le gestionnaire d’événements Project Server.  <br/> |
|ServerEventHandlerDuplicateEntry = 22010  <br/> |Entrée en double pour le gestionnaire d’événements Project Server.  <br/> |
|ServerEventHandlerNotFound = 22011  <br/> |Gestionnaire d’événements Project Server introuvable.  <br/> |
|ServerEventHandlerDuplicateName = 22012  <br/> |Nom en double pour le gestionnaire d’événements Project Server.  <br/> |
|ServerEventHandlerNullAssemblyNameAndEndpointUrl = 22013  <br/> |Valider qu’il existe une URL de point de terminaison ou un nom d’assembly.  <br/> |

<a name="pj15_ErrorCodes_Statusing"></a>

## <a name="table-25-statusing-web-service"></a>Tableau 25. Service web de gestion des états 

|Code d’erreur relatif au service web de gestion des états|Description|
|:-----|:-----|
|StatusingInvalidEntity = 3102  <br/> |L’entité pour **Gestion des états** n’est pas valide.  <br/> |
|StatusingGetDataForTaskFailed = 3103  <br/> |Échec de l’obtention des données pour l’état de la tâche.  <br/> |
|StatusingGetTaskOrAssnCntrFailed = 3104  <br/> |Échec de l’obtention de la tâche ou du centre d’affectation pour l’état.  <br/> |
|StatusingInvalidPIDForProjCntr = 3105  <br/> |Le numéro d’identification de la propriété **Gestion des états** pour le centre de projets n’est pas valide.  <br/> |
|StatusingDeleteAssnFailed = 3106  <br/> |Impossible de supprimer une affectation dans le processus **Gestion des états**.  <br/> |
|StatusingAssnSaveFailed = 3107  <br/> |Impossible d’enregistrer une affectation dans le processus **Gestion des états**.  <br/> |
|StatusingTaskSaveFailed = 3108  <br/> |Impossible d’enregistrer une tâche dans le processus **Gestion des états**.  <br/> |
|StatusingInvalidPID = 3109  <br/> |Le numéro d’identification de la propriété **Gestion des états** n’est pas valide.  <br/> |
|StatusingSetDataValueInvalid = 3111  <br/> |La valeur de données **Gestion des états** n’est pas valide.  <br/> |
|StatusingSetDataFailed = 3112  <br/> |Impossible de définir la valeur de données **Gestion des états**.  <br/> |
|StatusingInvalidDelegationStart = 3113  <br/> |L’heure de début pour une affectation dans la méthode **DelegateAssignments** n’est pas valide.  <br/> |
|StatusingApprovalUpdateFailed = 3114  <br/> |Échec de la mise à jour de l’approbation d’état.  <br/> |
|StatusingInvalidApprovalType = 3115  <br/> |Type d’approbation d’état non valide.  <br/> |
|StatusingInternalError = 3116  <br/> |Erreur de traitement interne dans une méthode **Gestion des états**.  <br/> |
|StatusingInvalidUpdateData = 3117  <br/> |Les données de mise à jour dans une méthode **Gestion des états** n’est pas valide.  <br/> |
|StatusingProjectUpdateFailed = 3118  <br/> |La mise à jour **Gestion des états** du projet a échoué.  <br/> |
|StatusingInvalidPreviewData = 3119  <br/> |Les données d’aperçu **Gestion des états** ne sont pas valides.  <br/> |
|StatusingInvalidTransaction = 3120  <br/> |La transaction **Gestion des états** n’est pas valide.  <br/> |
|StatusingTooManyResults = 3121  <br/> |Trop de résultats. Plus de 5 000 lignes seraient renvoyées lors de la lecture des données d’état chronologiques.  <br/> |
|StatusingInvalidInterval = 3122  <br/> |L’intervalle dans une méthode **Gestion des états** n’est pas valide. L’intervalle doit être en minutes et doit être supérieur à zéro.<br/> |
|StatusingApplyUpdatesFailed = 3123  <br/> |Impossible d’appliquer les mises à jour **Gestion des états** lors de la mise en file d’attente de la demande.  <br/> |
|StatusingApplyUpdatesFailure = 3124  <br/> |Impossible d’appliquer les mises à jour **Gestion des états** lors du traitement de la file d’attente.  <br/> |
|StatusingInvalidWorkData = 3125  <br/> |Les données de travail pour **Gestion des états** ne sont pas valides.  <br/> |
|StatusingMissingNameAttribute = 3126  <br/> |Attribut de nom manquant pour **Gestion des états**.  <br/> |
|StatusingInvalidNameAttribute = 3127  <br/> |L’attribut de nom pour **Gestion des états** n’est pas valide.  <br/> |
|StatusingInvalidData = 3128  <br/> |Les données **Gestion des états** ne sont pas valides.  <br/> |
|StatusingInvalidChangelist = 3130  <br/> |Données XML non valides dans le paramètre _changexml_ de la méthode **UpdateStatus**.  <br/> |
|StatusingInsufficientAssignmentRights = 3131  <br/> |**SetAssignmentWorkData** ne peut pas mettre à jour une affectation car l’utilisateur ne dispose pas d’autorisation.  <br/> |
|StatusingInvalidChangeNumber = 3132  <br/> |Le numéro de modification **Gestion des états** n’est pas valide.  <br/> |
|StatusingPidNotEditable = 3133  <br/> |Le numéro d’identification de la propriété **Gestion des états** n’est pas modifiable.  <br/> |
|StatusingCannotSetTimephasedDataInManualTasks = 3134  <br/> |Impossible de définir des données chronologiques dans des tâches manuelles pour **Gestion des états**.  <br/> |
|StatusingCannotChangeTaskMode = 3135  <br/> |Impossible de modifier le mode de tâche pour **Gestion des états**.  <br/> |
   
Les codes d’erreur du tableau 26 sont liés aux méthodes **StatusReports** du service web **PWA**. Ils sont utilisés en interne dans Project Web App. 

<a name="pj15_ErrorCodes_StatusReports"></a>

## <a name="table-26-statusreports"></a>Tableau 26. StatusReports 

|Code d’erreur de rapport d’état|Description|
|:-----|:-----|
|StatusReportsUnknownError = 12100  <br/> |Erreur inconnue dans **StatusReports**.  <br/> |
|StatusReportsPeriodUnmatched = 12101  <br/> |Impossible de faire correspondre la période du rapport d’état.  <br/> |
|StatusReportsPeriodUnavailable = 12102  <br/> |Période du rapport d’état non disponible.  <br/> |
|StatusReportsInvalidFormInput = 12103  <br/> |Les données dans le formulaire du rapport d’état ne sont pas valides.  <br/> |

<a name="pj15_ErrorCodes_Tasks"></a>

## <a name="table-27-task"></a>Tableau 27. Tâche 

|Code d’erreur de tâche|Description|
|:-----|:-----|
|TaskIDInvalid = 7001  <br/> |GUID de tâche non valide.  <br/> |
|TaskNameTooLong = 7003  <br/> |Le nom de la tâche est trop long.  <br/> |
|TaskTypeInvalid = 7005  <br/> |Type de tâche non valide.  <br/> |
|TaskPriorityInvalid = 7006  <br/> |Priorité de la tâche non valide.  <br/> |
|TaskConstraintTypeInvalid = 7007  <br/> |Type de contrainte de la tâche non valide.  <br/> |
|TaskNameInvalid = 7008  <br/> |Nom de la tâche non valide.  <br/> |
|TaskConstraintTypeRequiresConstraint = 7010  <br/> |La tâche requiert un type de contrainte.  <br/> |
|TaskConstraintTypeCannotHaveConstraintDate = 7011  <br/> |Le type de contrainte ne peut pas être une date de contrainte.  <br/> |
|TaskSummaryTaskCannotBeMilestone = 7013  <br/> |La tâche récapitulative ne peut pas être un jalon.  <br/> |
|TaskFixedCostAccrualInvalid = 7014  <br/> |Allocation des coûts fixes non valide pour une tâche.  <br/> |
|TaskPercentCompleteInvalid = 7015  <br/> |Valeur de pourcentage d’achèvement de la tâche non valide.  <br/> |
|TaskWorkPercentCompleteInvalid = 7016  <br/> |Valeur de pourcentage d’achèvement de travail de la tâche non valide.  <br/> |
|TaskPhysicalPercentCompleteInvalid = 7017  <br/> |Valeur de pourcentage d’achèvement physique de la tâche non valide.  <br/> |
|TaskLinkTypeInvalid = 7018  <br/> |Type de liaison de tâche non valide.  <br/> |
|TaskAlreadyExists = 7019  <br/> |La tâche existe déjà.  <br/> |
|TaskLinkAlreadyExists = 7020  <br/> |La liaison de tâche existe déjà.  <br/> |
|TaskNotFound = 7021  <br/> |Tâche introuvable.  <br/> |
|TaskLinkNotFound = 7022  <br/> |Liaison de tâche introuvable.  <br/> |
|TaskLinkLagInvalid = 7023  <br/> |Décalage non valide pour la liaison de tâche.  <br/> |
|TaskUnableToInsert = 7025  <br/> |Impossible d’insérer une tâche.  <br/> |
|TaskAddPositionInvalid = 7026  <br/> |Position d’ajout d’une tâche non valide.  <br/> |
|TaskOutlineLevelInvalid = 7027  <br/> |Niveau hiérarchique de la tâche non valide.  <br/> |
|TaskDurationFormatInvalid = 7028  <br/> |Format de durée de la tâche non valide.  <br/> |
|TaskCannotAddWhereSpecified = 7029  <br/> |Impossible d’ajouter la tâche à l’endroit spécifié.  <br/> |
|TaskEarnedValueMethodInvalid = 7030  <br/> |Méthode non valide pour la valeur acquise de la tâche.  <br/> |
|TaskCannotModifyProjectSummary = 7031  <br/> |Impossible de modifier la tâche récapitulative du projet.  <br/> |
|TaskCannotDeleteProjectSummary = 7032  <br/> |Impossible de supprimer la tâche récapitulative du projet.  <br/> |
|TaskCannotSetActualCost = 7033  <br/> |Impossible de définir le coût réel de la tâche.  <br/> |
|TaskLevelingDelayInvalid = 7034  <br/> |Retard de nivellement non valide pour une tâche.  <br/> |
|TaskCannotEditSummary = 7035  <br/> |Impossible de modifier la tâche récapitulative.  <br/> |
|TaskCannotCreateSubTasksUnderTasksWithAssignments = 7036  <br/> |Impossible de créer des tâches subordonnées sous une tâche qui comporte des affectations.  <br/> |
|TaskCannotDeleteSubProject = 7037  <br/> |Impossible de supprimer le sous-projet pour la tâche.  <br/> |
|TaskCannotEditExternal = 7038  <br/> |Impossible de modifier la tâche externe.  <br/> |
|TaskCannotDeleteExternal = 7039  <br/> |Impossible de supprimer la tâche externe.  <br/> |
|TaskLinkCannotDeleteExternal = 7040  <br/> |Impossible de supprimer une liaison vers une tâche externe.  <br/> |
|TaskCannotModifyNullTask = 7041  <br/> |Impossible de modifier une tâche NULL.  <br/> |
|TaskCannotModifyLeafTaskWithNoAssignment = 7042  <br/> |Impossible de modifier une tâche feuille qui ne comporte aucune affectation.  <br/> |
|TaskCannotModifyExternalTask = 7043  <br/> |Impossible de modifier une tâche externe.  <br/> |
|TaskStatusManagerInvalid = 7044  <br/> |Gestionnaire d’état de tâche non valide.  <br/> |
|TaskLinkCyclicDependency = 7045  <br/> |La liaison de tâche comporte une dépendance cyclique.  <br/> |
|TaskCannotCreateOrModifySubTasksUnderTasksWithAssignments = 7046  <br/> |Impossible de créer ou de modifier des tâches subordonnées sous une tâche récapitulative qui comporte des affectations.  <br/> |
|TaskLinkCannotEditExternal = 7047  <br/> |Impossible de modifier le lien vers une tâche externe.  <br/> |

<a name="pj15_ErrorCodes_Timesheets"></a>

## <a name="table-28-timesheet"></a>Tableau 28. Feuille de temps 

|Code d’erreur de feuille de temps|Description|
|:-----|:-----|
|TimesheetMaxHourPerDayExceeded = 3201  <br/> |Le nombre maximal d’heures par jour dans la feuille de temps a été dépassé.  <br/> |
|TimesheetHoursPerTSLimitExceeded = 3202  <br/> |La limite du nombre d’heures dans une feuille de temps a été dépassée.  <br/> |
|TimesheetUnverifiedTSLineNotAllowed = 3203  <br/> |Une ligne de feuille de temps non vérifiée n’est pas autorisée dans ce cas.  <br/> |
|TimesheetIncorrectMode = 3204  <br/> |Mode de feuille de temps non valide.  <br/> |
|TimesheetInvalidApprover = 3205  <br/> |Approbateur de feuille de temps non valide.  <br/> |
|TimesheetFutureReportingNotAllowed = 3206  <br/> |La création d’un rapport concernant des éléments futurs n’est pas autorisée pour la feuille de temps.  <br/> |
|TimesheetIncorrectPeriod = 3208  <br/> |Période de la feuille de temps non valide.  <br/> |
|TimesheetPeriodClosed = 3209  <br/> |Période de la feuille de temps fermée.  <br/> |
|TimesheetPendingLines = 3210  <br/> |Des lignes de la feuille de temps sont en attente.  <br/> |
|TimesheetInvalidDateRange = 3211  <br/> |Plage de dates de la feuille de temps non valide.  <br/> |
|TimesheetLineClassDisabled = 3212  <br/> |Classe de ligne de feuille de temps désactivée.  <br/> |
|TimesheetLineHasNonExistentItem = 3213  <br/> |La ligne de temps contient un élément qui n’existe pas.  <br/> |
|TimesheetLineInvalidStatus = 3214  <br/> |L’état de la ligne de feuille de temps n’est pas valide.  <br/> |

<a name="pj15_ErrorCodes_UserDelegation"></a>

## <a name="table-29-user-delegation"></a>Tableau 29. Délégation d’utilisateur 

|Code d’erreur de délégation d’utilisateur|Description|
|:-----|:-----|
|UserDelegationExpired = 43000  <br/> |La délégation d’utilisateur a expiré.  <br/> |
|UserDelegationCannotSelfDelegate = 43001  <br/> |Un utilisateur ne peut pas se déléguer une tâche à lui-même.  <br/> |
|UserDelegationInvalidDelegate = 43002  <br/> |Délégué d’utilisateur non valide.  <br/> |
|UserDelegationInvalidUser = 43003  <br/> |Utilisateur non valide pour la délégation.  <br/> |
|UserDelegationInvalidDates = 43004  <br/> |Dates de délégation d’utilisateur non valides.  <br/> |
|UserDelegationCannotDoubleDelegate = 43005  <br/> |Impossible de créer deux délégués.  <br/> |
|UserDelegationDelegateCannotLogon = 43006  <br/> |Le délégué d’utilisateur ne peut pas se connecter à Project Server.  <br/> |
|UserDelegationDelegateIsInactive = 43007  <br/> |Le délégué d’utilisateur est inactif.  <br/> |
|UserDelegationInvalidFilter = 43008  <br/> |Filtre de délégué d’utilisateur non valide.  <br/> |
|UserDelegationUserCannotLogon = 43010  <br/> |L’utilisateur ne peut pas se connecter à Project Server.  <br/> |
|UserDelegationUserIsInactive = 43011  <br/> |Le délégué d’utilisateur est inactif.  <br/> |

<a name="pj15_ErrorCodes_Workflow"></a>

## <a name="table-30-workflow"></a>Tableau 30. Flux de travail 

|Code d’erreur de flux de travail|Description|
|:-----|:-----|
|WorkflowPhasesCannotCreatePhase = 35000  <br/> |Impossible de créer la phase de flux de travail.  <br/> |
|WorkflowPhasesCannotUpdatePhase = 35001  <br/> |Impossible de mettre à jour la phase de flux de travail.  <br/> |
|WorkflowPhasesCannotDeletePhase = 35002  <br/> |Impossible de supprimer la phase de flux de travail.  <br/> |
|WorkflowPhaseNameIsRequired = 35003  <br/> |Le flux de travail [PHASE_NAME](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.WorkflowPhaseRow.PHASE_NAME.aspx) est requis.  <br/> |
|WorkflowStagesCannotCreateStage = 35004  <br/> |Impossible de créer l’étape de flux de travail.  <br/> |
|WorkflowStagesCannotUpdateStage = 35005  <br/> |Impossible de mettre à jour l’étape de flux de travail.  <br/> |
|WorkflowStagesCannotDeleteStage = 35006  <br/> |Impossible de supprimer l’étape de flux de travail.  <br/> |
|WorkflowStagesProjectsInStage = 35007  <br/> |Il existe des projets dans l’étape de flux de travail.  <br/> |
|WorkflowCannotAccessPDPLibrary = 35008  <br/> |Impossible d’accéder à la bibliothèque de pages de détails de projet.  <br/> |
|WorkflowInvalidPDPUid = 35009  <br/> |GUID de page de détails de projet non valide.  <br/> |
|WorkflowInvalidCustomFieldUid = 35010  <br/> |GUID de champ personnalisé non valide.  <br/> |
|WorkflowCustomFieldNotWorkflowControlled = 35011  <br/> |Le champ personnalisé n’est pas contrôlé par un flux de travail.  <br/> |
|WorkflowCustomFieldCannotBeRequiredAndReadOnly = 35012  <br/> |Le champ personnalisé de flux de travail ne peut pas être à la fois obligatoire et en lecture seule.  <br/> |
|WorkflowInvalidWorkflowPhaseUid = 35013  <br/> |Le flux de travail [PHASE_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.WorkflowPhaseRow.PHASE_UID.aspx) n’est pas valide.  <br/> |
|WorkflowInsertWorkflowPhaseNotAllowed = 35014  <br/> |Impossible d’insérer une phase de flux de travail.  <br/> |
|WorkflowInvalidWorkflowStageUid = 35015  <br/> |Le flux de travail [STAGE_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.WorkflowStageRow.STAGE_UID.aspx) n’est pas valide.  <br/> |
|WorkflowPhaseHasStages = 35016  <br/> |La phase de flux de travail comporte des étapes.  <br/> |
|WorkflowStageNameIsRequired = 35020  <br/> |Le flux de travail [STAGE_NAME](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.WorkflowStageRow.STAGE_NAME.aspx) est requis.  <br/> |
|WorkflowStageAtLeastOnePDPIsRequired = 35021  <br/> |Au moins une page de détails de projet est obligatoire pour l’étape de flux de travail.  <br/> |
|WorkflowCannotStartWorkflow = 35100  <br/> |Impossible de démarrer le flux de travail.  <br/> |
|WorkflowStatusCannotUpdateStatus = 35101  <br/> |Impossible de mettre à jour l’état du flux de travail.  <br/> |
|WorkflowOnlyProjectsHaveWorkflow = 35102  <br/> |Seuls les projets peuvent comporter un flux de travail.  <br/> |
|WorkflowNoWorkflowsDefined = 35103  <br/> |Aucun flux de travail n’est défini.  <br/> |
|WorkflowInvalidStageForProject = 35104  <br/> |Étape de flux de travail du projet non valide.  <br/> |
|WorkflowNoWorkflowForProject = 35105  <br/> |Le projet ne comporte pas de flux de travail.  <br/> |
|WorkflowCheckinRequiredAndProjectNotCheckedin = 35106  <br/> |Le projet doit être archivé pour que le flux de travail soit fonctionnel.  <br/> |
|WorkflowWaitingForRequiredData = 35107  <br/> |Le flux de travail est en attente de données obligatoires.  <br/> |
|WorkflowFlagCustomFieldsCannotBeRequired = 35108  <br/> |Un champ personnalisé d’indicateur ne peut pas être obligatoire dans un flux de travail.  <br/> |
|WorkflowCannotChangeWorkflow = 35109  <br/> |Impossible de modifier le flux de travail.  <br/> |
|WorkflowWorkflowStatusPDPNotAllowed = 35110  <br/> |Page de détails de projet non autorisée pour l’état de flux de travail.  <br/> |
|WorkflowInvalidWorkflowStatusPDPUid = 35111  <br/> |GUID de la page de détails de projet de l’état du flux de travail non valide.  <br/> |
|WorkflowInvalidStageStatusValue = 35112  <br/> |La valeur de l’état de l’étape du flux de travail n’est pas valide. Lorsque vous définissez l’état de l’étape dans le flux de travail, seules les valeurs **InProgressRequestSent**, **InProgressRunning** ou **InProgressWaiting** dans [Workflow.StageStatus](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.Workflow.StageStatus.aspx) sont autorisées.  <br/> |
|WorkflowCannotCheckinNotify = 35113  <br/> |Impossible d’indiquer au flux de travail que le projet est archivé.  <br/> |
|WorkflowCannotCommitNotify = 35114  <br/> |Impossible d’indiquer au flux de travail que le projet est validé dans le planificateur ou l’optimiseur.  <br/> |
|WorkflowExceptionStartingWorkflow = 35115  <br/> |Erreur lors du démarrage du flux de travail.  <br/> |
|WorkflowStatusPDPMustBeSupplied = 35116  <br/> |Une page de détails de projet est obligatoire pour l’état du flux de travail.  <br/> |
|WorkflowWorkflowProxyAccountNotFound = 35117  <br/> |Le compte proxy du flux de travail est introuvable.  <br/> |
|WorkflowInvalidCurrentStage = 35118  <br/> |Étape actuelle du flux de travail non valide.  <br/> |
|WorkflowMultipleStagesInProgress = 35119  <br/> |Plusieurs étapes sont en cours dans le flux de travail.  <br/> |
|WorkflowActivityInvalidArgument = 35120  <br/> |Message renvoyé lorsqu’une activité de flux de travail a reçu un argument non valide.  <br/> |
|WorkflowMTWConfigurationError = 35121  <br/> |Erreur de configuration du flux de travail de Microsoft Azure.  <br/> |
|EnterpriseProjectTypeInvalidEnterpriseProjectTypeUid = 35200  <br/> |La valeur **ENTERPRISE_PROJECT_TYPE_UID** n’est pas valide.  <br/> |
|EnterpriseProjectTypeCannotCreateEnterpriseProjectType = 35201  <br/> |Impossible de créer le type de projet d’entreprise.  <br/> |
|EnterpriseProjectTypeCannotUpdateEnterpriseProjectType = 35202  <br/> |Impossible de mettre à jour le type de projet d’entreprise.  <br/> |
|EnterpriseProjectTypeCannotDeleteEnterpriseProjectType = 35203  <br/> |Impossible de supprimer le type de projet d’entreprise.  <br/> |
|EnterpriseProjectTypeCannotCreateMultipleEnterpriseProjectTypes = 35204  <br/> |Impossible de créer plusieurs types de projet d’entreprise.  <br/> |
|EnterpriseProjectTypeCannotUpdateMultipleEnterpriseProjectTypes = 35205  <br/> |Impossible de mettre à jour plusieurs types de projet d’entreprise.  <br/> |
|EnterpriseProjectTypeInvalidCreatePDPUid = 35206  <br/> |Un modèle de projet d’entreprise (EPT) requiert une page de détails de projet (PDP) associée pour créer un projet à l’aide de ce modèle. Si ce dernier est lié à un flux de travail, cette erreur se produit au cours de la validation du modèle de projet d’entreprise, lorsque la page de détails de projet (PDP) n’est pas de type *Créer*. Les autres types de PDP sont *Normal* pour la modification d’un projet et *État du flux de travail* pour l’affichage des détails d’un projet lié au flux de travail.<br/> |
|EnterpriseProjectTypeInvalidProjectPlanTemplateUid = 35207  <br/> |La valeur [ENTERPRISE_PROJECT_PLAN_TEMPLATE_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeRow.ENTERPRISE_PROJECT_PLAN_TEMPLATE_UID.aspx) n’est pas valide.  <br/> |
|EnterpriseProjectTypeInvalidWorkspaceTemplateName = 35208  <br/> |La valeur [ENTERPRISE_PROJECT_WORKSPACE_TEMPLATE_NAME](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeRow.ENTERPRISE_PROJECT_WORKSPACE_TEMPLATE_NAME.aspx) n’est pas valide.  <br/> |
|EnterpriseProjectTypeInvalidWorkflowAssociationUid = 35209  <br/> |La valeur [WORKFLOW_ASSOCIATION_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeRow.WORKFLOW_ASSOCIATION_UID.aspx) n’est pas valide.  <br/> |
|EnterpriseProjectTypeCannotReadWssSettings = 35210  <br/> |Impossible de lire les paramètres SharePoint.  <br/> |
|EnterpriseProjectTypeCannotReadWssLanguagesAndTemplates = 35211  <br/> |Impossible de lire les langues et les modèles de site SharePoint.  <br/> |
|EnterpriseProjectTypeInvalidDepartmentUid = 35212  <br/> |Le [DEPARTMENT_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeDepartmentsRow.DEPARTMENT_UID.aspx) n’est pas valide.  <br/> |
|EnterpriseProjectTypeInvalidUri = 35213  <br/> |La valeur [ENTERPRISE_PROJECT_TYPE_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeDepartmentsRow.ENTERPRISE_PROJECT_TYPE_UID.aspx) n’est pas valide.  <br/> |
|EnterpriseProjectTypeUriRequiresHttp = 35214  <br/> |L’URI de type de projet d’entreprise requiert le protocole HTTP.  <br/> |
|EnterpriseProjectTypeCannotDeleteDefault = 35215  <br/> |Impossible de supprimer le type de projet d’entreprise par défaut.  <br/> |
|EnterpriseProjectTypeCannotChangeDefault = 35216  <br/> |Impossible de modifier le type de projet d’entreprise par défaut.  <br/> |
|EnterpriseProjectTypeHasProjectsCannotDelete = 35217  <br/> |Impossible de supprimer un type de projet d’entreprise qui comporte des projets.  <br/> |
|EnterpriseProjectTypeCreatePDPIsRequired = 35218  <br/> |Un modèle de projet d’entreprise (EPT) pour un flux de travail requiert une page de détails de projet (PDP) de type *Créer* associée pour créer un projet à l’aide de ce modèle. Cette erreur se produit lorsque la PDP n’est pas incluse dans la définition du modèle de projet d’entreprise. Les autres types de PDP sont *Normal* pour la modification d’un projet et *État du flux de travail* pour l’affichage des détails d’un projet lié à un flux de travail.  <br/> |
|EnterpriseProjectTypeOnlyOneCreatePDPAllowed = 35219  <br/> |La définition du modèle de projet d’entreprise n’autorise qu’une seule page de détails de projet de type *Créer*.  <br/> |
|EnterpriseProjectTypeHasWorkflowOnlyCreatePDPAllowed = 35220  <br/> |Un modèle de projet d’entreprise (EPT) pour un flux de travail requiert une page de détails de projet (PDP) de type *Créer* associée pour créer un projet à l’aide de ce modèle. Cette erreur se produit lorsque la PDP incluse dans la définition du modèle de projet d’entreprise du flux de travail est d’un autre type. Les autres types de PDP sont *Normal* pour la modification d’un projet et *État du flux de travail* pour l’affichage des détails d’un projet lié au flux de travail.  <br/> |
|EnterpriseProjectTypeInvalidData = 35221  <br/> |Le **WorkflowDataSet** de l’entreprise du type de projet d’entreprise comporte des données qui ne sont pas valides.  <br/> |
|EnterpriseProjectNoDefaultEnterpriseProjectTypeDefined = 35222  <br/> |Aucun type de projet d’entreprise par défaut n’est défini.  <br/> |
|EnterpriseProjectTypeAtLeastOnePDPIsRequired = 35223  <br/> |Au moins une page de détails de projet est requise pour le type de projet d’entreprise.  <br/> |
|EnterpriseProjectTypeWorkflowStatusPDPNotAllowed = 35224  <br/> |Une page de détails de projet associée à l’état du flux de travail n’est pas autorisée pour le type de projet d’entreprise.  <br/> |
|EnterpriseProjectTypeCannotChangeWorkflowAssociation = 35225  <br/> |Le projet comporte déjà un type de projet d’entreprise (EPT) ; vous ne pouvez pas modifier l’EPT pour le projet.  <br/> |

<a name="pj15_ErrorCodes_WSS"></a>

## <a name="table-31-wssinterop-and-objectlinkprovider-sharepoint-integration"></a>Tableau 31. WssInterop et ObjectLinkProvider (intégration SharePoint)

|Code d’erreur d’intégration SharePoint|Description|
|:-----|:-----|
|WSSCreateSiteFailure = 16400  <br/> |Échec de la création du site SharePoint pour l’espace de travail de projet.  <br/> |
|WSSCannotCreateWebWithBlankName = 16401  <br/> |Impossible de créer un site web SharePoint avec un nom vide.  <br/> |
|WSSWebAlreadyExists = 16402  <br/> |Le site web SharePoint existe déjà.  <br/> |
|WSSInvalidProjectUID = 16403  <br/> |GUID de projet non valide pour l’espace de travail de projet SharePoint.  <br/> |
|WSSProjectAlreadyHasSpWeb = 16404  <br/> |Le projet comporte déjà un site d’espace de travail SharePoint.  <br/> |
|WSSWebDoesNotExist = 16405  <br/> |Le site web SharePoint n’existe pas.  <br/> |
|WSSSpWebAlreadyLinkedToProject = 16406  <br/> |Le site web SharePoint est déjà lié à un projet.  <br/> |
|WSSWebHierarchyDoesNotExist = 16407  <br/> |La hiérarchie du site web SharePoint n’existe pas.  <br/> |
|WSSSPWebHasChildren = 16408  <br/> |Le site web SharePoint comporte des sites web enfant.  <br/> |
|WSSURIInvalidFormat = 16409  <br/> |Format de l’URI du site web SharePoint non valide.  <br/> |
|WSSSyncReportingDataFailed = 16410  <br/> |Échec de la synchronisation des données de création de rapports pour SharePoint.  <br/> |
|WSSWorkspaceUrlPathTooLong = 16411  <br/> |Le chemin de l’URL de l’espace de travail de projet SharePoint est trop long.  <br/> |
|WSSWorkspaceNameContainsIllegalChars = 16412  <br/> |Un ou plusieurs caractères dans un nom de site de projet SharePoint ne sont pas valides. Les caractères suivants ne sont pas valides dans un nom de projet : / " : \< \> | , . ' ? \* #  <br/> |
|WSSInvalidWssServerUid = 16413  <br/> |GUID du serveur SharePoint non valide.  <br/> |
|WSSSyncUsersFailed = 16414  <br/> |Échec de la synchronisation des utilisateurs de Project Server avec SharePoint.  <br/> |
|WSSWrongWebTemplateLCID = 16415  <br/> |Identificateur de paramètres régionaux (ID de langue) du modèle web SharePoint non valide.  <br/> |
|WSSWrongWebTemplate = 16416  <br/> |Modèle web SharePoint non valide.  <br/> |
|WSSWebIsNotProjectWorkspace = 16417  <br/> |Le site web SharePoint n’est pas un espace de travail de projet.  <br/> |
|WSSWebCannotStartOrEndOnPeriod = 16418  <br/> |Un nom de site web SharePoint ne peut pas commencer ou se terminer par un point.  <br/> |
|WSSCannotDeleteSiteCollection = 16419  <br/> |Impossible de supprimer la collection de sites web.  <br/> |
|WSSListUidInvalid = 16420  <br/> |GUID de liste SharePoint non valide.  <br/> |
|WSSSyncDataSetListUidMismatch = 16421  <br/> |Le GUID de liste SharePoint ne correspond pas au GUID de liste du **DataSet** de synchronisation.  <br/> |
|WSSSyncDataSetMissingProjectSettingsRow = 16422  <br/> |Ligne de paramètres de projet manquante dans le **DataSet** pour la synchronisation avec SharePoint.  <br/> |
|WSSSyncDataSetTaskMappingsNotAllowed = 16423  <br/> |Les mappages de tâche ne sont pas autorisés dans le **DataSet** pour la synchronisation avec SharePoint.  <br/> |
|WSSSyncDataSetWssListUidEmpty = 16424  <br/> |Le GUID de liste SharePoint est vide dans le **DataSet** pour la synchronisation avec SharePoint.  <br/> |
|WSSSyncDataNotFound = 16425  <br/> |Données manquantes lors de la synchronisation avec SharePoint.  <br/> |
|WSSSyncCriticalDataValidationError = 16426  <br/> |Erreur critique de validation des données lors de la synchronisation avec SharePoint.  <br/> |
|WSSSyncSharePointListNotAccessibleError = 16427  <br/> |La liste SharePoint est inaccessible.  <br/> |
|WSSSyncInvalidEntityUids = 16428  <br/> |Les GUID d’entité ne sont pas valides pour la synchronisation avec SharePoint.  <br/> |
|WSSSyncInvalidSyncData = 16429  <br/> |La synchronisation SharePoint comporte des données non valides.  <br/> |
|WSSSyncSPSummaryTaskAssignedToResourceError = 16430  <br/> |La synchronisation SharePoint comporte une tâche récapitulative affectée à une ressource.  <br/> |
|WSSSyncInsufficientPermissionsToCreateWinUser = 16431  <br/> |Les autorisations ne sont pas suffisantes pour créer un utilisateur Windows lors de la synchronisation avec SharePoint.  <br/> |
|WSSSyncNoDefaultValueForCustomField = 16432  <br/> |Valeur par défaut manquante dans un champ personnalisé lors de la synchronisation SharePoint.  <br/> |
|WSSOLPCreateLinkFailure = 18000  <br/> |Échec de la création d’un lien pour le fournisseur de liaison d’objet SharePoint.  <br/> |
|WSSOLPDeleteWebObjectLinkError = 18001  <br/> |Erreur lors de la suppression d’une liaison d’objet web dans le fournisseur de liaison d’objet SharePoint.  <br/> |
|WSSInvalidPermissionsToWssList = 18002  <br/> |Autorisations non valides pour la liste SharePoint.  <br/> |
|WSSWebIsNotUnderDefaultCollection = 18003  <br/> |Le site web SharePoint ne se trouve pas dans la collection par défaut.  <br/> |
|WSSWorkspaceUrlIsNotUnderPrimaryCollection = 18004  <br/> |L’URL d’espace de travail spécifiée ne se trouve pas dans la collection de sites associée à cette instance de Project Server. Obligatoire pour le mode d’autorisation actuel.  <br/> |
|WSSWorkspacesMustBeRestrictedToDefaultCollection = 18005  <br/> |Les espaces de travail doivent être limités à la collection de sites par défaut dans le mode d’autorisation actuel.  <br/> |

<a name="pj15_ErrorCodes_ASMXExample"> </a>

## <a name="error-code-example-for-asmx"></a>Exemple de code d’erreur pour ASMX

Pour obtenir une liste des erreurs si vous recevez une exception lorsque vous appelez une méthode PSI, transmettez l’objet **SoapException** au constructeur de classe [Microsoft.Office.Project.Server.Library.PSClientError](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.PSClientError.aspx). Vous pouvez ensuite utiliser [GetAllErrors](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.PSClientError.GetAllErrors.aspx) pour stocker les informations d’erreur dans un tableau **PSErrorInfo** et énumérer les erreurs, comme dans l’exemple suivant. 
  
> [!NOTE]
> L’objet **PSErrorInfo** n’inclut pas toutes les informations dont vous avez peut-être besoin. Par exemple, si vous utilisez **Resource.CheckOutResources** lorsque l’une des ressources est déjà extraite, **PSErrorInfo** indique la raison de l’échec pour chaque ressource ne pouvant pas être extraite, mais n’inclut pas le nom de la ressource ou le GUID. Pour obtenir plus d’informations dans une application ASMX, voir [CheckOutResources](https://msdn.microsoft.com/library/WebSvcResource.Resource.CheckOutResources.aspx). 
  
```cs
using System;
using System.Collections.Generic;
using System.Text;
using System.Web.Services.Protocols;
using System.Windows.Forms;
using PSLibrary = Microsoft.Office.Project.Server.Library;
. . .
try
{
    /* Call a PSI method. */
}
catch (SoapException ex)
{
    string errAttributeName;
    string errAttribute;
    string errMess = "".PadRight(30, '=') + "\r\n" + "Error: " + "\r\n";
    PSLibrary.PSClientError error = new PSLibrary.PSClientError(ex);
    PSLibrary.PSErrorInfo[] errors = error.GetAllErrors();
    PSLibrary.PSErrorInfo thisError;
    for (int i = 0; i < errors.Length; i++)
    {
        thisError = errors[i];
        errMess += "\n" + ex.Message.ToString() + "\r\n";
        errMess += "".PadRight(30, '=') + "\r\nPSCLientError Output:\r\n \r\n";
        errMess += thisError.ErrId.ToString() + "\n";
        for (int j = 0; j < thisError.ErrorAttributes.Length; j++)
        {
            errAttributeName = thisError.ErrorAttributeNames()[j];
            errAttribute = thisError.ErrorAttributes[j];
            errMess += "\r\n\t" + errAttributeName +
                       ": " + errAttribute;
        }
        errMess += "\r\n".PadRight(30, '=');
    }
    MessageBox.Show(errMess, "Error", MessageBoxButtons.OK,
        MessageBoxIcon.Error);
}
```

<a name="pj15_ErrorCodes_WCFExample"> </a>

## <a name="error-code-example-for-wcf"></a>Exemple de code d’erreur pour WCF

Pour obtenir une liste des erreurs si vous recevez une exception **System.ServiceModel.FaultException** lorsque vous appelez une méthode PSI dans une application WCF, vous pouvez extraire un objet **PSClientError** de l’objet **FaultException**. Vous pouvez ensuite utiliser [GetAllErrors](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.PSClientError.GetAllErrors.aspx) pour stocker les informations d’erreur dans un tableau **PSErrorInfo** et énumérer les erreurs, comme dans l’exemple ASMX précédent. 
  
```cs
using System;
using System.Text;
using System.ServiceModel;
using System.Xml;
using PSLibrary = Microsoft.Office.Project.Server.Library;
. . .
try
{
    /* Call a PSI method. */
}
catch(FaultException fault)
{
    // Use the WCF FaultException, because the ASMX SoapException does not 
    // exist in a WCF-based application.
    WriteFaultOutput(fault);
}
// Get a PSClientError object from the WCF FaultException object, and
// then display the exception details and each error in the PSClientError stack.
private static void WriteFaultOutput(FaultException fault)
{
    string errAttributeName;
    string errAttribute;
    string errOut;
    string errMess = "".PadRight(30, '=') + "\r\n"
        + "Error details: " + "\r\n";
    PSLibrary.PSClientError error = GetPSClientError(fault, out errOut);
    errMess += errOut;
    PSLibrary.PSErrorInfo[] errors = error.GetAllErrors();
    PSLibrary.PSErrorInfo thisError;
    for (int i = 0; i < errors.Length; i++)
    {
        thisError = errors[i];
        errMess += "\r\n".PadRight(30, '=') + "\r\nPSClientError output:\r\n";
        errMess += thisError.ErrId.ToString() + "\n";
        for (int j = 0; j < thisError.ErrorAttributes.Length; j++)
        {
            errAttributeName = thisError.ErrorAttributeNames()[j];
            errAttribute = thisError.ErrorAttributes[j];
            errMess += "\r\n\t" + errAttributeName
                + ": " + errAttribute;
        }
    }
    Console.ForegroundColor = ConsoleColor.Red;
    Console.WriteLine(errMess);
    Console.ResetColor();
}
/// <summary>
/// Extract a PSClientError object from the ServiceModel.FaultException,
/// for use in output of the GetPSClientError stack of errors.
/// </summary>
/// <param name="e"></param>
/// <param name="errOut">Shows that FaultException has more information 
/// about the errors than PSClientError has. FaultException can also contain 
/// other types of errors, such as failure to connect to the server.</param>
/// <returns>PSClientError object, for enumerating errors.</returns>
public static PSLibrary.PSClientError GetPSClientError(FaultException e, 
                                                        out string errOut)
{
    const string PREFIX = "GetPSClientError() returns null: ";
    errOut = string.Empty;
    PSLibrary.PSClientError psClientError = null;
    if (e == null)
    {
        errOut = PREFIX + "Null parameter (FaultException e) passed in.";
        psClientError = null;
    }
    else
    {
        // Get a ServiceModel.MessageFault object.
        var messageFault = e.CreateMessageFault();
        if (messageFault.HasDetail)
        {
            using (var xmlReader = messageFault.GetReaderAtDetailContents())
            {
                var xml = new XmlDocument();
                xml.Load(xmlReader);
                var serverExecutionFault = xml["ServerExecutionFault"];
                if (serverExecutionFault != null)
                {
                    var exceptionDetails = serverExecutionFault["ExceptionDetails"];
                    if (exceptionDetails != null)
                    {
                        try
                        {
                            errOut = exceptionDetails.InnerXml + "\r\n";
                            psClientError = 
                                new PSLibrary.PSClientError(exceptionDetails.InnerXml);
                        }
                        catch (InvalidOperationException ex)
                        {
                            errOut = PREFIX + "Unable to convert fault exception info ";
                            errOut += "a valid Project Server error message. Message: \n\t";
                            errOut += ex.Message;
                            psClientError = null;
                        }
                    }
                    else
                    {
                        errOut = PREFIX + "The FaultException e is a ServerExecutionFault, "
                            + "but does not have ExceptionDetails.";
                    }
                }
                else
                {
                    errOut = PREFIX + "The FaultException e is not a ServerExecutionFault.";
                }
            }
        }
        else // No detail in the MessageFault.
        {
            errOut = PREFIX + "The FaultException e does not have any detail.";
        }
    }
    errOut += "\r\n" + e.ToString() + "\r\n";
    return psClientError;
}

```


Outre les données dans l’objet **PSClientError**, l’objet **FaultException** peut inclure d’autres types d’erreurs, comme l’impossibilité de se connecter à Project Server. Le paramètre _errOut_ de la méthode **GetPSClientError** dans l’exemple précédent affiche des informations supplémentaires. Par exemple, l’exemple de code **CreateProject4Department** dans la méthode [QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) inclut des commentaires qui montrent comment créer des erreurs lors de la définition des propriétés dans le tableau **ProjectCustomFields**. Lors de l’exécution de l’application, le paramètre _errOut_ inclut l’élément **errinfo** et d’autres données (formatées ici à partir de la sortie console). 
  
```XML
==============================
Error details:
<errinfo xmlns="">
  <dataset name="ProjectDataSet">
    <table name="ProjectCustomFields">
      <row CUSTOM_FIELD_UID="976d3bd9-95ff-40a2-a938-960c410b0341">
        <error id="11704" name="CustomFieldInvalidTypeColumnFilledIn" 
               uid="aa8a2fab-9262-422f-b022-ca1cb12bc75f"></error>
        <error id="11713" name="CustomFieldRequiredValueNotProvided" 
               uid="dc2e2156-86e9-4aac-bede-d07dc44dfedc"></error>
      </row>
    </table>
  </dataset>
</errinfo>
System.ServiceModel.FaultException`1[SvcProject.ServerExecutionFault]: 
ProjectServerError(s) LastError=CustomFieldRequiredValueNotProvided Instructions: 
Pass this into PSClientError constructor to access all error information 
(Fault Detail is equal to SvcProject.ServerExecutionFault).
============================
PSClientError output:
CustomFieldInvalidTypeColumnFilledIn
============================
PSClientError output:
CustomFieldRequiredValueNotProvided
```

<a name="pj15_ErrorCodes_AR"> </a>

## <a name="see-also"></a>Voir aussi

- [Articles conceptuels et procédures liés à Project](project-conceptual-and-how-to-articles.md)
- [SQL Server Profiler](https://msdn.microsoft.com/library/3ad5f33d-559e-41a4-bde6-bb98792f7f1a.aspx)
- [Project Server 2010 : ce qui est attendu en cas d’erreur inattendue](https://blogs.msdn.com/b/brismith/archive/2010/03/24/project-server-2010-what-to-expect-when-you-get-the-unexpected.aspx)
- [Visionneuse ULS](https://www.codeproject.com/Articles/458052/ULS-Log-Viewer)
    

