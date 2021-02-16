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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 26d6ffe66a5e7749c9d8c4e5210e9f72de808932
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416292"
---
# <a name="imapitablequeryrows"></a><span data-ttu-id="174da-103">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="174da-103">IMAPITable::QueryRows</span></span>

  
  
<span data-ttu-id="174da-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="174da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="174da-105">Renvoie une ou plusieurs lignes d’un tableau, en commençant à la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="174da-105">Returns one or more rows from a table, beginning at the current cursor position.</span></span>
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a><span data-ttu-id="174da-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="174da-106">Parameters</span></span>

 <span data-ttu-id="174da-107">_lRowCount_</span><span class="sxs-lookup"><span data-stu-id="174da-107">_lRowCount_</span></span>
  
> <span data-ttu-id="174da-108">[in] Nombre maximal de lignes à retourner.</span><span class="sxs-lookup"><span data-stu-id="174da-108">[in] Maximum number of rows to be returned.</span></span>
    
 <span data-ttu-id="174da-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="174da-109">_ulFlags_</span></span>
  
> <span data-ttu-id="174da-110">[in] Masque de bits d’indicateurs qui contrôlent la façon dont les lignes sont renvoyées.</span><span class="sxs-lookup"><span data-stu-id="174da-110">[in] Bitmask of flags that control how rows are returned.</span></span> <span data-ttu-id="174da-111">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="174da-111">The following flag can be set:</span></span>
    
<span data-ttu-id="174da-112">TBL_NOADVANCE</span><span class="sxs-lookup"><span data-stu-id="174da-112">TBL_NOADVANCE</span></span> 
  
> <span data-ttu-id="174da-113">Empêche le curseur d’avancer suite à la récupération de ligne.</span><span class="sxs-lookup"><span data-stu-id="174da-113">Prevents the cursor from advancing as a result of the row retrieval.</span></span> <span data-ttu-id="174da-114">Si l TBL_NOADVANCE est définie, le curseur pointe vers la première ligne renvoyée.</span><span class="sxs-lookup"><span data-stu-id="174da-114">If the TBL_NOADVANCE flag is set, the cursor points to the first row returned.</span></span> <span data-ttu-id="174da-115">Si l TBL_NOADVANCE n’est pas définie, le curseur pointe vers la ligne qui suit la dernière ligne renvoyée.</span><span class="sxs-lookup"><span data-stu-id="174da-115">If the TBL_NOADVANCE flag is not set, the cursor points to the row following the last row returned.</span></span>
    
 <span data-ttu-id="174da-116">_lppRows_</span><span class="sxs-lookup"><span data-stu-id="174da-116">_lppRows_</span></span>
  
> <span data-ttu-id="174da-117">[out] Pointeur vers un pointeur vers une structure [SRowSet](srowset.md) qui détient les lignes du tableau.</span><span class="sxs-lookup"><span data-stu-id="174da-117">[out] Pointer to a pointer to an [SRowSet](srowset.md) structure holding the table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="174da-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="174da-118">Return value</span></span>

<span data-ttu-id="174da-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="174da-119">S_OK</span></span> 
  
> <span data-ttu-id="174da-120">Les lignes ont été renvoyées avec succès.</span><span class="sxs-lookup"><span data-stu-id="174da-120">The rows were successfully returned.</span></span>
    
<span data-ttu-id="174da-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="174da-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="174da-122">Une autre opération est en cours qui empêche le démarrage de l’opération de récupération de lignes.</span><span class="sxs-lookup"><span data-stu-id="174da-122">Another operation is in progress that prevents the row retrieval operation from starting.</span></span> <span data-ttu-id="174da-123">L’opération en cours doit être autorisée ou arrêtée.</span><span class="sxs-lookup"><span data-stu-id="174da-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="174da-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="174da-124">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="174da-125">Le  _paramètre IRowCount_ est définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="174da-125">The  _IRowCount_ parameter is set to zero.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="174da-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="174da-126">Remarks</span></span>

<span data-ttu-id="174da-127">La **méthode IMAPITable::QueryRows** obtient une ou plusieurs lignes de données d’une table.</span><span class="sxs-lookup"><span data-stu-id="174da-127">The **IMAPITable::QueryRows** method gets one or more rows of data from a table.</span></span> <span data-ttu-id="174da-128">La valeur du  _paramètre IRowCount_ affecte le point de départ de la récupération.</span><span class="sxs-lookup"><span data-stu-id="174da-128">The value of the  _IRowCount_ parameter affects the starting point for the retrieval.</span></span> <span data-ttu-id="174da-129">Si  _IRowCount est_ positif, les lignes sont lues dans une direction vers l’avant, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="174da-129">If  _IRowCount_ is positive, rows are read in a forward direction, starting at the current position.</span></span> <span data-ttu-id="174da-130">Si  _IRowCount est_ négatif, **QueryRows** réinitialise le point de départ en déplaçant le nombre de lignes indiqué vers l’arrière.</span><span class="sxs-lookup"><span data-stu-id="174da-130">If  _IRowCount_ is negative, **QueryRows** resets the starting point by moving backward the indicated number of rows.</span></span> <span data-ttu-id="174da-131">Une fois le curseur réinitialisé, les lignes sont lues dans l’ordre avant.</span><span class="sxs-lookup"><span data-stu-id="174da-131">After the cursor is reset, rows are read in forward order.</span></span> 
  
