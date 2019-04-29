---
title: ScBinFromHexBounded
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScBinFromHexBounded
api_type:
- COM
ms.assetid: edac715c-6edb-4b05-82e5-c08c3c7cb6d4
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 813fab28e3e865c9f04f85c854b292ce7229dad5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439757"
---
# <a name="scbinfromhexbounded"></a><span data-ttu-id="84e78-103">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="84e78-103">ScBinFromHexBounded</span></span>

  
  
<span data-ttu-id="84e78-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84e78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84e78-105">ConVertit la partie spécifiée d'une représentation sous forme de chaîne d'un nombre hexadécimal en nombre binaire.</span><span class="sxs-lookup"><span data-stu-id="84e78-105">Converts the specified portion of a string representation of a hexadecimal number into a binary number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84e78-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="84e78-106">Header file:</span></span>  <br/> |<span data-ttu-id="84e78-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="84e78-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="84e78-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="84e78-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="84e78-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="84e78-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="84e78-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="84e78-110">Called by:</span></span>  <br/> |<span data-ttu-id="84e78-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="84e78-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a><span data-ttu-id="84e78-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84e78-112">Parameters</span></span>

 <span data-ttu-id="84e78-113">_t_</span><span class="sxs-lookup"><span data-stu-id="84e78-113">_sz_</span></span>
  
> <span data-ttu-id="84e78-114">dans Pointeur vers la chaîne terminée par un caractère null à convertir.</span><span class="sxs-lookup"><span data-stu-id="84e78-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="84e78-115">Les caractères valides incluent les caractères hexadécimaux compris entre 0 et 9, ainsi que les caractères majuscules et minuscules a à f.</span><span class="sxs-lookup"><span data-stu-id="84e78-115">Valid characters include the hexadecimal characters 0 through 9 and both uppercase and lowercase characters a through f.</span></span>
    
 <span data-ttu-id="84e78-116">_pb_</span><span class="sxs-lookup"><span data-stu-id="84e78-116">_pb_</span></span>
  
> <span data-ttu-id="84e78-117">remarquer Pointeur vers le nombre binaire renvoyé.</span><span class="sxs-lookup"><span data-stu-id="84e78-117">[out] Pointer to the returned binary number.</span></span>
    
 <span data-ttu-id="84e78-118">_cb_</span><span class="sxs-lookup"><span data-stu-id="84e78-118">_cb_</span></span>
  
> <span data-ttu-id="84e78-119">dans Taille, en octets, du paramètre _PB_ .</span><span class="sxs-lookup"><span data-stu-id="84e78-119">[in] Size, in bytes, of the  _pb_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="84e78-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="84e78-120">Return value</span></span>

<span data-ttu-id="84e78-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="84e78-121">S_OK</span></span>
  
> <span data-ttu-id="84e78-122">La conversion a réussi.</span><span class="sxs-lookup"><span data-stu-id="84e78-122">Conversion was successful.</span></span>
    
<span data-ttu-id="84e78-123">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="84e78-123">MAPI_E_CALL_FAILED</span></span>
  
> <span data-ttu-id="84e78-124">Des caractères non valides ont été détectés.</span><span class="sxs-lookup"><span data-stu-id="84e78-124">Invalid characters were encountered.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="84e78-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84e78-125">See also</span></span>



[<span data-ttu-id="84e78-126">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="84e78-126">FBinFromHex</span></span>](fbinfromhex.md)

