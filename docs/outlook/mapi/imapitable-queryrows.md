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
ms.openlocfilehash: a6659f64f6e8d2e3dc61819b2263efe672cdd15c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784111"
---
# <a name="imapitablequeryrows"></a><span data-ttu-id="1d6e2-103">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="1d6e2-103">IMAPITable::QueryRows</span></span>

  
  
<span data-ttu-id="1d6e2-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1d6e2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1d6e2-105">Renvoie une ou plusieurs lignes d’une table, en commençant à l’emplacement du curseur.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-105">Returns one or more rows from a table, beginning at the current cursor position.</span></span>
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a><span data-ttu-id="1d6e2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d6e2-106">Parameters</span></span>

 <span data-ttu-id="1d6e2-107">_lRowCount_</span><span class="sxs-lookup"><span data-stu-id="1d6e2-107">_lRowCount_</span></span>
  
> <span data-ttu-id="1d6e2-108">[in] Nombre maximal de lignes à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-108">[in] Maximum number of rows to be returned.</span></span>
    
 <span data-ttu-id="1d6e2-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1d6e2-109">_ulFlags_</span></span>
  
> <span data-ttu-id="1d6e2-110">[in] Masque de bits d’indicateurs qui contrôlent la façon dont les lignes sont retournées.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-110">[in] Bitmask of flags that control how rows are returned.</span></span> <span data-ttu-id="1d6e2-111">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="1d6e2-111">The following flag can be set:</span></span>
    
<span data-ttu-id="1d6e2-112">TBL_NOADVANCE</span><span class="sxs-lookup"><span data-stu-id="1d6e2-112">TBL_NOADVANCE</span></span> 
  
> <span data-ttu-id="1d6e2-113">Empêche le curseur de passer à la suite de la récupération de la ligne.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-113">Prevents the cursor from advancing as a result of the row retrieval.</span></span> <span data-ttu-id="1d6e2-114">Si l’indicateur TBL_NOADVANCE est défini, les points de curseur à la première ligne renvoyée.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-114">If the TBL_NOADVANCE flag is set, the cursor points to the first row returned.</span></span> <span data-ttu-id="1d6e2-115">Si l’indicateur TBL_NOADVANCE n’est pas définie, le curseur pointe vers la ligne qui suit la dernière ligne renvoyée.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-115">If the TBL_NOADVANCE flag is not set, the cursor points to the row following the last row returned.</span></span>
    
 <span data-ttu-id="1d6e2-116">_lppRows_</span><span class="sxs-lookup"><span data-stu-id="1d6e2-116">_lppRows_</span></span>
  
> <span data-ttu-id="1d6e2-117">[out] Pointeur vers un pointeur vers une structure [SRowSet](srowset.md) contenant les lignes du tableau.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-117">[out] Pointer to a pointer to an [SRowSet](srowset.md) structure holding the table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1d6e2-118">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="1d6e2-118">Return value</span></span>

<span data-ttu-id="1d6e2-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="1d6e2-119">S_OK</span></span> 
  
> <span data-ttu-id="1d6e2-120">Les lignes ont été correctement renvoyées.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-120">The rows were successfully returned.</span></span>
    
<span data-ttu-id="1d6e2-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="1d6e2-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="1d6e2-122">Une autre opération est en cours qui empêche l’opération de récupération de ligne de démarrage.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-122">Another operation is in progress that prevents the row retrieval operation from starting.</span></span> <span data-ttu-id="1d6e2-123">L’opération en cours doit être autorisée à effectuer ou il doit être arrêté.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="1d6e2-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1d6e2-124">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="1d6e2-125">Le paramètre _IRowCount_ est défini sur zéro.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-125">The  _IRowCount_ parameter is set to zero.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1d6e2-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="1d6e2-126">Remarks</span></span>

<span data-ttu-id="1d6e2-127">La méthode **IMAPITable::QueryRows** Obtient une ou plusieurs lignes de données d’une table.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-127">The **IMAPITable::QueryRows** method gets one or more rows of data from a table.</span></span> <span data-ttu-id="1d6e2-128">La valeur du paramètre _IRowCount_ affecte le point de départ pour la récupération.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-128">The value of the  _IRowCount_ parameter affects the starting point for the retrieval.</span></span> <span data-ttu-id="1d6e2-129">Si _IRowCount_ est positif, les lignes sont lues dans une direction avant, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-129">If  _IRowCount_ is positive, rows are read in a forward direction, starting at the current position.</span></span> <span data-ttu-id="1d6e2-130">Si _IRowCount_ est négatif, **QueryRows** réinitialise le point de départ en déplacement vers l’arrière du nombre spécifié de lignes.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-130">If  _IRowCount_ is negative, **QueryRows** resets the starting point by moving backward the indicated number of rows.</span></span> <span data-ttu-id="1d6e2-131">Une fois que le curseur est réinitialisé, les lignes sont lues dans l’ordre chronologique.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-131">After the cursor is reset, rows are read in forward order.</span></span> 
  
