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
# <a name="algorithm-to-encode-entry-ids-and-attachment-ids"></a><span data-ttu-id="0ce28-103">Algorithme permettant de coder les ID d’entrée et les ID de pièce jointe</span><span class="sxs-lookup"><span data-stu-id="0ce28-103">Algorithm to Encode Entry IDs and Attachment IDs</span></span>

  
  
<span data-ttu-id="0ce28-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ce28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ce28-105">Un fournisseur de magasin peut envoyer dans le cadre d’une URL MAPI un ID d’entrée et un ID de pièce jointe au responsable du protocole MAPI pour identifier un objet prêt pour l’indexation.</span><span class="sxs-lookup"><span data-stu-id="0ce28-105">A store provider can send as part of a MAPI Uniform Resource Locator (URL) an entry ID and an attachment ID to the MAPI Protocol Handler to identify an object that is ready for indexing.</span></span> <span data-ttu-id="0ce28-106">Le fournisseur de banque d’informations encode l’ID d’entrée et l’ID de pièce jointe en tant que chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="0ce28-106">The store provider encodes the entry ID and attachment ID as Unicode strings.</span></span> <span data-ttu-id="0ce28-107">Cette rubrique présente un algorithme qui génère une représentation compacte de l’ID d’entrée ou de l’ID de pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="0ce28-107">This topic shows an algorithm that generates a compact representation of the entry ID or attachment ID.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="0ce28-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ce28-108">See also</span></span>



[<span data-ttu-id="0ce28-109">À propos Notification-Based'indexation dans le Store</span><span class="sxs-lookup"><span data-stu-id="0ce28-109">About Notification-Based Store Indexing</span></span>](about-notification-based-store-indexing.md)
  
[<span data-ttu-id="0ce28-110">À propos des URL MAPI pour lNotification-Based indexation</span><span class="sxs-lookup"><span data-stu-id="0ce28-110">About MAPI URLs for Notification-Based Indexing</span></span>](about-mapi-urls-for-notification-based-indexing.md)

