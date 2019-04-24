---
title: IMAPITableQuerySortOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QuerySortOrder
api_type:
- COM
ms.assetid: 7b4ca523-0703-417c-8586-c4324c200020
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 61991972fdf8674a9ffd2b790e26c7fa669df357
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328860"
---
# <a name="imapitablequerysortorder"></a><span data-ttu-id="45d9d-103">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="45d9d-103">IMAPITable::QuerySortOrder</span></span>

  
  
<span data-ttu-id="45d9d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45d9d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45d9d-105">Récupère l'ordre de tri actuel d'une table.</span><span class="sxs-lookup"><span data-stu-id="45d9d-105">Retrieves the current sort order for a table.</span></span>
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a><span data-ttu-id="45d9d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="45d9d-106">Parameters</span></span>

 <span data-ttu-id="45d9d-107">_lppSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="45d9d-107">_lppSortCriteria_</span></span>
  
> <span data-ttu-id="45d9d-108">remarquer Pointeur vers un pointeur vers la structure [SSortOrderSet](ssortorderset.md) qui contient l'ordre de tri actuel.</span><span class="sxs-lookup"><span data-stu-id="45d9d-108">[out] Pointer to a pointer to the [SSortOrderSet](ssortorderset.md) structure holding the current sort order.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="45d9d-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="45d9d-109">Return value</span></span>

<span data-ttu-id="45d9d-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="45d9d-110">S_OK</span></span> 
  
> <span data-ttu-id="45d9d-111">L'ordre de tri actuel a été renvoyé.</span><span class="sxs-lookup"><span data-stu-id="45d9d-111">The current sort order was successfully returned.</span></span>
    
<span data-ttu-id="45d9d-112">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="45d9d-112">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="45d9d-113">Une autre opération est en cours, ce qui empêche le démarrage de l'opération de récupération de l'ordre de tri.</span><span class="sxs-lookup"><span data-stu-id="45d9d-113">Another operation is in progress that prevents the sort order retrieval operation from starting.</span></span> <span data-ttu-id="45d9d-114">L'opération en cours doit être autorisée ou elle doit être arrêtée.</span><span class="sxs-lookup"><span data-stu-id="45d9d-114">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="45d9d-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="45d9d-115">Remarks</span></span>

<span data-ttu-id="45d9d-116">La méthode **IMAPITable:: QuerySortOrder** extrait l'ordre de tri actuel d'une table.</span><span class="sxs-lookup"><span data-stu-id="45d9d-116">The **IMAPITable::QuerySortOrder** method retrieves the current sort order for a table.</span></span> <span data-ttu-id="45d9d-117">Les ordres de tri sont décrits par une structure [SSortOrderSet](ssortorderset.md) .</span><span class="sxs-lookup"><span data-stu-id="45d9d-117">Sort orders are described with an [SSortOrderSet](ssortorderset.md) structure.</span></span> 
  
- <span data-ttu-id="45d9d-118">Le membre **cSorts** de la structure **SSortOrderSet** peut être défini sur zéro si:</span><span class="sxs-lookup"><span data-stu-id="45d9d-118">The **cSorts** member of the **SSortOrderSet** structure can be set to zero if:</span></span> 
    
- <span data-ttu-id="45d9d-119">Le tableau n'est pas trié.</span><span class="sxs-lookup"><span data-stu-id="45d9d-119">The table is unsorted.</span></span>
    
- <span data-ttu-id="45d9d-120">Il n'existe aucune information sur la façon dont le tableau est trié.</span><span class="sxs-lookup"><span data-stu-id="45d9d-120">There is no information about how the table is sorted.</span></span>
    
- <span data-ttu-id="45d9d-121">La structure **SSortOrderSet** n'est pas appropriée pour décrire l'ordre de tri.</span><span class="sxs-lookup"><span data-stu-id="45d9d-121">The **SSortOrderSet** structure is not appropriate for describing the sort order.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="45d9d-122">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="45d9d-122">Notes to implementers</span></span>

<span data-ttu-id="45d9d-123">Si un appel est passé à votre méthode [IMAPITable:: SortTable](imapitable-sorttable.md) avec une structure **SSortOrderSet** contenant zéro colonne dans la clé de tri, supprimez l'ordre de tri actuel et appliquez l'ordre par défaut, s'il en existe un.</span><span class="sxs-lookup"><span data-stu-id="45d9d-123">If a call is made to your [IMAPITable::SortTable](imapitable-sorttable.md) method with an **SSortOrderSet** structure containing zero columns in the sort key, remove the current sort order and apply the default order, if there is one.</span></span> <span data-ttu-id="45d9d-124">Dans les appels suivants à **QuerySortOrder**, vous pouvez choisir de renvoyer zéro ou plusieurs colonnes pour la clé de tri.</span><span class="sxs-lookup"><span data-stu-id="45d9d-124">In subsequent calls to **QuerySortOrder**, you can choose whether to return zero or more columns for the sort key.</span></span> <span data-ttu-id="45d9d-125">Vous pouvez renvoyer plus de colonnes que ce qui est dans la vue actuelle.</span><span class="sxs-lookup"><span data-stu-id="45d9d-125">You can return more columns than are in the present view.</span></span>
  
<span data-ttu-id="45d9d-126">Pour plus d'informations sur le tri, reportez-vous à la rubrique [Tri et catégorisation](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="45d9d-126">For more information about sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="45d9d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45d9d-127">See also</span></span>



[<span data-ttu-id="45d9d-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="45d9d-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="45d9d-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="45d9d-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="45d9d-130">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="45d9d-130">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="45d9d-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="45d9d-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