<span data-ttu-id="1d6e2-132">Le membre **cRows** dans la structure [SRowSet](srowset.md) désigné par le paramètre _lppRows_ indique le nombre de lignes retournées.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-132">The **cRows** member in the [SRowSet](srowset.md) structure pointed to by the  _lppRows_ parameter indicates the number of rows returned.</span></span> <span data-ttu-id="1d6e2-133">Si aucune ligne n’est retournée :</span><span class="sxs-lookup"><span data-stu-id="1d6e2-133">If zero rows are returned:</span></span> 
  
- <span data-ttu-id="1d6e2-134">Le curseur a été déjà positionné au début de la table et la valeur de _IRowCount_ est négative.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-134">The cursor was already positioned at the beginning of the table and the value of  _IRowCount_ is negative.</span></span> <span data-ttu-id="1d6e2-135">- Ou -</span><span class="sxs-lookup"><span data-stu-id="1d6e2-135">-Or-</span></span> 
    
- <span data-ttu-id="1d6e2-136">Le curseur était placé déjà à la fin de la table et la valeur de _IRowCount_ est positive.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-136">The cursor was already positioned at the end of the table and the value of  _IRowCount_ is positive.</span></span> 
    
<span data-ttu-id="1d6e2-137">Le nombre de colonnes et leur ordre est le même pour chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-137">The number of columns and their ordering is the same for each row.</span></span> <span data-ttu-id="1d6e2-138">Si une propriété n’existe pas pour une ligne ou une erreur de lecture d’une propriété, la structure **SPropValue** pour la propriété dans la ligne contient les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="1d6e2-138">If a property does not exist for a row or there is an error reading a property, the **SPropValue** structure for the property in the row contains the following values:</span></span> 
  
- <span data-ttu-id="1d6e2-139">PT_ERROR pour le type de propriété dans le membre **ulPropTag** .</span><span class="sxs-lookup"><span data-stu-id="1d6e2-139">PT_ERROR for the property type in the **ulPropTag** member.</span></span> 
    
- <span data-ttu-id="1d6e2-140">MAPI_E_NOT_FOUND du membre de **valeur** .</span><span class="sxs-lookup"><span data-stu-id="1d6e2-140">MAPI_E_NOT_FOUND for the **Value** member.</span></span> 
    
