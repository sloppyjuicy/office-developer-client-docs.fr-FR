---
title: Recherche des messages envoyés ou enregistrés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 6b6714a5-7f36-4a72-9a2a-0d7fdf0e21b7
ms.openlocfilehash: 80e24ec3893b0cebe7082bd118fab93c88627e54
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63520720"
---
# <a name="finding-sent-or-saved-messages"></a>Recherche des messages envoyés ou enregistrés

**S’applique à** : Outlook 2013 | Outlook 2016
  
 **Pour localiser tous les messages sortants que vous avez enregistrés ou envoyés**
  
1. [Appelez IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) pour comparer le dossier qui contient vos messages envoyés avec le dossier qui contient vos messages entrants.

2. Définissez le paramètre _lpEntryID1_ sur **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) et le paramètre _lpEntryID2_ sur **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).

N’ignorez pas que si vous supprimez des messages après leur envoi ou que vous les avez déplacés vers un autre dossier, cette stratégie ne fonctionne pas.
  
Si, lors de l’examen d’un message entrant, vous remarquez que les propriétés généralement définies par un fournisseur de transport sont manquantes, vous pouvez supposer que le message n’a jamais été géré par un fournisseur de transport. Ces propriétés sont les suivantes :
  
- **PR_RECEIVED_BY** propriétés

- **PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))

- **PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))

- **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))

- **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))

- **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))
