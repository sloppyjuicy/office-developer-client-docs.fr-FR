---
title: IMAPITableExpandRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.ExpandRow
api_type:
- COM
ms.assetid: b96dd8f6-e648-4014-8a1d-ae1da771c439
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1b3d8c74d85696e733b378a4cac2b8e2a3b6a072
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784069"
---
# <a name="imapitableexpandrow"></a><span data-ttu-id="246e6-103">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="246e6-103">IMAPITable::ExpandRow</span></span>

  
  
<span data-ttu-id="246e6-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="246e6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="246e6-105">Développe une catégorie de table réduite, ajout de la feuille ou des lignes d’en-tête de niveau inférieur appartenant à la catégorie à l’affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="246e6-105">Expands a collapsed table category, adding the leaf or lower-level heading rows belonging to the category to the table view.</span></span>
  
```cpp
HRESULT ExpandRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows,
ULONG FAR * lpulMoreRows
);
```

## <a name="parameters"></a><span data-ttu-id="246e6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="246e6-106">Parameters</span></span>

 <span data-ttu-id="246e6-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="246e6-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="246e6-108">[in] Le nombre d’octets dans la propriété PR_INSTANCE_KEY indiqué par le paramètre _pbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="246e6-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="246e6-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="246e6-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="246e6-110">[in] Pointeur vers la propriété **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) qui identifie la ligne d’en-tête de la catégorie.</span><span class="sxs-lookup"><span data-stu-id="246e6-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="246e6-111">_ulRowCount_</span><span class="sxs-lookup"><span data-stu-id="246e6-111">_ulRowCount_</span></span>
  
> <span data-ttu-id="246e6-112">[in] Le nombre maximal de lignes à renvoyer dans le paramètre _lppRows_ .</span><span class="sxs-lookup"><span data-stu-id="246e6-112">[in] The maximum number of rows to return in the  _lppRows_ parameter.</span></span> 
    
 <span data-ttu-id="246e6-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="246e6-113">_ulFlags_</span></span>
  
> <span data-ttu-id="246e6-114">Réservé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="246e6-114">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="246e6-115">_lppRows_</span><span class="sxs-lookup"><span data-stu-id="246e6-115">_lppRows_</span></span>
  
