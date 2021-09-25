---
title: Recherche des messages envoyés ou enregistrés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 6b6714a5-7f36-4a72-9a2a-0d7fdf0e21b7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 77d7173a6a62a375108f0d8bcffa3b99237417b2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587999"
---
# <a name="finding-sent-or-saved-messages"></a>Recherche des messages envoyés ou enregistrés

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 **Pour localiser tous les messages sortants que vous avez enregistrés ou envoyés**
  
1. Appelez [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) pour comparer le dossier qui contient vos messages envoyés avec le dossier qui contient vos messages entrants. 
    
2. Définissez le paramètre  _lpEntryID1_ pour qu’il pointe vers **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) et le paramètre  _lpEntryID2_ pour pointer vers **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).
    
N’ignorez pas que si vous supprimez des messages après leur envoi ou que vous avez déplacé l’un des messages envoyés vers un autre dossier, cette stratégie ne fonctionne pas. 
  
Si, lors de l’examen d’un message entrant, vous remarquez que les propriétés généralement définies par un fournisseur de transport sont manquantes, vous pouvez supposer que le message n’a jamais été géré par un fournisseur de transport. Ces propriétés sont les suivantes :
  
- **PR_RECEIVED_BY** propriétés 
    
- **PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))
    
- **PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))
    
- **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))
    
- **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))
    
- **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))
    

