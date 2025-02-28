---
title: Propriétés requises pour tous les messages
description: Décrit les propriétés dans Outlook 2013 et Outlook 2016 que les clients peuvent s’attendre à définir ou à voir prises en charge sur les messages de toutes les classes.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: df7e122f-0c44-4d81-8174-3a2d51671ba9
ms.openlocfilehash: 216eb34a6239eeaf38df76e5f500fa04b90a3103
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894543"
---
# <a name="required-properties-for-all-messages"></a>Propriétés requises pour tous les messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le tableau suivant décrit les propriétés que les clients peuvent s’attendre à définir ou à voir prises en charge sur les messages de toutes les classes.
  
|**Propriété**|**Description**|
|:-----|:-----|
|**PR_CREATION_TIME**[Propriété canonique PidTagCreationTime](pidtagcreationtime-canonical-property.md) ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |Défini par les fournisseurs de magasins de messages sur les messages sortants. |
|**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))  <br/> **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |Défini par les fournisseurs de magasins de messages sur les messages sortants. |
|||
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Défini par les fournisseurs de magasins de messages sur les messages sortants. |
|**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |Défini par les fournisseurs de magasins de messages sur les messages sortants. |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Défini par les fournisseurs de magasins de messages sur les messages sortants. |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Peut être défini par les clients sur les messages sortants ; doit être défini par les fournisseurs de magasins de messages s’ils ne sont pas définis par les clients. |
|**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |Défini par les clients sur les messages sortants avant qu’ils ne soient enregistrés et les fournisseurs de magasins de messages après leur enregistrement. |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |Défini par les fournisseurs de magasins de messages sur les messages sortants. |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |Défini par les fournisseurs de magasins de messages sur les messages sortants. |
|**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))  <br/> **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))  <br/> |Défini par les fournisseurs de transport sur les messages entrants. |
|||
|**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |Défini par les fournisseurs de magasins de messages sur les messages sortants  <br/> |
|**PR_ORIGINATOR_AND_DL_EXPANSION_HISTORY** ([PidTagOriginatorAndDistributionListExpansionHistory](pidtagoriginatoranddistributionlistexpansionhistory-canonical-property.md))  <br/> **PR_ORIGINATOR_CERTIFICATE** ([PidTagOriginatorCertificate](pidtagoriginatorcertificate-canonical-property.md))  <br/> **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))  <br/> **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md))  <br/> **PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT** ([PidTagOriginatorRequestedAlternateRecipient](pidtagoriginatorrequestedalternaterecipient-canonical-property.md))  <br/> **PR_ORIGINATOR_RETURN_ADDRESS** ([PidTagOriginatorReturnAddress](pidtagoriginatorreturnaddress-canonical-property.md))  <br/> |Défini par les fournisseurs de transport sur les messages sortants. |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md))  <br/> |Défini par les fournisseurs de magasins de messages sur les messages sortants. |
|||
|**PR_RCVD_REPRESENTING_ADDRTYPE** ([PidTagReceivedRepresentingAddressType](pidtagreceivedrepresentingaddresstype-canonical-property.md))  <br/> **PR_RCVD_REPRESENTING_EMAIL_ADDRESS** ([PidTagReceivedRepresentingEmailAddress](pidtagreceivedrepresentingemailaddress-canonical-property.md))  <br/> **PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))  <br/> **PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))  <br/> **PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))  <br/> |Défini par les fournisseurs de transport sur les messages entrants. |
|**PR_RECEIVED_BY_ADDRTYPE** ([PidTagReceivedByAddressType](pidtagreceivedbyaddresstype-canonical-property.md))  <br/> **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md))  <br/> **PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md))  <br/> **PR_RECEIVED_BY_NAME** ([PidTagReceivedByName](pidtagreceivedbyname-canonical-property.md))  <br/> **PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md))  <br/> |Défini par les fournisseurs de transport sur les messages entrants. |
|**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))  <br/> |Défini par les fournisseurs de magasins de messages sur les messages entrants. |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Défini par les fournisseurs de magasins de messages sur les messages sortants. |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Défini par les fournisseurs de magasins de messages sur les messages sortants. |
|**PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))  <br/> **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))  <br/> **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))  <br/> **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))  <br/> |Les clients peuvent définir ces propriétés sur les messages sortants, mais les fournisseurs de transport doivent les définir. |
|**PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md))  <br/> **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md))  <br/> **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))  <br/> |Les clients peuvent définir ces propriétés sur les messages sortants, mais les fournisseurs de transport doivent les définir. |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Défini par les fournisseurs de magasins de messages sur les messages sortants. |
   

