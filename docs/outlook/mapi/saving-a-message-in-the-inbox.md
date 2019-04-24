---
title: Enregistrement d'un message dans la boîte de réception
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3df04d4e-7e80-4232-aadc-c05c99ab59cb
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 672a9df55ce711b88451a517a2813c9ad8c599ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357532"
---
# <a name="saving-a-message-in-the-inbox"></a>Enregistrement d'un message dans la boîte de réception

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 **Pour stocker un message dans la boîte de réception sans destinataire**
  
1. Appelez [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) pour récupérer l'identificateur d'entrée de la boîte de réception. 
    
2. Appelez [IMsgStore:: OpenEntry](imsgstore-openentry.md) pour ouvrir la boîte de réception et y récupérer un pointeur. 
    
3. Appelez la méthode [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) pour créer le message. 
    
4. Appelez la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) du message pour ajouter les **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) ou **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) et **PR_SUBJECT** ([ PidTagSubject](pidtagsubject-canonical-property.md)). 
    
5. Créez chaque pièce jointe, définissez ses propriétés et enregistrez-la. Pour plus d'informations sur l'ajout de pièces jointes aux messages, consultez [la rubrique Création d'une pièce jointe](creating-a-message-attachment.md).
    
6. Appelez **IMessage:: SaveChanges** pour enregistrer le message. À ce stade, il apparaîtra dans le tableau des matières de la boîte de réception. 
    
Si vous souhaitez enregistrer un message intermittantly avant de l'afficher dans le tableau des matières de la boîte de réception, créez-le à la place dans un dossier masqué, tel que le dossier racine de la sous-arborescence IPM, puis déplacez-le vers la boîte de réception. 
  

