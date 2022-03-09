---
title: Publication d’un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: cc3e1546-e58b-413f-82d7-4efeb86b0000
ms.openlocfilehash: eb2aa5dcadf3efaa572bae74c9289e347fb6e20a
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63369643"
---
# <a name="posting-a-message"></a>Publication d’un message

**S’applique à** : Outlook 2013 | Outlook 2016 
  
La publication d’un message est similaire à l’envoi d’un message. La principale différence est la destination. Au lieu d’être dirigé vers un ou plusieurs destinataires dans un ou plusieurs systèmes de messagerie, un message publié reste dans un dossier de la boutique de messages actuelle.
  
### <a name="to-post-a-message"></a>Pour publier un message
  
1. Ouvrez le dossier de destination en appelant [IMsgStore::OpenEntry](imsgstore-openentry.md). Si le dossier de destination est la boîte de réception, recherchez l’identificateur d’entrée à transmettre à **OpenEntry** en appelant [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md). 
    
2. [Appelez IMAPIFolder::CreateMessage](imapifolder-createmessage.md) pour créer le message. 
    
3. Appelez la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) du message pour définir : 
    
   - L MSGFLAG_READ de la **propriété PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)).
    
   - **Propriétés PR_SENDER** propriétés. 
    
   - **Propriétés PR_SENT_REPRESENTING** propriétés. 
    
   - Propriété **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)).
    
   - Propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) **ou PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).
    
   - Propriété **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).
    
   - Propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).
    
   - Toutes les propriétés requises par la classe de message.
    
4. Appelez la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du message pour enregistrer le message. 
    
5. Si nécessaire, créez une pièce jointe, définissez ses propriétés et enregistrez-la. Pour plus d’informations sur l’ajout de pièces jointes à des messages, voir [Création d’une pièce jointe de message](creating-a-message-attachment.md).
    
6. **Appelez IMessage::SaveChanges** pour enregistrer le message. À ce stade, elle apparaît dans la table des matières du dossier de destination. 
    
Notez que vous ne créez pas de liste de destinataires. Au lieu de cela, vous définissez plusieurs propriétés qui sont normalement définies par un fournisseur de transport pour un message envoyé. 
  
Si vous souhaitez enregistrer un message par intermittence avant de le faire apparaître dans la table des matières du dossier visible, créez-le dans un dossier masqué tel que le dossier racine de la sous-arbre IPM, puis déplacez-le vers le dossier cible. 
  

