---
title: Table de statut et objets de statut
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 203765c1-4b08-4032-a5bf-18f3e752a899
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7ebd0c21a43ddb1deb01699f0ddf77d319216a4d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590063"
---
# <a name="status-table-and-status-objects"></a>Table de statut et objets de statut

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
MAPI fournit un tableau avec des informations sur l’état du sous-système MAPI, spouleur MAPI, carnet d’adresses ou un fournisseur de services. Vous pouvez accéder à ce tableau en appelant [IMAPISession::GetStatusTable](imapisession-getstatustable.md).
  
Chaque ligne dans la table d’état représente un objet de statut implémenté par MAPI ou un fournisseur de services. Vous pouvez utiliser un objet d’état pour afficher la feuille de propriétés de configuration d’un fournisseur, pour modifier un mot de passe fournisseur, de télécharger des messages des et de communiquer avec un fournisseur de transport spécifique. 
  
Il existe deux façons d’accéder à un objet d’état :
  
- Par le biais de la table d’état
    
- Via la méthode **OpenStatusEntry** de l’objet d’une ouverture de session 
    
Étant donné que les objets d’ouverture de session ne sont pas disponibles pour les clients, vous devez utiliser la table d’état pour accéder aux objets de l’état. L’approche de table d’état est indirect, nécessitant quelques appels avant de l’objet de l’état est ouvert et un pointeur vers son implémentation **IMAPIStatus** renvoyé. 
  
 **Pour utiliser la table d’état pour ouvrir un objet d’état**
  
1. Appelez **IMAPIStatus::GetStatusTable** pour récupérer un pointeur [IMAPITable](imapitableiunknown.md) . 
    
2. Appeler la méthode de [IMAPITable::SetColumns](imapitable-setcolumns.md) de la table d’état pour limiter la colonne valeur **PR_DISPLAY_NAME** ([ **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) et **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
    
3. Limiter l’affichage de tableau à un objet état particulier. Pour des implémentations MAPI, un client peut définir une restriction de propriété à l’aide de **PR_RESOURCE_TYPE**. Pour les implémentations de fournisseur de service, un client peut restreindre sur **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)), le nom du fournisseur, ou sur **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)), le nom de la DLL du fournisseur fichier.
    
4. Appelez [IMAPITable](imapitable-restrict.md) pour définir la restriction. 
    
5. Appelez [HrQueryAllRows](hrqueryallrows.md), en passant la structure [SPropertyRestriction](spropertyrestriction.md) , pour récupérer la ligne qui représente l’état du fournisseur. 
    
6. Appelez [IMAPISession::OpenEntry](imapisession-openentry.md), spécifiant l’identificateur d’entrée à partir de la ligne de tableau d’état, pour ouvrir l’objet de l’état et de récupérer un pointeur **IMAPIStatus** . 
    
Pour afficher une feuille de propriétés, appeler la méthode [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) de l’objet état pour le fournisseur cible. **Dialogue** affiche une feuille de propriétés pour l’affichage et dans certains cas, modifier les propriétés de configuration d’un fournisseur. 
  
Pour communiquer avec un fournisseur de transport, appelez la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) de l’objet de son état. **ValidateState** pouvez reconfigurer un fournisseur de transport, empêcher le fournisseur d’afficher une interface utilisateur et contrôler une session impliquant le téléchargement des en-têtes des messages à partir d’un serveur distant, selon les indicateurs que vous passez. Pour annuler le téléchargement des en-têtes à distance, par exemple, passez l’indicateur ABORT_XP_HEADER_OPERATION à **ValidateState**. Pour se connecter ou se déconnecter du serveur distant, transmettez FORCE_XP_CONNECT ou FORCE_XP_DISCONNECT. Pour reconfigurer le fournisseur, transmettez CONFIG_CHANGED. 
  
Les clients qui implémentent l’envoi ou la réception de messages à la demande appellent soit un fournisseur de transport ou du spouleur MAPI [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) . Vous pouvez passer des trois indicateurs dans la méthode : FLUSH_UPLOAD, FLUSH_DOWNLOAD et FLUSH_FORCE. FLUSH_UPLOAD indique le fournisseur ou le spouleur MAPI pour envoyer des messages en attente dans la file d’attente de sortie, tandis que FLUSH_DOWNLOAD indique au fournisseur ou le spouleur MAPI qui recevra les messages entrants. FLUSH_FORCE peut être définie avec une des autres indicateurs à l’objet d’état effectuer le vidage, quel que soit le minutage. 
  
Ne pensez pas pouvoir appeler **dialogue** ou [ChangePassword](imapistatus-changepassword.md) sur n’importe quel le sous-système MAPI, spouleur MAPI ou l’adresse, objets d’état book. Objets d’état book le sous-système et l’adresse prennent uniquement en charge **ValidateState**; l’objet d’état spouleur MAPI prend en charge **FlushQueues** outre **ValidateState**.
  
## <a name="see-also"></a>Voir aussi



[Tables des états](status-tables.md)
  
[Objets d’état MAPI](mapi-status-objects.md)

