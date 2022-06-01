---
title: Procédure pour déterminer si Outlook a uniquement téléchargé l’en-tête d’un message
description: Cette rubrique montre un exemple de code dans Visual C++ pour déterminer si Outlook est téléchargé uniquement dans l’en-tête d’un message.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: acc96bb9-1592-c480-53ee-1325f65297e1
ms.openlocfilehash: 527b50d39ded8e37d8a4e653bcf132395cb2e554
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816429"
---
# <a name="determine-if-outlook-downloaded-only-the-header-of-a-message"></a>Procédure pour déterminer si Outlook a uniquement téléchargé l’en-tête d’un message

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique montre un exemple de code dans Visual C++ qui utilise la [propriété canonique PidLidHeaderItem](pidlidheaderitem-canonical-property.md) nommée pour déterminer si Microsoft Outlook 2013 a téléchargé uniquement l’en-tête d’un message ou l’en-tête et le corps d’un message. 
  
```cpp
BOOL bIsHeader(LPMESSAGE lpMessage) 
{ 
    HRESULT         hRes = S_OK; 
    BOOL            bRet = false; 
    ULONG    ulVal = 0; 
    LPSPropValue    lpPropVal = NULL; 
    LPSPropTagArray lpNamedPropTag = NULL; 
    MAPINAMEID      NamedID = {0}; 
    LPMAPINAMEID    lpNamedID = NULL; 
 
    NamedID.lpguid = (LPGUID) &PSETID_Common; 
    NamedID.ulKind = MNID_ID; 
    NamedID.Kind.lID = dispidHeaderItem; 
    lpNamedID = &NamedID; 
    hRes = lpMessage->GetIDsFromNames(1, &lpNamedID, NULL, &lpNamedPropTag); 
 
    if (lpNamedPropTag && 1 == lpNamedPropTag->cValues) 
    { 
lpNamedPropTag->aulPropTag[0] = CHANGE_PROP_TYPE(lpNamedPropTag->aulPropTag[0], PT_LONG); 
 
//Get the value of the property. 
hRes = lpMessage->GetProps(lpNamedPropTag, 0, &ulVal, &lpPropVal); 
if (lpPropVal && 1 == ulVal && PT_LONG == PROP_TYPE(lpPropVal->ulPropTag) && lpPropVal->Value.ul) 
{ 
    bRet = true; 
} 
    } 
 
    MAPIFreeBuffer(lpPropVal); 
    MAPIFreeBuffer(lpNamedPropTag); 
    return bRet; 
}

```


