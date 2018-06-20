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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f0cf6fa03d8f38b7d160a8747111445cfdac1ae9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787050"
---
# <a name="sbitmaskrestriction"></a><span data-ttu-id="63530-103">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="63530-103">SBitMaskRestriction</span></span>

  
  
<span data-ttu-id="63530-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="63530-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="63530-105">Décrit une restriction de masque de bits, qui est utilisée pour effectuer une opération de bits **AND** et tester le résultat.</span><span class="sxs-lookup"><span data-stu-id="63530-105">Describes a bitmask restriction, which is used to perform a bitwise **AND** operation and test the result.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="63530-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="63530-106">Header file:</span></span>  <br/> |<span data-ttu-id="63530-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="63530-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBitMaskRestriction
{
  ULONG relBMR;
  PT_LONG ulPropTag;
  ULONG ulMask;
} SBitMaskRestriction;

```

## <a name="members"></a><span data-ttu-id="63530-108">Membres</span><span class="sxs-lookup"><span data-stu-id="63530-108">Members</span></span>

 <span data-ttu-id="63530-109">**relBMR**</span><span class="sxs-lookup"><span data-stu-id="63530-109">**relBMR**</span></span>
  
> <span data-ttu-id="63530-110">Opérateur de relation qui décrit comment le masque spécifié dans le membre **ulMask** doit être appliqué à la balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="63530-110">Relational operator that describes how the mask specified in the **ulMask** member should be applied to the property tag.</span></span> <span data-ttu-id="63530-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="63530-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="63530-112">BMR_EQZ</span><span class="sxs-lookup"><span data-stu-id="63530-112">BMR_EQZ</span></span> 
  
> <span data-ttu-id="63530-113">Effectuer une opération de bits **AND** du masque dans le membre **ulMask** avec la propriété représentée par les membres **ulPropTag** et le test pour être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="63530-113">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being equal to zero.</span></span> 
    
<span data-ttu-id="63530-114">BMR_NEZ</span><span class="sxs-lookup"><span data-stu-id="63530-114">BMR_NEZ</span></span> 
  
> <span data-ttu-id="63530-115">Exécuter une opération **et** du masque dans le membre **ulMask** avec la propriété représentée par le membre **ulPropTag** et testez n’étant ne pas égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="63530-115">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being not equal to zero.</span></span> 
    
 <span data-ttu-id="63530-116">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="63530-116">**ulPropTag**</span></span>
  
> <span data-ttu-id="63530-117">Balise de propriété de la propriété à laquelle s’applique le masque de bits.</span><span class="sxs-lookup"><span data-stu-id="63530-117">Property tag of the property to which the bitmask is applied.</span></span>
    
 <span data-ttu-id="63530-118">**ulMask**</span><span class="sxs-lookup"><span data-stu-id="63530-118">**ulMask**</span></span>
  
> <span data-ttu-id="63530-119">Masque de bits à appliquer à la propriété identifiée par **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="63530-119">Bitmask to apply to the property identified by **ulPropTag**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="63530-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="63530-120">Remarks</span></span>

<span data-ttu-id="63530-121">La structure **SBitMaskRestriction** effectue une opération de bits **AND** à l’aide de masque de bits décrite dans le membre **ulMask** et la valeur de la propriété définie par le membre **ulPropTag** .</span><span class="sxs-lookup"><span data-stu-id="63530-121">The **SBitMaskRestriction** structure performs a bitwise **AND** operation using the bitmask described in the **ulMask** member and the value of the property described by the **ulPropTag** member.</span></span> <span data-ttu-id="63530-122">Si le résultat est égale à zéro, BMR_EQZ est remplie.</span><span class="sxs-lookup"><span data-stu-id="63530-122">If the result is zero, BMR_EQZ is satisfied.</span></span> <span data-ttu-id="63530-123">Si elle est différente de zéro, autrement dit, si la valeur de propriété comporte au moins un des bits même définir en tant **ulMask**, puis BMR_NEZ est satisfaite.</span><span class="sxs-lookup"><span data-stu-id="63530-123">If it is nonzero, that is, if the property value has at least one of the same bits set as **ulMask**, then BMR_NEZ is satisfied.</span></span>
  
<span data-ttu-id="63530-124">Pour plus d’informations sur les restrictions de structure **SBitMaskRestriction** en général, voir [à propos des Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="63530-124">For more information about the **SBitMaskRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="63530-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63530-125">See also</span></span>



[<span data-ttu-id="63530-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="63530-126">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="63530-127">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="63530-127">MAPI Structures</span></span>](mapi-structures.md)

