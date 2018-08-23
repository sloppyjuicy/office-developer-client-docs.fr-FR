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
ms.openlocfilehash: 48ca692779fb53cab386d8a18b5f0a50e11d531c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569434"
---
# <a name="imapitablequerysortorder"></a><span data-ttu-id="7d01a-103">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="7d01a-103">IMAPITable::QuerySortOrder</span></span>

  
  
<span data-ttu-id="7d01a-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d01a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d01a-105">Récupère l’ordre de tri en cours pour une table.</span><span class="sxs-lookup"><span data-stu-id="7d01a-105">Retrieves the current sort order for a table.</span></span>
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a><span data-ttu-id="7d01a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7d01a-106">Parameters</span></span>

 <span data-ttu-id="7d01a-107">_lppSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="7d01a-107">_lppSortCriteria_</span></span>
  
> <span data-ttu-id="7d01a-108">[out] Pointeur vers un pointeur vers la structure [SSortOrderSet](ssortorderset.md) maintenant l’ordre de tri en cours.</span><span class="sxs-lookup"><span data-stu-id="7d01a-108">[out] Pointer to a pointer to the [SSortOrderSet](ssortorderset.md) structure holding the current sort order.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7d01a-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="7d01a-109">Return value</span></span>

<span data-ttu-id="7d01a-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="7d01a-110">S_OK</span></span> 
  
> <span data-ttu-id="7d01a-111">L’ordre de tri en cours a été renvoyée avec succès.</span><span class="sxs-lookup"><span data-stu-id="7d01a-111">The current sort order was successfully returned.</span></span>
    
<span data-ttu-id="7d01a-112">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="7d01a-112">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="7d01a-113">Une autre opération est en cours qui empêche l’opération de récupération d’ordre de tri de démarrer.</span><span class="sxs-lookup"><span data-stu-id="7d01a-113">Another operation is in progress that prevents the sort order retrieval operation from starting.</span></span> <span data-ttu-id="7d01a-114">L’opération en cours doit être autorisée à effectuer ou il doit être arrêté.</span><span class="sxs-lookup"><span data-stu-id="7d01a-114">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7d01a-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="7d01a-115">Remarks</span></span>

<span data-ttu-id="7d01a-116">La méthode **IMAPITable::QuerySortOrder** récupère l’ordre de tri en cours pour une table.</span><span class="sxs-lookup"><span data-stu-id="7d01a-116">The **IMAPITable::QuerySortOrder** method retrieves the current sort order for a table.</span></span> <span data-ttu-id="7d01a-117">Ordres de tri sont décrits avec une structure [SSortOrderSet](ssortorderset.md) .</span><span class="sxs-lookup"><span data-stu-id="7d01a-117">Sort orders are described with an [SSortOrderSet](ssortorderset.md) structure.</span></span> 
  
- <span data-ttu-id="7d01a-118">Le membre **cSorts** de la structure **SSortOrderSet** peut être défini sur zéro si :</span><span class="sxs-lookup"><span data-stu-id="7d01a-118">The **cSorts** member of the **SSortOrderSet** structure can be set to zero if:</span></span> 
    
- <span data-ttu-id="7d01a-119">Le tableau n’est pas trié.</span><span class="sxs-lookup"><span data-stu-id="7d01a-119">The table is unsorted.</span></span>
    
- <span data-ttu-id="7d01a-120">Il n’existe pas d’informations sur la façon dont la table est triée.</span><span class="sxs-lookup"><span data-stu-id="7d01a-120">There is no information about how the table is sorted.</span></span>
    
- <span data-ttu-id="7d01a-121">La structure **SSortOrderSet** n’est pas appropriée pour la description de l’ordre de tri.</span><span class="sxs-lookup"><span data-stu-id="7d01a-121">The **SSortOrderSet** structure is not appropriate for describing the sort order.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="7d01a-122">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="7d01a-122">Notes to implementers</span></span>

<span data-ttu-id="7d01a-123">Si un appel est effectué à votre méthode [IMAPITable::SortTable](imapitable-sorttable.md) avec une structure **SSortOrderSet** contenant zéro colonnes dans la clé de tri, supprimez l’ordre de tri en cours et appliquer l’ordre par défaut, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="7d01a-123">If a call is made to your [IMAPITable::SortTable](imapitable-sorttable.md) method with an **SSortOrderSet** structure containing zero columns in the sort key, remove the current sort order and apply the default order, if there is one.</span></span> <span data-ttu-id="7d01a-124">Dans les appels suivants à **QuerySortOrder**, vous pouvez choisir s’il faut renvoyer zéro ou plusieurs colonnes de la clé de tri.</span><span class="sxs-lookup"><span data-stu-id="7d01a-124">In subsequent calls to **QuerySortOrder**, you can choose whether to return zero or more columns for the sort key.</span></span> <span data-ttu-id="7d01a-125">Vous pouvez retourner plus de colonnes que dans la vue actuelle.</span><span class="sxs-lookup"><span data-stu-id="7d01a-125">You can return more columns than are in the present view.</span></span>
  
<span data-ttu-id="7d01a-126">Pour plus d’informations sur le tri, voir [tri et catégorisation](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="7d01a-126">For more information about sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7d01a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d01a-127">See also</span></span>



[<span data-ttu-id="7d01a-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="7d01a-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="7d01a-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="7d01a-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="7d01a-130">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="7d01a-130">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="7d01a-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7d01a-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

