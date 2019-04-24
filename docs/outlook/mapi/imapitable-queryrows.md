---
title: IMAPITableQueryRows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryRows
api_type:
- COM
ms.assetid: f26384f1-467e-4343-92b3-0425da9d2123
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 26d6ffe66a5e7749c9d8c4e5210e9f72de808932
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328868"
---
# <a name="imapitablequeryrows"></a><span data-ttu-id="55ed9-103">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="55ed9-103">IMAPITable::QueryRows</span></span>

  
  
<span data-ttu-id="55ed9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55ed9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55ed9-105">Renvoie une ou plusieurs lignes d'un tableau, en commençant à la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="55ed9-105">Returns one or more rows from a table, beginning at the current cursor position.</span></span>
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a><span data-ttu-id="55ed9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55ed9-106">Parameters</span></span>

 <span data-ttu-id="55ed9-107">_lRowCount_</span><span class="sxs-lookup"><span data-stu-id="55ed9-107">_lRowCount_</span></span>
  
> <span data-ttu-id="55ed9-108">dans Nombre maximal de lignes à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="55ed9-108">[in] Maximum number of rows to be returned.</span></span>
    
 <span data-ttu-id="55ed9-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="55ed9-109">_ulFlags_</span></span>
  
> <span data-ttu-id="55ed9-110">dans Masque de des indicateurs qui contrôlent la façon dont les lignes sont renvoyées.</span><span class="sxs-lookup"><span data-stu-id="55ed9-110">[in] Bitmask of flags that control how rows are returned.</span></span> <span data-ttu-id="55ed9-111">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="55ed9-111">The following flag can be set:</span></span>
    
<span data-ttu-id="55ed9-112">TBL_NOADVANCE</span><span class="sxs-lookup"><span data-stu-id="55ed9-112">TBL_NOADVANCE</span></span> 
  
> <span data-ttu-id="55ed9-113">Empêche le curseur de progresser à la suite de la récupération de la ligne.</span><span class="sxs-lookup"><span data-stu-id="55ed9-113">Prevents the cursor from advancing as a result of the row retrieval.</span></span> <span data-ttu-id="55ed9-114">Si l'indicateur TBL_NOADVANCE est défini, le curseur pointe vers la première ligne renvoyée.</span><span class="sxs-lookup"><span data-stu-id="55ed9-114">If the TBL_NOADVANCE flag is set, the cursor points to the first row returned.</span></span> <span data-ttu-id="55ed9-115">Si l'indicateur TBL_NOADVANCE n'est pas défini, le curseur pointe sur la ligne suivant la dernière ligne renvoyée.</span><span class="sxs-lookup"><span data-stu-id="55ed9-115">If the TBL_NOADVANCE flag is not set, the cursor points to the row following the last row returned.</span></span>
    
 <span data-ttu-id="55ed9-116">_lppRows_</span><span class="sxs-lookup"><span data-stu-id="55ed9-116">_lppRows_</span></span>
  
> <span data-ttu-id="55ed9-117">remarquer Pointeur vers un pointeur vers une structure [SRowSet](srowset.md) contenant les lignes de tableau.</span><span class="sxs-lookup"><span data-stu-id="55ed9-117">[out] Pointer to a pointer to an [SRowSet](srowset.md) structure holding the table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="55ed9-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="55ed9-118">Return value</span></span>

<span data-ttu-id="55ed9-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="55ed9-119">S_OK</span></span> 
  
> <span data-ttu-id="55ed9-120">Les lignes ont été renvoyées avec succès.</span><span class="sxs-lookup"><span data-stu-id="55ed9-120">The rows were successfully returned.</span></span>
    
<span data-ttu-id="55ed9-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="55ed9-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="55ed9-122">Une autre opération est en cours, ce qui empêche le démarrage de l'opération de récupération de ligne.</span><span class="sxs-lookup"><span data-stu-id="55ed9-122">Another operation is in progress that prevents the row retrieval operation from starting.</span></span> <span data-ttu-id="55ed9-123">L'opération en cours doit être autorisée ou elle doit être arrêtée.</span><span class="sxs-lookup"><span data-stu-id="55ed9-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="55ed9-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="55ed9-124">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="55ed9-125">Le paramètre _IRowCount_ est défini sur zéro.</span><span class="sxs-lookup"><span data-stu-id="55ed9-125">The  _IRowCount_ parameter is set to zero.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="55ed9-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="55ed9-126">Remarks</span></span>

