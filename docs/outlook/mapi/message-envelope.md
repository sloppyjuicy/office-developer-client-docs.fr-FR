---
title: Enveloppe de message
manager: lindalu
ms.date: 09/14/2021
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 613956da-c49b-4836-9fde-4601510e8b89
description: 'Last modified: September 09, 2021'
ms.openlocfilehash: 787460bfbaebc6294f38dea4889cefec373c25a6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620442"
---
# <a name="message-envelope"></a>Enveloppe de message

**S’applique à** : Outlook 2013 | Outlook 2016
  
Les en-têtes RFC 822 sont mappés aux propriétés MAPI comme suit. PR_SENDER_ est \* une abréviation des 5 propriétés suivantes :
  
 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))
  
 **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))
  
 **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))
  
 **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))
  
 **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))
  
Des abréviations similaires sont utilisées pour PR_SENT_REPRESENTING_ \* et d’autres groupes de propriétés de message.
  
|**En-tête SMTP**|**Propriété MAPI**|
|:-----|:-----|
|De:  <br/> |Sortant : PR_SENDER_ \* ; entrant : PR_SENDER_ \* et PR_SENT_REPRESENTING_\*  <br/> |
|Date :  <br/> |Sortant : heure actuelle ; entrant : **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|À:  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) et **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) pour les destinataires pour PR_RECIPIENT_TYPE **(** [PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) est MAPI_TO  <br/> |
|Cc :  <br/> |**PR_DISPLAY_NAME** et **PR_EMAIL_ADDRESS** pour les destinataires **PR_RECIPIENT_TYPE’MAPI_CC**  <br/> |
|Bcc :  <br/> |**PR_DISPLAY_NAME** et **PR_EMAIL_ADDRESS** pour les destinataires **PR_RECIPIENT_TYPE’MAPI_BCC**  <br/> |
|||
|Reçu :  <br/> |Aucune propriété MAPI correspondante ; placer le nom d’hôte local et le nom de votre composant ici  <br/> |
|Return-receipt-to:  <br/> |**PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) et **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |
|Répondre à :  <br/> |**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) et **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |
|Objet:  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) Aucune limitation de longueur particulière.  <br/> |
|MIME-version :  <br/> |Toujours « 1.0 »  <br/> |
|||
|X-MS-Attachment :  <br/> |Pour la compatibilité avec la passerelle SMTP de messagerie MS. _filename taille mm-dd-yyy hh:mm_Details ci-dessous.  <br/> |
|||
| _enveloppe de message SMTP entière_ <br/> |**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))  <br/> |
|nom d’en-tête ÀD  <br/> |**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) _for expéditeur only._The TBDheader doit être utilisé pour déterminer si l’expéditeur est capable d’interpréter le contenu TNEF dans une réponse.  <br/> |
|MessageID :  <br/> |**PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))  <br/> |
|Content-type  <br/> |Texte/simple ou multipart/mixte. Voir la section « Contenu des messages ».  <br/> |
   
L’en-tête X-MS-Attachment est formaté sous la forme de quatre jetons, séparés par un espace :
  
 _date et heure de la taille du nom_
  
Le premier jeton est le nom de fichier, qui peut contenir des espaces incorporés, de sorte que cet en-tête doit être paré à partir de la droite sur les messages entrants. La taille est en octets ; la date est mise en  _forme mm-dd-yyyy et_ l’heure sous la forme  _hh:mm._
  
> [!NOTE]
> MessageID n’est pas mappé à **PR_SEARCH_KEY,** car le domaine SMTP a des exigences spécifiques sur le format de l’identificateur de message, ce qui rend impossible le code d’un identificateur de message MAPI arbitraire. Au lieu de cela, MessageID est mappé à **PR_TNEF_CORRELATION_KEY**. Cette propriété est une propriété définie par le transport qui est définie par le transport envoyant un message sortant et utilisée par un transport recevant un message entrant. Pour plus d’informations, [voir Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).
