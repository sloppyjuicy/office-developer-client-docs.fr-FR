---
title: IMAPITableCollapseRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.CollapseRow
api_type:
- COM
ms.assetid: 1a23e555-be26-43fb-a715-cfc4ffa623cd
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b4dd7e9715c2d3c99eda44f7eed0b3360a2e33be
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595299"
---
# <a name="imapitablecollapserow"></a><span data-ttu-id="84e3f-103">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="84e3f-103">IMAPITable::CollapseRow</span></span>

  
  
<span data-ttu-id="84e3f-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84e3f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84e3f-105">Réduire une catégorie de table étendue, supprimant tous les titres de niveau inférieur et les lignes de feuilles appartenant à la catégorie à partir de l’affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="84e3f-105">Collapses an expanded table category, removing any lower-level headings and leaf rows belonging to the category from the table view.</span></span>
  
```cpp
HRESULT CollapseRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulFlags,
ULONG FAR * lpulRowCount
);
```

## <a name="parameters"></a><span data-ttu-id="84e3f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84e3f-106">Parameters</span></span>

 <span data-ttu-id="84e3f-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="84e3f-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="84e3f-108">[in] Le nombre d’octets dans la propriété PR_INSTANCE_KEY indiqué par le paramètre _pbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="84e3f-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="84e3f-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="84e3f-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="84e3f-110">[in] Pointeur vers la propriété **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) qui identifie la ligne d’en-tête de la catégorie.</span><span class="sxs-lookup"><span data-stu-id="84e3f-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="84e3f-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="84e3f-111">_ulFlags_</span></span>
  
> <span data-ttu-id="84e3f-112">Réservé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="84e3f-112">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="84e3f-113">_lpulRowCount_</span><span class="sxs-lookup"><span data-stu-id="84e3f-113">_lpulRowCount_</span></span>
  
> <span data-ttu-id="84e3f-114">[out] Pointeur vers le nombre total de lignes qui sont supprimés de l’affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="84e3f-114">[out] A pointer to the total number of rows that are being removed from the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="84e3f-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="84e3f-115">Return value</span></span>

<span data-ttu-id="84e3f-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="84e3f-116">S_OK</span></span> 
  
> <span data-ttu-id="84e3f-117">L’opération de réduction a réussi.</span><span class="sxs-lookup"><span data-stu-id="84e3f-117">The collapse operation has succeeded.</span></span>
    
<span data-ttu-id="84e3f-118">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="84e3f-118">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="84e3f-119">La ligne identifiée par le paramètre _pbInstanceKey_ n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="84e3f-119">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
<span data-ttu-id="84e3f-120">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="84e3f-120">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="84e3f-121">La ligne identifiée par le paramètre _pbInstanceKey_ n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="84e3f-121">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> <span data-ttu-id="84e3f-122">Cette erreur est une alternative à MAPI_E_NOT_FOUND ; fournisseurs de services peuvent renvoyer le d’eux.</span><span class="sxs-lookup"><span data-stu-id="84e3f-122">This error is an alternative to MAPI_E_NOT_FOUND; service providers can return either one.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="84e3f-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="84e3f-123">Remarks</span></span>

<span data-ttu-id="84e3f-124">La méthode **IMAPITable::CollapseRow** réduire une catégorie de table et le supprime de l’affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="84e3f-124">The **IMAPITable::CollapseRow** method collapses a table category and removes it from the table view.</span></span> <span data-ttu-id="84e3f-125">Les lignes sont réduits commençant à la ligne identifiée par la propriété **PR_INSTANCE_KEY** désignée par le paramètre _pbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="84e3f-125">The rows are collapsed starting at the row identified by the **PR_INSTANCE_KEY** property pointed to by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="84e3f-126">Le nombre de lignes qui sont supprimés de l’affichage est retourné dans le contenu du paramètre _lpulRowCount_ .</span><span class="sxs-lookup"><span data-stu-id="84e3f-126">The number of rows that are removed from the view is returned in the contents of the  _lpulRowCount_ parameter.</span></span> 
  
<span data-ttu-id="84e3f-127">Les notifications ne sont jamais générées pour les lignes de tableau qui sont supprimés d’un affichage à la suite d’une opération de réduction.</span><span class="sxs-lookup"><span data-stu-id="84e3f-127">Notifications are never generated for table rows that are removed from a view as the result of a collapse operation.</span></span> 
  
<span data-ttu-id="84e3f-128">Lorsqu’une ligne est définie par un signet est réduite en dehors de l’affichage, le signet est déplacé pour pointer vers la ligne visible suivante.</span><span class="sxs-lookup"><span data-stu-id="84e3f-128">When a row that is defined by a bookmark is collapsed out of view, the bookmark is moved to point to the next visible row.</span></span> 
  
<span data-ttu-id="84e3f-129">Pour plus d’informations sur les tables, voir, consultez [tri et catégorisation](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="84e3f-129">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="84e3f-130">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="84e3f-130">MFCMAPI reference</span></span>

<span data-ttu-id="84e3f-131">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="84e3f-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="84e3f-132">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="84e3f-132">**File**</span></span>|<span data-ttu-id="84e3f-133">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="84e3f-133">**Function**</span></span>|<span data-ttu-id="84e3f-134">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="84e3f-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="84e3f-135">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="84e3f-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="84e3f-136">CContentsTableListCtrl::DoExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="84e3f-136">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="84e3f-137">MFCMAPI utilise la méthode **IMAPITable::CollapseRow** pour réduire une catégorie de table.</span><span class="sxs-lookup"><span data-stu-id="84e3f-137">MFCMAPI uses the **IMAPITable::CollapseRow** method to collapse a table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="84e3f-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84e3f-138">See also</span></span>



[<span data-ttu-id="84e3f-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="84e3f-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="84e3f-140">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="84e3f-140">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="84e3f-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="84e3f-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="84e3f-142">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="84e3f-142">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="84e3f-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="84e3f-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="84e3f-144">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="84e3f-144">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="84e3f-145">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="84e3f-145">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="84e3f-146">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="84e3f-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

