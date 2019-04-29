---
title: Recherche de messages envoyés ou enregistrés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b6714a5-7f36-4a72-9a2a-0d7fdf0e21b7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 86373fae2753df66d4456cc0fc00f8b289977650
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437419"
---
# <a name="finding-sent-or-saved-messages"></a>Recherche de messages envoyés ou enregistrés

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 **Pour localiser tous les messages sortants enregistrés ou envoyés**
  
1. Appelez [IMsgStore:: CompareEntryIDs](imsgstore-compareentryids.md) pour comparer le dossier qui contient les messages envoyés avec le dossier qui contient vos messages entrants. 
    
2. Définissez le paramètre _lpEntryID1_ de sorte qu'il pointe vers **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) et le paramètre _lpEntryID2_ de pointer vers **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).
    
N'oubliez pas que si vous supprimez des messages après les avoir envoyés ou si vous les avez déplacés vers un autre dossier, cette stratégie ne fonctionnera pas. 
  
Si, lors de l'examen d'un message entrant, vous remarquez que les propriétés qui sont généralement définies par un fournisseur de transport sont manquantes, vous pouvez supposer que le message n'a jamais été géré par un fournisseur de transport. Ces propriétés sont les suivantes :
  
- Propriétés **PR_RECEIVED_BY** 
    
- **PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))
    
- **PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))
    
- **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))
    
- **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))
    
- **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))
    