<span data-ttu-id="55ed9-127">La méthode **IMAPITable:: QueryRows** obtient une ou plusieurs lignes de données d'une table.</span><span class="sxs-lookup"><span data-stu-id="55ed9-127">The **IMAPITable::QueryRows** method gets one or more rows of data from a table.</span></span> <span data-ttu-id="55ed9-128">La valeur du paramètre _IRowCount_ affecte le point de départ de la récupération.</span><span class="sxs-lookup"><span data-stu-id="55ed9-128">The value of the  _IRowCount_ parameter affects the starting point for the retrieval.</span></span> <span data-ttu-id="55ed9-129">Si _IRowCount_ est positif, les lignes sont lues dans une direction de transfert, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="55ed9-129">If  _IRowCount_ is positive, rows are read in a forward direction, starting at the current position.</span></span> <span data-ttu-id="55ed9-130">Si _IRowCount_ est négatif, **QueryRows** réinitialise le point de départ en dépassant le nombre indiqué de lignes.</span><span class="sxs-lookup"><span data-stu-id="55ed9-130">If  _IRowCount_ is negative, **QueryRows** resets the starting point by moving backward the indicated number of rows.</span></span> <span data-ttu-id="55ed9-131">Une fois le curseur réinitialisé, les lignes sont lues dans l'ordre de transfert.</span><span class="sxs-lookup"><span data-stu-id="55ed9-131">After the cursor is reset, rows are read in forward order.</span></span> 
  
<span data-ttu-id="55ed9-132">Le \*\*\*\* membre Crows dans la structure [SRowSet](srowset.md) vers laquelle pointe le paramètre _lppRows_ indique le nombre de lignes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="55ed9-132">The **cRows** member in the [SRowSet](srowset.md) structure pointed to by the  _lppRows_ parameter indicates the number of rows returned.</span></span> <span data-ttu-id="55ed9-133">Si aucune ligne n'est renvoyée:</span><span class="sxs-lookup"><span data-stu-id="55ed9-133">If zero rows are returned:</span></span> 
  
- <span data-ttu-id="55ed9-134">Le curseur était déjà positionné au début de la table et la valeur de _IRowCount_ est négative.</span><span class="sxs-lookup"><span data-stu-id="55ed9-134">The cursor was already positioned at the beginning of the table and the value of  _IRowCount_ is negative.</span></span> <span data-ttu-id="55ed9-135">Des</span><span class="sxs-lookup"><span data-stu-id="55ed9-135">-Or-</span></span> 
    
- <span data-ttu-id="55ed9-136">Le curseur a déjà été positionné à la fin de la table et la valeur de _IRowCount_ est positive.</span><span class="sxs-lookup"><span data-stu-id="55ed9-136">The cursor was already positioned at the end of the table and the value of  _IRowCount_ is positive.</span></span> 
    
<span data-ttu-id="55ed9-137">Le nombre de colonnes et leur ordre sont les mêmes pour chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="55ed9-137">The number of columns and their ordering is the same for each row.</span></span> <span data-ttu-id="55ed9-138">Si une propriété n'existe pas pour une ligne ou s'il y a une erreur lors de la lecture d'une propriété, la structure **SPropValue** de la propriété dans la ligne contient les valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="55ed9-138">If a property does not exist for a row or there is an error reading a property, the **SPropValue** structure for the property in the row contains the following values:</span></span> 
  
- <span data-ttu-id="55ed9-139">PT_ERROR pour le type de propriété dans le membre **ulPropTag** .</span><span class="sxs-lookup"><span data-stu-id="55ed9-139">PT_ERROR for the property type in the **ulPropTag** member.</span></span> 
    
- <span data-ttu-id="55ed9-140">MAPI_E_NOT_FOUND pour le membre de la **valeur** .</span><span class="sxs-lookup"><span data-stu-id="55ed9-140">MAPI_E_NOT_FOUND for the **Value** member.</span></span> 
    
