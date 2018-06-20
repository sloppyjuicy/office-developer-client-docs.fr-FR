---
title: SPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropTagArray
api_type:
- COM
ms.assetid: 4a9e1579-bebe-4a51-8ced-6dba9c3bcb63
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5cfad1c75aaab9afae47de5798f9e6b7ea530940
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787232"
---
# <a name="sproptagarray"></a><span data-ttu-id="bd111-103">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="bd111-103">SPropTagArray</span></span>

  
  
<span data-ttu-id="bd111-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bd111-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bd111-105">Contient un tableau de balises de propriété.</span><span class="sxs-lookup"><span data-stu-id="bd111-105">Contains an array of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bd111-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="bd111-106">Header file:</span></span>  <br/> |<span data-ttu-id="bd111-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bd111-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="bd111-108">Macros connexes :</span><span class="sxs-lookup"><span data-stu-id="bd111-108">Related macros:</span></span>  <br/> |<span data-ttu-id="bd111-109">[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md)</span><span class="sxs-lookup"><span data-stu-id="bd111-109">[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropTagArray
{
  ULONG cValues;
  ULONG aulPropTag[MAPI_DIM];
} SPropTagArray, FAR *LPSPropTagArray;

```

## <a name="members"></a><span data-ttu-id="bd111-110">Membres</span><span class="sxs-lookup"><span data-stu-id="bd111-110">Members</span></span>

 <span data-ttu-id="bd111-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="bd111-111">**cValues**</span></span>
  
> <span data-ttu-id="bd111-112">Nombre de balises de propriété dans le tableau indiqué par le membre **aulPropTag** .</span><span class="sxs-lookup"><span data-stu-id="bd111-112">Count of property tags in the array indicated by the **aulPropTag** member.</span></span> 
    
 <span data-ttu-id="bd111-113">**aulPropTag**</span><span class="sxs-lookup"><span data-stu-id="bd111-113">**aulPropTag**</span></span>
  
> <span data-ttu-id="bd111-114">Tableau de balises de propriété.</span><span class="sxs-lookup"><span data-stu-id="bd111-114">Array of property tags.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bd111-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="bd111-115">Remarks</span></span>

<span data-ttu-id="bd111-116">Une balise de propriété est un entier non signé 32 bits qui se compose de deux parties :</span><span class="sxs-lookup"><span data-stu-id="bd111-116">A property tag is a 32-bit unsigned integer that consists of two parts:</span></span> 
  
- <span data-ttu-id="bd111-117">Un identificateur dans l’ordre de haut niveau 16 bits.</span><span class="sxs-lookup"><span data-stu-id="bd111-117">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="bd111-118">Un type dans les 16 bits de poids faible.</span><span class="sxs-lookup"><span data-stu-id="bd111-118">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="bd111-119">L’identificateur est une valeur numérique dans une plage spécifique.</span><span class="sxs-lookup"><span data-stu-id="bd111-119">The identifier is a numeric value in a particular range.</span></span> <span data-ttu-id="bd111-120">MAPI définit les plages pour les identificateurs décrire la propriété qui est utilisée pour et qui est chargé de maintenance.</span><span class="sxs-lookup"><span data-stu-id="bd111-120">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="bd111-121">MAPI définit des contraintes pour chacune des balises de propriété pris en charge dans le fichier d’en-tête Mapitags.h.</span><span class="sxs-lookup"><span data-stu-id="bd111-121">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="bd111-122">Le type indique le format de la valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="bd111-122">The type indicates the format for the property's value.</span></span> <span data-ttu-id="bd111-123">MAPI définit des constantes pour chacun des types de propriété pris en charge dans le fichier d’en-tête Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="bd111-123">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="bd111-124">Pour plus d’informations sur les balises de propriétés et leurs composants, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="bd111-124">For more information about property tags and their components, see one of the following topics:</span></span> 
  
[<span data-ttu-id="bd111-125">Balises de propriété MAPI</span><span class="sxs-lookup"><span data-stu-id="bd111-125">MAPI Property Tags</span></span>](mapi-property-tags.md)
  
[<span data-ttu-id="bd111-126">Vue d’ensemble d’identificateur de propriété MAPI</span><span class="sxs-lookup"><span data-stu-id="bd111-126">MAPI Property Identifier Overview</span></span>](mapi-property-identifier-overview.md)
  
[<span data-ttu-id="bd111-127">Vue d’ensemble des types de propriété MAPI</span><span class="sxs-lookup"><span data-stu-id="bd111-127">MAPI Property Type Overview</span></span>](mapi-property-type-overview.md)
  
<span data-ttu-id="bd111-128">Pour obtenir une liste complète des types de propriété à valeur unique et à valeurs multiples, voir l’annexe, [les Types et les identificateurs de propriété](property-identifiers-and-types.md).</span><span class="sxs-lookup"><span data-stu-id="bd111-128">For a complete list of the single-valued and multi-valued property types, see the appendix, [Property Identifiers and Types](property-identifiers-and-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bd111-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd111-129">See also</span></span>



[<span data-ttu-id="bd111-130">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="bd111-130">MAPI Structures</span></span>](mapi-structures.md)

