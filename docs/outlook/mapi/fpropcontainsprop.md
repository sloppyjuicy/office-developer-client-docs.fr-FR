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
ms.openlocfilehash: abf33e4167d836aeb88fdefb30ba05840e80ce63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783366"
---
# <a name="fpropcontainsprop"></a><span data-ttu-id="963e4-103">FPropContainsProp</span><span class="sxs-lookup"><span data-stu-id="963e4-103">FPropContainsProp</span></span>

<span data-ttu-id="963e4-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="963e4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="963e4-105">Compare deux valeurs de propriété, généralement des chaînes ou des tableaux binaires, pour voir si un contient l’autre.</span><span class="sxs-lookup"><span data-stu-id="963e4-105">Compares two property values, generally strings or binary arrays, to see if one contains the other.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="963e4-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="963e4-106">Header file:</span></span>  <br/> |<span data-ttu-id="963e4-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="963e4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="963e4-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="963e4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="963e4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="963e4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="963e4-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="963e4-110">Called by:</span></span>  <br/> |<span data-ttu-id="963e4-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="963e4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a><span data-ttu-id="963e4-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="963e4-112">Parameters</span></span>

<span data-ttu-id="963e4-113">_lpSPropValueDst_</span><span class="sxs-lookup"><span data-stu-id="963e4-113">_lpSPropValueDst_</span></span>
  
> <span data-ttu-id="963e4-114">[in] Pointeur vers une structure [SPropValue](spropvalue.md) définissant la valeur de la propriété qui peut contenir la chaîne de recherche indiqué par le paramètre _lpSPropValueSrc_ .</span><span class="sxs-lookup"><span data-stu-id="963e4-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property value that might contain the search string pointed to by the  _lpSPropValueSrc_ parameter.</span></span> 
    
<span data-ttu-id="963e4-115">_lpSPropValueSrc_</span><span class="sxs-lookup"><span data-stu-id="963e4-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="963e4-116">[in] Pointeur vers une structure **SPropValue** définition de la chaîne de recherche qui recherche **FPropContainsProp** dans la valeur de propriété indiqué par le paramètre _lpSPropValueDst_ .</span><span class="sxs-lookup"><span data-stu-id="963e4-116">[in] Pointer to an **SPropValue** structure defining the search string that **FPropContainsProp** is seeking in the property value pointed to by the  _lpSPropValueDst_ parameter.</span></span> 
    
<span data-ttu-id="963e4-117">_ulFuzzyLevel_</span><span class="sxs-lookup"><span data-stu-id="963e4-117">_ulFuzzyLevel_</span></span>
  
> <span data-ttu-id="963e4-118">[in] Paramètres d’option définissant le niveau de précision que permettent à utiliser dans la comparaison.</span><span class="sxs-lookup"><span data-stu-id="963e4-118">[in] Option settings defining the level of preciseness to use in the comparison.</span></span> 

  - <span data-ttu-id="963e4-119">Les **16 bits inférieurs** s’appliquent aux propriétés de type PT_BINARY et PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="963e4-119">The **lower 16 bits** apply to properties of type PT_BINARY and PT_STRING8.</span></span> <span data-ttu-id="963e4-120">Elles doivent être définies exactement une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="963e4-120">They must be set to exactly one of the following values:</span></span>
      
    - <span data-ttu-id="963e4-121">FL_FULLSTRING : La chaîne de recherche _lpSPropValueSrc_ doit être égale à la valeur de la propriété identifiée par _lpSPropValueDst_.</span><span class="sxs-lookup"><span data-stu-id="963e4-121">FL_FULLSTRING: The  _lpSPropValueSrc_ search string must be equal to the property value identified by  _lpSPropValueDst_.</span></span>
        
    - <span data-ttu-id="963e4-122">FL_PREFIX : La chaîne de recherche _lpSPropValueSrc_ doit apparaître au début de la valeur de la propriété identifié par _lpSPropValueDst_.</span><span class="sxs-lookup"><span data-stu-id="963e4-122">FL_PREFIX: The  _lpSPropValueSrc_ search string must appear at the beginning of the property value identified by  _lpSPropValueDst_.</span></span> <span data-ttu-id="963e4-123">Les deux valeurs doivent être comparées uniquement jusqu'à la longueur de la chaîne de recherche indiquée par _lpSPropValueSrc_.</span><span class="sxs-lookup"><span data-stu-id="963e4-123">The two values should be compared only up to the length of the search string indicated by  _lpSPropValueSrc_.</span></span> 
        
    - <span data-ttu-id="963e4-124">FL_SUBSTRING : La chaîne de recherche _lpSPropValueSrc_ doit figurer n’importe où dans la valeur de la propriété identifiée par _lpSPropValueDst_.</span><span class="sxs-lookup"><span data-stu-id="963e4-124">FL_SUBSTRING: The  _lpSPropValueSrc_ search string must be contained anywhere in the property value identified by  _lpSPropValueDst_.</span></span> 
      
  - <span data-ttu-id="963e4-125">Les **derniers 16 bits** s’appliquent uniquement aux propriétés de type PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="963e4-125">The **upper 16 bits** apply only to properties of type PT_STRING8.</span></span> <span data-ttu-id="963e4-126">Elles peuvent être définies aux valeurs suivantes dans n’importe quelle combinaison :</span><span class="sxs-lookup"><span data-stu-id="963e4-126">They can be set to the following values in any combination:</span></span>
    
    - <span data-ttu-id="963e4-127">FL_IGNORECASE : La comparaison doit être effectuée sans tenir compte de la casse.</span><span class="sxs-lookup"><span data-stu-id="963e4-127">FL_IGNORECASE: The comparison should be made without considering case sensitivity.</span></span> 
        
    - <span data-ttu-id="963e4-128">FL_IGNORENONSPACE : La comparaison doit ignorer Unicode définie par les caractères tels que diacritiques.</span><span class="sxs-lookup"><span data-stu-id="963e4-128">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined nonspacing characters such as diacritical marks.</span></span> 
        
    - <span data-ttu-id="963e4-129">FL_LOOSE : La comparaison doit indiquer une correspondance la mesure du possible, indépendamment de la casse sensibilité et les caractères.</span><span class="sxs-lookup"><span data-stu-id="963e4-129">FL_LOOSE: The comparison should indicate a match whenever possible, ignoring case sensitivity and nonspacing characters.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="963e4-130">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="963e4-130">Return value</span></span>

