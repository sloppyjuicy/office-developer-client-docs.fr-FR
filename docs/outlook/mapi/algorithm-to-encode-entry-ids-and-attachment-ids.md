---
title: Algorithme permettant de coder les ID d’entrée et les ID de pièce jointe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b9ae6679-99b7-6509-74d4-12aa13d54928
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6c39fe513be122f265fdc316629a3e64a156fdc1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420135"
---
# <a name="algorithm-to-encode-entry-ids-and-attachment-ids"></a>Algorithme permettant de coder les ID d’entrée et les ID de pièce jointe

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un fournisseur de magasin peut envoyer dans le cadre d’une URL MAPI un ID d’entrée et un ID de pièce jointe au responsable du protocole MAPI pour identifier un objet prêt pour l’indexation. Le fournisseur de banque d’informations encode l’ID d’entrée et l’ID de pièce jointe en tant que chaînes Unicode. Cette rubrique présente un algorithme qui génère une représentation compacte de l’ID d’entrée ou de l’ID de pièce jointe.
  
```cpp
const WORD kwBaseOffset = 0xAC00;  // Hangul char range (AC00-D7AF) 
LPWSTR EncodeID(ULONG cbEID, LPENTRYID rgbID) 
{ 
    ULONG   i = 0; 
    LPWSTR  pwzDst = NULL; 
    LPBYTE  pbSrc = NULL; 
    LPWSTR  pwzIDEncoded = NULL; 
 
    // rgbID is the item Entry ID or the attachment ID 
    // cbID is the size in bytes of rgbID 
 
    // Allocate memory for pwzIDEncoded 
    pwzIDEncoded = new WCHAR[cbEID]; 
    if (!pwzIDEncoded) return NULL; 
 
    for (i = 0, pbSrc = (LPBYTE)rgbID, pwzDst = pwzIDEncoded; 
        i < cbEID; 
        i++, pbSrc++, pwzDst++) 
    { 
        *pwzDst = (WCHAR) (*pbSrc + kwBaseOffset); 
    } 
 
    // Ensure NULL terminated 
    *pwzDst = L'\0'; 
 
    // pwzIDEncoded now contains the entry ID encoded. 
    return pwzIDEncoded; 
}
```

## <a name="see-also"></a>Voir aussi



[À propos Notification-Based'indexation dans le Store](about-notification-based-store-indexing.md)
  
[À propos des URL MAPI pour lNotification-Based indexation](about-mapi-urls-for-notification-based-indexing.md)

