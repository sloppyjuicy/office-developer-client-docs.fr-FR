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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5e2ce756baaefef7bd0028e746b1dbe10756365e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415165"
---
# <a name="imapitableexpandrow"></a><span data-ttu-id="ae369-103">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="ae369-103">IMAPITable::ExpandRow</span></span>

  
  
<span data-ttu-id="ae369-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae369-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae369-105">Développe une catégorie de table réduite, ajoutant la feuille ou les lignes de titre de niveau inférieur appartenant à la catégorie à l'affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="ae369-105">Expands a collapsed table category, adding the leaf or lower-level heading rows belonging to the category to the table view.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="ae369-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae369-106">Parameters</span></span>

 <span data-ttu-id="ae369-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="ae369-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="ae369-108">dans Nombre d'octets dans la propriété PR_INSTANCE_KEY vers laquelle pointe le paramètre _pbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="ae369-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="ae369-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="ae369-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="ae369-110">dans Pointeur vers la propriété **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) qui identifie la ligne d'en-tête pour la catégorie.</span><span class="sxs-lookup"><span data-stu-id="ae369-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="ae369-111">_ulRowCount_</span><span class="sxs-lookup"><span data-stu-id="ae369-111">_ulRowCount_</span></span>
  
> <span data-ttu-id="ae369-112">dans Nombre maximal de lignes à renvoyer dans le paramètre _lppRows_ .</span><span class="sxs-lookup"><span data-stu-id="ae369-112">[in] The maximum number of rows to return in the  _lppRows_ parameter.</span></span> 
    
 <span data-ttu-id="ae369-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ae369-113">_ulFlags_</span></span>
  
> <span data-ttu-id="ae369-114">MSR doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="ae369-114">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="ae369-115">_lppRows_</span><span class="sxs-lookup"><span data-stu-id="ae369-115">_lppRows_</span></span>
  
