---
title: Ouverture du texte d’un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
ms.openlocfilehash: c5a68eb0faa7305549bef6db71db1c7e0e603760
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370651"
---
# <a name="opening-message-text"></a>Ouverture du texte d’un message

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le texte d’un message est stocké dans sa propriété **PRBODY\_** ou **PRRTFCOMPRESSED\_\_**. Pour plus d’informations, voir **PRBODY\_** ([PidTagBody](pidtagbody-canonical-property.md)), **PRHTML\_** ([PidTagHtml](pidtaghtml-canonical-property.md)) et **PRRTFCOMPRESSED\_\_** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Si vous prisez en charge le format RTF (Rich Text Format), ouvrez **pr\_ RTF_COMPRESSED**. Si vous ne le faites pas, ouvrez **PRBODY\_**. Étant donné que le texte d’un message peut être grand, qu’il soit formaté ou non, utilisez **IMAPIProp::OpenProperty** pour ouvrir ces propriétés. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
  
### <a name="to-display-formatted-message-text"></a>Pour afficher le texte d’un message formaté
  
1. Si vous utilisez une magasin de messages non RTF, comme indiqué par l’absence de l’indicateur STORE_RTF_OK dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de la boutique :
    
    1. Appelez la méthode **IMAPIProp::GetProps** du message pour récupérer **la PR_RTF_IN_SYNC** message. Pour plus d’informations, voir [IMAPIProp::GetProps](imapiprop-getprops.md) et **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).
        
    2. Appelez RTFSync pour synchroniser la propriété de PR_BODY message avec la **PR_RTF_COMPRESSED** propriété. Pour plus d’informations, [voir RTFSync](rtfsync.md), **PR_BODY** et **PR_RTF_COMPRESSED**. Passez l’RTF_SYNC_BODY_CHANGED si l’appel de récupération PR_RTF_IN_SYNC échoué parce  que la propriété n’existe pas ou qu’elle est définie sur FALSE. 
        
    3. Si **RTFSync** a renvoyé TRUE, indiquant que des modifications ont été apportées, appelez la méthode **IMAPIProp::SaveChanges** du message pour les stocker définitivement. Pour plus d’informations, [voir IMAPIProp::SaveChanges](imapiprop-savechanges.md).
    
2. Que vous utilisiez ou non une magasin de messages rtF :
    
    1. **Appelez IMAPIProp::OpenProperty** pour ouvrir **PR_RTF_COMPRESSED propriété.** Pour plus d’informations, [voir IMAPIProp::OpenProperty](imapiprop-openproperty.md) et **PR_RTF_COMPRESSED**.
        
    2. Si **PR_RTF_COMPRESSED** n’est pas disponible, appelez **OpenProperty** pour ouvrir **PR_BODY** propriété. 
        
    3. Appelez la **fonction WrapCompressedRTFStream** pour créer une version non compressée des données RTF compressées, si disponible. Pour plus d’informations, [voir WrapCompressedRTFStream](wrapcompressedrtfstream.md).
        
    4. Copiez le texte formaté du flux à l’endroit approprié dans le formulaire de message. 
    
### <a name="to-display-plain-message-text"></a>Pour afficher du texte de message simple
  
1. Appelez la méthode **IMAPIProp::GetProps** du message pour récupérer **la PR_BODY** message. Pour plus d’informations, [voir IMAPIProp::GetProps](imapiprop-getprops.md).
    
2. Si **GetProps** renvoie une PT_ERROR pour le type de propriété dans la structure de valeurs de propriété ou MAPI_E_NOT_ENOUGH_MEMORY, appelez la méthode **IMAPIProp::OpenProperty** du message. Passez **PR_BODY en** tant que balise de propriété et IID_IStream l’identificateur d’interface. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
3. Copiez le texte simple du flux à l’endroit approprié dans le formulaire de message. 
    

