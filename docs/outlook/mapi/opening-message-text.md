---
title: Ouverture du texte d’un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 40d12c84088748d0801649a2fca59c12e60d0b92
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625139"
---
# <a name="opening-message-text"></a>Ouverture du texte d’un message

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le texte d’un message est stocké dans sa propriété **\_ PR BODY** ou PR **\_ RTF \_ COMPRESSED.** Pour plus d’informations, voir **PR \_ BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR \_ HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) et **PR \_ RTF \_ COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Si vous ouvrez le format RTF (Rich Text Format), ouvrez **la \_ RTF_COMPRESSED**. Si vous ne le faites pas, ouvrez **PR \_ BODY.** Étant donné que le texte d’un message peut être grand, qu’il soit formaté ou non, utilisez **IMAPIProp::OpenProperty** pour ouvrir ces propriétés. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
  
### <a name="to-display-formatted-message-text"></a>Pour afficher le texte d’un message formaté
  
1. Si vous utilisez une magasin de messages non RTF, comme indiqué par l’absence de l’indicateur STORE_RTF_OK dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de la boutique :
    
    1. Appelez la méthode **IMAPIProp::GetProps** du message pour récupérer **PR_RTF_IN_SYNC** propriété. Pour plus d’informations, voir [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).
        
    2. Appelez RTFSync pour synchroniser la propriété de PR_BODY message avec la **PR_RTF_COMPRESSED** propriété. Pour plus d’informations, [voir RTFSync,](rtfsync.md) **PR_BODY** et **PR_RTF_COMPRESSED**. Passez l’RTF_SYNC_BODY_CHANGED si l’appel de  récupération PR_RTF_IN_SYNC échoué parce que la propriété n’existe pas ou qu’elle est définie sur FALSE. 
        
    3. Si **RTFSync** a renvoyé TRUE, indiquant que des modifications ont été apportées, appelez la méthode **IMAPIProp::SaveChanges** du message pour les stocker définitivement. Pour plus d’informations, [voir IMAPIProp::SaveChanges](imapiprop-savechanges.md).
    
2. Que vous utilisiez ou non une magasin de messages rtF :
    
    1. Appelez **IMAPIProp::OpenProperty** pour ouvrir **PR_RTF_COMPRESSED** propriété. Pour plus d’informations, [voir IMAPIProp::OpenProperty](imapiprop-openproperty.md) et **PR_RTF_COMPRESSED**.
        
    2. Si **PR_RTF_COMPRESSED** n’est pas disponible, appelez **OpenProperty** pour ouvrir **PR_BODY** propriété. 
        
    3. Appelez la **fonction WrapCompressedRTFStream** pour créer une version non compressée des données RTF compressées, si disponible. Pour plus d’informations, [voir WrapCompressedRTFStream](wrapcompressedrtfstream.md).
        
    4. Copiez le texte formaté du flux à l’endroit approprié dans le formulaire de message. 
    
### <a name="to-display-plain-message-text"></a>Pour afficher du texte de message simple
  
1. Appelez la méthode **IMAPIProp::GetProps** du message pour récupérer la **PR_BODY** message. Pour plus d’informations, [voir IMAPIProp::GetProps](imapiprop-getprops.md).
    
2. Si **GetProps** renvoie une PT_ERROR pour le type de propriété dans la structure de valeurs de propriété ou MAPI_E_NOT_ENOUGH_MEMORY, appelez la méthode **IMAPIProp::OpenProperty** du message. Passez **PR_BODY** comme balise de propriété et IID_IStream comme identificateur d’interface. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
3. Copiez le texte simple du flux à l’endroit approprié dans le formulaire de message. 
    

