---
title: FPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropCompareProp
api_type:
- COM
ms.assetid: 17cb53c4-7154-4a4e-b4ec-de720fa055cb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: adccbaf65adec2c517c4890f722198e8262092cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564604"
---
# <a name="fpropcompareprop"></a><span data-ttu-id="ff641-103">FPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="ff641-103">FPropCompareProp</span></span>

<span data-ttu-id="ff641-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff641-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff641-105">Compare deux valeurs de propriété à l’aide d’un opérateur relationnel spécifié.</span><span class="sxs-lookup"><span data-stu-id="ff641-105">Compares two property values using a specified relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff641-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="ff641-106">Header file:</span></span>  <br/> |<span data-ttu-id="ff641-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ff641-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ff641-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="ff641-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ff641-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ff641-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ff641-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="ff641-110">Called by:</span></span>  <br/> |<span data-ttu-id="ff641-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="ff641-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a><span data-ttu-id="ff641-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff641-112">Parameters</span></span>

<span data-ttu-id="ff641-113">_lpSPropValue1_</span><span class="sxs-lookup"><span data-stu-id="ff641-113">_lpSPropValue1_</span></span>
  
> <span data-ttu-id="ff641-114">[in] Pointeur vers une structure [SPropValue](spropvalue.md) définition de la première valeur de propriété pour la comparaison.</span><span class="sxs-lookup"><span data-stu-id="ff641-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value for comparison.</span></span> 
    
<span data-ttu-id="ff641-115">_ulRelOp_</span><span class="sxs-lookup"><span data-stu-id="ff641-115">_ulRelOp_</span></span>
  
> <span data-ttu-id="ff641-116">[in] L’opérateur relationnel à utiliser dans la comparaison.</span><span class="sxs-lookup"><span data-stu-id="ff641-116">[in] The relational operator to use in the comparison.</span></span> <span data-ttu-id="ff641-117">Pour les valeurs possibles, voir la structure [SComparePropsRestriction](scomparepropsrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="ff641-117">For allowable values, see the [SComparePropsRestriction](scomparepropsrestriction.md) structure.</span></span> 
    
<span data-ttu-id="ff641-118">_lpSPropValue2_</span><span class="sxs-lookup"><span data-stu-id="ff641-118">_lpSPropValue2_</span></span>
  
> <span data-ttu-id="ff641-119">[in] Pointeur vers une structure **SPropValue** définissant la valeur de la propriété deuxième pour la comparaison.</span><span class="sxs-lookup"><span data-stu-id="ff641-119">[in] Pointer to an **SPropValue** structure defining the second property value for comparison.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ff641-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ff641-120">Return value</span></span>

<span data-ttu-id="ff641-121">TRUE</span><span class="sxs-lookup"><span data-stu-id="ff641-121">TRUE</span></span> 
  
> <span data-ttu-id="ff641-122">Les valeurs de propriété satisfont à l’objet relation spécifié.</span><span class="sxs-lookup"><span data-stu-id="ff641-122">The property values satisfy the specified relation.</span></span> 
    
<span data-ttu-id="ff641-123">FALSE</span><span class="sxs-lookup"><span data-stu-id="ff641-123">FALSE</span></span> 
  
> <span data-ttu-id="ff641-124">Les valeurs de propriété ne répondent pas à l’objet relation spécifié.</span><span class="sxs-lookup"><span data-stu-id="ff641-124">The property values do not satisfy the specified relation.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ff641-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="ff641-125">Remarks</span></span>

<span data-ttu-id="ff641-126">Les types de propriétés spécifiés dans les définitions de propriétés [SPropValue](spropvalue.md) dépend de la méthode de comparaison.</span><span class="sxs-lookup"><span data-stu-id="ff641-126">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions.</span></span> <span data-ttu-id="ff641-127">Les fonctions **FPropCompareProp** et [FPropContainsProp](fpropcontainsprop.md) peuvent servir à préparer des restrictions pour la génération d’une table.</span><span class="sxs-lookup"><span data-stu-id="ff641-127">The **FPropCompareProp** and [FPropContainsProp](fpropcontainsprop.md) functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="ff641-128">L’ordre de comparaison est _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span><span class="sxs-lookup"><span data-stu-id="ff641-128">The order of comparison is  _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span></span> <span data-ttu-id="ff641-129">Si les valeurs de propriété à comparer les types de propriétés ne correspondent pas, la fonction **FPropCompareProp** renvoie la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="ff641-129">If the property types of the property values to be compared do not match, the **FPropCompareProp** function returns FALSE.</span></span> 
  

