---
title: IMAPITableGetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetCollapseState
api_type:
- COM
ms.assetid: fd4ea496-4c83-49cd-854e-f373cc1ed2af
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 97575a65cd6825e07d6f11c813beec539f99f53a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436075"
---
# <a name="imapitablegetcollapsestate"></a><span data-ttu-id="5695c-103">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="5695c-103">IMAPITable::GetCollapseState</span></span>

  
  
<span data-ttu-id="5695c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5695c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5695c-105">Renvoie les données nécessaires pour recréer l'État réduit ou développé actuel d'une table catégorisée.</span><span class="sxs-lookup"><span data-stu-id="5695c-105">Returns the data that is needed to rebuild the current collapsed or expanded state of a categorized table.</span></span>
  
```cpp
HRESULT GetCollapseState(
ULONG ulFlags,
ULONG cbInstanceKey,
LPBYTE lpbInstanceKey,
ULONG FAR * lpcbCollapseState,
LPBYTE FAR * lppbCollapseState
);
```

## <a name="parameters"></a><span data-ttu-id="5695c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5695c-106">Parameters</span></span>

 <span data-ttu-id="5695c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5695c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5695c-108">MSR doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="5695c-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="5695c-109">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="5695c-109">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="5695c-110">dans Nombre d'octets dans la clé d'instance vers laquelle pointe le paramètre _lpbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="5695c-110">[in] The count of bytes in the instance key pointed to by the  _lpbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="5695c-111">_lpbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="5695c-111">_lpbInstanceKey_</span></span>
  
> <span data-ttu-id="5695c-112">dans Pointeur vers la propriété **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) de la ligne à laquelle l'État réduit ou développé actuel doit être reconstruit.</span><span class="sxs-lookup"><span data-stu-id="5695c-112">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property of the row at which the current collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="5695c-113">Le paramètre _lpbInstanceKey_ ne peut pas être null.</span><span class="sxs-lookup"><span data-stu-id="5695c-113">The  _lpbInstanceKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="5695c-114">_lpcbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="5695c-114">_lpcbCollapseState_</span></span>
  
> <span data-ttu-id="5695c-115">remarquer Pointeur vers le nombre de structures vers lesquelles pointe le paramètre _lppbCollapseState_ .</span><span class="sxs-lookup"><span data-stu-id="5695c-115">[out] A pointer to the count of structures pointed to by the  _lppbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="5695c-116">_lppbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="5695c-116">_lppbCollapseState_</span></span>
  
> <span data-ttu-id="5695c-117">remarquer Pointeur vers un pointeur vers des structures qui contiennent des données qui décrivent la vue de tableau actuelle.</span><span class="sxs-lookup"><span data-stu-id="5695c-117">[out] A pointer to a pointer to structures that contain data that describes the current table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5695c-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5695c-118">Return value</span></span>

<span data-ttu-id="5695c-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="5695c-119">S_OK</span></span> 
  
> <span data-ttu-id="5695c-120">L'état de la table catégorisée a été enregistré avec succès.</span><span class="sxs-lookup"><span data-stu-id="5695c-120">The state for the categorized table was successfully saved.</span></span>
    
<span data-ttu-id="5695c-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="5695c-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="5695c-122">Une autre opération est en cours, ce qui empêche le démarrage de l'opération.</span><span class="sxs-lookup"><span data-stu-id="5695c-122">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="5695c-123">L'opération en cours doit être autorisée ou elle doit être arrêtée.</span><span class="sxs-lookup"><span data-stu-id="5695c-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="5695c-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="5695c-124">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="5695c-125">Le tableau ne prend pas en charge la catégorisation, ni les vues développées et réduites.</span><span class="sxs-lookup"><span data-stu-id="5695c-125">The table does not support categorization and expanded and collapsed views.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5695c-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="5695c-126">Remarks</span></span>

<span data-ttu-id="5695c-127">La méthode **IMAPITable:: GetCollapseState** fonctionne avec la méthode [IMAPITable:: SetCollapseState](imapitable-setcollapsestate.md) pour modifier l'affichage de l'utilisateur d'une table catégorisée.</span><span class="sxs-lookup"><span data-stu-id="5695c-127">The **IMAPITable::GetCollapseState** method works with the [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) method to change the user's view of a categorized table.</span></span> <span data-ttu-id="5695c-128">**GetCollapseState** enregistre les données nécessaires à **SetCollapseState** pour recréer les vues appropriées des catégories d'une table classée.</span><span class="sxs-lookup"><span data-stu-id="5695c-128">**GetCollapseState** saves the data that is needed for **SetCollapseState** to use to rebuild the appropriate views of the categories of a categorized table.</span></span> <span data-ttu-id="5695c-129">Les fournisseurs de services déterminent les données à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="5695c-129">Service providers determine the data to be saved.</span></span> <span data-ttu-id="5695c-130">Toutefois, la plupart des fournisseurs de services qui implémentent **GetCollapseState** enregistrent les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="5695c-130">However, most service providers implementing **GetCollapseState** save the following:</span></span> 
  
- <span data-ttu-id="5695c-131">Les clés de tri (colonnes standard et colonnes de catégorie).</span><span class="sxs-lookup"><span data-stu-id="5695c-131">The sort keys (standard columns and category columns).</span></span>
    
- <span data-ttu-id="5695c-132">Informations sur la ligne représentée par la clé d'instance.</span><span class="sxs-lookup"><span data-stu-id="5695c-132">Information about the row that the instance key represents.</span></span>
    
- <span data-ttu-id="5695c-133">Informations permettant de restaurer les catégories réduites et développées du tableau.</span><span class="sxs-lookup"><span data-stu-id="5695c-133">Information to restore the collapsed and expanded categories of the table.</span></span>
    
<span data-ttu-id="5695c-134">Pour plus d'informations sur les tables classées, reportez-vous à la rubrique [Tri et catégorisation](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="5695c-134">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5695c-135">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="5695c-135">Notes to implementers</span></span>

<span data-ttu-id="5695c-136">Stockez l'état actuel de tous les nœuds d'une table dans le paramètre _lppbCollapseState_ .</span><span class="sxs-lookup"><span data-stu-id="5695c-136">Store the current state of all nodes of a table in the  _lppbCollapseState_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5695c-137">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="5695c-137">Notes to callers</span></span>

<span data-ttu-id="5695c-138">Appelez toujours **GetCollapseState** avant d'appeler **SetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="5695c-138">Always call **GetCollapseState** before you call **SetCollapseState**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5695c-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5695c-139">See also</span></span>



[<span data-ttu-id="5695c-140">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="5695c-140">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="5695c-141">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5695c-141">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