<span data-ttu-id="174da-132">Le **membre cRows** dans la structure [SRowSet](srowset.md) pointée par le paramètre  _lppRows_ indique le nombre de lignes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="174da-132">The **cRows** member in the [SRowSet](srowset.md) structure pointed to by the  _lppRows_ parameter indicates the number of rows returned.</span></span> <span data-ttu-id="174da-133">Si aucune ligne n’est renvoyée :</span><span class="sxs-lookup"><span data-stu-id="174da-133">If zero rows are returned:</span></span> 
  
- <span data-ttu-id="174da-134">Le curseur était déjà positionné au début du tableau et la valeur  _de IRowCount_ est négative.</span><span class="sxs-lookup"><span data-stu-id="174da-134">The cursor was already positioned at the beginning of the table and the value of  _IRowCount_ is negative.</span></span> <span data-ttu-id="174da-135">-Or-</span><span class="sxs-lookup"><span data-stu-id="174da-135">-Or-</span></span> 
    
- <span data-ttu-id="174da-136">Le curseur était déjà positionné à la fin du tableau et la valeur de  _IRowCount_ est positive.</span><span class="sxs-lookup"><span data-stu-id="174da-136">The cursor was already positioned at the end of the table and the value of  _IRowCount_ is positive.</span></span> 
    
<span data-ttu-id="174da-137">Le nombre de colonnes et leur ordre sont les mêmes pour chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="174da-137">The number of columns and their ordering is the same for each row.</span></span> <span data-ttu-id="174da-138">Si une propriété n’existe pas pour une ligne ou s’il existe une erreur lors de la lecture d’une propriété, la structure **SPropValue** de la propriété de la ligne contient les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="174da-138">If a property does not exist for a row or there is an error reading a property, the **SPropValue** structure for the property in the row contains the following values:</span></span> 
  
- <span data-ttu-id="174da-139">PT_ERROR pour le type de propriété dans le **membre ulPropTag.**</span><span class="sxs-lookup"><span data-stu-id="174da-139">PT_ERROR for the property type in the **ulPropTag** member.</span></span> 
    
- <span data-ttu-id="174da-140">MAPI_E_NOT_FOUND pour le **membre** Valeur.</span><span class="sxs-lookup"><span data-stu-id="174da-140">MAPI_E_NOT_FOUND for the **Value** member.</span></span> 
    