<span data-ttu-id="1d6e2-141">Mémoire utilisée pour les structures [SPropValue](spropvalue.md) dans le jeu de lignes indiqué par le paramètre _lppRows_ doit être allouée et libérée pour chaque ligne séparément.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-141">Memory used for the [SPropValue](spropvalue.md) structures in the row set pointed to by the  _lppRows_ parameter must be separately allocated and freed for each row.</span></span> <span data-ttu-id="1d6e2-142">Utilisez [MAPIFreeBuffer](mapifreebuffer.md) pour libérer les structures de valeur de propriété et pour libérer de la ligne.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-142">Use [MAPIFreeBuffer](mapifreebuffer.md) to free the property value structures and to free the row set.</span></span> <span data-ttu-id="1d6e2-143">Lorsqu’un appel **QueryRows** renvoie zéro, toutefois, indiquant le début ou la fin de la table, uniquement la structure de **SRowSet** doit être libéré.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-143">When a call to **QueryRows** returns zero, however, indicating the beginning or end of the table, only the **SRowSet** structure itself needs to be freed.</span></span> <span data-ttu-id="1d6e2-144">Pour plus d’informations sur la façon d’allouer et de libérer de la mémoire dans une structure **SRowSet** , consultez [Gestion de la mémoire ADRLIST des Structures SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="1d6e2-144">For more information about how to allocate and free memory in an **SRowSet** structure, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
<span data-ttu-id="1d6e2-145">Les lignes qui sont retournées et l’ordre dans lequel ils sont retournés dépendent ou non les appels ayant abouti ont été apportées à [IMAPITable](imapitable-restrict.md) et [IMAPITable::SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="1d6e2-145">The rows that are returned and the order in which they are returned depend on whether or not successful calls have been made to [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::SortTable](imapitable-sorttable.md).</span></span> <span data-ttu-id="1d6e2-146">**Restrict** filtre les lignes de l’affichage, à l’origine de **QueryRows** retourner uniquement les lignes qui correspondent aux critères spécifiés dans la restriction.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-146">**Restrict** filters rows from the view, causing **QueryRows** to return only the rows that match the criteria specified in the restriction.</span></span> <span data-ttu-id="1d6e2-147">**SortTable** établit une norme ou de catégorie ordre de tri, affecter la séquence de lignes retournées par **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-147">**SortTable** establishes a standard or categorized sort order, affecting the sequence of rows returned by **QueryRows**.</span></span> <span data-ttu-id="1d6e2-148">Les lignes renvoyées sont dans l’ordre spécifié dans la structure [SSortOrderSet](ssortorderset.md) transmise à **SortTable**.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-148">The returned rows are in the order specified in the [SSortOrderSet](ssortorderset.md) structure passed to **SortTable**.</span></span>
  
<span data-ttu-id="1d6e2-149">Les colonnes renvoyées pour chaque ligne et l’ordre dans lequel ils sont retournés dépendent ou non un appel réussi a été apporté à [IMAPITable::SetColumns](imapitable-setcolumns.md).</span><span class="sxs-lookup"><span data-stu-id="1d6e2-149">The columns returned for each row and the order in which they are returned depend on whether or not a successful call has been made to [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> <span data-ttu-id="1d6e2-150">**SetColumns** établit un ensemble de colonnes, spécifiez les propriétés à inclure dans les colonnes du tableau et l’ordre dans lequel ils doivent être inclus.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-150">**SetColumns** establishes a column set, specifying the properties to be included in columns in the table and the order in which they should be included.</span></span> <span data-ttu-id="1d6e2-151">Si un appel de la **méthode SetColumns** a été effectué, les colonnes dans chaque ligne et l’ordre de ces colonnes particuliers correspond à la colonne spécifiée dans l’appel.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-151">If a **SetColumns** call has been made, the particular columns in each row and the order of those columns match the column set specified in the call.</span></span> <span data-ttu-id="1d6e2-152">Si aucun appel **SetColumns** n’a été effectué, la table renvoie son jeu de colonne par défaut.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-152">If no **SetColumns** call has been made, the table returns its default column set.</span></span> 
  
<span data-ttu-id="1d6e2-153">Si aucun de ces appels a été effectué, **QueryRows** renvoie toutes les lignes de la table.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-153">If none of these calls has been made, **QueryRows** returns all of the rows in the table.</span></span> <span data-ttu-id="1d6e2-154">Chaque ligne contient la colonne par défaut définie dans l’ordre par défaut.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-154">Each row contains the default column set in default order.</span></span> 
  
<span data-ttu-id="1d6e2-155">Lorsque l’ensemble de colonnes d’établir un appel à [IMAPITable::SetColumns](imapitable-setcolumns.md) comprend les colonnes PR_NULL, tableau [SPropValue](spropvalue.md) dans le jeu de lignes retourné dans _lppRows_ contiendra des emplacements vides.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-155">When the column set established in a call to [IMAPITable::SetColumns](imapitable-setcolumns.md) includes columns set to PR_NULL, the [SPropValue](spropvalue.md) array within the row set returned in  _lppRows_ will contain empty slots.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1d6e2-156">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="1d6e2-156">Notes to implementers</span></span>

<span data-ttu-id="1d6e2-157">Vous pouvez autoriser un appelant demander une colonne à inclure dans l’ensemble de colonnes non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-157">You can allow a caller to request an unsupported column to be included in the column set.</span></span> <span data-ttu-id="1d6e2-158">Lorsque cela se produit, placez PT_ERROR dans la partie de type de propriété de la balise de propriété et MAPI_E_NOT_FOUND dans la valeur de propriété pour la colonne non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-158">When this occurs, place PT_ERROR in the property type portion of the property tag and MAPI_E_NOT_FOUND in the property value for the unsupported column.</span></span> 
  
<span data-ttu-id="1d6e2-159">Traite le nombre de lignes comme une demande plutôt qu’une condition requise.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-159">Treat the row count as a request rather than a requirement.</span></span> <span data-ttu-id="1d6e2-160">Vous pouvez retourner de n’importe où à partir de zéro lignes, s’il n’y a aucune ligne dans le sens de la requête, le nombre demandé.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-160">You can return anywhere from zero rows, if there are no rows in the direction of the query, to the number requested.</span></span> 
  
<span data-ttu-id="1d6e2-161">Retourner uniquement les lignes que l’utilisateur s’affiche lorsque les lignes sont demandées à partir d’un affichage tableau classés, permettant à l’appelant d’effectuer des hypothèses valides sur l’étendue des données et éviter le travail supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-161">Return only the rows that the user will see when rows are requested from a categorized table view, allowing the caller to make valid assumptions about the scope of the data and avoid extra work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1d6e2-162">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="1d6e2-162">Notes to callers</span></span>

<span data-ttu-id="1d6e2-163">Généralement vous finirez avec le même nombre de lignes que vous avez spécifié dans le paramètre _lRowCount_ .</span><span class="sxs-lookup"><span data-stu-id="1d6e2-163">Usually you will end up with as many rows as you have specified in the  _lRowCount_ parameter.</span></span> <span data-ttu-id="1d6e2-164">Toutefois, lorsque les limites de mémoire ou de mise en œuvre un problème ou lorsque l’opération atteint le début ou la fin de la table prématurément, **QueryRows** retourne moins de lignes que vous avez demandé.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-164">However, when memory or implementation limits are an issue or when the operation reaches the beginning or end of the table prematurely, **QueryRows** will return less rows than requested.</span></span> 
  
<span data-ttu-id="1d6e2-165">Si **QueryRows** renvoie MAPI_E_BUSY, appelez la méthode [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) et réessayez l’appel **QueryRows** lorsque l’opération asynchrone est terminée.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-165">If **QueryRows** returns MAPI_E_BUSY, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method and retry the call to **QueryRows** when the asynchronous operation is complete.</span></span> 
  
<span data-ttu-id="1d6e2-166">Lors de l’appel **QueryRows**, n’oubliez pas que la synchronisation des notifications asynchrones peut potentiellement provoquer le jeu de lignes que vous récupérez des **QueryRows** ne pas pour représenter précisément les données sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-166">When calling **QueryRows**, be aware that the timing of asynchronous notifications can potentially cause the row set that you get back from **QueryRows** not to accurately represent the underlying data.</span></span> <span data-ttu-id="1d6e2-167">Par exemple, un appel à **QueryRows** suivant de tableau de contenu d’un dossier que la suppression d’un message, mais avant la réception de la notification correspondante entraîne la ligne supprimée à renvoyer à partir de la ligne est définie.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-167">For example, a call to **QueryRows** to a folder's contents table following the deletion of a message but prior to the receipt of the corresponding notification will cause the deleted row to be returned in the row set.</span></span> <span data-ttu-id="1d6e2-168">Toujours attendre une notification avant la mise à jour de la vue des données.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-168">Always wait for a notification to arrive before updating the user's view of the data.</span></span> 
  
<span data-ttu-id="1d6e2-169">Pour plus d’informations sur la récupération des lignes à partir des tables, voir [Récupération de données à partir des lignes de tableau](retrieving-data-from-table-rows.md).</span><span class="sxs-lookup"><span data-stu-id="1d6e2-169">For more information about retrieving rows from tables, see [Retrieving Data from Table Rows](retrieving-data-from-table-rows.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1d6e2-170">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1d6e2-170">MFCMAPI reference</span></span>

<span data-ttu-id="1d6e2-171">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1d6e2-172">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="1d6e2-172">**File**</span></span>|<span data-ttu-id="1d6e2-173">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="1d6e2-173">**Function**</span></span>|<span data-ttu-id="1d6e2-174">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="1d6e2-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1d6e2-175">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="1d6e2-175">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="1d6e2-176">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="1d6e2-176">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="1d6e2-177">MFCMAPI utilise la méthode **IMAPITable::QueryRows** pour récupérer des lignes de la table à charger dans l’affichage.</span><span class="sxs-lookup"><span data-stu-id="1d6e2-177">MFCMAPI uses the **IMAPITable::QueryRows** method to retrieve rows in the table to load into the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1d6e2-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d6e2-178">See also</span></span>



[<span data-ttu-id="1d6e2-179">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="1d6e2-179">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="1d6e2-180">FreeProws</span><span class="sxs-lookup"><span data-stu-id="1d6e2-180">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="1d6e2-181">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="1d6e2-181">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="1d6e2-182">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="1d6e2-182">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="1d6e2-183">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="1d6e2-183">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="1d6e2-184">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="1d6e2-184">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="1d6e2-185">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="1d6e2-185">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="1d6e2-186">SRow</span><span class="sxs-lookup"><span data-stu-id="1d6e2-186">SRow</span></span>](srow.md)
  
[<span data-ttu-id="1d6e2-187">SRowSet</span><span class="sxs-lookup"><span data-stu-id="1d6e2-187">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="1d6e2-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1d6e2-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="1d6e2-189">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="1d6e2-189">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

