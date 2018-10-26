---
title: IMAPITableSortTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SortTable
api_type:
- COM
ms.assetid: ff5f78ac-06cf-46fb-93da-5f4a3a5d1b22
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: efeff92f1a21d076c1ee58b82ad3ab25797df014
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592303"
---
# <a name="imapitablesorttable"></a><span data-ttu-id="2de7d-103">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="2de7d-103">IMAPITable::SortTable</span></span>

<span data-ttu-id="2de7d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2de7d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2de7d-105">La méthode **IMAPITable::SortTable** trie les lignes du tableau, en fonction de tri critères.</span><span class="sxs-lookup"><span data-stu-id="2de7d-105">The **IMAPITable::SortTable** method orders the rows of the table, depending on sort criteria.</span></span> 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="2de7d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2de7d-106">Parameters</span></span>

<span data-ttu-id="2de7d-107">_lpSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="2de7d-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="2de7d-108">[in] Pointeur vers une structure [SSortOrderSet](ssortorderset.md) qui contient les critères de tri à appliquer.</span><span class="sxs-lookup"><span data-stu-id="2de7d-108">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the sort criteria to apply.</span></span> <span data-ttu-id="2de7d-109">Passage d’une structure **SSortOrderSet** qui contient zéro colonnes indique que le tableau n’a pas à trier selon un ordre particulier.</span><span class="sxs-lookup"><span data-stu-id="2de7d-109">Passing an **SSortOrderSet** structure that contains zero columns indicates that the table does not have to be sorted in any particular order.</span></span> 
    
<span data-ttu-id="2de7d-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2de7d-110">_ulFlags_</span></span>
  
> <span data-ttu-id="2de7d-111">[in] Masque de bits d’indicateurs qui contrôle le minutage de l’opération **IMAPITable::SortTable** .</span><span class="sxs-lookup"><span data-stu-id="2de7d-111">[in] Bitmask of flags that controls the timing of the **IMAPITable::SortTable** operation.</span></span> <span data-ttu-id="2de7d-112">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="2de7d-112">The following flags can be set:</span></span> 
    
<span data-ttu-id="2de7d-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="2de7d-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="2de7d-114">Démarre l’opération asynchrone et renvoie avant que l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="2de7d-114">Starts the operation asynchronously and returns before the operation is complete.</span></span>
    
<span data-ttu-id="2de7d-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="2de7d-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="2de7d-116">Diffère de la fin de l’ordre de tri jusqu'à ce que les données dans le tableau sont requises.</span><span class="sxs-lookup"><span data-stu-id="2de7d-116">Defers the completion of the sort until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2de7d-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2de7d-117">Return value</span></span>

<span data-ttu-id="2de7d-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="2de7d-118">S_OK</span></span> 
  
> <span data-ttu-id="2de7d-119">L’opération de tri a réussi.</span><span class="sxs-lookup"><span data-stu-id="2de7d-119">The sort operation was successful.</span></span>
    
<span data-ttu-id="2de7d-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="2de7d-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="2de7d-121">Une autre opération est en cours qui empêche l’opération de tri de démarrage.</span><span class="sxs-lookup"><span data-stu-id="2de7d-121">Another operation is in progress that prevents the sort operation from starting.</span></span> <span data-ttu-id="2de7d-122">L’opération en cours doit être autorisée à effectuer ou il doit être arrêté.</span><span class="sxs-lookup"><span data-stu-id="2de7d-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="2de7d-123">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="2de7d-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="2de7d-124">Le tableau ne gère pas le type de tri demandé.</span><span class="sxs-lookup"><span data-stu-id="2de7d-124">The table does not support the type of sorting requested.</span></span>
    