> <span data-ttu-id="246e6-116">[out] Pointeur vers une structure [SRowSet](srowset.md) recevoir des lignes qui ont été insérés dans la vue table à la suite de l’extension de la première (jusqu'à _ulRowCount_).</span><span class="sxs-lookup"><span data-stu-id="246e6-116">[out] A pointer to an [SRowSet](srowset.md) structure receiving the first (up to  _ulRowCount_) rows that have been inserted into the table view as a result of the expansion.</span></span> <span data-ttu-id="246e6-117">Ces lignes sont insérées après la ligne d’en-tête identifiée par le paramètre _pbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="246e6-117">These rows are inserted after the heading row identified by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="246e6-118">Le paramètre _lppRows_ peut être NULL si le paramètre _ulRowCount_ est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="246e6-118">The  _lppRows_ parameter can be NULL if the  _ulRowCount_ parameter is zero.</span></span> 
    
 <span data-ttu-id="246e6-119">_lpulMoreRows_</span><span class="sxs-lookup"><span data-stu-id="246e6-119">_lpulMoreRows_</span></span>
  
> <span data-ttu-id="246e6-120">[out] Pointeur vers le nombre total de lignes qui ont été ajoutés à l’affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="246e6-120">[out] A pointer to the total number of rows that were added to the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="246e6-121">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="246e6-121">Return value</span></span>

<span data-ttu-id="246e6-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="246e6-122">S_OK</span></span> 
  
> <span data-ttu-id="246e6-123">La catégorie a été développée avec succès.</span><span class="sxs-lookup"><span data-stu-id="246e6-123">The category was expanded successfully.</span></span>
    
<span data-ttu-id="246e6-124">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="246e6-124">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="246e6-125">La ligne identifiée par le paramètre _pbInstanceKey_ n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="246e6-125">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="246e6-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="246e6-126">Remarks</span></span>

<span data-ttu-id="246e6-127">La méthode **IMAPITable::ExpandRow** développe une catégorie de table réduite, ajout de la feuille ou les lignes d’en-tête de niveau inférieur qui appartiennent à la catégorie à l’affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="246e6-127">The **IMAPITable::ExpandRow** method expands a collapsed table category, adding the leaf or lower-level heading rows that belong to the category to the table view.</span></span> <span data-ttu-id="246e6-128">Limite le nombre de lignes à renvoyer dans le paramètre _lppRows_ peut être spécifiée dans le paramètre _ulRowCount_ .</span><span class="sxs-lookup"><span data-stu-id="246e6-128">A limit to the number of rows to be returned in the  _lppRows_ parameter can be specified in the  _ulRowCount_ parameter.</span></span> <span data-ttu-id="246e6-129">Lorsque _ulRowCount_ est défini sur une valeur supérieure à zéro, une ou plusieurs lignes sont retournées dans le jeu de lignes indiqué par _lppRows_la position du signet que bookmark_current est déplacé vers la ligne immédiatement après la dernière ligne de la ligne est définie.</span><span class="sxs-lookup"><span data-stu-id="246e6-129">When  _ulRowCount_ is set to a value greater than zero and one or more rows are returned in the row set pointed to by  _lppRows_, the position of the bookmark BOOKMARK_CURRENT is moved to the row immediately following the last row in the row set.</span></span>
  
<span data-ttu-id="246e6-130">Lorsque _ulRowCount_ est égale à zéro, demande qui zéro feuille ou lignes d’en-tête de niveau inférieur à ajouter à la catégorie ou zéro lignes sont retournées, car aucune feuille ou les lignes d’en-tête de niveau inférieur de la catégorie, la position de BOOKMARK_CURRENT est définie à la ligne la ligne identifié par _pbInstanceKey_.</span><span class="sxs-lookup"><span data-stu-id="246e6-130">When  _ulRowCount_ is set to zero, requesting that zero leaf or lower-level heading rows be added to the category, or zero rows are returned because there are no leaf or lower-level heading rows in the category, the position of BOOKMARK_CURRENT is set to the row following the row identified by  _pbInstanceKey_.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="246e6-131">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="246e6-131">Notes to implementers</span></span>

<span data-ttu-id="246e6-132">Ne génèrent pas de notifications sur les lignes qui sont ajoutés à un affichage de tableau en raison d’extension de catégorie.</span><span class="sxs-lookup"><span data-stu-id="246e6-132">Do not generate notifications on rows that are added to a table view due to category expansion.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="246e6-133">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="246e6-133">Notes to callers</span></span>

<span data-ttu-id="246e6-134">Le nombre de lignes dans le jeu de lignes indiqué par le paramètre _lppRows_ ne peut pas égal au nombre de lignes qui ont été ajoutés à la table, l’ensemble de la définir de feuille ou de lignes pour la catégorie d’en-tête de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="246e6-134">The number of rows in the row set pointed to by the  _lppRows_ parameter might not equal the number of rows that were actually added to the table, the entire set of leaf or lower-level heading rows for the category.</span></span> <span data-ttu-id="246e6-135">Erreurs peuvent se produire, telles que la mémoire ou le nombre de lignes dans la catégorie dépassant le nombre spécifié dans le paramètre _ulRowCount_ .</span><span class="sxs-lookup"><span data-stu-id="246e6-135">Errors can occur, such as insufficient memory, or the number of rows in the category exceeding the number specified in  _ulRowCount_ parameter.</span></span> <span data-ttu-id="246e6-136">Dans les deux cas, BOOKMARK_CURRENT sera positionné à la dernière ligne renvoyée.</span><span class="sxs-lookup"><span data-stu-id="246e6-136">In either case, BOOKMARK_CURRENT will be positioned at the last row returned.</span></span> <span data-ttu-id="246e6-137">Pour récupérer immédiatement le reste des lignes de la catégorie, appelez [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="246e6-137">To immediately retrieve the rest of the rows in the category, call [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
  
<span data-ttu-id="246e6-138">Ne prévoyez pas de recevoir une notification de table lorsqu’une catégorie modifie son état.</span><span class="sxs-lookup"><span data-stu-id="246e6-138">Do not expect to receive a table notification when a category changes its state.</span></span> <span data-ttu-id="246e6-139">Vous pouvez conserver un cache local des lignes qui peuvent être mises à jour à chaque appel **ExpandRow** ou **CollapseRow** .</span><span class="sxs-lookup"><span data-stu-id="246e6-139">You can maintain a local cache of rows that can be updated with every **ExpandRow** or **CollapseRow** call.</span></span> 
  
<span data-ttu-id="246e6-140">Pour plus d’informations sur les tables, voir, consultez [tri et catégorisation](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="246e6-140">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="246e6-141">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="246e6-141">MFCMAPI reference</span></span>

<span data-ttu-id="246e6-142">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="246e6-142">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="246e6-143">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="246e6-143">**File**</span></span>|<span data-ttu-id="246e6-144">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="246e6-144">**Function**</span></span>|<span data-ttu-id="246e6-145">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="246e6-145">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="246e6-146">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="246e6-146">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="246e6-147">CContentsTableListCtrl::DoExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="246e6-147">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="246e6-148">MFCMAPI utilise la méthode **IMAPITable::ExpandRow** pour développer une catégorie de table réduite.</span><span class="sxs-lookup"><span data-stu-id="246e6-148">MFCMAPI uses the **IMAPITable::ExpandRow** method to expand a collapsed table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="246e6-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="246e6-149">See also</span></span>



[<span data-ttu-id="246e6-150">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="246e6-150">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
  
[<span data-ttu-id="246e6-151">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="246e6-151">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="246e6-152">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="246e6-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

