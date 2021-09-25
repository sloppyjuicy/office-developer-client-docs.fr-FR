---
title: Algorithme permettant de coder les ID d’entrée et les ID de pièce jointe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: b9ae6679-99b7-6509-74d4-12aa13d54928
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: eb8ace42381002d96a4a89e2a9b7eb36898d7927
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556930"
---
# <a name="algorithm-to-encode-entry-ids-and-attachment-ids"></a>Algorithme permettant de coder les ID d’entrée et les ID de pièce jointe

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un fournisseur de magasins peut envoyer dans le cadre d’une URL MAPI un ID d’entrée et un ID de pièce jointe au responsable du protocole MAPI pour identifier un objet prêt pour l’indexation. Le fournisseur de banque d’informations encode l’ID d’entrée et l’ID de pièce jointe en tant que chaînes Unicode. Cette rubrique présente un algorithme qui génère une représentation compacte de l’ID d’entrée ou de l’ID de pièce jointe.
  
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



[À propos Notification-Based'indexation du Store](about-notification-based-store-indexing.md)
  
[À propos des URL MAPI pour lNotification-Based indexation](about-mapi-urls-for-notification-based-indexing.md)