<span data-ttu-id="55ed9-141">La mémoire utilisée pour les structures [SPropValue](spropvalue.md) dans l'ensemble de lignes pointé par le paramètre _lppRows_ doit être allouée et libérée séparément pour chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="55ed9-141">Memory used for the [SPropValue](spropvalue.md) structures in the row set pointed to by the  _lppRows_ parameter must be separately allocated and freed for each row.</span></span> <span data-ttu-id="55ed9-142">Utilisez [MAPIFreeBuffer](mapifreebuffer.md) pour libérer les structures de valeur de propriété et libérer le jeu de lignes.</span><span class="sxs-lookup"><span data-stu-id="55ed9-142">Use [MAPIFreeBuffer](mapifreebuffer.md) to free the property value structures and to free the row set.</span></span> <span data-ttu-id="55ed9-143">Quand un appel à **QueryRows** renvoie zéro, toutefois, en indiquant le début ou la fin de la table, seule la structure **SRowSet** elle-même doit être libérée.</span><span class="sxs-lookup"><span data-stu-id="55ed9-143">When a call to **QueryRows** returns zero, however, indicating the beginning or end of the table, only the **SRowSet** structure itself needs to be freed.</span></span> <span data-ttu-id="55ed9-144">Pour plus d'informations sur la façon d'allouer et de libérer de la mémoire dans une structure **SRowSet** , consultez la rubrique [Managing Memory for ADRLIST and SRowSet structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="55ed9-144">For more information about how to allocate and free memory in an **SRowSet** structure, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
<span data-ttu-id="55ed9-145">Les lignes renvoyées et l'ordre dans lequel elles sont renvoyées dépendent du fait que des appels ont été effectués ou non comme suit: [: Restrict](imapitable-restrict.md) et [IMAPITable:: SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="55ed9-145">The rows that are returned and the order in which they are returned depend on whether or not successful calls have been made to [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::SortTable](imapitable-sorttable.md).</span></span> <span data-ttu-id="55ed9-146">**Limiter** les lignes de filtrage à partir de l'affichage, entraînAnt la **QueryRows** à renvoyer uniquement les lignes correspondant aux critères spécifiés dans la restriction.</span><span class="sxs-lookup"><span data-stu-id="55ed9-146">**Restrict** filters rows from the view, causing **QueryRows** to return only the rows that match the criteria specified in the restriction.</span></span> <span data-ttu-id="55ed9-147">**SortTable** établit un ordre de tri standard ou par catégorie, affectant la séquence de lignes renvoyées par **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="55ed9-147">**SortTable** establishes a standard or categorized sort order, affecting the sequence of rows returned by **QueryRows**.</span></span> <span data-ttu-id="55ed9-148">Les lignes renvoyées sont dans l'ordre spécifié dans la structure [SSortOrderSet](ssortorderset.md) transmise à **SortTable**.</span><span class="sxs-lookup"><span data-stu-id="55ed9-148">The returned rows are in the order specified in the [SSortOrderSet](ssortorderset.md) structure passed to **SortTable**.</span></span>
  
