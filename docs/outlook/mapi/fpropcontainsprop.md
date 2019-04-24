---
title: FPropContainsProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropContainsProp
api_type:
- COM
ms.assetid: 43da5b59-7691-49aa-b83c-753d43bfd8fd
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ea56996ad56bb4ce93d103a75eba2c29e6059a87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328041"
---
# <a name="fpropcontainsprop"></a><span data-ttu-id="56094-103">FPropContainsProp</span><span class="sxs-lookup"><span data-stu-id="56094-103">FPropContainsProp</span></span>

<span data-ttu-id="56094-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56094-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56094-105">Compare deux valeurs de propriété, généralement des chaînes ou des tableaux binaires, pour voir si l'une d'entre elles contient l'autre.</span><span class="sxs-lookup"><span data-stu-id="56094-105">Compares two property values, generally strings or binary arrays, to see if one contains the other.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="56094-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="56094-106">Header file:</span></span>  <br/> |<span data-ttu-id="56094-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="56094-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="56094-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="56094-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="56094-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="56094-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="56094-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="56094-110">Called by:</span></span>  <br/> |<span data-ttu-id="56094-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="56094-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a><span data-ttu-id="56094-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56094-112">Parameters</span></span>

<span data-ttu-id="56094-113">_lpSPropValueDst_</span><span class="sxs-lookup"><span data-stu-id="56094-113">_lpSPropValueDst_</span></span>
  
> <span data-ttu-id="56094-114">dans Pointeur vers une structure [SPropValue](spropvalue.md) définissant la valeur de la propriété susceptible de contenir la chaîne de recherche désignée par le paramètre _lpSPropValueSrc_ .</span><span class="sxs-lookup"><span data-stu-id="56094-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property value that might contain the search string pointed to by the  _lpSPropValueSrc_ parameter.</span></span> 
    
<span data-ttu-id="56094-115">_lpSPropValueSrc_</span><span class="sxs-lookup"><span data-stu-id="56094-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="56094-116">dans Pointeur vers une structure **SPropValue** définissant la chaîne de recherche que **FPropContainsProp** cherche dans la valeur de la propriété vers laquelle pointe le paramètre _lpSPropValueDst_ .</span><span class="sxs-lookup"><span data-stu-id="56094-116">[in] Pointer to an **SPropValue** structure defining the search string that **FPropContainsProp** is seeking in the property value pointed to by the  _lpSPropValueDst_ parameter.</span></span> 
    
<span data-ttu-id="56094-117">_ulFuzzyLevel_</span><span class="sxs-lookup"><span data-stu-id="56094-117">_ulFuzzyLevel_</span></span>
  
> <span data-ttu-id="56094-118">dans Paramètres d'option définissant le niveau de précision à utiliser dans la comparaison.</span><span class="sxs-lookup"><span data-stu-id="56094-118">[in] Option settings defining the level of preciseness to use in the comparison.</span></span> 

  - <span data-ttu-id="56094-119">Les **16 bits inférieurs** s'appliquent aux propriétés de type PT_BINARY et PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="56094-119">The **lower 16 bits** apply to properties of type PT_BINARY and PT_STRING8.</span></span> <span data-ttu-id="56094-120">Elles doivent être définies sur l'une des valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="56094-120">They must be set to exactly one of the following values:</span></span>
      
    - <span data-ttu-id="56094-121">FL_FULLSTRING: la chaîne de recherche _lpSPropValueSrc_ doit être égale à la valeur de la propriété identifiée par _lpSPropValueDst_.</span><span class="sxs-lookup"><span data-stu-id="56094-121">FL_FULLSTRING: The  _lpSPropValueSrc_ search string must be equal to the property value identified by  _lpSPropValueDst_.</span></span>
        
    - <span data-ttu-id="56094-122">FL_PREFIX: la chaîne de recherche _lpSPropValueSrc_ doit apparaître au début de la valeur de propriété identifiée par _lpSPropValueDst_.</span><span class="sxs-lookup"><span data-stu-id="56094-122">FL_PREFIX: The  _lpSPropValueSrc_ search string must appear at the beginning of the property value identified by  _lpSPropValueDst_.</span></span> <span data-ttu-id="56094-123">Les deux valeurs ne doivent être comparées qu'à la longueur de la chaîne de recherche indiquée par _lpSPropValueSrc_.</span><span class="sxs-lookup"><span data-stu-id="56094-123">The two values should be compared only up to the length of the search string indicated by  _lpSPropValueSrc_.</span></span> 
        
    - <span data-ttu-id="56094-124">FL_SUBSTRING: la chaîne de recherche _lpSPropValueSrc_ doit être contenue n'importe où dans la valeur de la propriété identifiée par _lpSPropValueDst_.</span><span class="sxs-lookup"><span data-stu-id="56094-124">FL_SUBSTRING: The  _lpSPropValueSrc_ search string must be contained anywhere in the property value identified by  _lpSPropValueDst_.</span></span> 
      
  - <span data-ttu-id="56094-125">Les **16 bits supérieurs** s'appliquent uniquement aux propriétés de type PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="56094-125">The **upper 16 bits** apply only to properties of type PT_STRING8.</span></span> <span data-ttu-id="56094-126">Elles peuvent être définies sur les valeurs suivantes dans n'importe quelle combinaison:</span><span class="sxs-lookup"><span data-stu-id="56094-126">They can be set to the following values in any combination:</span></span>
    
    - <span data-ttu-id="56094-127">FL_IGNORECASE: la comparaison doit être effectuée sans prendre en compte le respect de la casse.</span><span class="sxs-lookup"><span data-stu-id="56094-127">FL_IGNORECASE: The comparison should be made without considering case sensitivity.</span></span> 
        
    - <span data-ttu-id="56094-128">FL_IGNORENONSPACE: la comparaison doit ignorer les caractères d'espacement définis par Unicode tels que les signes diacritiques.</span><span class="sxs-lookup"><span data-stu-id="56094-128">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined nonspacing characters such as diacritical marks.</span></span> 
        
    - <span data-ttu-id="56094-129">FL_LOOSE: la comparaison doit indiquer une correspondance dans la mesure du possible, sans tenir compte du respect de la casse et des caractères sans espacement.</span><span class="sxs-lookup"><span data-stu-id="56094-129">FL_LOOSE: The comparison should indicate a match whenever possible, ignoring case sensitivity and nonspacing characters.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="56094-130">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="56094-130">Return value</span></span>

