---
title: FBinFromHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBinFromHex
api_type:
- COM
ms.assetid: 47e6c576-bd99-4410-8e41-7dd3159b23b7
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 64d205ee7f51c0ce6a6eb1e982659c6cda675f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783303"
---
# <a name="fbinfromhex"></a><span data-ttu-id="56a20-103">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="56a20-103">FBinFromHex</span></span>

  
  
<span data-ttu-id="56a20-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="56a20-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="56a20-105">Convertit une représentation sous forme de chaîne d’un nombre hexadécimal à des données binaires.</span><span class="sxs-lookup"><span data-stu-id="56a20-105">Converts a string representation of a hexadecimal number to binary data.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="56a20-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="56a20-106">Header file:</span></span>  <br/> |<span data-ttu-id="56a20-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="56a20-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="56a20-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="56a20-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="56a20-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="56a20-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="56a20-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="56a20-110">Called by:</span></span>  <br/> |<span data-ttu-id="56a20-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="56a20-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a><span data-ttu-id="56a20-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56a20-112">Parameters</span></span>

 <span data-ttu-id="56a20-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="56a20-113">_sz_</span></span>
  
> <span data-ttu-id="56a20-114">[in] Pointeur vers la chaîne ASCII à convertir.</span><span class="sxs-lookup"><span data-stu-id="56a20-114">[in] Pointer to the null-terminated ASCII string to be converted.</span></span> <span data-ttu-id="56a20-115">Il n’est pas une chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="56a20-115">It is not a Unicode string.</span></span> <span data-ttu-id="56a20-116">Caractères valides incluent les caractères hexadécimaux zéro par le biais de neuf et les deux caractères majuscules et minuscules A à F.</span><span class="sxs-lookup"><span data-stu-id="56a20-116">Valid characters include the hexadecimal characters zero through nine and both uppercase and lowercase characters A through F.</span></span>
    
 <span data-ttu-id="56a20-117">_pb_</span><span class="sxs-lookup"><span data-stu-id="56a20-117">_pb_</span></span>
  
> <span data-ttu-id="56a20-118">[out] Pointeur vers le nombre binaire renvoyé.</span><span class="sxs-lookup"><span data-stu-id="56a20-118">[out] Pointer to the returned binary number.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="56a20-119">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="56a20-119">Return value</span></span>

<span data-ttu-id="56a20-120">TRUE</span><span class="sxs-lookup"><span data-stu-id="56a20-120">TRUE</span></span> 
  
> <span data-ttu-id="56a20-121">La chaîne a été convertie en nombre binaire.</span><span class="sxs-lookup"><span data-stu-id="56a20-121">The string was successfully converted into a binary number.</span></span> 
    
<span data-ttu-id="56a20-122">FALSE</span><span class="sxs-lookup"><span data-stu-id="56a20-122">FALSE</span></span> 
  
> <span data-ttu-id="56a20-123">La chaîne d’entrée contient des caractères hexadécimaux ASCII non valides.</span><span class="sxs-lookup"><span data-stu-id="56a20-123">The input string contains invalid ASCII hexadecimal characters.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="56a20-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56a20-124">See also</span></span>



[<span data-ttu-id="56a20-125">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="56a20-125">ScBinFromHexBounded</span></span>](scbinfromhexbounded.md)

