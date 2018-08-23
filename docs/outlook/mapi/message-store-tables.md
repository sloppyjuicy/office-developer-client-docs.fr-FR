---
title: Tables de banques de messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cdb7d8c5-8e35-47ff-8be7-2cb17e341ad3
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 735c778cd8e6ccb41de3d3d8cb0fdc163493f712
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572017"
---
# <a name="message-store-tables"></a>Tables de banques de messages

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
La table contient des informations sur les fournisseurs de banque de messages dans le profil actif. Il existe une table de banque de messages pour chaque session MAPI, implémentés par MAPI et utilisé par les clients. Clients peuvent utiliser ce tableau, par exemple, pour rechercher toutes les instances d’un fournisseur spécifique ou pour localiser un message spécifique. 
  
La table est dynamique. Si l’utilisateur d’une application cliente modifie le profil, modification de la banque de messages par défaut, par exemple, les valeurs de l' **PR_DEFAULT_STORE** pour les banques de messages affectés sont immédiatement mises à jour. 
  
Clients accèdent à la table en appelant la méthode [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) . 
  
Les propriétés suivantes constituent la colonne requise dans la table de la banque de message :
  
|||
|:-----|:-----|
|**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

