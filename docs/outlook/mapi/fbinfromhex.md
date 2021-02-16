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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 55c7deec9d29ae22a07b2f5ccd1c832d56782c03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414934"
---
# <a name="fbinfromhex"></a><span data-ttu-id="895c6-103">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="895c6-103">FBinFromHex</span></span>

  
  
<span data-ttu-id="895c6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="895c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="895c6-105">Convertit une représentation sous forme de chaîne d’un nombre hexadécimal en données binaires.</span><span class="sxs-lookup"><span data-stu-id="895c6-105">Converts a string representation of a hexadecimal number to binary data.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="895c6-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="895c6-106">Header file:</span></span>  <br/> |<span data-ttu-id="895c6-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="895c6-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="895c6-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="895c6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="895c6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="895c6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="895c6-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="895c6-110">Called by:</span></span>  <br/> |<span data-ttu-id="895c6-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="895c6-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a><span data-ttu-id="895c6-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="895c6-112">Parameters</span></span>

 <span data-ttu-id="895c6-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="895c6-113">_sz_</span></span>
  
> <span data-ttu-id="895c6-114">[in] Pointeur vers la chaîne ASCII terminée par null à convertir.</span><span class="sxs-lookup"><span data-stu-id="895c6-114">[in] Pointer to the null-terminated ASCII string to be converted.</span></span> <span data-ttu-id="895c6-115">Il ne s’agit pas d’une chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="895c6-115">It is not a Unicode string.</span></span> <span data-ttu-id="895c6-116">Les caractères valides incluent les caractères hexadécimals de zéro à neuf, ainsi que les caractères en minuscules et en minuscules A à F.</span><span class="sxs-lookup"><span data-stu-id="895c6-116">Valid characters include the hexadecimal characters zero through nine and both uppercase and lowercase characters A through F.</span></span>
    
 <span data-ttu-id="895c6-117">_pb_</span><span class="sxs-lookup"><span data-stu-id="895c6-117">_pb_</span></span>
  
> <span data-ttu-id="895c6-118">[out] Pointeur vers le nombre binaire renvoyé.</span><span class="sxs-lookup"><span data-stu-id="895c6-118">[out] Pointer to the returned binary number.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="895c6-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="895c6-119">Return value</span></span>

<span data-ttu-id="895c6-120">TRUE</span><span class="sxs-lookup"><span data-stu-id="895c6-120">TRUE</span></span> 
  
> <span data-ttu-id="895c6-121">La chaîne a été convertie en nombre binaire.</span><span class="sxs-lookup"><span data-stu-id="895c6-121">The string was successfully converted into a binary number.</span></span> 
    
<span data-ttu-id="895c6-122">FALSE</span><span class="sxs-lookup"><span data-stu-id="895c6-122">FALSE</span></span> 
  
> <span data-ttu-id="895c6-123">La chaîne d’entrée contient des caractères hexadécimals ASCII non valides.</span><span class="sxs-lookup"><span data-stu-id="895c6-123">The input string contains invalid ASCII hexadecimal characters.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="895c6-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="895c6-124">See also</span></span>



[<span data-ttu-id="895c6-125">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="895c6-125">ScBinFromHexBounded</span></span>](scbinfromhexbounded.md)

