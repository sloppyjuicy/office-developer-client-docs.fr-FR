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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e6a180ceb325a705ebf226bb728c52cce7396490
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416173"
---
# <a name="imapitablecollapserow"></a><span data-ttu-id="ebc2e-103">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="ebc2e-103">IMAPITable::CollapseRow</span></span>

  
  
<span data-ttu-id="ebc2e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ebc2e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ebc2e-105">Réduit une catégorie de tableau étendu, en supprimant les en-tête de niveau inférieur et les lignes de feuille appartenant à la catégorie de l’affichage Tableau.</span><span class="sxs-lookup"><span data-stu-id="ebc2e-105">Collapses an expanded table category, removing any lower-level headings and leaf rows belonging to the category from the table view.</span></span>
  
```cpp
HRESULT CollapseRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulFlags,
ULONG FAR * lpulRowCount
);
```

## <a name="parameters"></a><span data-ttu-id="ebc2e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebc2e-106">Parameters</span></span>

 <span data-ttu-id="ebc2e-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="ebc2e-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="ebc2e-108">[in] Nombre d’octets dans la propriété PR_INSTANCE_KEY pointant vers le _paramètre pbInstanceKey._</span><span class="sxs-lookup"><span data-stu-id="ebc2e-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="ebc2e-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="ebc2e-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="ebc2e-110">[in] Pointeur vers la **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) qui identifie la ligne de titre de la catégorie.</span><span class="sxs-lookup"><span data-stu-id="ebc2e-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="ebc2e-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ebc2e-111">_ulFlags_</span></span>
  
> <span data-ttu-id="ebc2e-112">Réservé ; doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="ebc2e-112">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="ebc2e-113">_lpulRowCount_</span><span class="sxs-lookup"><span data-stu-id="ebc2e-113">_lpulRowCount_</span></span>
  
> <span data-ttu-id="ebc2e-114">[out] Pointeur vers le nombre total de lignes supprimées de l’affichage Tableau.</span><span class="sxs-lookup"><span data-stu-id="ebc2e-114">[out] A pointer to the total number of rows that are being removed from the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ebc2e-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ebc2e-115">Return value</span></span>

<span data-ttu-id="ebc2e-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="ebc2e-116">S_OK</span></span> 
  
> <span data-ttu-id="ebc2e-117">L’opération de réduire a réussi.</span><span class="sxs-lookup"><span data-stu-id="ebc2e-117">The collapse operation has succeeded.</span></span>
    
<span data-ttu-id="ebc2e-118">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ebc2e-118">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ebc2e-119">La ligne identifiée par le  _paramètre pbInstanceKey_ n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="ebc2e-119">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
<span data-ttu-id="ebc2e-120">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ebc2e-120">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="ebc2e-121">La ligne identifiée par le  _paramètre pbInstanceKey_ n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="ebc2e-121">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> <span data-ttu-id="ebc2e-122">Cette erreur est une alternative à la MAPI_E_NOT_FOUND ; les fournisseurs de services peuvent renvoyer l’un ou l’autre.</span><span class="sxs-lookup"><span data-stu-id="ebc2e-122">This error is an alternative to MAPI_E_NOT_FOUND; service providers can return either one.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ebc2e-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="ebc2e-123">Remarks</span></span>

<span data-ttu-id="ebc2e-124">La **méthode IMAPITable::CollapseRow** permet de réduire une catégorie de tableau et de la supprimer de l’affichage Tableau.</span><span class="sxs-lookup"><span data-stu-id="ebc2e-124">The **IMAPITable::CollapseRow** method collapses a table category and removes it from the table view.</span></span> <span data-ttu-id="ebc2e-125">Les lignes sont réduire à partir de la ligne identifiée par la **propriété PR_INSTANCE_KEY** pointée par le _paramètre pbInstanceKey._</span><span class="sxs-lookup"><span data-stu-id="ebc2e-125">The rows are collapsed starting at the row identified by the **PR_INSTANCE_KEY** property pointed to by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="ebc2e-126">Le nombre de lignes supprimées de l’affichage est renvoyé dans le contenu du _paramètre lpulRowCount._</span><span class="sxs-lookup"><span data-stu-id="ebc2e-126">The number of rows that are removed from the view is returned in the contents of the  _lpulRowCount_ parameter.</span></span> 
  
<span data-ttu-id="ebc2e-127">Les notifications ne sont jamais générées pour les lignes de tableau qui sont supprimées d’un affichage suite à une opération de réduire.</span><span class="sxs-lookup"><span data-stu-id="ebc2e-127">Notifications are never generated for table rows that are removed from a view as the result of a collapse operation.</span></span> 
  
<span data-ttu-id="ebc2e-128">Lorsqu’une ligne définie par un signet est en dehors de l’affichage, le signet est déplacé pour pointer vers la ligne visible suivante.</span><span class="sxs-lookup"><span data-stu-id="ebc2e-128">When a row that is defined by a bookmark is collapsed out of view, the bookmark is moved to point to the next visible row.</span></span> 
  
<span data-ttu-id="ebc2e-129">Pour plus d’informations sur les tableaux classés, voir [Tri et catégorisation.](sorting-and-categorization.md)</span><span class="sxs-lookup"><span data-stu-id="ebc2e-129">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ebc2e-130">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ebc2e-130">MFCMAPI reference</span></span>

<span data-ttu-id="ebc2e-131">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ebc2e-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ebc2e-132">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="ebc2e-132">**File**</span></span>|<span data-ttu-id="ebc2e-133">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="ebc2e-133">**Function**</span></span>|<span data-ttu-id="ebc2e-134">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="ebc2e-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ebc2e-135">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="ebc2e-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="ebc2e-136">CContentsTableListCtrl::D oExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="ebc2e-136">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="ebc2e-137">MFCMAPI utilise la **méthode IMAPITable::CollapseRow** pour réduire une catégorie de tableau.</span><span class="sxs-lookup"><span data-stu-id="ebc2e-137">MFCMAPI uses the **IMAPITable::CollapseRow** method to collapse a table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ebc2e-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebc2e-138">See also</span></span>



[<span data-ttu-id="ebc2e-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="ebc2e-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="ebc2e-140">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="ebc2e-140">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="ebc2e-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="ebc2e-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="ebc2e-142">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="ebc2e-142">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="ebc2e-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="ebc2e-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="ebc2e-144">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="ebc2e-144">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="ebc2e-145">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ebc2e-145">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="ebc2e-146">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="ebc2e-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