<span data-ttu-id="2de7d-125">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="2de7d-125">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="2de7d-126">Le tableau ne peut pas effectuer l’opération car les critères de tri particulier vers laquelle pointe le paramètre _lpSortCriteria_ est trop complexe.</span><span class="sxs-lookup"><span data-stu-id="2de7d-126">The table cannot perform the operation because the particular sort criteria pointed to by the  _lpSortCriteria_ parameter is too complex.</span></span> <span data-ttu-id="2de7d-127">**SortTable** peut renvoyer MAPI_E_TOO_COMPLEX dans les conditions suivantes.</span><span class="sxs-lookup"><span data-stu-id="2de7d-127">**SortTable** can return MAPI_E_TOO_COMPLEX under the following conditions.</span></span> 
    
   - <span data-ttu-id="2de7d-128">Une opération de tri est demandée pour une colonne de propriété que l’implémentation ne peut pas trier.</span><span class="sxs-lookup"><span data-stu-id="2de7d-128">A sort operation is requested for a property column that the implementation cannot sort.</span></span>
    
   - <span data-ttu-id="2de7d-129">L’implémentation ne gère pas l’ordre de tri demandée dans le membre **ulOrder** de la structure **SSortOrderSet** .</span><span class="sxs-lookup"><span data-stu-id="2de7d-129">The implementation does not support the sort order requested in the **ulOrder** member of the **SSortOrderSet** structure.</span></span> 
    
   - <span data-ttu-id="2de7d-130">Le nombre de colonnes à trier, tel que spécifié dans le membre **cSorts** dans **SSortOrderSet**, est plus importante que l’implémentation peut gérer.</span><span class="sxs-lookup"><span data-stu-id="2de7d-130">The number of columns to be sorted, as specified in the **cSorts** member in **SSortOrderSet**, is larger than the implementation can handle.</span></span>
    
   - <span data-ttu-id="2de7d-131">Une opération de tri est demandée, comme indiqué par une balise de propriété **SSortOrderSet**, basée sur une propriété qui n’est pas dans l’ensemble actif ou disponible et l’implémentation ne gère pas le tri sur les propriétés pas dans l’ensemble disponible.</span><span class="sxs-lookup"><span data-stu-id="2de7d-131">A sort operation is requested, as indicated by a property tag in **SSortOrderSet**, based on a property that is not in the available or active set and the implementation does not support sorting on properties not in the available set.</span></span>
    
   - <span data-ttu-id="2de7d-132">Une propriété est spécifiée plusieurs fois dans un jeu d’ordre de tri, comme indiqué par plusieurs instances de la même balise de propriété, et l’implémentation ne peut pas effectuer une opération de tri de ce type.</span><span class="sxs-lookup"><span data-stu-id="2de7d-132">One property is specified multiple times in a sort order set, as indicated by multiple instances of the same property tag, and the implementation cannot perform such a sort operation.</span></span>
    
   - <span data-ttu-id="2de7d-133">Une opération de tri basée sur les colonnes de la propriété à valeurs multiples est demandée à l’aide de MVI_FLAG et l’implémentation ne gère pas le tri sur les propriétés à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="2de7d-133">A sort operation based on multivalued property columns is requested using MVI_FLAG and the implementation does not support sorting on multivalued properties.</span></span> 
    
   - <span data-ttu-id="2de7d-134">Une balise de propriété pour une propriété dans **SSortOrderSet** spécifie une propriété ou un type de l’implémentation ne prenant pas en charge.</span><span class="sxs-lookup"><span data-stu-id="2de7d-134">A property tag for a property in **SSortOrderSet** specifies a property or type that the implementation does not support.</span></span> 
    
   - <span data-ttu-id="2de7d-135">Une opération de tri autre que celui qui s’effectue par le biais de la table à partir de la propriété **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) transférer est spécifiée uniquement pour une table de pièce jointe qui prend en charge ce type de tri.</span><span class="sxs-lookup"><span data-stu-id="2de7d-135">A sort operation other than one that proceeds through the table from the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property forward is specified only for an attachment table that supports this type of sorting.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2de7d-136">Remarques</span><span class="sxs-lookup"><span data-stu-id="2de7d-136">Remarks</span></span>

