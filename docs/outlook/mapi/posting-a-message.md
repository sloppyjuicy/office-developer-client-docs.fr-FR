---
title: Publication d’un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc3e1546-e58b-413f-82d7-4efeb86b0000
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 2c174d48a19e23de725e1d5a1533130175f2ab00
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350749"
---
# <a name="posting-a-message"></a>Publication d’un message

**S’applique à** : Outlook 2013 | Outlook 2016 
  
La publication d'un message est similaire à l'envoi d'un message. La différence principale est la destination. Au lieu d'être dirigé vers un ou plusieurs destinataires dans un ou plusieurs systèmes de messagerie, un message publié reste dans un dossier dans la Banque de messages actuelle.
  
### <a name="to-post-a-message"></a>Pour publier un message
  
1. Ouvrez le dossier de destination en appelant [IMsgStore:: OpenEntry](imsgstore-openentry.md). Si le dossier de destination est la boîte de réception, localisez l'identificateur d'entrée à transmettre à **OpenEntry** en appelant [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md). 
    
2. Appelez [IMAPIFolder: CreateMessage](imapifolder-createmessage.md) pour créer le message. 
    
3. Appelez la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) du message pour définir: 
    
   - L'indicateur MSGFLAG_READ dans la propriété **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)).
    
   - Propriétés **PR_SENDER** . 
    
   - Propriétés **PR_SENT_REPRESENTING** . 
    
   - Propriété **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)).
    
   - Propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).
    
   - Propriété **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).
    
   - La propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).
    
   - Toutes les propriétés requises par la classe de message.
    
4. Appelez la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) du message pour enregistrer le message. 
    
5. Si nécessaire, créez une pièce jointe, définissez ses propriétés et enregistrez-la. Pour plus d'informations sur l'ajout de pièces jointes aux messages, consultez [la rubrique Création d'une pièce jointe](creating-a-message-attachment.md).
    
6. Appelez **IMessage:: SaveChanges** pour enregistrer le message. À ce stade, il apparaîtra dans la table des matières du dossier de destination. 
    
Notez que vous ne créez pas de liste de destinataires. Au lieu de cela, vous définissez plusieurs propriétés qui sont normalement définies par un fournisseur de transport pour un message envoyé. 
  
Si vous souhaitez enregistrer un message par intermittence avant de l'afficher dans la table des matières du dossier visible, créez-le à la place dans un dossier masqué, tel que le dossier racine de la sous-arborescence IPM, puis déplacez-le vers le dossier cible. 
  

