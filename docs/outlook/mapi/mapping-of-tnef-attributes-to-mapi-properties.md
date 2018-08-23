---
title: Mappage d’attributs TNEF aux propriétés MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1a724fac-2e64-48a7-92b5-d7cf1528cb2c
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 810895836ea4d9e4aa82c189f68d13eefd409163
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568727"
---
# <a name="mapping-of-tnef-attributes-to-mapi-properties"></a>Mappage d’attributs TNEF aux propriétés MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Le tableau suivant répertorie tous les attributs définis dans l’implémentation de TNEF et leurs mappages sur les propriétés MAPI. Dans certains cas, plusieurs propriétés MAPI sont codées en tant qu’attribut unique. Certains attributs ont étendues descriptions plus loin dans cette section.
  
|**Attribut TNEF**|**La propriété MAPI ou des propriétés**|
|:-----|:-----|
|**attAidOwner** <br/> |**Propriété PR_OWNER_APPT_ID** ([PidTagOwnerAppointmentId](pidtagownerappointmentid-canonical-property.md))  <br/> |
|**attAttachCreateDate** <br/> |**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |
|**attAttachData** <br/> |**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) ou **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md))  <br/> |
|**attAttachment** <br/> |Pour plus d’informations sur ce mappage, voir [Attributs TNEF](tnef-attributes.md).  <br/> |
|**attAttachMetaFile** <br/> |**PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md))  <br/> |
|**attAttachModifyDate** <br/> |**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |
|**attAttachRenddata** <br/> |**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)), **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))  <br/> |
|**attAttachTitle** <br/> |**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md))  <br/> |
|**attAttachTransportFilename** <br/> |**PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))  <br/> |
|**attBody** <br/> |**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |
|**attConversationID** <br/> |**PR_CONVERSATION_KEY** ([PidTagConversationKey](pidtagconversationkey-canonical-property.md)) Cette propriété a été déconseillée dans Microsoft Exchange Server : son utilisation persiste dans Outlook uniquement, qui permettent de rechercher **IPM. MessageManager** messages.  <br/> |
|**attDateEnd** <br/> |**PR_END_DATE** ([PidTagEndDate](pidtagenddate-canonical-property.md)) Pour plus d’informations, consultez [attributs attDate](attdate-attributes.md) .  <br/> |
|**attDateModified** <br/> |**PR_LAST_MODIFICATION_TIME** Pour plus d’informations, consultez [attributs attDate](attdate-attributes.md) .  <br/> |
|**attDateRecd** <br/> |**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) Pour plus d’informations, consultez [attributs attDate](attdate-attributes.md) .  <br/> |
|**attDateSent** <br/> |**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) Pour plus d’informations, consultez [attributs attDate](attdate-attributes.md) .  <br/> |
|**attDateStart** <br/> |**PR_START_DATE** ([PidTagStartDate](pidtagstartdate-canonical-property.md)) Pour plus d’informations, consultez [attributs attDate](attdate-attributes.md) .  <br/> |
|**attFrom** <br/> |**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) et **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
|**attMAPIProps** <br/> |Pour plus d’informations sur cet attribut, voir [attMAPIProps](attmapiprops.md).  <br/> |
|**attMessageClass** <br/> |**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |
|**attMessageID** <br/> |**Clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) Voir [corrélation TNEF dans les passerelles X.400 et des Transports](tnef-correlation-in-x-400-gateways-and-transports.md).  <br/> |
|**attMessageStatus** <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**attOriginalMessageClass** <br/> |** PR_ORIG_MESSAGE_CLASS ** ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md))  <br/> |
|**attOwner** <br/> |Voir [attOwner](attowner.md).  <br/> |
|**attParentID** <br/> |**PR_PARENT_KEY** (**PidTagParentKey**) Cette propriété est déconseillée. Pour plus d’informations, voir [API éléments déconseillée dans cette édition](api-elements-deprecated-in-this-edition.md) .  <br/> |
|**attPriority** <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
|**attRecipTable** <br/> |**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |
|**attRequestRes** <br/> |**PR_RESPONSE_REQUESTED** ([PidTagResponseRequested](pidtagresponserequested-canonical-property.md))  <br/> |
|**attSentFor** <br/> |**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |
|**attSubject** <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   

