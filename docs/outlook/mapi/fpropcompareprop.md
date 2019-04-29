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
ms.openlocfilehash: 7726811467324242037ec11a69ae0b1b123d7f21
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427156"
---
# <a name="fpropcompareprop"></a><span data-ttu-id="64017-103">FPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="64017-103">FPropCompareProp</span></span>

<span data-ttu-id="64017-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64017-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64017-105">Compare deux valeurs de propriété à l'aide d'un opérateur relationnel spécifié.</span><span class="sxs-lookup"><span data-stu-id="64017-105">Compares two property values using a specified relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="64017-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="64017-106">Header file:</span></span>  <br/> |<span data-ttu-id="64017-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="64017-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="64017-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="64017-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="64017-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="64017-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="64017-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="64017-110">Called by:</span></span>  <br/> |<span data-ttu-id="64017-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="64017-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a><span data-ttu-id="64017-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64017-112">Parameters</span></span>

<span data-ttu-id="64017-113">_lpSPropValue1_</span><span class="sxs-lookup"><span data-stu-id="64017-113">_lpSPropValue1_</span></span>
  
> <span data-ttu-id="64017-114">dans Pointeur vers une structure [SPropValue](spropvalue.md) définissant la première valeur de la propriété à comparer.</span><span class="sxs-lookup"><span data-stu-id="64017-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value for comparison.</span></span> 
    
<span data-ttu-id="64017-115">_ulRelOp_</span><span class="sxs-lookup"><span data-stu-id="64017-115">_ulRelOp_</span></span>
  
> <span data-ttu-id="64017-116">dans Opérateur relationnel à utiliser dans la comparaison.</span><span class="sxs-lookup"><span data-stu-id="64017-116">[in] The relational operator to use in the comparison.</span></span> <span data-ttu-id="64017-117">Pour les valeurs autorisées, consultez la structure [SComparePropsRestriction](scomparepropsrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="64017-117">For allowable values, see the [SComparePropsRestriction](scomparepropsrestriction.md) structure.</span></span> 
    
<span data-ttu-id="64017-118">_lpSPropValue2_</span><span class="sxs-lookup"><span data-stu-id="64017-118">_lpSPropValue2_</span></span>
  
> <span data-ttu-id="64017-119">dans Pointeur vers une structure **SPropValue** définissant la deuxième valeur de la propriété à comparer.</span><span class="sxs-lookup"><span data-stu-id="64017-119">[in] Pointer to an **SPropValue** structure defining the second property value for comparison.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="64017-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="64017-120">Return value</span></span>

<span data-ttu-id="64017-121">TRUE</span><span class="sxs-lookup"><span data-stu-id="64017-121">TRUE</span></span> 
  
> <span data-ttu-id="64017-122">Les valeurs de propriété répondent à la relation spécifiée.</span><span class="sxs-lookup"><span data-stu-id="64017-122">The property values satisfy the specified relation.</span></span> 
    
<span data-ttu-id="64017-123">FALSE</span><span class="sxs-lookup"><span data-stu-id="64017-123">FALSE</span></span> 
  
> <span data-ttu-id="64017-124">Les valeurs de propriété ne satisfont pas la relation spécifiée.</span><span class="sxs-lookup"><span data-stu-id="64017-124">The property values do not satisfy the specified relation.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="64017-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="64017-125">Remarks</span></span>

<span data-ttu-id="64017-126">La méthode de comparaison dépend des types de propriétés spécifiés dans les définitions de propriété [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="64017-126">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions.</span></span> <span data-ttu-id="64017-127">Les fonctions **FPropCompareProp** et [FPropContainsProp](fpropcontainsprop.md) peuvent être utilisées pour préparer les restrictions de génération d'une table.</span><span class="sxs-lookup"><span data-stu-id="64017-127">The **FPropCompareProp** and [FPropContainsProp](fpropcontainsprop.md) functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="64017-128">L'ordre de comparaison est _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span><span class="sxs-lookup"><span data-stu-id="64017-128">The order of comparison is  _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span></span> <span data-ttu-id="64017-129">Si les types de propriétés des valeurs de propriété à comparer ne correspondent pas, la fonction **FPropCompareProp** renvoie false.</span><span class="sxs-lookup"><span data-stu-id="64017-129">If the property types of the property values to be compared do not match, the **FPropCompareProp** function returns FALSE.</span></span> 
  