<span data-ttu-id="56094-131">TRUE</span><span class="sxs-lookup"><span data-stu-id="56094-131">TRUE</span></span> 
  
> <span data-ttu-id="56094-132">Les paramètres sont tous valides et la chaîne de recherche _lpSPropValueSrc_ est contenue comme indiqué dans la valeur de la propriété _lpSPropValueDst_ .</span><span class="sxs-lookup"><span data-stu-id="56094-132">The parameters are all valid and the  _lpSPropValueSrc_ search string is contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
<span data-ttu-id="56094-133">FALSE</span><span class="sxs-lookup"><span data-stu-id="56094-133">FALSE</span></span> 
  
> <span data-ttu-id="56094-134">Les valeurs de propriété comparées ne sont pas de type PT_STRING8 ou PT_BINARY, les valeurs de propriété sont de types différents ou la chaîne de recherche _lpSPropValueSrc_ n'est pas contenue comme spécifié dans la valeur de la propriété _lpSPropValueDst_ .</span><span class="sxs-lookup"><span data-stu-id="56094-134">The property values being compared are not of type PT_STRING8 or PT_BINARY, the property values are of different types, or the  _lpSPropValueSrc_ search string is not contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="56094-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="56094-135">Remarks</span></span>

<span data-ttu-id="56094-136">La méthode de comparaison dépend des types de propriétés spécifiés dans les définitions de propriété [SPropValue](spropvalue.md) et de l'heuristique de niveau de fuzzing fournie dans le paramètre _ulFuzzyLevel_ .</span><span class="sxs-lookup"><span data-stu-id="56094-136">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions and the fuzzy level heuristic provided in the  _ulFuzzyLevel_ parameter.</span></span> <span data-ttu-id="56094-137">Les fonctions [FPropCompareProp](fpropcompareprop.md) et **FPropContainsProp** peuvent être utilisées pour préparer les restrictions de génération d'une table.</span><span class="sxs-lookup"><span data-stu-id="56094-137">The [FPropCompareProp](fpropcompareprop.md) and **FPropContainsProp** functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="56094-138">Les 16 bits supérieurs de _ulFuzzyLevel_ sont ignorés pour le type de propriété PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="56094-138">The upper 16 bits of  _ulFuzzyLevel_ are ignored for property type PT_BINARY.</span></span> <span data-ttu-id="56094-139">Si les paramètres dans _ulFuzzyLevel_ sont manquants ou non valides, une correspondance exacte de chaîne complète est effectuée.</span><span class="sxs-lookup"><span data-stu-id="56094-139">If the settings in  _ulFuzzyLevel_ are missing or invalid, a full-string exact match is performed.</span></span> <span data-ttu-id="56094-140">Pour plus d'informations sur la relation contenant-contenu des propriétés, voir la structure [SContentRestriction](scontentrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="56094-140">For more information about property containment, see the [SContentRestriction](scontentrestriction.md) structure.</span></span> 
  

