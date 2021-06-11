---
title: IMAPITableSetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SetCollapseState
api_type:
- COM
ms.assetid: 31325e8f-1cf9-49b2-8118-953996b0037f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7351457dc5b72cfc4a7ef9f91e9d33a80ca98c39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414066"
---
# <a name="imapitablesetcollapsestate"></a><span data-ttu-id="d953e-103">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="d953e-103">IMAPITable::SetCollapseState</span></span>

  
  
<span data-ttu-id="d953e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d953e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d953e-105">Reconstruit l’état étendu ou réduire actuel d’une table classée à l’aide de données enregistrées par un appel précédent à la méthode [IMAPITable::GetCollapseState.](imapitable-getcollapsestate.md)</span><span class="sxs-lookup"><span data-stu-id="d953e-105">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) method.</span></span> 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a><span data-ttu-id="d953e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d953e-106">Parameters</span></span>

 <span data-ttu-id="d953e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d953e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d953e-108">Réservé ; doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="d953e-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="d953e-109">_cbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="d953e-109">_cbCollapseState_</span></span>
  
> <span data-ttu-id="d953e-110">[in] Nombre d’octets dans la structure pointée par le _paramètre pbCollapseState._</span><span class="sxs-lookup"><span data-stu-id="d953e-110">[in] Count of bytes in the structure pointed to by the  _pbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="d953e-111">_pbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="d953e-111">_pbCollapseState_</span></span>
  
> <span data-ttu-id="d953e-112">[in] Pointeur vers les structures contenant les données nécessaires à la reconstruction de la vue de table.</span><span class="sxs-lookup"><span data-stu-id="d953e-112">[in] Pointer to the structures containing the data needed to rebuild the table view.</span></span>
    
 <span data-ttu-id="d953e-113">_lpbkLocation_</span><span class="sxs-lookup"><span data-stu-id="d953e-113">_lpbkLocation_</span></span>
  
> <span data-ttu-id="d953e-114">[out] Pointeur vers un signet identifiant la ligne du tableau à partir de laquelle l’état réduire ou développé doit être reconstruit.</span><span class="sxs-lookup"><span data-stu-id="d953e-114">[out] Pointer to a bookmark identifying the row in the table at which the collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="d953e-115">Ce signet et la clé d’instance transmises dans le paramètre  _lpbInstanceKey_ dans l’appel à [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) identifient la même ligne.</span><span class="sxs-lookup"><span data-stu-id="d953e-115">This bookmark and the instance key passed in the  _lpbInstanceKey_ parameter in the call to [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) identify the same row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d953e-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d953e-116">Return value</span></span>

<span data-ttu-id="d953e-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="d953e-117">S_OK</span></span> 
  
> <span data-ttu-id="d953e-118">L’état de la table classée a été correctement reconstruit.</span><span class="sxs-lookup"><span data-stu-id="d953e-118">The state of the categorized table was successfully rebuilt.</span></span>
    
<span data-ttu-id="d953e-119">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="d953e-119">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="d953e-120">Une autre opération est en cours qui empêche le démarrage de l’opération.</span><span class="sxs-lookup"><span data-stu-id="d953e-120">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="d953e-121">L’opération en cours doit être autorisée ou arrêtée.</span><span class="sxs-lookup"><span data-stu-id="d953e-121">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="d953e-122">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="d953e-122">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="d953e-123">Le tableau n’a pas pu terminer la reconstruction de la vue collapsed ou expanded.</span><span class="sxs-lookup"><span data-stu-id="d953e-123">The table could not finish rebuilding the collapsed or expanded view.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d953e-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="d953e-124">Remarks</span></span>

<span data-ttu-id="d953e-125">La **méthode IMAPITable::SetCollapseState** rétablit l’état développé ou réduire de l’affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="d953e-125">The **IMAPITable::SetCollapseState** method reestablishes the expanded or collapsed state of the table view.</span></span> <span data-ttu-id="d953e-126">**SetCollapseState et** **GetCollapseState** fonctionnent ensemble comme suit :</span><span class="sxs-lookup"><span data-stu-id="d953e-126">**SetCollapseState** and **GetCollapseState** work together as follows:</span></span> 
  
