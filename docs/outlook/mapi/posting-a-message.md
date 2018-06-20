---
title: Publier un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc3e1546-e58b-413f-82d7-4efeb86b0000
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 33bf6780979ee25739abf93d89744e1517363c63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786938"
---
# <a name="posting-a-message"></a>Publier un message

**S’applique à**: Outlook 
  
Publier un message est similaire à l’envoi d’un message. La principale différence est la destination. Au lieu d’être dirigées vers un ou plusieurs destinataires sur un ou plusieurs systèmes de messagerie, un message publié reste dans un dossier dans la banque de messages en cours.
  
### <a name="to-post-a-message"></a>Pour envoyer un message
  
1. Ouvrez le dossier de destination en appelant [IMsgStore::OpenEntry](imsgstore-openentry.md). Si le dossier de destination est la boîte de réception, recherchez l’identificateur d’entrée à transmettre à **OpenEntry** en appelant [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md). 
    
2. Appelez [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) pour créer le message. 
    
3. Appeler la méthode de [IMAPIProp::SetProps](imapiprop-setprops.md) du message pour définir : 
    
   - L’indicateur MSGFLAG_READ dans la propriété **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)).
    
   - Les propriétés **PR_SENDER** . 
    
   - Les propriétés **PR_SENT_REPRESENTING** . 
    
   - La propriété **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)).
    
   - Le **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).
    
   - La propriété **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).
    
   - La propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).
    
   - Toutes les propriétés requises par la classe de message.
    
4. Appelez la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du message pour enregistrer le message. 
    
5. Si nécessaire, créez une pièce jointe, définissez ses propriétés et enregistrez-le. Pour plus d’informations sur l’ajout de pièces jointes aux messages, consultez [Création d’une pièce jointe du Message](creating-a-message-attachment.md).
    
6. Appelez **IMessage::SaveChanges** pour enregistrer le message. À ce stade, il apparaîtra dans le tableau contenu du dossier de destination. 
    
Notez que vous ne créez pas d’une liste de destinataires. Au lieu de cela, vous définissez plusieurs propriétés qui sont normalement définies par un fournisseur de transport pour un message. 
  
Si vous souhaitez enregistrer un message par intermittence avant de s’affichent dans le tableau contenu du dossier visible, créer à la place dans un dossier masqué, tel que le dossier racine de la sous-arborescence IPM et déplacer ensuite vers le dossier cible. 
  