<span data-ttu-id="963e4-131">TRUE</span><span class="sxs-lookup"><span data-stu-id="963e4-131">TRUE</span></span> 
  
> <span data-ttu-id="963e4-132">Les paramètres sont valides et du contenu de la chaîne de recherche _lpSPropValueSrc_ comme indiqué dans la valeur de la propriété _lpSPropValueDst_ .</span><span class="sxs-lookup"><span data-stu-id="963e4-132">The parameters are all valid and the  _lpSPropValueSrc_ search string is contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
<span data-ttu-id="963e4-133">FALSE</span><span class="sxs-lookup"><span data-stu-id="963e4-133">FALSE</span></span> 
  
> <span data-ttu-id="963e4-134">Les valeurs de propriété comparées ne sont pas du type PT_STRING8 ou PT_BINARY, les valeurs de propriété sont de types différents, ou la chaîne de recherche _lpSPropValueSrc_ n’est pas contenue comme indiqué dans la valeur de la propriété _lpSPropValueDst_ .</span><span class="sxs-lookup"><span data-stu-id="963e4-134">The property values being compared are not of type PT_STRING8 or PT_BINARY, the property values are of different types, or the  _lpSPropValueSrc_ search string is not contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="963e4-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="963e4-135">Remarks</span></span>

<span data-ttu-id="963e4-136">La méthode de comparaison varie selon les types de propriétés spécifiés dans les définitions de propriétés [SPropValue](spropvalue.md) et l’heuristique de niveau approximative fournies dans le paramètre _ulFuzzyLevel_ .</span><span class="sxs-lookup"><span data-stu-id="963e4-136">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions and the fuzzy level heuristic provided in the  _ulFuzzyLevel_ parameter.</span></span> <span data-ttu-id="963e4-137">Les fonctions [FPropCompareProp](fpropcompareprop.md) et **FPropContainsProp** peuvent servir à préparer des restrictions pour la génération d’une table.</span><span class="sxs-lookup"><span data-stu-id="963e4-137">The [FPropCompareProp](fpropcompareprop.md) and **FPropContainsProp** functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="963e4-138">Les 16 bits de _ulFuzzyLevel_ sont ignorés pour le type de propriété PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="963e4-138">The upper 16 bits of  _ulFuzzyLevel_ are ignored for property type PT_BINARY.</span></span> <span data-ttu-id="963e4-139">Si les paramètres de _ulFuzzyLevel_ sont manquants ou non valides, une correspondance exacte de chaîne complète est effectuée.</span><span class="sxs-lookup"><span data-stu-id="963e4-139">If the settings in  _ulFuzzyLevel_ are missing or invalid, a full-string exact match is performed.</span></span> <span data-ttu-id="963e4-140">Pour plus d’informations sur la relation contenant-contenu propriété, voir la structure [SContentRestriction](scontentrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="963e4-140">For more information about property containment, see the [SContentRestriction](scontentrestriction.md) structure.</span></span> 
  

