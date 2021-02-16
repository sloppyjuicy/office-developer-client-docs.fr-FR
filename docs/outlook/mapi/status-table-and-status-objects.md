---
title: Table d’état et objets d’état
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 203765c1-4b08-4032-a5bf-18f3e752a899
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3eb190069b43ea1960c3b6edf30a9e0b782d2c41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425175"
---
# <a name="status-table-and-status-objects"></a>Table d’état et objets d’état

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI fournit un tableau avec des informations sur l’état du sous-système MAPI, dupooler MAPI, du carnet d’adresses ou d’un fournisseur de services particulier. Vous pouvez accéder à ce tableau en appelant [IMAPISession::GetStatusTable](imapisession-getstatustable.md).
  
Chaque ligne de la table d’état représente un objet d’état implémenté par MAPI ou un fournisseur de services. Vous pouvez utiliser un objet d’état pour afficher la feuille des propriétés de configuration d’un fournisseur, pour modifier un mot de passe de fournisseur, pour télécharger ou télécharger des messages et pour communiquer avec un fournisseur de transport particulier. 
  
Il existe deux façons d’accéder à un objet d’état :
  
- Par le biais du tableau d’état
    
- Via la méthode **OpenStatusEntry** d’un objet d’ouverture de ouvert 
    
Étant donné que les objets d’accès sont indisponibles pour les clients, vous devez utiliser la table d’état pour accéder aux objets d’état. L’approche de la table d’état est indirecte, nécessitant quelques appels avant l’ouverture de l’objet d’état et le retour d’un pointeur vers son **implémentation IMAPIStatus.** 
  
 **Pour utiliser la table d’état pour ouvrir un objet d’état**
  
1. Appelez **IMAPIStatus::GetStatusTable** pour récupérer un [pointeur IMAPITable.](imapitableiunknown.md) 
    
2. Appelez la méthode [IMAPITable::SetColumns](imapitable-setcolumns.md) de la table d’état pour limiter le jeu de colonnes à **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) et **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
    
3. Limitez l’affichage Tableau à un objet d’état particulier. Pour les implémentations MAPI, un client peut définir une restriction de propriété à l’aide **PR_RESOURCE_TYPE**. Pour les implémentations de fournisseur de services, un client peut restreindre sur **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)), le nom du fournisseur, ou sur **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)), le nom du fichier DLL du fournisseur.
    
4. Appelez [IMAPITable::Restrict](imapitable-restrict.md) pour définir la restriction. 
    
5. Appelez [HrQueryAllRows,](hrqueryallrows.md)en passant la structure [SPropertyRestriction,](spropertyrestriction.md) pour récupérer la ligne qui représente l’état du fournisseur. 
    
6. Appelez [IMAPISession::OpenEntry](imapisession-openentry.md), en spécifiant l’identificateur d’entrée à partir de la ligne de table d’état, pour ouvrir l’objet d’état et récupérer un pointeur **IMAPIStatus.** 
    
Pour afficher une feuille de propriétés, appelez la méthode [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) de l’objet d’état pour le fournisseur cible. **SettingsDialog affiche une** feuille de propriétés pour l’affichage et, dans certains cas, la modification des propriétés de configuration d’un fournisseur. 
  
Pour communiquer avec un fournisseur de transport, appelez la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) de son objet d’état. **ValidateState** peut reconfigurer un fournisseur de transport, l’empêcher d’afficher une interface utilisateur et contrôler une session qui implique le téléchargement d’en-têtes de message à partir d’un serveur distant, en fonction des indicateurs que vous passez. Par exemple, pour annuler le téléchargement des en-têtes distants, passez l’ABORT_XP_HEADER_OPERATION à **ValidateState**. Pour vous connecter ou vous déconnecter du serveur distant, FORCE_XP_CONNECT ou FORCE_XP_DISCONNECT. Pour reconfigurer le fournisseur, passez CONFIG_CHANGED. 
  
Les clients qui implémentent l’envoi ou la réception de messages à la demande appellent la méthode [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) d’un fournisseur de transport ou dupooler MAPI. Vous pouvez passer trois indicateurs dans la méthode : FLUSH_UPLOAD, FLUSH_DOWNLOAD et FLUSH_FORCE. FLUSH_UPLOAD demande au fournisseur ou aupooler MAPI d’envoyer tous les messages en attente dans la file d’attente de sortie pendant que FLUSH_DOWNLOAD demande au fournisseur ou aupooler MAPI de recevoir les messages entrants. FLUSH_FORCE peut être définie avec l’un des autres indicateurs pour que l’objet d’état effectue le purge indépendamment du minutage. 
  
Ne vous attendez pas à pouvoir appeler **SettingsDialog** ou [ChangePassword](imapistatus-changepassword.md) sur l’un des objets d’état du sous-système MAPI, dupooler MAPI ou du carnet d’adresses. Les objets d’état du sous-système et du carnet d’adresses ne peuvent prendre en charge **que ValidateState**; l’objet d’état dupooler MAPI prend en charge **FlushQueues** en plus de **ValidateState**.
  
## <a name="see-also"></a>Voir aussi



[Tables d’état](status-tables.md)
  
[Objets d’état MAPI](mapi-status-objects.md)

