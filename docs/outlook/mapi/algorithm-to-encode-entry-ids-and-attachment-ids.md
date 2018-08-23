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
# <a name="algorithm-to-encode-entry-ids-and-attachment-ids"></a><span data-ttu-id="2a7f8-103">Algorithme permettant d’encoder les ID d’entrée et les ID de pièce jointe</span><span class="sxs-lookup"><span data-stu-id="2a7f8-103">Algorithm to Encode Entry IDs and Attachment IDs</span></span>

  
  
<span data-ttu-id="2a7f8-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a7f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a7f8-105">Un fournisseur de magasins peut envoyer dans le cadre d’un MAPI URL Uniform Resource Locator () un ID d’entrée et un ID de pièce jointe au Gestionnaire de protocole MAPI pour identifier un objet est prêt pour l’indexation.</span><span class="sxs-lookup"><span data-stu-id="2a7f8-105">A store provider can send as part of a MAPI Uniform Resource Locator (URL) an entry ID and an attachment ID to the MAPI Protocol Handler to identify an object that is ready for indexing.</span></span> <span data-ttu-id="2a7f8-106">Le fournisseur de banque encode l’entrée ID et l’ID de pièce jointe en tant que chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="2a7f8-106">The store provider encodes the entry ID and attachment ID as Unicode strings.</span></span> <span data-ttu-id="2a7f8-107">Cette rubrique montre un algorithme qui génère une représentation compacte de l’identificateur d’entrée ou un ID de pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="2a7f8-107">This topic shows an algorithm that generates a compact representation of the entry ID or attachment ID.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="2a7f8-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a7f8-108">See also</span></span>



[<span data-ttu-id="2a7f8-109">À propos de l’indexation de magasin basée sur une notification</span><span class="sxs-lookup"><span data-stu-id="2a7f8-109">About Notification-Based Store Indexing</span></span>](about-notification-based-store-indexing.md)
  
[<span data-ttu-id="2a7f8-110">À propos des URL MAPI pour l’indexation basée sur une notification</span><span class="sxs-lookup"><span data-stu-id="2a7f8-110">About MAPI URLs for Notification-Based Indexing</span></span>](about-mapi-urls-for-notification-based-indexing.md)