<span data-ttu-id="174da-141">La mémoire utilisée pour les structures [SPropValue](spropvalue.md) dans le jeu de lignes pointé par le paramètre  _lppRows_ doit être allouée séparément et libérée pour chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="174da-141">Memory used for the [SPropValue](spropvalue.md) structures in the row set pointed to by the  _lppRows_ parameter must be separately allocated and freed for each row.</span></span> <span data-ttu-id="174da-142">Utilisez [MAPIFreeBuffer pour](mapifreebuffer.md) libérer les structures de valeurs de propriété et pour libérer le jeu de lignes.</span><span class="sxs-lookup"><span data-stu-id="174da-142">Use [MAPIFreeBuffer](mapifreebuffer.md) to free the property value structures and to free the row set.</span></span> <span data-ttu-id="174da-143">Toutefois, lorsqu’un appel **à QueryRows** renvoie zéro, indiquant le début ou la fin de la table, seule la structure **SRowSet** elle-même doit être libérée.</span><span class="sxs-lookup"><span data-stu-id="174da-143">When a call to **QueryRows** returns zero, however, indicating the beginning or end of the table, only the **SRowSet** structure itself needs to be freed.</span></span> <span data-ttu-id="174da-144">Pour plus d’informations sur la façon d’allouer et de libérer de la mémoire dans une structure **SRowSet,** voir [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="174da-144">For more information about how to allocate and free memory in an **SRowSet** structure, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
<span data-ttu-id="174da-145">Les lignes renvoyées et l’ordre dans lequel elles sont renvoyées varient selon que des appels réussis ont été effectués ou non à [IMAPITable::Restrict](imapitable-restrict.md) et [IMAPITable::SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="174da-145">The rows that are returned and the order in which they are returned depend on whether or not successful calls have been made to [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::SortTable](imapitable-sorttable.md).</span></span> <span data-ttu-id="174da-146">**Limitez** les filtres des lignes de l’affichage, ce qui a pour effet **que QueryRows** ne retourne que les lignes qui correspondent aux critères spécifiés dans la restriction.</span><span class="sxs-lookup"><span data-stu-id="174da-146">**Restrict** filters rows from the view, causing **QueryRows** to return only the rows that match the criteria specified in the restriction.</span></span> <span data-ttu-id="174da-147">**SortTable** établit un ordre de tri standard ou catégorisé, affectant la séquence de lignes renvoyée par **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="174da-147">**SortTable** establishes a standard or categorized sort order, affecting the sequence of rows returned by **QueryRows**.</span></span> <span data-ttu-id="174da-148">Les lignes renvoyées sont dans l’ordre spécifié dans la structure [SSortOrderSet](ssortorderset.md) transmise **à SortTable**.</span><span class="sxs-lookup"><span data-stu-id="174da-148">The returned rows are in the order specified in the [SSortOrderSet](ssortorderset.md) structure passed to **SortTable**.</span></span>
  
<span data-ttu-id="174da-149">Les colonnes renvoyées pour chaque ligne et l’ordre dans lequel elles sont renvoyées varient selon qu’un appel réussi a été effectué ou non à [IMAPITable::SetColumns](imapitable-setcolumns.md).</span><span class="sxs-lookup"><span data-stu-id="174da-149">The columns returned for each row and the order in which they are returned depend on whether or not a successful call has been made to [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> <span data-ttu-id="174da-150">**SetColumns** établit un jeu de colonnes, en spécifiant les propriétés à inclure dans les colonnes du tableau et l’ordre dans lequel elles doivent être incluses.</span><span class="sxs-lookup"><span data-stu-id="174da-150">**SetColumns** establishes a column set, specifying the properties to be included in columns in the table and the order in which they should be included.</span></span> <span data-ttu-id="174da-151">Si un **appel SetColumns** a été effectué, les colonnes spécifiques de chaque ligne et l’ordre de ces colonnes correspondent à l’ensemble de colonnes spécifié dans l’appel.</span><span class="sxs-lookup"><span data-stu-id="174da-151">If a **SetColumns** call has been made, the particular columns in each row and the order of those columns match the column set specified in the call.</span></span> <span data-ttu-id="174da-152">Si aucun **appel SetColumns n’a** été effectué, la table renvoie son jeu de colonnes par défaut.</span><span class="sxs-lookup"><span data-stu-id="174da-152">If no **SetColumns** call has been made, the table returns its default column set.</span></span> 
  
<span data-ttu-id="174da-153">Si aucun de ces appels n’a été effectué, **QueryRows** renvoie toutes les lignes du tableau.</span><span class="sxs-lookup"><span data-stu-id="174da-153">If none of these calls has been made, **QueryRows** returns all of the rows in the table.</span></span> <span data-ttu-id="174da-154">Chaque ligne contient la colonne par défaut définie dans l’ordre par défaut.</span><span class="sxs-lookup"><span data-stu-id="174da-154">Each row contains the default column set in default order.</span></span> 
  
<span data-ttu-id="174da-155">Lorsque le jeu de colonnes établi dans un appel à [IMAPITable::SetColumns](imapitable-setcolumns.md) inclut des colonnes définies sur PR_NULL, le tableau [SPropValue](spropvalue.md) dans le jeu de lignes renvoyé dans  _lppRows_ contient des emplacements vides.</span><span class="sxs-lookup"><span data-stu-id="174da-155">When the column set established in a call to [IMAPITable::SetColumns](imapitable-setcolumns.md) includes columns set to PR_NULL, the [SPropValue](spropvalue.md) array within the row set returned in  _lppRows_ will contain empty slots.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="174da-156">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="174da-156">Notes to implementers</span></span>

<span data-ttu-id="174da-157">Vous pouvez autoriser un appelant à demander qu’une colonne non pris en compte soit incluse dans le jeu de colonnes.</span><span class="sxs-lookup"><span data-stu-id="174da-157">You can allow a caller to request an unsupported column to be included in the column set.</span></span> <span data-ttu-id="174da-158">Lorsque cela se produit, placez PT_ERROR dans la partie type de propriété de la balise de propriété et MAPI_E_NOT_FOUND dans la valeur de la propriété pour la colonne non pris en MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="174da-158">When this occurs, place PT_ERROR in the property type portion of the property tag and MAPI_E_NOT_FOUND in the property value for the unsupported column.</span></span> 
  
<span data-ttu-id="174da-159">Traite le nombre de lignes comme une demande plutôt qu’une exigence.</span><span class="sxs-lookup"><span data-stu-id="174da-159">Treat the row count as a request rather than a requirement.</span></span> <span data-ttu-id="174da-160">Vous pouvez revenir n’importe où de zéro ligne, s’il n’y a aucune ligne dans la direction de la requête, au numéro demandé.</span><span class="sxs-lookup"><span data-stu-id="174da-160">You can return anywhere from zero rows, if there are no rows in the direction of the query, to the number requested.</span></span> 
  
<span data-ttu-id="174da-161">Renvoyer uniquement les lignes que l’utilisateur verra lorsque des lignes sont demandées à partir d’une vue de table classée, ce qui permet à l’appelant d’effectuer des hypothèses valides sur l’étendue des données et d’éviter tout travail supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="174da-161">Return only the rows that the user will see when rows are requested from a categorized table view, allowing the caller to make valid assumptions about the scope of the data and avoid extra work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="174da-162">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="174da-162">Notes to callers</span></span>

<span data-ttu-id="174da-163">En règle générale, vous finirez par avoir autant de lignes que vous l’avez spécifié dans _le paramètre lRowCount._</span><span class="sxs-lookup"><span data-stu-id="174da-163">Usually you will end up with as many rows as you have specified in the  _lRowCount_ parameter.</span></span> <span data-ttu-id="174da-164">Toutefois, lorsque les limites de mémoire ou d’implémentation sont un problème ou lorsque l’opération atteint prématurément le début ou la fin de la table, **QueryRows** retourne moins de lignes que demandé.</span><span class="sxs-lookup"><span data-stu-id="174da-164">However, when memory or implementation limits are an issue or when the operation reaches the beginning or end of the table prematurely, **QueryRows** will return less rows than requested.</span></span> 
  
<span data-ttu-id="174da-165">Si **QueryRows** renvoie MAPI_E_BUSY, appelez la méthode [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) et réessayez l’appel à **QueryRows** une fois l’opération asynchrone terminée.</span><span class="sxs-lookup"><span data-stu-id="174da-165">If **QueryRows** returns MAPI_E_BUSY, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method and retry the call to **QueryRows** when the asynchronous operation is complete.</span></span> 
  
<span data-ttu-id="174da-166">Lorsque vous appelez **QueryRows,** sachez que le minutage des notifications asynchrones peut potentiellement entraîner le fait que le jeu de lignes que vous obtenez de **QueryRows** ne représente pas précisément les données sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="174da-166">When calling **QueryRows**, be aware that the timing of asynchronous notifications can potentially cause the row set that you get back from **QueryRows** not to accurately represent the underlying data.</span></span> <span data-ttu-id="174da-167">Par exemple, un appel de **QueryRows** à la table des matières d’un dossier après la suppression d’un message mais avant la réception de la notification correspondante entraîne le retour de la ligne supprimée dans le jeu de lignes.</span><span class="sxs-lookup"><span data-stu-id="174da-167">For example, a call to **QueryRows** to a folder's contents table following the deletion of a message but prior to the receipt of the corresponding notification will cause the deleted row to be returned in the row set.</span></span> <span data-ttu-id="174da-168">Attendez toujours l’arrivée d’une notification avant de mettre à jour la vue des données de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="174da-168">Always wait for a notification to arrive before updating the user's view of the data.</span></span> 
  
<span data-ttu-id="174da-169">Pour plus d’informations sur la récupération de lignes à partir de tables, voir Récupération des données à partir des [lignes de tableau.](retrieving-data-from-table-rows.md)</span><span class="sxs-lookup"><span data-stu-id="174da-169">For more information about retrieving rows from tables, see [Retrieving Data from Table Rows](retrieving-data-from-table-rows.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="174da-170">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="174da-170">MFCMAPI reference</span></span>

<span data-ttu-id="174da-171">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="174da-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="174da-172">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="174da-172">**File**</span></span>|<span data-ttu-id="174da-173">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="174da-173">**Function**</span></span>|<span data-ttu-id="174da-174">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="174da-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="174da-175">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="174da-175">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="174da-176">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="174da-176">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="174da-177">MFCMAPI utilise la **méthode IMAPITable::QueryRows** pour récupérer les lignes de la table à charger dans l’affichage.</span><span class="sxs-lookup"><span data-stu-id="174da-177">MFCMAPI uses the **IMAPITable::QueryRows** method to retrieve rows in the table to load into the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="174da-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="174da-178">See also</span></span>



[<span data-ttu-id="174da-179">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="174da-179">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="174da-180">FreeProws</span><span class="sxs-lookup"><span data-stu-id="174da-180">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="174da-181">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="174da-181">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="174da-182">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="174da-182">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="174da-183">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="174da-183">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="174da-184">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="174da-184">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="174da-185">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="174da-185">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="174da-186">SRow</span><span class="sxs-lookup"><span data-stu-id="174da-186">SRow</span></span>](srow.md)
  
[<span data-ttu-id="174da-187">SRowSet</span><span class="sxs-lookup"><span data-stu-id="174da-187">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="174da-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="174da-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="174da-189">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="174da-189">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

