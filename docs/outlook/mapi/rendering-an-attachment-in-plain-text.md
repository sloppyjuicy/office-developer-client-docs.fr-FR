---
title: Rendu d’une pièce jointe en texte simple
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 72b447e9-b4f2-4557-baf5-0afefe463749
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 959716e6067f0eb4fd808c4ccacbd4ffb11db025
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591303"
---
# <a name="rendering-an-attachment-in-plain-text"></a>Rendu d’une pièce jointe en texte simple

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour restituer une pièce jointe dans un message en texte simple, récupérez la propriété **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) de la pièce jointe et appliquez-la aux données de la propriété **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)). Il existe deux façons de récupérer **PR_RENDERING_POSITION**:
  
- Ouvrez la pièce jointe en appelant la méthode **IMessage::OpenAttach** du message, puis demandez la propriété **PR_RENDERING_POSITION** en appelant la méthode **IMAPIProp::GetProps** de la pièce jointe. Pour plus d’informations, voir [IMessage::OpenAttach](imessage-openattach.md) et [IMAPIProp::GetProps](imapiprop-getprops.md).
    
- Appelez la méthode **IMessage::GetAttachmentTable** du message pour accéder à sa table de pièces jointes et récupérer la colonne qui contient la propriété **PR_RENDERING_POSITION.** De cette façon, il est toujours préférable. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
N’oubliez pas que de nombreuses magasins  de messages rtF ne calculent pas PR_RENDERING_POSITION tant qu’un client n’a pas demandé la **propriété PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) d’un message. Jusqu’à ce **moment, PR_RENDERING_POSITION** représente généralement une valeur approximative. Les fournisseurs de magasins de messages sont autorisés à fournir aux clients une valeur approximative pour améliorer les performances. 
  
Le rendu d’un fichier ou d’une pièce jointe binaire est stocké dans **sa PR_ATTACH_RENDERING** de données. Vous avez la possibilité d’extraire PR_ATTACH_RENDERING de la même manière que vous avez récupéré **PR_RENDERING_POSITION**: directement à partir de la pièce jointe ou de la table de pièces jointes.  Par **PR_ATTACH_RENDERING,** la première stratégie, bien que plus longue, est plus sûre. Étant donné que certains fournisseurs de magasins de messages tronquées leurs colonnes de tableau à 255 octets, ou dans certains cas 510 octets, il est difficile de s’assurer que la colonne **PR_ATTACH_RENDERING** contient le rendu complet. Lorsque vous récupérez la propriété directement à partir de la pièce jointe, elle est toujours complète. 
  
Ni les pièces jointes OLE ni les pièces jointes **de message PR_ATTACH_RENDERING**. Au lieu de cela, les informations de rendu des pièces jointes OLE 1 sont stockées dans le flux de texte du message. Pour les pièces jointes OLE 2, elle est stockée dans un flux enfant spécial de l’objet de stockage. Les informations de rendu des pièces jointes des messages sont disponibles via le gestionnaire de formulaires. 
  
 **Pour récupérer le rendu d’une pièce jointe de message**
  
1. Utilisez la classe de message du message pour accéder au gestionnaire de formulaires.
    
2. Accédez à la propriété PR_MINI_ICON du gestionnaire **de** formulaires. Pour plus d’informations, **voir PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).
    

