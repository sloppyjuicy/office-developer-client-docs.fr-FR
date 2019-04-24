---
title: Rendu d'une pièce jointe en texte brut
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72b447e9-b4f2-4557-baf5-0afefe463749
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 587736e7ca2f30468b169a33cea34927f857382c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328356"
---
# <a name="rendering-an-attachment-in-plain-text"></a>Rendu d'une pièce jointe en texte brut

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour afficher une pièce jointe dans un message en texte brut, récupérez la propriété **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) de la pièce jointe et appliquez-la aux données de **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) inspecteur. Il existe deux façons de récupérer **PR_RENDERING_POSITION**:
  
- Ouvrez la pièce jointe en appelant la méthode **IMessage:: OpenAttach** du message, puis demandez la propriété **PR_RENDERING_POSITION** en appelant la méthode **IMAPIProp:: GetProps** de la pièce jointe. Pour plus d'informations, consultez [IMessage:: OpenAttach](imessage-openattach.md) et [IMAPIProp:: GetProps](imapiprop-getprops.md).
    
- Appelez la méthode **IMessage:: GetAttachmentTable** du message pour accéder à sa table de pièces jointes et récupérer la colonne qui contient la propriété **PR_RENDERING_POSITION** . Cette méthode est toujours préférable. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
N'oubliez pas que de nombreuses banques de messages prenant en charge le format RTF ne calculent pas **PR_RENDERING_POSITION** tant que le client ne demande pas la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) d'un message. Jusqu'à ce moment, **PR_RENDERING_POSITION** représente généralement une valeur approximative. Les fournisseurs de banques de messages sont autorisés à fournir aux clients une valeur approximative pour améliorer les performances. 
  
Le rendu d'un fichier ou d'une pièce jointe binaire est stocké dans sa propriété **PR_ATTACH_RENDERING** . Vous pouvez extraire **PR_ATTACH_RENDERING** de la même façon que vous avez récupéré **PR_RENDERING_POSITION**: directement à partir de la pièce jointe ou de la table des pièces jointes. Pour **PR_ATTACH_RENDERING**, la première stratégie, bien qu'elle prend plus de temps, est plus sûre. Étant donné que certains fournisseurs de banques de messages tronquent leurs colonnes de table à 255 octets, ou dans quelques cas 510 octets, il est difficile de s'assurer que la colonne **PR_ATTACH_RENDERING** contient le rendu complet. Lors de la récupération de la propriété directement à partir de la pièce jointe, elle sera toujours terminée. 
  
Ni OLE ni les pièces jointes de message ne définissent **PR_ATTACH_RENDERING**. Au lieu de cela, les informations de rendu pour les pièces jointes OLE 1 sont stockées dans le flux de texte du message. Pour les pièces jointes OLE 2, elle est stockée dans un flux enfant spécial de l'objet de stockage. Le rendu des informations pour les pièces jointes des messages est disponible via le gestionnaire de formulaires. 
  
 **Pour récupérer le rendu d'une pièce jointe de message**
  
1. Utilisez la classe de message du message pour accéder au gestionnaire de formulaires.
    
2. Accéder à la propriété **PR_MINI_ICON** du gestionnaire de formulaire. Pour plus d'informations, voir **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).
    