1. <span data-ttu-id="d953e-127">Lorsque l’état d’une table classée est sur le point de changer, [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) est appelé pour enregistrer toutes les données relatives à l’état avant la modification.</span><span class="sxs-lookup"><span data-stu-id="d953e-127">When the state of a categorized table is about to change, [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) is called to save all of the data pertaining to the state prior to the change.</span></span> 
    
2. <span data-ttu-id="d953e-128">Pour restaurer l’état enregistré de la table, **SetCollapseState** est appelé.</span><span class="sxs-lookup"><span data-stu-id="d953e-128">To restore the view of the table to its saved state, **SetCollapseState** is called.</span></span> <span data-ttu-id="d953e-129">Les données enregistrées **par GetCollapseState** sont **transmises à SetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="d953e-129">The data saved by **GetCollapseState** is passed to **SetCollapseState**.</span></span> <span data-ttu-id="d953e-130">**SetCollapseState** est en mesure d’utiliser ces données pour restaurer l’état.</span><span class="sxs-lookup"><span data-stu-id="d953e-130">**SetCollapseState** is able to use that data to restore the state.</span></span> 
    
3. <span data-ttu-id="d953e-131">**SetCollapseState** renvoie en tant que paramètre de sortie un signet qui identifie la même ligne que la clé d’instance transmise en tant qu’entrée à **GetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="d953e-131">**SetCollapseState** returns as an output parameter a bookmark that identifies the same row as the instance key passed as input to **GetCollapseState**.</span></span>
    
<span data-ttu-id="d953e-132">Pour plus d’informations sur les tableaux classés, voir [Tri et catégorisation.](sorting-and-categorization.md)</span><span class="sxs-lookup"><span data-stu-id="d953e-132">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d953e-133">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="d953e-133">Notes to implementers</span></span>

<span data-ttu-id="d953e-134">Vous devez vérifier que l’ordre de tri et les restrictions sont exactement les mêmes qu’au moment de l’appel **getCollapseState.**</span><span class="sxs-lookup"><span data-stu-id="d953e-134">You are responsible for verifying that the sort order and restrictions are exactly the same as they were at the time of the **GetCollapseState** call.</span></span> <span data-ttu-id="d953e-135">Si une modification a été faite, **SetCollapseState** ne doit pas être appelé, car les résultats peuvent être imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="d953e-135">If a change has been made, **SetCollapseState** should not be called because the results can be unpredictable.</span></span> <span data-ttu-id="d953e-136">Cela peut se produire si, par exemple, un client appelle **GetCollapseState,** puis **SortTable** pour modifier la clé de tri avant d’appeler **SetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="d953e-136">This can happen if, for example, a client calls **GetCollapseState** and then **SortTable** to change the sort key before calling **SetCollapseState**.</span></span> <span data-ttu-id="d953e-137">Pour des raisons de sécurité, vérifiez que les données enregistrées sont toujours valides avant de poursuivre la restauration.</span><span class="sxs-lookup"><span data-stu-id="d953e-137">To be safe, check that the saved data is still valid before proceeding with the restoration.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d953e-138">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="d953e-138">Notes to callers</span></span>

<span data-ttu-id="d953e-139">Pour appeler **SetCollapseState,** vous devez avoir précédemment **appelé GetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="d953e-139">To call **SetCollapseState**, you must have previously called **GetCollapseState**.</span></span> <span data-ttu-id="d953e-140">L’ordre de tri qui établit les catégories doit être le même pour les deux méthodes.</span><span class="sxs-lookup"><span data-stu-id="d953e-140">The sort order establishing the categories should be the same for both methods.</span></span> <span data-ttu-id="d953e-141">Si les ordres de tri diffèrent, les résultats de l’opération **SetCollapseState** sont imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="d953e-141">If the sort orders differ, the results of the **SetCollapseState** operation are unpredictable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d953e-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d953e-142">See also</span></span>



[<span data-ttu-id="d953e-143">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="d953e-143">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="d953e-144">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="d953e-144">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="d953e-145">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="d953e-145">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="d953e-146">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d953e-146">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