<span data-ttu-id="2de7d-137">La méthode **IMAPITable::SortTable** trie les lignes dans un affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="2de7d-137">The **IMAPITable::SortTable** method orders the rows in a table view.</span></span> <span data-ttu-id="2de7d-138">Tandis que certaines tables prend en charge le tri sur plusieurs colonnes de clé de tri standard et par catégorie, les autres tables sont plus limitées dans leur prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2de7d-138">Whereas some tables support both standard and categorized sorting on various sort key columns, other tables are more limited in their support.</span></span> <span data-ttu-id="2de7d-139">Fournisseurs de carnet d’adresses, ne prennent pas charge tri des tableaux.</span><span class="sxs-lookup"><span data-stu-id="2de7d-139">Address book providers ordinarily do not support table sorting.</span></span> <span data-ttu-id="2de7d-140">Fournisseurs de banque de messages prennent généralement en charge le tri dans la mesure où ils conservent l’ordre de tri des dossiers qui se produit lorsqu’une table complète (il s’agit d’une table sans restriction) est triée.</span><span class="sxs-lookup"><span data-stu-id="2de7d-140">Message store providers usually support sorting to the extent that they keep the sort order of folders that results when a full table (a table without restrictions) is sorted.</span></span> 
  
<span data-ttu-id="2de7d-141">Certaines tables autorisent le tri est effectué sur n’importe quelle colonne du tableau.</span><span class="sxs-lookup"><span data-stu-id="2de7d-141">Some tables allow sorting to be done on any table column.</span></span> <span data-ttu-id="2de7d-142">Autres tables mais pas ; colonnes non inclus dans l’affichage tableau ne sont pas affectés par un appel **SortTable** .</span><span class="sxs-lookup"><span data-stu-id="2de7d-142">Other tables do not; columns not included in the table view are unaffected by a **SortTable** call.</span></span> <span data-ttu-id="2de7d-143">Certaines tables nécessitent que les clés de tri générés uniquement avec les colonnes dans le jeu de colonne en cours.</span><span class="sxs-lookup"><span data-stu-id="2de7d-143">Some tables require that sort keys be built only with columns in the table's current column set.</span></span> 
  
<span data-ttu-id="2de7d-144">Un tableau peut retourner MAPI_E_NO_SUPPORT ou MAPI_E_TOO_COMPLEX à partir de **SortTable** lorsqu’il ne peut pas effectuer une opération de tri.</span><span class="sxs-lookup"><span data-stu-id="2de7d-144">A table can return either MAPI_E_NO_SUPPORT or MAPI_E_TOO_COMPLEX from **SortTable** when it cannot complete a sort operation.</span></span> <span data-ttu-id="2de7d-145">En outre, les fournisseurs de magasins ne sont pas nécessairement de respecter l’ordre de tri spécifié pour les tables de hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="2de7d-145">Moreover, store providers are not guaranteed to honor the sort order set specified for hierarchy tables.</span></span> 
  
<span data-ttu-id="2de7d-146">Lorsqu’il n’y a aucune colonne dans la structure [SSortOrderSet](ssortorderset.md) désignée par le paramètre _lpSortCriteria_ , la table renvoie l’ensemble actuel de la colonne.</span><span class="sxs-lookup"><span data-stu-id="2de7d-146">When there are zero columns in the [SSortOrderSet](ssortorderset.md) structure pointed to by the  _lpSortCriteria_ parameter, the table returns the current column set.</span></span> <span data-ttu-id="2de7d-147">L’ordre de tri actuel peut être récupéré en appelant la méthode [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) de la table.</span><span class="sxs-lookup"><span data-stu-id="2de7d-147">The current sort order can be retrieved by calling the table's [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="2de7d-148">Tous les signets pour une table sont invalidés et doivent être supprimés lorsqu’un appel à **SortTable** est effectué et le signet BOOKMARK_CURRENT qui indique l’emplacement du curseur, doit être défini au début de la table.</span><span class="sxs-lookup"><span data-stu-id="2de7d-148">All bookmarks for a table are invalidated and should be deleted when a call to **SortTable** is made, and the BOOKMARK_CURRENT bookmark that indicates the current cursor position, should be set to the beginning of the table.</span></span> 
  
