---
title: Propriétés de message de rapport requises
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 68b14538-332d-4bdb-9a5c-8bb27272e089
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: d42bcf531c09ca2486b0181b86bae72e223d2007
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577162"
---
# <a name="required-report-message-properties"></a>Propriétés de message de rapport requises

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Le tableau suivant décrit les propriétés clients peuvent s’attendre à voir pris en charge sur les messages d’état.
  
|**Propriété**|**Description**|
|:-----|:-----|
|**PR_ORIGINAL_DISPLAY_BCC** ([PidTagOriginalDisplayBcc](pidtagoriginaldisplaybcc-canonical-property.md))  <br/> **PR_ORIGINAL_DISPLAY_CC** ([PidTagOriginalDisplayCc](pidtagoriginaldisplaycc-canonical-property.md))  <br/> **PR_ORIGINAL_DISPLAY_TO** ([PidTagOriginalDisplayTo](pidtagoriginaldisplayto-canonical-property.md))  <br/> |Défini par le créateur du rapport, généralement MAPI.  <br/> |
|||
|**PR_ORIGINAL_SUBJECT** ([PidTagOriginalSubject](pidtagoriginalsubject-canonical-property.md))  <br/> |Défini par le créateur du rapport, généralement MAPI.  <br/> |
|**PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md))  <br/> |Défini par le créateur du rapport, généralement MAPI.  <br/> |
|**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))  <br/> |Défini par le créateur du rapport, généralement MAPI.  <br/> |
|||
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Défini par le créateur du rapport, généralement MAPI.  <br/> |
|**PR_REPORT_TEXT** ([PidTagReportText](pidtagreporttext-canonical-property.md))  <br/> |Défini par le créateur du rapport, généralement MAPI.  <br/> |
|**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |Défini par le client avant l’affichage de rapport.  <br/> |
|**PR_REPORT_TIME** ([PidTagReportTime](pidtagreporttime-canonical-property.md))  <br/> |Défini par le créateur du rapport, généralement MAPI.  <br/> |
|**PR_ORIGINAL_DELIVERY_TIME** ([PidTagOriginalDeliveryTime](pidtagoriginaldeliverytime-canonical-property.md))  <br/> |Défini par le créateur du rapport, généralement MAPI. Pour les rapports d’état de lecture uniquement.  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Défini par le client avant l’affichage de rapport.  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |Défini par le créateur du rapport, généralement MAPI.  <br/> |
|**PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md))  <br/> |Défini par le créateur du rapport, généralement MAPI.  <br/> |
|**Clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Défini par le créateur du rapport, généralement MAPI.  <br/> |
|**PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))  <br/> **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))  <br/> **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))  <br/> **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))  <br/> |Défini par le créateur du rapport, généralement MAPI.  <br/> |
   

