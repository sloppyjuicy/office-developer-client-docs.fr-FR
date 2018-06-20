---
title: Rendu d’une pièce jointe en texte brut
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72b447e9-b4f2-4557-baf5-0afefe463749
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 38db1d18f240188c7566a57afa23291a307446dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787004"
---
# <a name="rendering-an-attachment-in-plain-text"></a>Rendu d’une pièce jointe en texte brut

  
  
**S’applique à**: Outlook 
  
Pour afficher une pièce jointe dans un message avec le texte brut, récupérer la propriété **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) de la pièce jointe et s’appliquent aux données de la **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) propriété. Il existe deux façons de récupérer **PR_RENDERING_POSITION**:
  
- Ouvrez la pièce jointe en appelant la méthode **IMessage::OpenAttach** du message et demandez ensuite la propriété **PR_RENDERING_POSITION** en appelant la méthode **IMAPIProp::GetProps** de la pièce jointe. Pour plus d’informations, voir [IMessage::OpenAttach](imessage-openattach.md) et [IMAPIProp::GetProps](imapiprop-getprops.md).
    
- Appelez la méthode **IMessage::GetAttachmentTable** du message pour accéder à la table des pièces jointes et récupérer la colonne qui contient la propriété **PR_RENDERING_POSITION** . Cette méthode est toujours préférable. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
N’oubliez pas que les banques de messages RTF prenant en charge plusieurs ne sont pas calculent **PR_RENDERING_POSITION** jusqu'à ce que le client demande la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) d’un message. En attendant, **PR_RENDERING_POSITION** représente généralement une valeur approximative. Fournisseurs de magasins de message sont autorisés à fournir aux clients avec une valeur approximative pour améliorer les performances. 
  
Le rendu d’un fichier ou d’une pièce jointe binaire est stocké dans sa propriété **PR_ATTACH_RENDERING** . Vous avez le choix de récupération **PR_ATTACH_RENDERING** de la même façon que vous avez récupéré **PR_RENDERING_POSITION**: directement à partir de la pièce jointe ou à partir de la table des pièces jointes. Pour **PR_ATTACH_RENDERING**, la première stratégie, bien que plus longue est plus sûr. Étant donné que certains fournisseurs de banque de messages tronquent les colonnes de tableau à 255 octets ou dans quelques cas 510 octets, il est difficile de vous assurer que la colonne **PR_ATTACH_RENDERING** contienne le rendu complet. Lorsque vous récupérez la propriété directement à partir de la pièce jointe, il sera toujours terminée. 
  
Pièces jointes OLE ni message défini **PR_ATTACH_RENDERING**. Au lieu de cela, les informations de rendu pour les pièces jointes OLE 1 sont stockées dans le flux de texte du message. Les pièces jointes OLE 2, il est stocké dans un flux spécial enfant de l’objet de stockage. Rendu d’informations sur les pièces jointes du message est disponible par le biais du Gestionnaire de formulaire. 
  
 **Pour récupérer le rendu d’une pièce jointe**
  
1. Utilisez la classe de message du message pour accéder au gestionnaire du formulaire.
    
2. Accéder à la forme propriété du gestionnaire **PR_MINI_ICON** . Pour plus d’informations, voir **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).
    