<span data-ttu-id="55ed9-149">Les colonnes renvoyées pour chaque ligne et l'ordre dans lequel elles sont renvoyées dépendent du succès ou non de l'appel de la fonction [IMAPITable:: SetColumns](imapitable-setcolumns.md).</span><span class="sxs-lookup"><span data-stu-id="55ed9-149">The columns returned for each row and the order in which they are returned depend on whether or not a successful call has been made to [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> <span data-ttu-id="55ed9-150">**SetColumns** établit un jeu de colonnes, en spécifiant les propriétés à inclure dans les colonnes du tableau et l'ordre dans lequel elles doivent être incluses.</span><span class="sxs-lookup"><span data-stu-id="55ed9-150">**SetColumns** establishes a column set, specifying the properties to be included in columns in the table and the order in which they should be included.</span></span> <span data-ttu-id="55ed9-151">Si un appel **SetColumns** a été effectué, les colonnes spécifiques de chaque ligne et l'ordre de ces colonnes correspondent au jeu de colonnes spécifié dans l'appel.</span><span class="sxs-lookup"><span data-stu-id="55ed9-151">If a **SetColumns** call has been made, the particular columns in each row and the order of those columns match the column set specified in the call.</span></span> <span data-ttu-id="55ed9-152">Si aucun appel de **SetColumns** n'a été effectué, le tableau renvoie son jeu de colonnes par défaut.</span><span class="sxs-lookup"><span data-stu-id="55ed9-152">If no **SetColumns** call has been made, the table returns its default column set.</span></span> 
  
<span data-ttu-id="55ed9-153">Si aucun de ces appels n'a été effectué, **QueryRows** renvoie toutes les lignes du tableau.</span><span class="sxs-lookup"><span data-stu-id="55ed9-153">If none of these calls has been made, **QueryRows** returns all of the rows in the table.</span></span> <span data-ttu-id="55ed9-154">Chaque ligne contient la colonne par défaut définie dans l'ordre par défaut.</span><span class="sxs-lookup"><span data-stu-id="55ed9-154">Each row contains the default column set in default order.</span></span> 
  
<span data-ttu-id="55ed9-155">Lorsque le jeu de colonnes établi dans un appel de la PR_NULL: [SetColumns](imapitable-setcolumns.md) inclut des colonnes définies sur, le tableau [SPropValue](spropvalue.md) dans le jeu de lignes renvoyé dans _lppRows_ contiendra des slots vides.</span><span class="sxs-lookup"><span data-stu-id="55ed9-155">When the column set established in a call to [IMAPITable::SetColumns](imapitable-setcolumns.md) includes columns set to PR_NULL, the [SPropValue](spropvalue.md) array within the row set returned in  _lppRows_ will contain empty slots.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="55ed9-156">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="55ed9-156">Notes to implementers</span></span>

<span data-ttu-id="55ed9-157">Vous pouvez permettre à un appelant de demander qu'une colonne non prise en charge soit incluse dans le jeu de colonnes.</span><span class="sxs-lookup"><span data-stu-id="55ed9-157">You can allow a caller to request an unsupported column to be included in the column set.</span></span> <span data-ttu-id="55ed9-158">Lorsque cela se produit, placez PT_ERROR dans la partie type de propriété de la balise de propriété et MAPI_E_NOT_FOUND dans la valeur de propriété pour la colonne non prise en charge.</span><span class="sxs-lookup"><span data-stu-id="55ed9-158">When this occurs, place PT_ERROR in the property type portion of the property tag and MAPI_E_NOT_FOUND in the property value for the unsupported column.</span></span> 
  
<span data-ttu-id="55ed9-159">Traite le nombre de lignes comme une demande plutôt qu'une exigence.</span><span class="sxs-lookup"><span data-stu-id="55ed9-159">Treat the row count as a request rather than a requirement.</span></span> <span data-ttu-id="55ed9-160">Vous pouvez renvoyer n'importe quel emplacement à partir de zéro ligne, s'il n'y a aucune ligne dans le sens de la requête, vers le nombre demandé.</span><span class="sxs-lookup"><span data-stu-id="55ed9-160">You can return anywhere from zero rows, if there are no rows in the direction of the query, to the number requested.</span></span> 
  
<span data-ttu-id="55ed9-161">Renvoyer uniquement les lignes que l'utilisateur verra quand des lignes sont demandées à partir d'une vue de table classée, ce qui permet à l'appelant de formuler des hypothèses valides sur l'étendue des données et d'éviter tout travail supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="55ed9-161">Return only the rows that the user will see when rows are requested from a categorized table view, allowing the caller to make valid assumptions about the scope of the data and avoid extra work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="55ed9-162">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="55ed9-162">Notes to callers</span></span>

<span data-ttu-id="55ed9-163">En règle générale, vous vous retrouvez avec autant de lignes que vous avez spécifiées dans le paramètre _lRowCount_ .</span><span class="sxs-lookup"><span data-stu-id="55ed9-163">Usually you will end up with as many rows as you have specified in the  _lRowCount_ parameter.</span></span> <span data-ttu-id="55ed9-164">Toutefois, lorsque la mémoire ou les limites d'implémentation posent problème ou lorsque l'opération atteint le début ou la fin de la table de façon prématurée, **QueryRows** renvoie moins de lignes que le nombre demandé.</span><span class="sxs-lookup"><span data-stu-id="55ed9-164">However, when memory or implementation limits are an issue or when the operation reaches the beginning or end of the table prematurely, **QueryRows** will return less rows than requested.</span></span> 
  
<span data-ttu-id="55ed9-165">Si **QueryRows** renvoie MAPI_E_BUSY, appelez la méthode [IMAPITable:: WaitForCompletion](imapitable-waitforcompletion.md) et renouvelez l'appel à **QueryRows** une fois l'opération asynchrone terminée.</span><span class="sxs-lookup"><span data-stu-id="55ed9-165">If **QueryRows** returns MAPI_E_BUSY, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method and retry the call to **QueryRows** when the asynchronous operation is complete.</span></span> 
  
<span data-ttu-id="55ed9-166">Lors de l'appel de **QueryRows**, sachez que le temps de notifications asynchrones peut potentiellement provoquer l'ensemble de lignes que vous obtenez de **QueryRows** afin de ne pas représenter correctement les données sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="55ed9-166">When calling **QueryRows**, be aware that the timing of asynchronous notifications can potentially cause the row set that you get back from **QueryRows** not to accurately represent the underlying data.</span></span> <span data-ttu-id="55ed9-167">Par exemple, un appel à **QueryRows** à la table de contenu d'un dossier à la suite de la suppression d'un message, mais avant la réception de la notification correspondante, entraîne le renvoi de la ligne Deleted dans l'ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="55ed9-167">For example, a call to **QueryRows** to a folder's contents table following the deletion of a message but prior to the receipt of the corresponding notification will cause the deleted row to be returned in the row set.</span></span> <span data-ttu-id="55ed9-168">Attendez toujours qu'une notification arrive avant de mettre à jour la vue des données de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="55ed9-168">Always wait for a notification to arrive before updating the user's view of the data.</span></span> 
  
<span data-ttu-id="55ed9-169">Pour plus d'informations sur la récupération de lignes de tables, consultez la rubrique [extraction de données à partir de lignes de table](retrieving-data-from-table-rows.md).</span><span class="sxs-lookup"><span data-stu-id="55ed9-169">For more information about retrieving rows from tables, see [Retrieving Data from Table Rows](retrieving-data-from-table-rows.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="55ed9-170">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="55ed9-170">MFCMAPI reference</span></span>

<span data-ttu-id="55ed9-171">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="55ed9-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="55ed9-172">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="55ed9-172">**File**</span></span>|<span data-ttu-id="55ed9-173">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="55ed9-173">**Function**</span></span>|<span data-ttu-id="55ed9-174">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="55ed9-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="55ed9-175">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="55ed9-175">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="55ed9-176">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="55ed9-176">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="55ed9-177">MFCMAPI utilise la méthode **IMAPITable:: QueryRows** pour récupérer les lignes de la table à charger dans la vue.</span><span class="sxs-lookup"><span data-stu-id="55ed9-177">MFCMAPI uses the **IMAPITable::QueryRows** method to retrieve rows in the table to load into the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="55ed9-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55ed9-178">See also</span></span>



[<span data-ttu-id="55ed9-179">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="55ed9-179">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="55ed9-180">FreeProws</span><span class="sxs-lookup"><span data-stu-id="55ed9-180">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="55ed9-181">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="55ed9-181">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="55ed9-182">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="55ed9-182">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="55ed9-183">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="55ed9-183">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="55ed9-184">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="55ed9-184">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="55ed9-185">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="55ed9-185">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="55ed9-186">SRow</span><span class="sxs-lookup"><span data-stu-id="55ed9-186">SRow</span></span>](srow.md)
  
[<span data-ttu-id="55ed9-187">SRowSet</span><span class="sxs-lookup"><span data-stu-id="55ed9-187">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="55ed9-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="55ed9-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="55ed9-189">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="55ed9-189">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

