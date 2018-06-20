---
title: Recevoir des Tables de dossier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 5f3bcda3beb29fa91629ea1639522ef24dc6eb32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786970"
---
# <a name="receive-folder-tables"></a>Recevoir des Tables de dossier

  
  
**S’applique à**: Outlook 
  
Une table de dossier de réception contient des informations pour tous les dossiers désignés en tant que dossiers de réception pour une banque de messages. Un dossier de réception est un dossier où les messages entrants d’une classe de message particulier sont placés. Message d’implémentés par les fournisseurs de banque de recevoir des tables du dossier et applications clientes les utilisent en effectuant un appel à la méthode [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) . 
  
Le suivant propriétés constituent la colonne obligatoire recevoir des tables de dossier :
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 
  
 **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) 
  
 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

