---
title: Enregistrement d’un message dans la boîte de réception
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3df04d4e-7e80-4232-aadc-c05c99ab59cb
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e79133ed4928495dcf75b59877a82d3228773883
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586283"
---
# <a name="saving-a-message-in-the-inbox"></a>Enregistrement d’un message dans la boîte de réception

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
 **Pour stocker un message dans la boîte de réception sans les destinataires**
  
1. Appelez [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) pour récupérer l’identificateur d’entrée de la boîte de réception. 
    
2. Appelez [IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir la boîte de réception et de récupérer un pointeur vers elle. 
    
3. Appelez la méthode de [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) de la boîte de réception pour créer le message. 
    
4. Appeler la méthode de [IMAPIProp::SetProps](imapiprop-setprops.md) du message pour ajouter la **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), ou **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) et **PR_SUBJECT** ([ PidTagSubject](pidtagsubject-canonical-property.md)) Propriétés. 
    
5. Créer chaque pièce jointe, définissez ses propriétés et enregistrez-le. Pour plus d’informations sur l’ajout de pièces jointes aux messages, consultez [Création d’une pièce jointe du Message](creating-a-message-attachment.md).
    
6. Appelez **IMessage::SaveChanges** pour enregistrer le message. À ce stade, il apparaîtra dans le tableau contenu de la boîte de réception. 
    
Si vous souhaitez enregistrer une intermittantly message avant de s’affichent dans le tableau contenu de la boîte de réception, créer à la place dans un dossier masqué, tel que le dossier racine de la sous-arborescence IPM et déplacer ensuite vers la boîte de réception. 
  