> <span data-ttu-id="ae369-116">remarquer Pointeur vers une structure [SRowSet](srowset.md) qui reçoit les premières lignes (jusqu'à _ulRowCount_) qui ont été insérées dans l'affichage de tableau à la suite de l'expansion.</span><span class="sxs-lookup"><span data-stu-id="ae369-116">[out] A pointer to an [SRowSet](srowset.md) structure receiving the first (up to  _ulRowCount_) rows that have been inserted into the table view as a result of the expansion.</span></span> <span data-ttu-id="ae369-117">Ces lignes sont insérées après la ligne d'en-tête identifiée par le paramètre _pbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="ae369-117">These rows are inserted after the heading row identified by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="ae369-118">Le paramètre _lppRows_ peut être null si le paramètre _ulRowCount_ est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="ae369-118">The  _lppRows_ parameter can be NULL if the  _ulRowCount_ parameter is zero.</span></span> 
    
 <span data-ttu-id="ae369-119">_lpulMoreRows_</span><span class="sxs-lookup"><span data-stu-id="ae369-119">_lpulMoreRows_</span></span>
  
> <span data-ttu-id="ae369-120">remarquer Pointeur vers le nombre total de lignes qui ont été ajoutées à l'affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="ae369-120">[out] A pointer to the total number of rows that were added to the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ae369-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ae369-121">Return value</span></span>

<span data-ttu-id="ae369-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae369-122">S_OK</span></span> 
  
> <span data-ttu-id="ae369-123">La catégorie a été développée.</span><span class="sxs-lookup"><span data-stu-id="ae369-123">The category was expanded successfully.</span></span>
    
<span data-ttu-id="ae369-124">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ae369-124">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ae369-125">La ligne identifiée par le paramètre _pbInstanceKey_ n'existe pas.</span><span class="sxs-lookup"><span data-stu-id="ae369-125">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ae369-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="ae369-126">Remarks</span></span>

<span data-ttu-id="ae369-127">La méthode **IMAPITable:: ExpandRow** développe une catégorie de table réduite, ajoutant la feuille ou les lignes de titre de niveau inférieur qui appartiennent à la catégorie à la vue de table.</span><span class="sxs-lookup"><span data-stu-id="ae369-127">The **IMAPITable::ExpandRow** method expands a collapsed table category, adding the leaf or lower-level heading rows that belong to the category to the table view.</span></span> <span data-ttu-id="ae369-128">Une limite au nombre de lignes à renvoyer dans le paramètre _lppRows_ peut être spécifiée dans le paramètre _ulRowCount_ .</span><span class="sxs-lookup"><span data-stu-id="ae369-128">A limit to the number of rows to be returned in the  _lppRows_ parameter can be specified in the  _ulRowCount_ parameter.</span></span> <span data-ttu-id="ae369-129">Lorsque _ulRowCount_ est défini sur une valeur supérieure à zéro et qu'une ou plusieurs lignes sont renvoyées dans l'ensemble de lignes désigné par _lppRows_, la position du signet BOOKMARK_CURRENT est déplacée vers la ligne qui suit immédiatement la dernière ligne du jeu de lignes.</span><span class="sxs-lookup"><span data-stu-id="ae369-129">When  _ulRowCount_ is set to a value greater than zero and one or more rows are returned in the row set pointed to by  _lppRows_, the position of the bookmark BOOKMARK_CURRENT is moved to the row immediately following the last row in the row set.</span></span>
  
<span data-ttu-id="ae369-130">Lorsque _ulRowCount_ est défini sur zéro, demander l'ajout de lignes de titre zéro ou de niveau inférieur à la catégorie, ou la renvoi de lignes null est possible, car il n'existe aucune ligne de titre de niveau inférieur ou de niveau inférieur dans la catégorie, la position de BOOKMARK_CURRENT est définie sur la ligne suivi de la ligne identifiée par _pbInstanceKey_.</span><span class="sxs-lookup"><span data-stu-id="ae369-130">When  _ulRowCount_ is set to zero, requesting that zero leaf or lower-level heading rows be added to the category, or zero rows are returned because there are no leaf or lower-level heading rows in the category, the position of BOOKMARK_CURRENT is set to the row following the row identified by  _pbInstanceKey_.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ae369-131">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="ae369-131">Notes to implementers</span></span>

<span data-ttu-id="ae369-132">Ne générez pas de notifications sur les lignes ajoutées à une vue de table en raison de l'expansion de catégorie.</span><span class="sxs-lookup"><span data-stu-id="ae369-132">Do not generate notifications on rows that are added to a table view due to category expansion.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="ae369-133">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="ae369-133">Notes to callers</span></span>

<span data-ttu-id="ae369-134">Le nombre de lignes dans l'ensemble de lignes désigné par le paramètre _lppRows_ ne peut pas être égal au nombre de lignes réellement ajoutées à la table, l'ensemble de lignes feuille ou de titre de niveau inférieur de la catégorie.</span><span class="sxs-lookup"><span data-stu-id="ae369-134">The number of rows in the row set pointed to by the  _lppRows_ parameter might not equal the number of rows that were actually added to the table, the entire set of leaf or lower-level heading rows for the category.</span></span> <span data-ttu-id="ae369-135">Des erreurs peuvent se produire, comme une mémoire insuffisante ou le nombre de lignes de la catégorie dépassant le nombre spécifié dans le paramètre _ulRowCount_ .</span><span class="sxs-lookup"><span data-stu-id="ae369-135">Errors can occur, such as insufficient memory, or the number of rows in the category exceeding the number specified in  _ulRowCount_ parameter.</span></span> <span data-ttu-id="ae369-136">Dans les deux cas, BOOKMARK_CURRENT est positionné sur la dernière ligne renvoyée.</span><span class="sxs-lookup"><span data-stu-id="ae369-136">In either case, BOOKMARK_CURRENT will be positioned at the last row returned.</span></span> <span data-ttu-id="ae369-137">Pour récupérer immédiatement les autres lignes de la catégorie, appelez [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="ae369-137">To immediately retrieve the rest of the rows in the category, call [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
  
<span data-ttu-id="ae369-138">Ne prévoyez pas de recevoir une notification de table lorsqu'une catégorie modifie son état.</span><span class="sxs-lookup"><span data-stu-id="ae369-138">Do not expect to receive a table notification when a category changes its state.</span></span> <span data-ttu-id="ae369-139">Vous pouvez gérer un cache local de lignes qui peuvent être mis à jour à chaque appel de **ExpandRow** ou de **CollapseRow** .</span><span class="sxs-lookup"><span data-stu-id="ae369-139">You can maintain a local cache of rows that can be updated with every **ExpandRow** or **CollapseRow** call.</span></span> 
  
<span data-ttu-id="ae369-140">Pour plus d'informations sur les tables classées, reportez-vous à la rubrique [Tri et catégorisation](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="ae369-140">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ae369-141">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ae369-141">MFCMAPI reference</span></span>

<span data-ttu-id="ae369-142">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ae369-142">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ae369-143">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="ae369-143">**File**</span></span>|<span data-ttu-id="ae369-144">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="ae369-144">**Function**</span></span>|<span data-ttu-id="ae369-145">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="ae369-145">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ae369-146">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="ae369-146">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="ae369-147">CContentsTableListCtrl::D oExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="ae369-147">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="ae369-148">MFCMAPI utilise la méthode **IMAPITable:: ExpandRow** pour développer une catégorie de table réduite.</span><span class="sxs-lookup"><span data-stu-id="ae369-148">MFCMAPI uses the **IMAPITable::ExpandRow** method to expand a collapsed table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ae369-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae369-149">See also</span></span>



[<span data-ttu-id="ae369-150">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="ae369-150">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
  
[<span data-ttu-id="ae369-151">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ae369-151">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="ae369-152">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="ae369-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

