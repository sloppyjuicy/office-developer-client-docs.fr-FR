---
title: Algorithme pour coder les ID d’entrée et de pièce jointe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b9ae6679-99b7-6509-74d4-12aa13d54928
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 710ba5173dcce6e948e1f49c7d82e46bc83b8200
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782923"
---
# <a name="algorithm-to-encode-entry-ids-and-attachment-ids"></a><span data-ttu-id="58ead-103">Algorithme pour coder les ID d’entrée et de pièce jointe</span><span class="sxs-lookup"><span data-stu-id="58ead-103">Algorithm to Encode Entry IDs and Attachment IDs</span></span>

  
  
<span data-ttu-id="58ead-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="58ead-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="58ead-105">Un fournisseur de magasins peut envoyer dans le cadre d’un MAPI URL Uniform Resource Locator () un ID d’entrée et un ID de pièce jointe au Gestionnaire de protocole MAPI pour identifier un objet est prêt pour l’indexation.</span><span class="sxs-lookup"><span data-stu-id="58ead-105">A store provider can send as part of a MAPI Uniform Resource Locator (URL) an entry ID and an attachment ID to the MAPI Protocol Handler to identify an object that is ready for indexing.</span></span> <span data-ttu-id="58ead-106">Le fournisseur de banque encode l’entrée ID et l’ID de pièce jointe en tant que chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="58ead-106">The store provider encodes the entry ID and attachment ID as Unicode strings.</span></span> <span data-ttu-id="58ead-107">Cette rubrique montre un algorithme qui génère une représentation compacte de l’identificateur d’entrée ou un ID de pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="58ead-107">This topic shows an algorithm that generates a compact representation of the entry ID or attachment ID.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="58ead-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58ead-108">See also</span></span>



[<span data-ttu-id="58ead-109">Indexation de magasin de Notification</span><span class="sxs-lookup"><span data-stu-id="58ead-109">About Notification-Based Store Indexing</span></span>](about-notification-based-store-indexing.md)
  
[<span data-ttu-id="58ead-110">À propos des URL MAPI pour l’indexation basée sur une Notification</span><span class="sxs-lookup"><span data-stu-id="58ead-110">About MAPI URLs for Notification-Based Indexing</span></span>](about-mapi-urls-for-notification-based-indexing.md)

