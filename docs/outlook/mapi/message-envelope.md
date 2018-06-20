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
ms.openlocfilehash: bbdc5993a07209f381065ce1b60f860ba54c35d5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784894"
---
# <a name="message-envelope"></a>Enveloppe de message

  
  
**S’applique à**: Outlook 
  
En-têtes RFC 822 sont mappées sur des propriétés MAPI comme suit. PR_SENDER_\* est l’abréviation de 5 propriétés suivantes :
  
 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))
  
 **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))
  
 **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))
  
 **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))
  
 **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))
  
Les abréviations similaires sont utilisées pour PR_SENT_REPRESENTING_\* et d’autres groupes de propriétés de message.
  
|**En-tête SMTP**|**Propriété MAPI**|
|:-----|:-----|
|De :  <br/> |Sortant : PR_SENDER_\*; entrant : PR_SENDER_\* et PR_SENT_REPRESENTING_\*  <br/> |
|Date :  <br/> |Sortant : heure actuelle ; entrant : **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|À :  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) et **ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) pour les destinataires dont **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) est MAPI_TO  <br/> |
|Cc :  <br/> |**PR_DISPLAY_NAME** et **ADRESSE_EMAIL_PR** pour les destinataires dont **PR_RECIPIENT_TYPE** est ni  <br/> |
|Cci :  <br/> |**PR_DISPLAY_NAME** et **ADRESSE_EMAIL_PR** pour les destinataires dont **PR_RECIPIENT_TYPE** est MAPI_BCC  <br/> |
|||
|Reçus :  <br/> |Aucune propriété MAPI correspondante. Placez ici le nom d’hôte local et votre nom de composant  <br/> |
|Réception de retour pour :  <br/> |**PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) et **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |
|Répondre à :  <br/> |**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) et **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |
|Objet :  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) Aucune limite de longueur spécifique.  <br/> |
|Version MIME :  <br/> |Toujours « 1.0 »  <br/> |
|||
|X-MS-Attachment :  <br/> |Pour assurer la compatibilité avec la passerelle MS Mail SMTP. _filename taille mm-jj-yyy hh:mm_Details ci-dessous.  <br/> |
|||
| _enveloppe de message SMTP entière_ <br/> |**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))  <br/> |
|TBD de nom d’en-tête  <br/> |**PR_SEND_RICH_INFO** ._The uniquement ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) _for expéditeur TBDheader doit être utilisé pour déterminer si l’expéditeur est capable d’interpréter le contenu TNEF dans une réponse.  <br/> |
|Identificateur du message :  <br/> |**PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))  <br/> |
|Content-type  <br/> |Texte/ordinaire ou mixte/multipartie. Consultez la section « Message contenu ».  <br/> |
   
L’en-tête X-MS-pièce jointe est en quatre jetons, séparés par un espace :
  
 _nom taille date et heure_
  
Le premier jeton est le nom de fichier, qui peut contenir des espaces, et cet en-tête doit être analysé à partir des messages entrants droite sur. La taille est exprimée en octets ; la date est au format _mm-jj-aaaa_ et qu’il _hh : mm._
  
> [!NOTE]
> MessageID n’est pas mappé à la **clé PR_SEARCH_KEY** , car le domaine SMTP a des exigences spécifiques sur le format de l’identificateur de message qui permettent de coder un identificateur de message MAPI arbitraire. Au lieu de cela, MessageID est mappé sur **PR_TNEF_CORRELATION_KEY**. Cette propriété est une propriété de transport défini qui est définie par le transport de l’envoi d’un message sortant et utilisée par un transport de recevoir un message entrant. Pour plus d’informations, voir [développement d’un fournisseur de Transport TNEF-Enabled](developing-a-tnef-enabled-transport-provider.md). 
  

