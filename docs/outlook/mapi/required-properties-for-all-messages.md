---
title: Propriétés requises pour tous les Messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: df7e122f-0c44-4d81-8174-3a2d51671ba9
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ebe4622ec9ed25be5ee8a736ed15e2f230ff05e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787016"
---
# <a name="required-properties-for-all-messages"></a>Propriétés requises pour tous les Messages

  
  
**S’applique à**: Outlook 
  
Le tableau suivant décrit les propriétés dont les clients peuvent bénéficier de définir ou de voir pris en charge sur les messages de toutes les classes.
  
|**Propriété**|**Description**|
|:-----|:-----|
|**PR_CREATION_TIME** [Propriété canonique PidTagCreationTime](pidtagcreationtime-canonical-property.md) ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |Définis par le fournisseur de banque de messages pour les messages sortants.  <br/> |
|**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))  <br/> **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |Définis par le fournisseur de banque de messages pour les messages sortants.  <br/> |
|||
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Définis par le fournisseur de banque de messages pour les messages sortants.  <br/> |
|**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |Définis par le fournisseur de banque de messages pour les messages sortants.  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Définis par le fournisseur de banque de messages pour les messages sortants.  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Peut être définie par les clients pour les messages sortants ; doivent être définis par le fournisseur de banque de message si n’est pas défini par les clients.  <br/> |
|**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |Définies par les clients pour les messages sortants avant qu’elles sont enregistrées et les fournisseurs de magasins de message après que qu’ils sont enregistrés.  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |Définis par le fournisseur de banque de messages pour les messages sortants.  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |Définis par le fournisseur de banque de messages pour les messages sortants.  <br/> |
|**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))  <br/> **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))  <br/> |Définis par le fournisseur de transport sur les messages entrants.  <br/> |
|||
|**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |Définis par le fournisseur de banque de messages pour les messages sortants  <br/> |
|**PR_ORIGINATOR_AND_DL_EXPANSION_HISTORY** ([PidTagOriginatorAndDistributionListExpansionHistory](pidtagoriginatoranddistributionlistexpansionhistory-canonical-property.md))  <br/> **PR_ORIGINATOR_CERTIFICATE** ([PidTagOriginatorCertificate](pidtagoriginatorcertificate-canonical-property.md))  <br/> **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))  <br/> **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md))  <br/> **PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT** ([PidTagOriginatorRequestedAlternateRecipient](pidtagoriginatorrequestedalternaterecipient-canonical-property.md))  <br/> **PR_ORIGINATOR_RETURN_ADDRESS** ([PidTagOriginatorReturnAddress](pidtagoriginatorreturnaddress-canonical-property.md))  <br/> |Définis par le fournisseur de transport pour les messages sortants.  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md))  <br/> |Définis par le fournisseur de banque de messages pour les messages sortants.  <br/> |
|||
|**PR_RCVD_REPRESENTING_ADDRTYPE** ([PidTagReceivedRepresentingAddressType](pidtagreceivedrepresentingaddresstype-canonical-property.md))  <br/> **PR_RCVD_REPRESENTING_EMAIL_ADDRESS** ([PidTagReceivedRepresentingEmailAddress](pidtagreceivedrepresentingemailaddress-canonical-property.md))  <br/> **PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))  <br/> **PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))  <br/> **PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))  <br/> |Définis par le fournisseur de transport sur les messages entrants.  <br/> |
|**PR_RECEIVED_BY_ADDRTYPE** ([PidTagReceivedByAddressType](pidtagreceivedbyaddresstype-canonical-property.md))  <br/> **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md))  <br/> **PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md))  <br/> **PR_RECEIVED_BY_NAME** ([PidTagReceivedByName](pidtagreceivedbyname-canonical-property.md))  <br/> **PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md))  <br/> |Définis par le fournisseur de transport sur les messages entrants.  <br/> |
|**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))  <br/> |Définis par le fournisseur de banque de messages sur les messages entrants.  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Définis par le fournisseur de banque de messages pour les messages sortants.  <br/> |
|**Clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Définis par le fournisseur de banque de messages pour les messages sortants.  <br/> |
|**PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))  <br/> **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))  <br/> **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))  <br/> **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))  <br/> |Clients peuvent définir ces propriétés dans les messages sortants, mais doivent les définir des fournisseurs de transport.  <br/> |
|**PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md))  <br/> **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md))  <br/> **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))  <br/> |Clients peuvent définir ces propriétés dans les messages sortants, mais doivent les définir des fournisseurs de transport.  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Définis par le fournisseur de banque de messages pour les messages sortants.  <br/> |
   

