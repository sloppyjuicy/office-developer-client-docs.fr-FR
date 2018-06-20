---
title: L’enregistrement d’un Message dans la boîte de réception
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3df04d4e-7e80-4232-aadc-c05c99ab59cb
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 3c48ded73d924a400632a94feab65f7afca6e526
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787037"
---
# <a name="saving-a-message-in-the-inbox"></a>L’enregistrement d’un Message dans la boîte de réception

  
  
**S’applique à**: Outlook 
  
 **Pour stocker un message dans la boîte de réception sans les destinataires**
  
1. Appelez [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) pour récupérer l’identificateur d’entrée de la boîte de réception. 
    
2. Appelez [IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir la boîte de réception et de récupérer un pointeur vers elle. 
    
3. Appelez la méthode de [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) de la boîte de réception pour créer le message. 
    
4. Appeler la méthode de [IMAPIProp::SetProps](imapiprop-setprops.md) du message pour ajouter la **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), ou **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) et **PR_SUBJECT** ([ PidTagSubject](pidtagsubject-canonical-property.md)) Propriétés. 
    
5. Créer chaque pièce jointe, définissez ses propriétés et enregistrez-le. Pour plus d’informations sur l’ajout de pièces jointes aux messages, consultez [Création d’une pièce jointe du Message](creating-a-message-attachment.md).
    
6. Appelez **IMessage::SaveChanges** pour enregistrer le message. À ce stade, il apparaîtra dans le tableau contenu de la boîte de réception. 
    
Si vous souhaitez enregistrer une intermittantly message avant de s’affichent dans le tableau contenu de la boîte de réception, créer à la place dans un dossier masqué, tel que le dossier racine de la sous-arborescence IPM et déplacer ensuite vers la boîte de réception. 
  

