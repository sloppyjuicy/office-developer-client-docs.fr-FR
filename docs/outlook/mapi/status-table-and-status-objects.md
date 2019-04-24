---
title: Table d'État et objets d'État
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 203765c1-4b08-4032-a5bf-18f3e752a899
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 3eb190069b43ea1960c3b6edf30a9e0b782d2c41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336329"
---
# <a name="status-table-and-status-objects"></a>Table d'État et objets d'État

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI fournit un tableau contenant des informations sur l'état du sous-système MAPI, du spouleur MAPI, du carnet d'adresses ou d'un fournisseur de services particulier. Vous pouvez accéder à ce tableau en appelant [IMAPISession:: GetStatusTable](imapisession-getstatustable.md).
  
Chaque ligne de la table d'état représente un objet d'État implémenté par MAPI ou un fournisseur de services. Vous pouvez utiliser un objet Status pour afficher la feuille de propriétés de configuration d'un fournisseur, pour modifier le mot de passe d'un fournisseur, pour télécharger ou télécharger des messages et pour communiquer avec un fournisseur de transport particulier. 
  
Il existe deux façons d'accéder à un objet état:
  
- Via la table d'État
    
- Via la méthode **OpenStatusEntry** d'un objet d'ouverture de session 
    
Étant donné que les objets d'ouverture de session ne sont pas disponibles pour les clients, vous devez utiliser la table d'État pour accéder aux objets d'État. L'approche de table d'État est indirecte, ce qui nécessite quelques appels avant l'ouverture de l'objet d'État et un pointeur vers son implémentation **IMAPIStatus** renvoyée. 
  
 **Pour ouvrir un objet Status à l'aide de la table d'État**
  
1. Appelez **IMAPIStatus:: GetStatusTable** pour récupérer un pointeur [IMAPITable](imapitableiunknown.md) . 
    
2. Appelez la méthode [IMAPITable:: SetColumns](imapitable-setcolumns.md) de la table d'État pour limiter le jeu de colonnes à la valeur **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) et **PR_DISPLAY_NAME** ([ PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
    
3. Limitez l'affichage tableau à un objet d'état particulier. Pour les implémentations MAPI, un client peut définir une restriction de propriété à l'aide de **PR_RESOURCE_TYPE**. Pour les implémentations de fournisseurs de services, un client peut restreindre sur **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)), le nom du fournisseur ou **PR_PROVIDER_DLL_NAME** ([PIDTAGPROVIDERDLLNAME](pidtagproviderdllname-canonical-property.md)), le nom de la dll du fournisseur txt.
    
4. Appelez [IMAPITable:: Restrict](imapitable-restrict.md) pour définir la restriction. 
    
5. Appelez [HrQueryAllRows](hrqueryallrows.md), en transmettant la structure [SPropertyRestriction](spropertyrestriction.md) , pour récupérer la ligne qui représente l'état du fournisseur. 
    
6. Appelez [IMAPISession:: OpenEntry](imapisession-openentry.md), en spécifiant l'identificateur d'entrée dans la ligne table d'État, pour ouvrir l'objet Status et récupérer un pointeur **IMAPIStatus** . 
    
Pour afficher une feuille de propriétés, appelez la méthode [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) de l'objet Status pour le fournisseur cible. **SettingsDialog** affiche une feuille de propriétés pour l'affichage et, dans certains cas, la modification des propriétés de configuration d'un fournisseur. 
  
Pour communiquer avec un fournisseur de transport, appelez la méthode [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) de l'objet d'État. **ValidateState** permet de reconfigurer un fournisseur de transport, d'empêcher le fournisseur d'afficher une interface utilisateur et de contrôler une session qui implique le téléchargement des en-têtes des messages à partir d'un serveur distant, en fonction des indicateurs que vous transférez. Par exemple, pour annuler le téléchargement des en-têtes distants, transmettez l'indicateur ABORT_XP_HEADER_OPERATION à **ValidateState**. Pour vous connecter au serveur distant ou s'en déconnecter, transmettez FORCE_XP_CONNECT ou FORCE_XP_DISCONNECT. Pour reconfigurer le fournisseur, transmettez CONFIG_CHANGED. 
  
Les clients qui implémentent l'envoi ou la réception de messages à la demande appellent un fournisseur de transport ou la méthode [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) du spouleur MAPI. Vous pouvez transmettre trois indicateurs à la méthode: FLUSH_UPLOAD, FLUSH_DOWNLOAD et FLUSH_FORCE. FLUSH_UPLOAD indique au fournisseur ou au spouleur MAPI d'envoyer les messages en attente dans la file d'attente de sortie pendant que FLUSH_DOWNLOAD demande au fournisseur ou au spouleur MAPI de recevoir les messages entrants. FLUSH_FORCE peut être défini avec l'un des autres indicateurs pour que l'objet d'état effectue le vidage indépendamment du minutage. 
  
Ne vous attendez pas à pouvoir appeler **SettingsDialog** ou [ChangePassword](imapistatus-changepassword.md) sur l'un des objets du sous-système MAPI, le spouleur MAPI ou le carnet d'adresses. Les objets d'état de sous-système et de carnet d'adresses prennent en charge uniquement **ValidateState**; l'objet d'État du spouleur MAPI prend en charge **FlushQueues** en plus de **ValidateState**.
  
## <a name="see-also"></a>Voir aussi



[Tables d'État](status-tables.md)
  
[Objets d'État MAPI](mapi-status-objects.md)

