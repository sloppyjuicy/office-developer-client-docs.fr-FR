---
title: Enveloppe de message
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 613956da-c49b-4836-9fde-4601510e8b89
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ccd14244bf7ee76396dc239437ca19f080edb170
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356923"
---
# <a name="message-envelope"></a>Enveloppe de message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les en-têtes RFC 822 sont mappés aux propriétés MAPI comme suit. PR_SENDER_\* est une abréviation pour les 5 propriétés suivantes:
  
 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))
  
 **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))
  
 **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))
  
 **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))
  
 **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))
  
Des abréviations similaires sont utilisées pour\* PR_SENT_REPRESENTING_ et d'autres groupes de propriétés de message.
  
|**En-tête SMTP**|**Propriété MAPI**|
|:-----|:-----|
|De:  <br/> |Sortant: PR_SENDER_\*; entrant: PR_SENDER_\* et PR_SENT_REPRESENTING_\*  <br/> |
|Jours  <br/> |Sortant: heure actuelle; entrant: **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|À:  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) et **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) pour les destinataires pour lesquels **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) est MAPI_TO  <br/> |
|CC  <br/> |**PR_DISPLAY_NAME** et **PR_EMAIL_ADDRESS** pour les destinataires pour lesquels **PR_RECIPIENT_TYPE** est MAPI_CC  <br/> |
|Cachée  <br/> |**PR_DISPLAY_NAME** et **PR_EMAIL_ADDRESS** pour les destinataires pour lesquels **PR_RECIPIENT_TYPE** est MAPI_BCC  <br/> |
|||
|Ont  <br/> |Aucune propriété MAPI correspondante; Placer le nom d'hôte local et le nom de votre composant ici  <br/> |
|Renvoyer-accusé de réception:  <br/> |**PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) et **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |
|Répondre à:  <br/> |**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) et **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |
|Objet:  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) Aucune limitation de longueur particulière.  <br/> |
|Version MIME:  <br/> |Toujours «1,0»  <br/> |
|||
|X-MS-Attachment:  <br/> |Pour la compatibilité avec la passerelle SMTP MS Mail. taille _FileName mm-dd-yyy hh: mm_Details ci-dessous.  <br/> |
|||
| _enveloppe de message SMTP entière_ <br/> |**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))  <br/> |
|nom d'en-tête TBD  <br/> |**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) _for de l'expéditeur uniquement. _The TBDheader doit être utilisé pour déterminer si l'expéditeur est capable d'interpréter le contenu TNEF dans une réponse.  <br/> |
|MessageID  <br/> |**PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))  <br/> |
|Content-type  <br/> |Text/plain ou multipart/mixed. Consultez la section «contenu du message».  <br/> |
   
L'en-tête X-MS-Attachment est mis en forme comme quatre jetons, séparés par un espace:
  
 _nom taille date heure_
  
Le premier jeton est le nom de fichier, qui peut contenir des espaces incorporés, de sorte que cet en-tête doit être analysé à partir de la droite sur les messages entrants. La taille est exprimée en octets; la date est au format _mm-jj-aaaa_ et l'heure est _hh: mm._
  
> [!NOTE]
> MessageID n'est pas mappé sur **PR_SEARCH_KEY** car le domaine SMTP a des exigences spécifiques sur le format de l'identificateur de message, ce qui rend impossible le codage d'un identificateur de message MAPI arbitraire. À la place, MessageID est mappé à **PR_TNEF_CORRELATION_KEY**. Cette propriété est une propriété définie par le transport qui est définie par le transport envoyant un message sortant et utilisée par un transport qui reçoit un message entrant. Pour plus d'informations, consultez [la rubrique développement d'un fournisseur de transport avec TNEF](developing-a-tnef-enabled-transport-provider.md). 
  

