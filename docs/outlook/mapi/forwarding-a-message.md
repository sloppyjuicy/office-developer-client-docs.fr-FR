---
title: Transfert d’un message
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0027fd5a-f30a-4025-b670-c21869b3a480
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 18113fd48f33eaf067942116f168a54e8b91c55c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579234"
---
# <a name="forwarding-a-message"></a>Transfert d’un message

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Transfert d’un message implique de nombreuses tâches de même que l’envoi d’un message d’origine. Tout d’abord, vous devez ouvrir la banque de messages par défaut et le dossier désigné pour contenir les messages sortants, généralement la boîte d’envoi, et appeler la méthode de [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) de ce dossier pour créer le message à transférer. Vous devez également ouvrir le dossier qui contient le message d’origine, généralement la boîte de réception. Pour plus d’informations sur l’ouverture des dossiers différents, consultez [ouverture d’un dossier de la banque de messages](opening-a-message-store-folder.md).
  
La principale différence entre la création d’un message à transférer et création d’origine est que les messages transférés, la plupart des propriétés est soit basée sur ou copiée directement à partir des propriétés du message d’origine. 
  
**Pour transférer un message**
  
1. Ouvrez la banque de messages par défaut. Pour plus d’informations, voir [l’ouverture de la banque de messages par défaut](opening-the-default-message-store.md).
    
2. Ouvrez le dossier boîte d’envoi. Pour plus d’informations, consultez [ouverture d’un dossier de la banque de messages](opening-a-message-store-folder.md).
    
3. Appeler la méthode de [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) de la boîte d’envoi pour créer un nouveau message transféré. 
    
4. Appeler la méthode de [IMAPIProp::CopyTo](imapiprop-copyto.md) du message d’origine pour copier les propriétés suivantes dans le message transféré : 
    
   - **PR\_corps** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), ou **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), en fonction de si vous prenez en charge le Format RTF, texte brut ou HTML.
    
   - **PR\_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) 
    
5. Copier les pièces jointes des messages à partir du message d’origine en appelant la méthode **IMAPIProp::CopyTo** du message d’origine pour copier la propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) ou en appelant les éléments suivants procédure à trois étapes pour chaque pièce jointe à copier :
    
   1. Appelez le transféré méthode [IMessage::CreateAttach](imessage-createattach.md) du message pour créer une nouvelle pièce jointe. 
      
   2. Appeler la méthode de [IMessage::OpenAttach](imessage-openattach.md) du message d’origine pour ouvrir la pièce jointe à copier. 
      
   3. Appeler la méthode de **IMAPIProp::CopyTo** du message d’origine pour copier toutes les propriétés de la pièce jointe à partir de la pièce jointe ancienne vers le nouveau. 
    
6. N’incluez pas les propriétés suivantes dans votre appel à **IMAPIProp::CopyTo**: 
    
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))  <br/> |Propriétés **PR_RCVD_REPRESENTING**  <br/> |
|**PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md))  <br/> |**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))  <br/> |
|Propriétés **PR_RECEIVED_BY**  <br/> |Propriétés **PR_REPLY_RECIPIENT**  <br/> |
|**PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |Propriétés **PR_SENDER**  <br/> |
|Propriétés **PR_SENT_REPRESENTING**  <br/> |**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))  <br/> |
|**PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md))  <br/> | <br/> |
   
1. Mettre en forme le texte du message en ajoutant le retrait et un paragraphe d’en-tête qui inclut l’expéditeur d’origine, la date de transmission, l’objet et la liste de destinataires. N’incluez pas de caractères de préfixe de style Internet avec le contenu.
    
2. Appelez [ScCreateConversationIndex](sccreateconversationindex.md), en passant la valeur de la propriété **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) du message d’origine.
    
3. Définir un préfixe pour le message transféré. Si vous utilisez la norme « TR : », concaténez ces caractères sur le début du **PR_NORMALIZED_SUBJECT** et définir **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) à la nouvelle chaîne. Ne définissez pas **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)). Si vous utilisez un préfixe non standard, comme une chaîne de plus de trois caractères, stockez-la dans **PR_SUBJECT_PREFIX**. 
    
4. Définissez les propriétés **PR_SENT_REPRESENTING** sur les valeurs correspondantes dans les propriétés de **PR_RCVD_REPRESENTING** . 
    
5. Créer une liste de destinataires. Pour plus d’informations, voir [Création d’une liste de destinataires](creating-a-recipient-list.md).
    
6. Appelez la méthode de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du message transmis pour enregistrer ou [IMessage::SubmitMessage](imessage-submitmessage.md) pour enregistrer et envoyer. 
    
## <a name="see-also"></a>Voir aussi

- [Propriété canonique PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)

