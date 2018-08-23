---
title: Tables de dossiers de réception
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b88545ede6275bd834fad5869d972e2860a6c77e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573179"
---
# <a name="receive-folder-tables"></a>Tables de dossiers de réception

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Une table de dossier de réception contient des informations pour tous les dossiers désignés en tant que dossiers de réception pour une banque de messages. Un dossier de réception est un dossier où les messages entrants d’une classe de message particulier sont placés. Message d’implémentés par les fournisseurs de banque de recevoir des tables du dossier et applications clientes les utilisent en effectuant un appel à la méthode [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) . 
  
Le suivant propriétés constituent la colonne obligatoire recevoir des tables de dossier :
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 
  
 **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) 
  
 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

