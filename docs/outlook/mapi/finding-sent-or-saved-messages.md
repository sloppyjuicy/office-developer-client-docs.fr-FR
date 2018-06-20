---
title: Recherche envoyé ou l’enregistrement des Messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b6714a5-7f36-4a72-9a2a-0d7fdf0e21b7
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 6e8b618e477475e8e7f45c266791086af63d8bfb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783318"
---
# <a name="finding-sent-or-saved-messages"></a>Recherche envoyé ou l’enregistrement des Messages

  
  
**S’applique à**: Outlook 
  
 **Pour rechercher tous les messages sortants que vous avez enregistré ou envoyé**
  
1. Appelez [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) pour comparer le dossier qui contient vos messages envoyés par le dossier qui contient les messages entrants. 
    
2. Définissez le paramètre _lpEntryID1_ pour pointer vers **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) et le paramètre _lpEntryID2_ pour pointer vers **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).
    
Sachez que si vous supprimer les messages après leur sont envoyés ou que vous ont déplacé des messages envoyés vers un autre dossier, cette stratégie ne fonctionne pas. 
  
Si en examinant un message entrant, vous constatez que les propriétés qui sont généralement définies par un fournisseur de transport sont manquantes, vous pouvez supposer que le message a été jamais géré par un fournisseur de transport. Ces propriétés sont les suivantes :
  
- Propriétés **PR_RECEIVED_BY** 
    
- **PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))
    
- **PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))
    
- **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))
    
- **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))
    
- **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))
    

