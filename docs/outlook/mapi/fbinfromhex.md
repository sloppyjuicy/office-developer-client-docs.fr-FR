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
ms.openlocfilehash: 55c7deec9d29ae22a07b2f5ccd1c832d56782c03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341642"
---
# <a name="fbinfromhex"></a><span data-ttu-id="b4806-103">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="b4806-103">FBinFromHex</span></span>

  
  
<span data-ttu-id="b4806-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4806-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4806-105">ConVertit une représentation sous forme de chaîne d'un nombre hexadécimal en données binaires.</span><span class="sxs-lookup"><span data-stu-id="b4806-105">Converts a string representation of a hexadecimal number to binary data.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4806-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b4806-106">Header file:</span></span>  <br/> |<span data-ttu-id="b4806-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="b4806-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b4806-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="b4806-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b4806-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b4806-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b4806-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="b4806-110">Called by:</span></span>  <br/> |<span data-ttu-id="b4806-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="b4806-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a><span data-ttu-id="b4806-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4806-112">Parameters</span></span>

 <span data-ttu-id="b4806-113">_t_</span><span class="sxs-lookup"><span data-stu-id="b4806-113">_sz_</span></span>
  
> <span data-ttu-id="b4806-114">dans Pointeur vers la chaîne ASCII terminée par un caractère null à convertir.</span><span class="sxs-lookup"><span data-stu-id="b4806-114">[in] Pointer to the null-terminated ASCII string to be converted.</span></span> <span data-ttu-id="b4806-115">Il ne s'agit pas d'une chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="b4806-115">It is not a Unicode string.</span></span> <span data-ttu-id="b4806-116">Les caractères valides incluent les caractères hexadécimaux 0 à 9, ainsi que les caractères majuscules et minuscules A à F.</span><span class="sxs-lookup"><span data-stu-id="b4806-116">Valid characters include the hexadecimal characters zero through nine and both uppercase and lowercase characters A through F.</span></span>
    
 <span data-ttu-id="b4806-117">_pb_</span><span class="sxs-lookup"><span data-stu-id="b4806-117">_pb_</span></span>
  
> <span data-ttu-id="b4806-118">remarquer Pointeur vers le nombre binaire renvoyé.</span><span class="sxs-lookup"><span data-stu-id="b4806-118">[out] Pointer to the returned binary number.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b4806-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b4806-119">Return value</span></span>

<span data-ttu-id="b4806-120">TRUE</span><span class="sxs-lookup"><span data-stu-id="b4806-120">TRUE</span></span> 
  
> <span data-ttu-id="b4806-121">La chaîne a été convertie correctement en un nombre binaire.</span><span class="sxs-lookup"><span data-stu-id="b4806-121">The string was successfully converted into a binary number.</span></span> 
    
<span data-ttu-id="b4806-122">FALSE</span><span class="sxs-lookup"><span data-stu-id="b4806-122">FALSE</span></span> 
  
> <span data-ttu-id="b4806-123">La chaîne d'entrée contient des caractères hexadécimaux ASCII non valides.</span><span class="sxs-lookup"><span data-stu-id="b4806-123">The input string contains invalid ASCII hexadecimal characters.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b4806-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4806-124">See also</span></span>



[<span data-ttu-id="b4806-125">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="b4806-125">ScBinFromHexBounded</span></span>](scbinfromhexbounded.md)

