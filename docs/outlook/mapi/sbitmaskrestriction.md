---
title: SBitMaskRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBitMaskRestriction
api_type:
- COM
ms.assetid: ddd42180-6e4f-410c-9f78-d868a91452dc
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: afac8c352ad0a07fcb1cd98683b6a5c87940ab4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424475"
---
# <a name="sbitmaskrestriction"></a><span data-ttu-id="447ee-103">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="447ee-103">SBitMaskRestriction</span></span>

  
  
<span data-ttu-id="447ee-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="447ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="447ee-105">Décrit une restriction de masque de bits, qui est utilisée pour \*\*\*\* effectuer une opération and au niveau du bit et tester le résultat.</span><span class="sxs-lookup"><span data-stu-id="447ee-105">Describes a bitmask restriction, which is used to perform a bitwise **AND** operation and test the result.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="447ee-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="447ee-106">Header file:</span></span>  <br/> |<span data-ttu-id="447ee-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="447ee-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBitMaskRestriction
{
  ULONG relBMR;
  PT_LONG ulPropTag;
  ULONG ulMask;
} SBitMaskRestriction;

```

## <a name="members"></a><span data-ttu-id="447ee-108">Members</span><span class="sxs-lookup"><span data-stu-id="447ee-108">Members</span></span>

 <span data-ttu-id="447ee-109">**relBMR**</span><span class="sxs-lookup"><span data-stu-id="447ee-109">**relBMR**</span></span>
  
> <span data-ttu-id="447ee-110">Opérateur relationnel qui décrit comment le masque spécifié dans le membre **ulMask** doit être appliqué à la balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="447ee-110">Relational operator that describes how the mask specified in the **ulMask** member should be applied to the property tag.</span></span> <span data-ttu-id="447ee-111">Les valeurs possibles sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="447ee-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="447ee-112">BMR_EQZ</span><span class="sxs-lookup"><span data-stu-id="447ee-112">BMR_EQZ</span></span> 
  
> <span data-ttu-id="447ee-113">Effectuer une opération \*\*\*\* and au niveau du bit du masque dans le membre **ulMask** avec la propriété représentée par le membre **ulPropTag** et vérifier qu'il est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="447ee-113">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being equal to zero.</span></span> 
    
<span data-ttu-id="447ee-114">BMR_NEZ</span><span class="sxs-lookup"><span data-stu-id="447ee-114">BMR_NEZ</span></span> 
  
> <span data-ttu-id="447ee-115">Effectuer une opération \*\*\*\* and au niveau du bit du masque dans le membre **ulMask** avec la propriété représentée par le membre **ulPropTag** et vérifier qu'elle n'est pas égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="447ee-115">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being not equal to zero.</span></span> 
    
 <span data-ttu-id="447ee-116">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="447ee-116">**ulPropTag**</span></span>
  
> <span data-ttu-id="447ee-117">Balise de propriété de la propriété à laquelle le masque de masque est appliqué.</span><span class="sxs-lookup"><span data-stu-id="447ee-117">Property tag of the property to which the bitmask is applied.</span></span>
    
 <span data-ttu-id="447ee-118">**ulMask**</span><span class="sxs-lookup"><span data-stu-id="447ee-118">**ulMask**</span></span>
  
> <span data-ttu-id="447ee-119">Masque de à appliquer à la propriété identifiée par **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="447ee-119">Bitmask to apply to the property identified by **ulPropTag**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="447ee-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="447ee-120">Remarks</span></span>

<span data-ttu-id="447ee-121">La structure **SBitMaskRestriction** effectue une opération de bits **and** à l'aide du masque de bits décrit dans le membre **ulMask** et de la valeur de la propriété décrite par le membre **ulPropTag** .</span><span class="sxs-lookup"><span data-stu-id="447ee-121">The **SBitMaskRestriction** structure performs a bitwise **AND** operation using the bitmask described in the **ulMask** member and the value of the property described by the **ulPropTag** member.</span></span> <span data-ttu-id="447ee-122">Si le résultat est égal à zéro, BMR_EQZ est satisfait.</span><span class="sxs-lookup"><span data-stu-id="447ee-122">If the result is zero, BMR_EQZ is satisfied.</span></span> <span data-ttu-id="447ee-123">S'il est différent de zéro, autrement dit, si la valeur de la propriété a au moins un des mêmes bits défini comme **ulMask**, BMR_NEZ est satisfait.</span><span class="sxs-lookup"><span data-stu-id="447ee-123">If it is nonzero, that is, if the property value has at least one of the same bits set as **ulMask**, then BMR_NEZ is satisfied.</span></span>
  
<span data-ttu-id="447ee-124">Pour plus d'informations sur la structure **SBitMaskRestriction** et les restrictions en général, consultez la rubrique [à propos des restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="447ee-124">For more information about the **SBitMaskRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="447ee-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="447ee-125">See also</span></span>



[<span data-ttu-id="447ee-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="447ee-126">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="447ee-127">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="447ee-127">MAPI Structures</span></span>](mapi-structures.md)

