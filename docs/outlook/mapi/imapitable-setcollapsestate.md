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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 252b6d6c7ff74acd5f0b288af48ff2901c2330ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784110"
---
# <a name="imapitablesetcollapsestate"></a><span data-ttu-id="a2298-103">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="a2298-103">IMAPITable::SetCollapseState</span></span>

  
  
<span data-ttu-id="a2298-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a2298-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a2298-105">Reconstruit l’état actuel de développés ou réduit d’une table, voir l’aide de données qui a été enregistrées par un appel antérieur à la méthode [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) .</span><span class="sxs-lookup"><span data-stu-id="a2298-105">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) method.</span></span> 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a><span data-ttu-id="a2298-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="a2298-106">Parameters</span></span>

 <span data-ttu-id="a2298-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a2298-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a2298-108">Réservé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="a2298-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="a2298-109">_cbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="a2298-109">_cbCollapseState_</span></span>
  
> <span data-ttu-id="a2298-110">[in] Nombre d’octets de la structure vers laquelle pointe le paramètre _pbCollapseState_ .</span><span class="sxs-lookup"><span data-stu-id="a2298-110">[in] Count of bytes in the structure pointed to by the  _pbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="a2298-111">_pbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="a2298-111">_pbCollapseState_</span></span>
  
> <span data-ttu-id="a2298-112">[in] Pointeur vers les structures contenant les données nécessaires à la recréation de l’affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="a2298-112">[in] Pointer to the structures containing the data needed to rebuild the table view.</span></span>
    
 <span data-ttu-id="a2298-113">_lpbkLocation_</span><span class="sxs-lookup"><span data-stu-id="a2298-113">_lpbkLocation_</span></span>
  
> <span data-ttu-id="a2298-114">[out] Pointeur vers un signet qui identifie la ligne dans la table à laquelle l’état réduit ou développé doit être reconstruite.</span><span class="sxs-lookup"><span data-stu-id="a2298-114">[out] Pointer to a bookmark identifying the row in the table at which the collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="a2298-115">Ce signet et la clé d’instance passé dans le paramètre _lpbInstanceKey_ dans l’appel à [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) identifient la même ligne.</span><span class="sxs-lookup"><span data-stu-id="a2298-115">This bookmark and the instance key passed in the  _lpbInstanceKey_ parameter in the call to [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) identify the same row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a2298-116">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="a2298-116">Return value</span></span>

<span data-ttu-id="a2298-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="a2298-117">S_OK</span></span> 
  
> <span data-ttu-id="a2298-118">L’état de la table par catégorie a été correctement recréé.</span><span class="sxs-lookup"><span data-stu-id="a2298-118">The state of the categorized table was successfully rebuilt.</span></span>
    
<span data-ttu-id="a2298-119">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="a2298-119">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="a2298-120">Une autre opération est en cours qui empêche l’opération de démarrage.</span><span class="sxs-lookup"><span data-stu-id="a2298-120">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="a2298-121">L’opération en cours doit être autorisée à effectuer ou il doit être arrêté.</span><span class="sxs-lookup"><span data-stu-id="a2298-121">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="a2298-122">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="a2298-122">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="a2298-123">Le tableau n’a pas pu terminer la reconstruction de l’affichage réduit ou développé.</span><span class="sxs-lookup"><span data-stu-id="a2298-123">The table could not finish rebuilding the collapsed or expanded view.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a2298-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="a2298-124">Remarks</span></span>

<span data-ttu-id="a2298-125">La méthode **IMAPITable::SetCollapseState** rétablit l’état développé ou réduit de l’affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="a2298-125">The **IMAPITable::SetCollapseState** method reestablishes the expanded or collapsed state of the table view.</span></span> <span data-ttu-id="a2298-126">**SetCollapseState** et **GetCollapseState** collaborent comme suit :</span><span class="sxs-lookup"><span data-stu-id="a2298-126">**SetCollapseState** and **GetCollapseState** work together as follows:</span></span> 
  
