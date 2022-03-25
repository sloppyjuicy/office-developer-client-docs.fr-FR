---
title: Tables de la boutique de messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: cdb7d8c5-8e35-47ff-8be7-2cb17e341ad3
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b91d2cc6f4af867f2ea631830651a19159c26e6c
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63780899"
---
# <a name="message-store-tables"></a>Tables de la boutique de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La table de la boutique de messages contient des informations sur les fournisseurs de magasins de messages dans le profil actuel. Il existe une table de magasin de messages pour chaque session MAPI, implémentée par MAPI et utilisée par les clients. Les clients peuvent utiliser cette table, par exemple, pour localiser toutes les instances d’un fournisseur particulier ou pour localiser une magasin de messages spécifique. 
  
La table de la boutique de messages est dynamique. Si l’utilisateur d’une application cliente modifie le profil, en modifiant la magasin de messages par défaut, par exemple, les valeurs des propriétés **PR_DEFAULT_STORE** des magasins de messages affectés sont immédiatement mises à jour. 
  
Les clients accèdent à la table de la boutique de messages en appelant la méthode [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) . 
  
Les propriétés suivantes définissent la colonne requise dans la table de la boutique de messages :
  
|Propriétés|Propriétés (suite)|
|:-----|:-----|
|**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

