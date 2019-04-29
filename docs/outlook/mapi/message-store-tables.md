---
title: Tables de banque de messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cdb7d8c5-8e35-47ff-8be7-2cb17e341ad3
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dd28c146f6b05b2dea03f73fab7131f23ca99e5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405351"
---
# <a name="message-store-tables"></a>Tables de banque de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La table de banque de messages contient des informations sur les fournisseurs de banques de messages dans le profil actuel. Il existe une table de banque de messages pour chaque session MAPI, implémentée par MAPI et utilisée par les clients. Les clients peuvent utiliser cette table, par exemple, pour rechercher toutes les instances d'un fournisseur particulier ou pour localiser une banque de messages spécifique. 
  
La table de banque de messages est dynamique. Si l'utilisateur d'une application cliente modifie le profil, en modifiant la Banque de messages par défaut, par exemple, les valeurs des propriétés **PR_DEFAULT_STORE** pour les banques de messages affectées sont immédiatement mises à jour. 
  
Les clients accèdent à la table de banque de messages en appelant la méthode [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) . 
  
Les propriétés suivantes constituent le jeu de colonnes obligatoire dans la table de banque de messages:
  
|||
|:-----|:-----|
|**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

