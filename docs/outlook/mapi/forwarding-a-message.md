---
title: Transfert d’un message
description: Cet article fournit une vue d’ensemble détaillée du transfert de messages.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 0027fd5a-f30a-4025-b670-c21869b3a480
ms.openlocfilehash: 4e77d7582fd83f2d23beee1689eaeaecb55b1010
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816639"
---
# <a name="forwarding-a-message"></a>Transfert d’un message

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le transfert d’un message implique la plupart des mêmes tâches que l’envoi d’un message d’origine. Tout d’abord, vous devez ouvrir le magasin de messages par défaut et le dossier désigné pour contenir les messages sortants, généralement la boîte de réception, et appeler la méthode [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) de ce dossier pour créer le message à transférer. Vous devez également ouvrir le dossier qui contient le message d’origine, généralement la boîte de réception. Pour plus d’informations sur l’ouverture de différents dossiers, consultez [Ouvrir un dossier de magasin de messages](opening-a-message-store-folder.md).
  
La principale différence entre la création d’un message à transférer et la création de l’original est qu’avec un message transféré, la plupart des propriétés sont basées ou copiées directement à partir des propriétés du message d’origine. 
  
**Pour transférer un message**
  
1. Ouvrez le magasin de messages par défaut. Pour plus d’informations, consultez [l’ouverture du magasin de messages par défaut](opening-the-default-message-store.md).
    
2. Ouvrez le dossier Outbox. Pour plus d’informations, consultez [Ouvrir un dossier de magasin de messages](opening-a-message-store-folder.md).
    
3. Appelez la méthode [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) de la boîte d’envoi pour créer un message transféré. 
    
4. Appelez la méthode [IMAPIProp::CopyTo](imapiprop-copyto.md) du message d’origine pour copier les propriétés suivantes dans le message transféré : 
    
   - **PR\_ BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) ou **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), selon que vous prenez ou non en charge le format de texte enrichi, le texte brut ou HTML.
    
   - **PR\_ NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) 
    
5. Copiez les pièces jointes du message d’origine en appelant la méthode **IMAPIProp::CopyTo** du message d’origine pour copier la propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) ou en appelant la procédure en trois étapes suivante pour chaque pièce jointe à copier :
    
   1. Appelez la méthode [IMessage::CreateAttach](imessage-createattach.md) du nouveau message transféré pour créer une pièce jointe. 
      
   2. Appelez la méthode [IMessage::OpenAttach](imessage-openattach.md) du message d’origine pour ouvrir la pièce jointe à copier. 
      
   3. Appelez la méthode **IMAPIProp::CopyTo** du message d’origine pour copier toutes les propriétés de pièce jointe de l’ancienne pièce jointe vers la nouvelle. 
    
6. N’incluez pas les propriétés suivantes dans votre appel à **IMAPIProp::CopyTo** : 
    
|Propriétés|Propriétés (suite)|
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))  <br/> |**propriétés PR_RCVD_REPRESENTING**  <br/> |
|**PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md))  <br/> |**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))  <br/> |
|**propriétés PR_RECEIVED_BY**  <br/> |**propriétés PR_REPLY_RECIPIENT**  <br/> |
|**PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |**propriétés PR_SENDER**  <br/> |
|**propriétés PR_SENT_REPRESENTING**  <br/> |**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))  <br/> |
|**PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md))  <br/> | <br/> |
   
1. Mettez en forme le texte du message en ajoutant un retrait et un paragraphe d’en-tête qui inclut l’expéditeur d’origine, la date de transmission, l’objet et la liste des destinataires. N’incluez pas de caractères de préfixe de style Internet avec le contenu.
    
2. Appelez [ScCreateConversationIndex](sccreateconversationindex.md), en passant la valeur de la propriété **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) du message d’origine.
    
3. Définissez un préfixe pour le message transféré. Si vous utilisez le « FW : » standard, concaténez ces caractères au début de **PR_NORMALIZED_SUBJECT** et définissez **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) sur cette nouvelle chaîne. Ne définissez pas **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)). Si vous utilisez un préfixe non standard, tel qu’une chaîne de plus de trois caractères, stockez-le dans **PR_SUBJECT_PREFIX**. 
    
4. Définissez les propriétés **PR_SENT_REPRESENTING** sur les valeurs correspondantes dans les propriétés **PR_RCVD_REPRESENTING** . 
    
5. Créez une liste de destinataires. Pour plus d’informations, consultez [Création d’une liste de destinataires](creating-a-recipient-list.md).
    
6. Appelez la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du message transféré pour l’enregistrer ou [IMessage::SubmitMessage](imessage-submitmessage.md) pour l’enregistrer et l’envoyer. 
    
## <a name="see-also"></a>Voir aussi

- [Propriété canonique PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)

