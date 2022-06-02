---
title: Tables du Magasin de messages
description: La table du magasin de messages contient des informations sur les fournisseurs de magasins de messages dans le profil actuel. Il existe une table de magasin de messages pour chaque session MAPI.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: cdb7d8c5-8e35-47ff-8be7-2cb17e341ad3
ms.openlocfilehash: bf0c8f48259e098c4ac405aaad67f43c91e19679
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828191"
---
# <a name="message-store-tables"></a>Tables du Magasin de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La table du magasin de messages contient des informations sur les fournisseurs de magasins de messages dans le profil actuel. Il existe une table de magasin de messages pour chaque session MAPI, implémentée par MAPI et utilisée par les clients. Les clients peuvent utiliser cette table, par exemple, pour localiser toutes les instances d’un fournisseur particulier ou pour localiser un magasin de messages spécifique. 
  
La table du magasin de messages est dynamique. Si l’utilisateur d’une application cliente modifie le profil, en modifiant le magasin de messages par défaut, par exemple, les valeurs des propriétés **PR_DEFAULT_STORE** pour les magasins de messages affectés sont immédiatement mises à jour. 
  
Les clients accèdent à la table du magasin de messages en appelant la méthode [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) . 
  
Les propriétés suivantes constituent l’ensemble de colonnes requis dans la table du magasin de messages :
  
|Propriétés|Propriétés (suite)|
|:-----|:-----|
|**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

