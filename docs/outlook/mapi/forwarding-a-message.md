---
title: Transfert d’un message
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 0027fd5a-f30a-4025-b670-c21869b3a480
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 37515d7a45115988945112bef892975bb193ff3c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551589"
---
# <a name="forwarding-a-message"></a>Transfert d’un message

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le forwarding d’un message implique de nombreuses tâches identiques à l’envoi d’un message d’origine. Tout d’abord, vous devez ouvrir la boîte aux lettres par défaut et le dossier désigné pour contenir les messages sortants, généralement la boîte d’envoi, et appeler la méthode [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) de ce dossier pour créer le message à transmettre. Vous devez également ouvrir le dossier qui contient le message d’origine, généralement la boîte de réception. Pour plus d’informations sur l’ouverture de différents dossiers, voir [Ouverture d’un dossier de la boutique de messages.](opening-a-message-store-folder.md)
  
La principale différence entre la création d’un message à transmettre et la création de l’original est qu’avec un message transmis, la plupart des propriétés sont basées sur ou copiées directement à partir des propriétés du message d’origine. 
  
**Pour transmettre un message**
  
1. Ouvrez la boutique de messages par défaut. Pour plus d’informations, voir [Ouverture de la boutique de messages par défaut.](opening-the-default-message-store.md)
    
2. Ouvrez le dossier Boîte d’envoi. Pour plus d’informations, voir [Ouverture d’un dossier de la boutique de messages.](opening-a-message-store-folder.md)
    
3. Appelez la méthode [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) de la boîte d’envoi pour créer un message transmis. 
    
4. Appelez la méthode [IMAPIProp::CopyTo](imapiprop-copyto.md) du message d’origine pour copier les propriétés suivantes dans le message transmis : 
    
   - **PR \_ BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR \_ HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) ou **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), selon que vous prise en charge ou non format de texte enrichi, texte brut ou HTML.
    
   - **PR \_ NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) 
    
5. Copiez les pièces jointes du message d’origine en appelant la méthode **IMAPIProp::CopyTo** du message d’origine pour copier la propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) ou en appelant la procédure en trois étapes suivante pour chaque pièce jointe à copier :
    
   1. Appelez la méthode [IMessage::CreateAttach](imessage-createattach.md) du nouveau message transmis pour créer une pièce jointe. 
      
   2. Appelez la méthode [IMessage::OpenAttach](imessage-openattach.md) du message d’origine pour ouvrir la pièce jointe à copier. 
      
   3. Appelez la méthode **IMAPIProp::CopyTo** du message d’origine pour copier toutes les propriétés de pièce jointe de l’ancienne pièce jointe vers la nouvelle. 
    
6. N’incluez pas les propriétés suivantes dans votre appel **à IMAPIProp::CopyTo**: 
    
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))  <br/> |**PR_RCVD_REPRESENTING** propriétés  <br/> |
|**PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md))  <br/> |**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))  <br/> |
|**PR_RECEIVED_BY** propriétés  <br/> |**PR_REPLY_RECIPIENT** propriétés  <br/> |
|**PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |**PR_SENDER** propriétés  <br/> |
|**PR_SENT_REPRESENTING** propriétés  <br/> |**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))  <br/> |
|**PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md))  <br/> | <br/> |
   
1. Mettre en forme le texte du message en ajoutant un retrait et un paragraphe d’en-tête qui inclut l’expéditeur d’origine, la date de transmission, l’objet et la liste des destinataires. N’incluez pas de caractères de préfixe de style Internet avec le contenu.
    
2. Appelez [ScCreateConversationIndex](sccreateconversationindex.md), en passant la valeur de la propriété PR_CONVERSATION_INDEX **(** [PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) du message d’origine.
    
3. Définissez un préfixe pour le message transmis. Si vous utilisez la norme « FW: », concaténer ces caractères au début de **PR_NORMALIZED_SUBJECT** et définissez **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) sur cette nouvelle chaîne. Ne définissez **pas PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)). Si vous utilisez un préfixe nonstandard, tel qu’une chaîne de plus de trois caractères, stockez-le **dans PR_SUBJECT_PREFIX**. 
    
4. Définissez **les PR_SENT_REPRESENTING** sur les valeurs correspondantes dans la **PR_RCVD_REPRESENTING** propriétés. 
    
5. Créez une liste de destinataires. Pour plus d’informations, voir [Création d’une liste de destinataires.](creating-a-recipient-list.md)
    
6. Appelez la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du message transmis pour l’enregistrer ou [IMessage::SubmitMessage](imessage-submitmessage.md) pour l’enregistrer et l’envoyer. 
    
## <a name="see-also"></a>Voir aussi

- [Propriété canonique PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)

