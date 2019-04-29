---
title: Ouverture du texte d’un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 305b0534f828ea72c1e116fd38fb8f578062e32e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407535"
---
# <a name="opening-message-text"></a>Ouverture du texte d’un message

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le texte d'un message est stocké dans sa **propriété\_PR Body** ou sa propriété **\_\_Compressed PR** . Pour plus d'informations, reportez-vous à la rubrique **\_PR Body** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_html** ([PidTagHtml](pidtaghtml-canonical-property.md)) et **PR\_Rich RTF\_compressé** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Si vous prenez en charge le format RTF (Rich Text Format), ouvrez **PR\_RTF_COMPRESSED**. Si vous ne prenez pas en charge le format RTF, ouvrez le **\_corps du message**. Étant donné que le texte d'un message peut être volumineux, qu'il soit ou non mis en forme, utilisez **IMAPIProp:: OpenProperty** pour ouvrir ces propriétés. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
  
### <a name="to-display-formatted-message-text"></a>Pour afficher le texte du message mis en forme
  
1. Si vous utilisez une banque de messages non compatible avec le format RTF, comme indiqué par l'absence de l'indicateur STORE_RTF_OK dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de la Banque:
    
    1. Appelez la méthode **IMAPIProp:: GetProps** pour récupérer la propriété **PR_RTF_IN_SYNC** . Pour plus d'informations, voir [IMAPIProp:: GetProps](imapiprop-getprops.md) et **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).
        
    2. Appelez RTFSync pour synchroniser la propriété PR_BODY du message avec la propriété **PR_RTF_COMPRESSED** . Pour plus d'informations, voir [RTFSync](rtfsync.md), **PR_BODY**et **PR_RTF_COMPRESSED**. TransMettez l'indicateur RTF_SYNC_BODY_CHANGED si l'appel de récupération de **PR_RTF_IN_SYNC** a échoué car la propriété n'existe pas ou est définie sur false. 
        
    3. Si **RTFSync** a renvoyé la valeur true, ce qui indique que des modifications ont été apportées, appelez la méthode **IMAPIProp:: SaveChanges** pour les stocker définitivement. Pour plus d'informations, voir [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).
    
2. Que vous utilisiez ou non une banque de messages prenant en charge le format RTF:
    
    1. Appelez **IMAPIProp:: OpenProperty** pour ouvrir la propriété **PR_RTF_COMPRESSED** . Pour plus d'informations, voir [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) et **PR_RTF_COMPRESSED**.
        
    2. Si **PR_RTF_COMPRESSED** n'est pas disponible, appelez **OpenProperty** pour ouvrir la propriété **PR_BODY** . 
        
    3. Appelez la fonction **WrapCompressedRTFStream** pour créer une version non compressée des données RTF compressées, le cas échéant. Pour plus d'informations, consultez la rubrique [WrapCompressedRTFStream](wrapcompressedrtfstream.md).
        
    4. Copiez le texte mis en forme à partir du flux vers l'emplacement approprié dans le formulaire de message. 
    
### <a name="to-display-plain-message-text"></a>Pour afficher le texte d'un message brut
  
1. Appelez la méthode **IMAPIProp:: GetProps** pour récupérer la propriété **PR_BODY** . Pour plus d'informations, voir [IMAPIProp:: GetProps](imapiprop-getprops.md).
    
2. Si **GetProps** renvoie soit PT_ERROR pour le type de propriété dans la structure de la valeur de la propriété, soit MAPI_E_NOT_ENOUGH_MEMORY, appelez la méthode **IMAPIProp:: OpenProperty** du message. TransMettez **PR_BODY** comme balise de propriété et IID_IStream comme identificateur d'interface. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
3. Copiez le texte brut du flux vers l'emplacement approprié dans le formulaire de message. 
    

