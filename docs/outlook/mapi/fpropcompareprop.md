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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7726811467324242037ec11a69ae0b1b123d7f21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328069"
---
# <a name="fpropcompareprop"></a><span data-ttu-id="826ae-103">FPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="826ae-103">FPropCompareProp</span></span>

<span data-ttu-id="826ae-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="826ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="826ae-105">Compare deux valeurs de propriété à l'aide d'un opérateur relationnel spécifié.</span><span class="sxs-lookup"><span data-stu-id="826ae-105">Compares two property values using a specified relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="826ae-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="826ae-106">Header file:</span></span>  <br/> |<span data-ttu-id="826ae-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="826ae-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="826ae-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="826ae-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="826ae-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="826ae-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="826ae-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="826ae-110">Called by:</span></span>  <br/> |<span data-ttu-id="826ae-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="826ae-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a><span data-ttu-id="826ae-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="826ae-112">Parameters</span></span>

<span data-ttu-id="826ae-113">_lpSPropValue1_</span><span class="sxs-lookup"><span data-stu-id="826ae-113">_lpSPropValue1_</span></span>
  
> <span data-ttu-id="826ae-114">dans Pointeur vers une structure [SPropValue](spropvalue.md) définissant la première valeur de la propriété à comparer.</span><span class="sxs-lookup"><span data-stu-id="826ae-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value for comparison.</span></span> 
    
<span data-ttu-id="826ae-115">_ulRelOp_</span><span class="sxs-lookup"><span data-stu-id="826ae-115">_ulRelOp_</span></span>
  
> <span data-ttu-id="826ae-116">dans Opérateur relationnel à utiliser dans la comparaison.</span><span class="sxs-lookup"><span data-stu-id="826ae-116">[in] The relational operator to use in the comparison.</span></span> <span data-ttu-id="826ae-117">Pour les valeurs autorisées, consultez la structure [SComparePropsRestriction](scomparepropsrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="826ae-117">For allowable values, see the [SComparePropsRestriction](scomparepropsrestriction.md) structure.</span></span> 
    
<span data-ttu-id="826ae-118">_lpSPropValue2_</span><span class="sxs-lookup"><span data-stu-id="826ae-118">_lpSPropValue2_</span></span>
  
> <span data-ttu-id="826ae-119">dans Pointeur vers une structure **SPropValue** définissant la deuxième valeur de la propriété à comparer.</span><span class="sxs-lookup"><span data-stu-id="826ae-119">[in] Pointer to an **SPropValue** structure defining the second property value for comparison.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="826ae-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="826ae-120">Return value</span></span>

<span data-ttu-id="826ae-121">TRUE</span><span class="sxs-lookup"><span data-stu-id="826ae-121">TRUE</span></span> 
  
> <span data-ttu-id="826ae-122">Les valeurs de propriété répondent à la relation spécifiée.</span><span class="sxs-lookup"><span data-stu-id="826ae-122">The property values satisfy the specified relation.</span></span> 
    
<span data-ttu-id="826ae-123">FALSE</span><span class="sxs-lookup"><span data-stu-id="826ae-123">FALSE</span></span> 
  
> <span data-ttu-id="826ae-124">Les valeurs de propriété ne satisfont pas la relation spécifiée.</span><span class="sxs-lookup"><span data-stu-id="826ae-124">The property values do not satisfy the specified relation.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="826ae-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="826ae-125">Remarks</span></span>

<span data-ttu-id="826ae-126">La méthode de comparaison dépend des types de propriétés spécifiés dans les définitions de propriété [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="826ae-126">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions.</span></span> <span data-ttu-id="826ae-127">Les fonctions **FPropCompareProp** et [FPropContainsProp](fpropcontainsprop.md) peuvent être utilisées pour préparer les restrictions de génération d'une table.</span><span class="sxs-lookup"><span data-stu-id="826ae-127">The **FPropCompareProp** and [FPropContainsProp](fpropcontainsprop.md) functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="826ae-128">L'ordre de comparaison est _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span><span class="sxs-lookup"><span data-stu-id="826ae-128">The order of comparison is  _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span></span> <span data-ttu-id="826ae-129">Si les types de propriétés des valeurs de propriété à comparer ne correspondent pas, la fonction **FPropCompareProp** renvoie false.</span><span class="sxs-lookup"><span data-stu-id="826ae-129">If the property types of the property values to be compared do not match, the **FPropCompareProp** function returns FALSE.</span></span> 
  