<span data-ttu-id="2de7d-149">Si vous triez sur une colonne qui contient une propriété à valeurs multiples sans l’indicateur MVI_FLAG est défini, les valeurs de la colonne sont considérés comme un tuple complètement triée.</span><span class="sxs-lookup"><span data-stu-id="2de7d-149">If you are sorting on a column that contains a multivalued property without the MVI_FLAG flag set, the column's values are treated as a completely ordered tuple.</span></span> <span data-ttu-id="2de7d-150">Une comparaison de deux colonnes à valeurs multiples compare les éléments de la colonne dans l’ordre, la relation entre les colonnes de la première inégalité, de création de rapports et renvoie l’égalité uniquement si les colonnes comparées contiennent les mêmes valeurs dans le même ordre.</span><span class="sxs-lookup"><span data-stu-id="2de7d-150">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality, and returns equality only if the columns being compared contain the same values in the same order.</span></span> <span data-ttu-id="2de7d-151">Si une colonne a moins de valeurs à l’autre, la relation signalée est celui d’une valeur null à l’autre valeur.</span><span class="sxs-lookup"><span data-stu-id="2de7d-151">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="2de7d-152">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="2de7d-152">Notes to callers</span></span>

<span data-ttu-id="2de7d-153">**SortTable** fonctionne de manière synchrone, sauf si vous définissez un des indicateurs.</span><span class="sxs-lookup"><span data-stu-id="2de7d-153">**SortTable** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="2de7d-154">Si vous définissez l’indicateur TBL_BATCH, **SortTable** diffère de l’opération de tri, sauf si vous demandez les données.</span><span class="sxs-lookup"><span data-stu-id="2de7d-154">If you set the TBL_BATCH flag, **SortTable** postpones the sort operation unless you request the data.</span></span> <span data-ttu-id="2de7d-155">Si l’indicateur TBL_ASYNC est défini, **SortTable** fonctionne de manière asynchrone, potentiellement renvoi avant la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="2de7d-155">If the TBL_ASYNC flag is set, **SortTable** operates asynchronously, potentially returning before the completion of the operation.</span></span> 
  
<span data-ttu-id="2de7d-156">Appelez la méthode [IMAPITable::Abort](imapitable-abort.md) pour arrêter une opération asynchrone en cours si le tri doit être effectué immédiatement.</span><span class="sxs-lookup"><span data-stu-id="2de7d-156">Call the [IMAPITable::Abort](imapitable-abort.md) method to stop an asynchronous operation in progress if your sort must be done immediately.</span></span> <span data-ttu-id="2de7d-157">Si **SortTable** ne peut pas continuer car un ou plusieurs des opérations asynchrones dans le tableau sont en cours, elle renvoie MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="2de7d-157">If **SortTable** cannot continue because one or more asynchronous operations on the table are in progress, it returns MAPI_E_BUSY.</span></span> 
  
<span data-ttu-id="2de7d-158">Pour optimiser les performances, appelez **SetColumns** pour personnaliser l’ensemble de colonnes de la table et **Restrict** pour limiter le nombre de lignes dans le tableau avant d’appeler **SortTable** pour effectuer le tri.</span><span class="sxs-lookup"><span data-stu-id="2de7d-158">For best performance, call **SetColumns** to customize the table's column set and **Restrict** to limit the number of rows in the table before you call **SortTable** to perform the sort.</span></span> 
  
<span data-ttu-id="2de7d-159">Chaque fois que **SortTable** échoue, l’ordre de tri qui était en vigueur avant la défaillance est toujours en vigueur.</span><span class="sxs-lookup"><span data-stu-id="2de7d-159">Whenever **SortTable** fails, the sort order that was in effect before the failure is still in effect.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2de7d-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2de7d-160">See also</span></span>

- [<span data-ttu-id="2de7d-161">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="2de7d-161">IMAPITable::Abort</span></span>](imapitable-abort.md)
- [<span data-ttu-id="2de7d-162">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="2de7d-162">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
- [<span data-ttu-id="2de7d-163">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="2de7d-163">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
- [<span data-ttu-id="2de7d-164">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="2de7d-164">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
- [<span data-ttu-id="2de7d-165">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="2de7d-165">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
- [<span data-ttu-id="2de7d-166">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="2de7d-166">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="2de7d-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2de7d-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

