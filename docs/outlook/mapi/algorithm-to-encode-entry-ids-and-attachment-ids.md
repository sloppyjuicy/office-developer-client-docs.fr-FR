---
title: Algorithme permettant d’encoder les ID d’entrée et les ID de pièce jointe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b9ae6679-99b7-6509-74d4-12aa13d54928
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4d3ca89ea7d3d72f625d38e37494e253b05b1569
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577918"
---
# <a name="algorithm-to-encode-entry-ids-and-attachment-ids"></a>Algorithme permettant d’encoder les ID d’entrée et les ID de pièce jointe

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Un fournisseur de magasins peut envoyer dans le cadre d’un MAPI URL Uniform Resource Locator () un ID d’entrée et un ID de pièce jointe au Gestionnaire de protocole MAPI pour identifier un objet est prêt pour l’indexation. Le fournisseur de banque encode l’entrée ID et l’ID de pièce jointe en tant que chaînes Unicode. Cette rubrique montre un algorithme qui génère une représentation compacte de l’identificateur d’entrée ou un ID de pièce jointe.
  
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



[À propos de l’indexation de magasin basée sur une notification](about-notification-based-store-indexing.md)
  
[À propos des URL MAPI pour l’indexation basée sur une notification](about-mapi-urls-for-notification-based-indexing.md)

