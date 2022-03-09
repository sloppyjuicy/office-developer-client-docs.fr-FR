---
title: Prise en charge du texte RTF pour les fournisseurs de magasins de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 0022fe70-cf11-49a5-9c97-a6bc5b5b13aa
ms.openlocfilehash: d2d1bd5a714a63ac1be0deebdad996f801028555
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63376055"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a>Prise en charge du texte RTF pour les fournisseurs de magasins de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Certaines applications clientes permettent aux utilisateurs d’utiliser du texte RTF (Rich Text Format) dans leurs messages. Si votre fournisseur de magasins de messages doit prendre en charge le texte RTF dans les messages, il doit gérer la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), en plus de la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)). Cela consiste principalement à stocker les deux propriétés et à s’assurer **que** PR_BODY contient une version en texte simple du **texte PR_RTF_COMPRESSED**. La [fonction RTFSync](rtfsync.md) est utile à cet effet. 
  
Il existe deux indicateurs qui peuvent être définies dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de l’objet de la boutique de messages qui indique aux clients ce qu’ils peuvent attendre du fournisseur de la boutique de messages en ce qui concerne les propriétés **PR_BODY** et **PR_RTF_COMPRESSED** sur les messages dans la magasin de messages. L’indicateur STORE_RTF_OK indique que le magasin peut générer dynamiquement la valeur de la propriété **PR_BODY** à partir de la propriété **PR_RTF_COMPRESSED** , ce qui décharge les clients de la charge de leur synchronisation explicite. L STORE_UNCOMPRESSED_RTF indique que le fournisseur de magasins de messages peut prendre en charge les données non compressées **dans PR_RTF_COMPRESSED**.
  
Les fournisseurs de magasins de messages qui ne supportent pas le texte RTF doivent supprimer la propriété **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) lorsque la propriété **PR_BODY** change afin d’interopérer correctement avec les applications clientes qui ne supportent pas le texte RTF. 
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

