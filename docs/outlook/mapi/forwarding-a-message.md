---
title: Transfert d’un message
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0027fd5a-f30a-4025-b670-c21869b3a480
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d1df84c37cc2a24806c35ae0c90e4bf2a5e438d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328062"
---
# <a name="forwarding-a-message"></a>Transfert d’un message

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le transfert d'un message implique de nombreuses tâches identiques à celles de l'envoi d'un message d'origine. Tout d'abord, vous devez ouvrir la Banque de messages par défaut et le dossier destiné à contenir les messages sortants, généralement la boîte d'envoi, et appeler la méthode [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) de ce dossier pour créer le message à transférer. Vous devez également ouvrir le dossier qui contient le message d'origine, généralement la boîte de réception. Pour plus d'informations sur l'ouverture de dossiers différents, voir [ouverture d'un dossier de la Banque de messages](opening-a-message-store-folder.md).
  
La principale différence entre la création d'un message à transférer et la création de l'original est qu'avec un message transféré, la plupart des propriétés sont basées ou copiées directement à partir des propriétés du message d'origine. 
  
**Pour transférer un message**
  
1. Ouvrez la Banque de messages par défaut. Pour plus d'informations, consultez [la rubrique ouverture de la Banque de messages par défaut](opening-the-default-message-store.md).
    
2. Ouvrez le dossier boîte d'envoi. Pour plus d'informations, consultez [la rubrique ouverture d'un dossier de banque de messages](opening-a-message-store-folder.md).
    
3. Appelez la méthode [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) de la boîte d'envoi pour créer un nouveau message transféré. 
    
4. Appelez la méthode [IMAPIProp:: CopyTo](imapiprop-copyto.md) du message d'origine pour copier les propriétés suivantes dans le message transféré: 
    
   - **PR\_Body** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_html** ([PidTagHtml](pidtaghtml-canonical-property.md)) ou **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), selon que vous prenez ou non en charge le format RTF, le texte brut ou le html.
    
   - **PR\_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) 
    
5. Copiez les pièces jointes du message d'origine en appelant la méthode **IMAPIProp:: CopyTo** du message d'origine pour copier la propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) ou en appelant les éléments suivants procédure en trois étapes pour chaque pièce jointe à copier:
    
   1. Appelez la méthode [IMessage:: CreateAttach](imessage-createattach.md) du nouveau message transféré pour créer une nouvelle pièce jointe. 
      
   2. Appelez la méthode [IMessage:: OpenAttach](imessage-openattach.md) du message d'origine pour ouvrir la pièce jointe à copier. 
      
   3. Appelez la méthode **IMAPIProp:: CopyTo** du message d'origine pour copier toutes les propriétés des pièces jointes à partir de l'ancienne pièce jointe vers la nouvelle. 
    
6. N'incluez pas les propriétés suivantes dans votre appel à **IMAPIProp:: CopyTo**: 
    
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
   
1. Mettre en forme le texte du message en ajoutant une mise en retrait et un paragraphe d'en-tête qui inclut l'expéditeur, la date de transmission, l'objet et la liste des destinataires d'origine. N'incluez pas de caractères de préfixe de style Internet avec le contenu.
    
2. Appelez [ScCreateConversationIndex](sccreateconversationindex.md), en transmettant la valeur de la propriété **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) du message d'origine.
    
3. Définissez un préfixe pour le message transféré. Si vous utilisez le «FW:» standard, concaténez ces caractères au début de **PR_NORMALIZED_SUBJECT** et définissez **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) sur cette nouvelle chaîne. Ne pas définir **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)). Si vous utilisez un préfixe non standard, tel qu'une chaîne de plus de trois caractères, stockez-le dans **PR_SUBJECT_PREFIX**. 
    
4. Définissez les propriétés **PR_SENT_REPRESENTING** sur les valeurs correspondantes dans les propriétés **PR_RCVD_REPRESENTING** . 
    
5. Créer une liste de destinataires. Pour plus d'informations, consultez [la rubrique Création d'une liste de destinataires](creating-a-recipient-list.md).
    
6. Appelez la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) du message transféré pour l'enregistrer ou [IMessage:: SubmitMessage](imessage-submitmessage.md) pour l'enregistrer et l'envoyer. 
    
## <a name="see-also"></a>Voir aussi

- [Propriété canonique PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)

