---
title: Texte du message d’ouverture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7a2dbe8d2143fd330ae1f5ca5804e30b79909576
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569405"
---
# <a name="opening-message-text"></a>Texte du message d’ouverture

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Le texte d’un message est stocké dans son **PR\_corps** propriété ou **PR\_RTF\_compressés** propriété. Pour plus d’informations, voir **PR\_corps** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), et **PR\_RTF\_compressés** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Si vous prenez en charge le Format de texte enrichi (RTF), ouvrez **PR\_RTF_COMPRESSED**. Si vous ne prennent pas en charge les RTF, ouvrez **PR\_BODY**. Le texte d’un message pouvant être volumineux, quel que soit ou non mis en forme, utilisez **IMAPIProp::OpenProperty** pour ouvrir ces propriétés. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
  
### <a name="to-display-formatted-message-text"></a>Pour afficher le texte du message mis en forme
  
1. Si vous utilisez une banque de messages connaissance non RTF, comme indiqué par l’absence de l’indicateur STORE_RTF_OK dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de la banque :
    
    1. Appelez la méthode **IMAPIProp::GetProps** du message pour récupérer la propriété **PR_RTF_IN_SYNC** . Pour plus d’informations, voir [IMAPIProp::GetProps](imapiprop-getprops.md) et **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).
        
    2. Appelez RTFSync pour synchroniser la propriété du message PR_BODY avec la propriété **PR_RTF_COMPRESSED** . Pour plus d’informations, voir [RTFSync](rtfsync.md) **PR_BODY**et **PR_RTF_COMPRESSED**. Passe le RTF_SYNC_BODY_CHANGED signale si l’appel à récupérer **PR_RTF_IN_SYNC** a échoué, car la propriété n’existe pas ou qu’il est défini sur FALSE. 
        
    3. Si **RTFSync** renvoie la valeur TRUE, indiquant que les modifications ont été apportées, appeler la méthode de **IMAPIProp::SaveChanges** du message pour les stocker définitivement. Pour plus d’informations, voir [IMAPIProp::SaveChanges](imapiprop-savechanges.md).
    
2. Quel que soit ou non, vous utilisez un message au format RTF prenant en charge stocker :
    
    1. Appelez **IMAPIProp::OpenProperty** pour ouvrir la propriété **PR_RTF_COMPRESSED** . Pour plus d’informations, voir [IMAPIProp::OpenProperty](imapiprop-openproperty.md) et **PR_RTF_COMPRESSED**.
        
    2. Si **PR_RTF_COMPRESSED** n’est pas disponible, appelez **OpenProperty** pour ouvrir la propriété **PR_BODY** . 
        
    3. Appelez la fonction **WrapCompressedRTFStream** pour créer une version non compressée des données au format RTF compressées, si elle est disponible. Pour plus d’informations, voir [WrapCompressedRTFStream](wrapcompressedrtfstream.md).
        
    4. Copiez le texte mis en forme à partir du flux à l’emplacement approprié dans le formulaire de message. 
    
### <a name="to-display-plain-message-text"></a>Pour afficher le texte du message brut
  
1. Appelez la méthode **IMAPIProp::GetProps** du message pour récupérer la propriété **PR_BODY** . Pour plus d’informations, voir [IMAPIProp::GetProps](imapiprop-getprops.md).
    
2. Si **GetProps** renvoie soit PT_ERROR pour le type de propriété dans la structure de valeur de propriété ou d’un MAPI_E_NOT_ENOUGH_MEMORY, appelez la méthode de **IMAPIProp::OpenProperty** du message. Transmettez **PR_BODY** , ainsi que la balise de propriété IID_IStream l’identificateur d’interface. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
3. Copiez le texte brut à partir du flux à l’emplacement approprié dans le formulaire de message. 
    

