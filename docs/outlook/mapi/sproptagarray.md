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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9a5be98298ab1f9333ac1c223a6ef594e60dd86a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430699"
---
# <a name="sproptagarray"></a><span data-ttu-id="44a79-103">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="44a79-103">SPropTagArray</span></span>

  
  
<span data-ttu-id="44a79-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44a79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44a79-105">Contient un tableau de balises de propriété.</span><span class="sxs-lookup"><span data-stu-id="44a79-105">Contains an array of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="44a79-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="44a79-106">Header file:</span></span>  <br/> |<span data-ttu-id="44a79-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="44a79-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="44a79-108">Macros connexes:</span><span class="sxs-lookup"><span data-stu-id="44a79-108">Related macros:</span></span>  <br/> |<span data-ttu-id="44a79-109">[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md)</span><span class="sxs-lookup"><span data-stu-id="44a79-109">[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropTagArray
{
  ULONG cValues;
  ULONG aulPropTag[MAPI_DIM];
} SPropTagArray, FAR *LPSPropTagArray;

```

## <a name="members"></a><span data-ttu-id="44a79-110">Members</span><span class="sxs-lookup"><span data-stu-id="44a79-110">Members</span></span>

 <span data-ttu-id="44a79-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="44a79-111">**cValues**</span></span>
  
> <span data-ttu-id="44a79-112">Nombre de balises de propriété dans le tableau indiqué par le membre **aulPropTag** .</span><span class="sxs-lookup"><span data-stu-id="44a79-112">Count of property tags in the array indicated by the **aulPropTag** member.</span></span> 
    
 <span data-ttu-id="44a79-113">**aulPropTag**</span><span class="sxs-lookup"><span data-stu-id="44a79-113">**aulPropTag**</span></span>
  
> <span data-ttu-id="44a79-114">Tableau de balises de propriété.</span><span class="sxs-lookup"><span data-stu-id="44a79-114">Array of property tags.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="44a79-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="44a79-115">Remarks</span></span>

<span data-ttu-id="44a79-116">Une balise de propriété est un entier non signé 32 bits composé de deux parties:</span><span class="sxs-lookup"><span data-stu-id="44a79-116">A property tag is a 32-bit unsigned integer that consists of two parts:</span></span> 
  
- <span data-ttu-id="44a79-117">Identificateur dans l'ordre décroissant de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="44a79-117">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="44a79-118">Un type dans les bits de poids faible 16.</span><span class="sxs-lookup"><span data-stu-id="44a79-118">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="44a79-119">L'identificateur est une valeur numérique dans une plage particulière.</span><span class="sxs-lookup"><span data-stu-id="44a79-119">The identifier is a numeric value in a particular range.</span></span> <span data-ttu-id="44a79-120">MAPI définit des plages d'identificateurs pour décrire ce à quoi la propriété est utilisée et qui est responsable de sa maintenance.</span><span class="sxs-lookup"><span data-stu-id="44a79-120">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="44a79-121">MAPI définit des contraintes pour chacune des balises de propriété qu'il prend en charge dans le fichier d'en-tête Mapitags. h.</span><span class="sxs-lookup"><span data-stu-id="44a79-121">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="44a79-122">Le type indique le format de la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="44a79-122">The type indicates the format for the property's value.</span></span> <span data-ttu-id="44a79-123">MAPI définit des constantes pour chaque type de propriété qu'il prend en charge dans le fichier d'en-tête Mapidefs. h.</span><span class="sxs-lookup"><span data-stu-id="44a79-123">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="44a79-124">Pour plus d'informations sur les balises de propriétés et leurs composants, consultez l'une des rubriques suivantes:</span><span class="sxs-lookup"><span data-stu-id="44a79-124">For more information about property tags and their components, see one of the following topics:</span></span> 
  
[<span data-ttu-id="44a79-125">Balises de propriété MAPI</span><span class="sxs-lookup"><span data-stu-id="44a79-125">MAPI Property Tags</span></span>](mapi-property-tags.md)
  
[<span data-ttu-id="44a79-126">Vue d'ensemble de l'identificateur de propriété MAPI</span><span class="sxs-lookup"><span data-stu-id="44a79-126">MAPI Property Identifier Overview</span></span>](mapi-property-identifier-overview.md)
  
[<span data-ttu-id="44a79-127">Vue d'ensemble du type de propriété MAPI</span><span class="sxs-lookup"><span data-stu-id="44a79-127">MAPI Property Type Overview</span></span>](mapi-property-type-overview.md)
  
<span data-ttu-id="44a79-128">Pour obtenir la liste complète des types de propriétés à valeur unique et à valeurs multiples, consultez l'annexe, [identificateurs et types de propriétés](property-identifiers-and-types.md).</span><span class="sxs-lookup"><span data-stu-id="44a79-128">For a complete list of the single-valued and multi-valued property types, see the appendix, [Property Identifiers and Types](property-identifiers-and-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="44a79-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44a79-129">See also</span></span>



[<span data-ttu-id="44a79-130">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="44a79-130">MAPI Structures</span></span>](mapi-structures.md)

