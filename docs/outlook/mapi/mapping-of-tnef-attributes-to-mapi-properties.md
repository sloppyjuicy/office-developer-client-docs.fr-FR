---
title: Mappage des attributs TNEF aux propriétés MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1a724fac-2e64-48a7-92b5-d7cf1528cb2c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 25647a6488fec9a39f8b41441fe9afc4c4aa0a7d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357651"
---
# <a name="mapping-of-tnef-attributes-to-mapi-properties"></a>Mappage des attributs TNEF aux propriétés MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le tableau suivant répertorie tous les attributs définis dans l'implémentation TNEF et leurs mappages aux propriétés MAPI. Dans certains cas, plusieurs propriétés MAPI sont codées sous la forme d'un attribut unique. Certains attributs ont des descriptions étendues plus loin dans cette section.
  
|**Attribut TNEF**|**Propriété ou propriétés MAPI**|
|:-----|:-----|
|**attAidOwner** <br/> |**PR_OWNER_APPT_ID** ([PidTagOwnerAppointmentId](pidtagownerappointmentid-canonical-property.md))  <br/> |
|**attAttachCreateDate** <br/> |**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |
|**attAttachData** <br/> |**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) ou **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md))  <br/> |
|**attAttachment** <br/> |Pour plus d'informations sur ce mappage, voir [attributs TNEF](tnef-attributes.md).  <br/> |
|**attAttachMetaFile** <br/> |**PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md))  <br/> |
|**attAttachModifyDate** <br/> |**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |
|**attAttachRenddata** <br/> |**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)), **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))  <br/> |
|**attAttachTitle** <br/> |**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md))  <br/> |
|**attAttachTransportFilename** <br/> |**PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))  <br/> |
|**attBody** <br/> |**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |
|**attConversationID** <br/> |**PR_CONVERSATION_KEY** ([PidTagConversationKey](pidtagconversationkey-canonical-property.md)) Cette propriété a été déconseillée dans Microsoft Exchange Server: son utilisation persiste dans Outlook uniquement, pour localiser **IPM. **Messages de MessageManager.  <br/> |
|**attDateEnd** <br/> |**PR_END_DATE** ([PidTagEndDate](pidtagenddate-canonical-property.md)) Pour plus d'informations, voir [attributs attDate](attdate-attributes.md) .  <br/> |
|**attDateModified** <br/> |**PR_LAST_MODIFICATION_TIME** Pour plus d'informations, voir [attributs attDate](attdate-attributes.md) .  <br/> |
|**attDateRecd** <br/> |**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) Pour plus d'informations, voir [attributs attDate](attdate-attributes.md) .  <br/> |
|**attDateSent** <br/> |**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) Pour plus d'informations, voir [attributs attDate](attdate-attributes.md) .  <br/> |
|**attDateStart** <br/> |**PR_START_DATE** ([PidTagStartDate](pidtagstartdate-canonical-property.md)) Pour plus d'informations, voir [attributs attDate](attdate-attributes.md) .  <br/> |
|**attFrom** <br/> |**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) et **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
|**attMAPIProps** <br/> |Pour plus d'informations sur cet attribut, voir [attMAPIProps](attmapiprops.md).  <br/> |
|**attMessageClass** <br/> |**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |
|**attMessageID** <br/> |**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) Consultez la rubrique relative [à la corrélation TNEF dans les transports et les passerelleS X. 400](tnef-correlation-in-x-400-gateways-and-transports.md).  <br/> |
|**attMessageStatus** <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**attOriginalMessageClass** <br/> |* * PR_ORIG_MESSAGE_CLASS * * ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md))  <br/> |
|**attOwner** <br/> |Voir [attOwner](attowner.md).  <br/> |
|**attParentID** <br/> |**PR_PARENT_KEY** (**PidTagParentKey**) Cette propriété a été déconseillée. Pour plus d'informations, consultez [la rubrique éléments d'API déconseillés dans cette édition](api-elements-deprecated-in-this-edition.md) .  <br/> |
|**attPriority** <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
|**attRecipTable** <br/> |**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |
|**attRequestRes** <br/> |**PR_RESPONSE_REQUESTED** ([PidTagResponseRequested](pidtagresponserequested-canonical-property.md))  <br/> |
|**attSentFor** <br/> |**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |
|**attSubject** <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   

