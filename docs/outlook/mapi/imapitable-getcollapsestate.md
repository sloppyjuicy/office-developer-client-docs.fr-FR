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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 2c1246c46e9723cd3f6d92f0a44fc1419eef4a2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784075"
---
# <a name="imapitablegetcollapsestate"></a><span data-ttu-id="a2feb-103">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="a2feb-103">IMAPITable::GetCollapseState</span></span>

  
  
<span data-ttu-id="a2feb-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a2feb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a2feb-105">Retourne les données nécessaires à la recréation en cours réduit ou développé état d’une table, voir.</span><span class="sxs-lookup"><span data-stu-id="a2feb-105">Returns the data that is needed to rebuild the current collapsed or expanded state of a categorized table.</span></span>
  
```cpp
HRESULT GetCollapseState(
ULONG ulFlags,
ULONG cbInstanceKey,
LPBYTE lpbInstanceKey,
ULONG FAR * lpcbCollapseState,
LPBYTE FAR * lppbCollapseState
);
```

## <a name="parameters"></a><span data-ttu-id="a2feb-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="a2feb-106">Parameters</span></span>

 <span data-ttu-id="a2feb-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a2feb-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a2feb-108">Réservé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="a2feb-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="a2feb-109">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="a2feb-109">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="a2feb-110">[in] Le nombre d’octets dans la clé de l’instance indiqué par le paramètre _lpbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="a2feb-110">[in] The count of bytes in the instance key pointed to by the  _lpbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="a2feb-111">_lpbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="a2feb-111">_lpbInstanceKey_</span></span>
  
> <span data-ttu-id="a2feb-112">[in] Un pointeur vers la propriété **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) de la ligne à laquelle actuel réduit ou développé état doit être reconstruit.</span><span class="sxs-lookup"><span data-stu-id="a2feb-112">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property of the row at which the current collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="a2feb-113">Le paramètre _lpbInstanceKey_ ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="a2feb-113">The  _lpbInstanceKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="a2feb-114">_lpcbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="a2feb-114">_lpcbCollapseState_</span></span>
  
> <span data-ttu-id="a2feb-115">[out] Un pointeur vers le nombre de structures indiqué par le paramètre _lppbCollapseState_ .</span><span class="sxs-lookup"><span data-stu-id="a2feb-115">[out] A pointer to the count of structures pointed to by the  _lppbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="a2feb-116">_lppbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="a2feb-116">_lppbCollapseState_</span></span>
  
> <span data-ttu-id="a2feb-117">[out] Pointeur vers un pointeur vers les structures qui contiennent des données qui décrit l’affichage tableau actuel.</span><span class="sxs-lookup"><span data-stu-id="a2feb-117">[out] A pointer to a pointer to structures that contain data that describes the current table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a2feb-118">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="a2feb-118">Return value</span></span>

<span data-ttu-id="a2feb-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="a2feb-119">S_OK</span></span> 
  
> <span data-ttu-id="a2feb-120">L’état de la table par catégorie a été enregistré avec succès.</span><span class="sxs-lookup"><span data-stu-id="a2feb-120">The state for the categorized table was successfully saved.</span></span>
    
<span data-ttu-id="a2feb-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="a2feb-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="a2feb-122">Une autre opération est en cours qui empêche l’opération de démarrage.</span><span class="sxs-lookup"><span data-stu-id="a2feb-122">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="a2feb-123">L’opération en cours doit être autorisée à effectuer ou il doit être arrêté.</span><span class="sxs-lookup"><span data-stu-id="a2feb-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="a2feb-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="a2feb-124">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="a2feb-125">Le tableau ne gère pas la catégorisation et vues développée et réduite.</span><span class="sxs-lookup"><span data-stu-id="a2feb-125">The table does not support categorization and expanded and collapsed views.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a2feb-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="a2feb-126">Remarks</span></span>

<span data-ttu-id="a2feb-127">La méthode **IMAPITable::GetCollapseState** fonctionne avec la méthode [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) pour modifier l’affichage de l’utilisateur d’une table, voir.</span><span class="sxs-lookup"><span data-stu-id="a2feb-127">The **IMAPITable::GetCollapseState** method works with the [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) method to change the user's view of a categorized table.</span></span> <span data-ttu-id="a2feb-128">**GetCollapseState** enregistre les données nécessaires pour **SetCollapseState** à utiliser pour reconstruire les affichages des catégories d’une table, voir appropriés.</span><span class="sxs-lookup"><span data-stu-id="a2feb-128">**GetCollapseState** saves the data that is needed for **SetCollapseState** to use to rebuild the appropriate views of the categories of a categorized table.</span></span> <span data-ttu-id="a2feb-129">Fournisseurs de services de déterminent les données à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="a2feb-129">Service providers determine the data to be saved.</span></span> <span data-ttu-id="a2feb-130">Toutefois, la plupart des fournisseurs de services de mise en œuvre **GetCollapseState** enregistrement les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="a2feb-130">However, most service providers implementing **GetCollapseState** save the following:</span></span> 
  
- <span data-ttu-id="a2feb-131">Les clés de tri (colonnes standards et les colonnes de catégorie).</span><span class="sxs-lookup"><span data-stu-id="a2feb-131">The sort keys (standard columns and category columns).</span></span>
    
- <span data-ttu-id="a2feb-132">Plus d’informations sur la ligne qui représente la clé d’instance.</span><span class="sxs-lookup"><span data-stu-id="a2feb-132">Information about the row that the instance key represents.</span></span>
    
- <span data-ttu-id="a2feb-133">Informations pour restaurer les catégories de réduction et le développement de la table.</span><span class="sxs-lookup"><span data-stu-id="a2feb-133">Information to restore the collapsed and expanded categories of the table.</span></span>
    
<span data-ttu-id="a2feb-134">Pour plus d’informations sur les tables, voir, consultez [tri et catégorisation](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="a2feb-134">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a2feb-135">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="a2feb-135">Notes to implementers</span></span>

<span data-ttu-id="a2feb-136">Stocker l’état actuel de tous les nœuds d’un tableau dans le paramètre _lppbCollapseState_ .</span><span class="sxs-lookup"><span data-stu-id="a2feb-136">Store the current state of all nodes of a table in the  _lppbCollapseState_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a2feb-137">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="a2feb-137">Notes to callers</span></span>

<span data-ttu-id="a2feb-138">Toujours appeler **GetCollapseState** avant d’appeler **SetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="a2feb-138">Always call **GetCollapseState** before you call **SetCollapseState**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a2feb-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2feb-139">See also</span></span>



[<span data-ttu-id="a2feb-140">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="a2feb-140">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="a2feb-141">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a2feb-141">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