1. <span data-ttu-id="a2298-127">Lorsque l’état d’une table, voir va changer, [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) est appelée pour enregistrer toutes les données relatives à l’état avant la modification.</span><span class="sxs-lookup"><span data-stu-id="a2298-127">When the state of a categorized table is about to change, [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) is called to save all of the data pertaining to the state prior to the change.</span></span> 
    
2. <span data-ttu-id="a2298-128">Pour restaurer l’affichage de la table à son état enregistré, **SetCollapseState** est appelée.</span><span class="sxs-lookup"><span data-stu-id="a2298-128">To restore the view of the table to its saved state, **SetCollapseState** is called.</span></span> <span data-ttu-id="a2298-129">Les données enregistrées par **GetCollapseState** sont transmises à **SetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="a2298-129">The data saved by **GetCollapseState** is passed to **SetCollapseState**.</span></span> <span data-ttu-id="a2298-130">**SetCollapseState** est en mesure d’utiliser ces données pour restaurer l’état.</span><span class="sxs-lookup"><span data-stu-id="a2298-130">**SetCollapseState** is able to use that data to restore the state.</span></span> 
    
3. <span data-ttu-id="a2298-131">**SetCollapseState** retourne, sous la forme d’un paramètre de sortie, un signet qui identifie la même ligne que la clé d’instance passée comme entrée pour **GetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="a2298-131">**SetCollapseState** returns as an output parameter a bookmark that identifies the same row as the instance key passed as input to **GetCollapseState**.</span></span>
    
<span data-ttu-id="a2298-132">Pour plus d’informations sur les tables, voir, consultez [tri et catégorisation](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="a2298-132">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a2298-133">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="a2298-133">Notes to implementers</span></span>

<span data-ttu-id="a2298-134">Vous êtes responsable de vérifier que l’ordre de tri et les restrictions sont exactement les mêmes qu’elles étaient au moment de l’appel **GetCollapseState** .</span><span class="sxs-lookup"><span data-stu-id="a2298-134">You are responsible for verifying that the sort order and restrictions are exactly the same as they were at the time of the **GetCollapseState** call.</span></span> <span data-ttu-id="a2298-135">Si une modification a été apportée, **SetCollapseState** ne doit pas être appelée, car le résultat est imprévisible.</span><span class="sxs-lookup"><span data-stu-id="a2298-135">If a change has been made, **SetCollapseState** should not be called because the results can be unpredictable.</span></span> <span data-ttu-id="a2298-136">Cela peut se produire si, par exemple, un client appelle **GetCollapseState** , puis **SortTable** pour modifier la clé de tri avant d’appeler **SetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="a2298-136">This can happen if, for example, a client calls **GetCollapseState** and then **SortTable** to change the sort key before calling **SetCollapseState**.</span></span> <span data-ttu-id="a2298-137">Pour plus de sécurité, vérifiez que les données enregistrées sont toujours valides avant de procéder à la restauration.</span><span class="sxs-lookup"><span data-stu-id="a2298-137">To be safe, check that the saved data is still valid before proceeding with the restoration.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a2298-138">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="a2298-138">Notes to callers</span></span>

<span data-ttu-id="a2298-139">Pour appeler **SetCollapseState**, vous devez avez précédemment appelé **GetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="a2298-139">To call **SetCollapseState**, you must have previously called **GetCollapseState**.</span></span> <span data-ttu-id="a2298-140">L’ordre de tri établir les catégories doit être la même pour les deux méthodes.</span><span class="sxs-lookup"><span data-stu-id="a2298-140">The sort order establishing the categories should be the same for both methods.</span></span> <span data-ttu-id="a2298-141">Si les ordres de tri diffèrent, le résultat de l’opération **SetCollapseState** est imprévisible.</span><span class="sxs-lookup"><span data-stu-id="a2298-141">If the sort orders differ, the results of the **SetCollapseState** operation are unpredictable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a2298-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2298-142">See also</span></span>



[<span data-ttu-id="a2298-143">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="a2298-143">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="a2298-144">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="a2298-144">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="a2298-145">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="a2298-145">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="a2298-146">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a2298-146">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

