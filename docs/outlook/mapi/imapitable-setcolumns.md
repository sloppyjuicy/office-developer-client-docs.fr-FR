---
title: IMAPITableSetColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SetColumns
api_type:
- COM
ms.assetid: 9a39cf8d-df0f-493c-b272-f15c65b3f15e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 897330feb216dbc3ab143378977c77141cf488f0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416348"
---
# <a name="imapitablesetcolumns"></a><span data-ttu-id="ee256-103">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="ee256-103">IMAPITable::SetColumns</span></span>

  
  
<span data-ttu-id="ee256-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee256-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee256-105">Définit les propriétés et l’ordre particuliers des propriétés à voir apparaître sous la valeur de colonnes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="ee256-105">Defines the particular properties and order of properties to appear as columns in the table.</span></span>
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ee256-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ee256-106">Parameters</span></span>

 <span data-ttu-id="ee256-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="ee256-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="ee256-108">[in] Pointeur vers un tableau de balises de propriétés identifiant les propriétés à inclure en tant que colonnes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="ee256-108">[in] Pointer to an array of property tags identifying properties to be included as columns in the table.</span></span> <span data-ttu-id="ee256-109">La partie type de propriété de chaque balise peut être définie sur un type valide ou sur **PR_NULL** pour réserver de l’espace pour les ajouts suivants.</span><span class="sxs-lookup"><span data-stu-id="ee256-109">The property type portion of each tag can be set to a valid type or to **PR_NULL** to reserve space for subsequent additions.</span></span> <span data-ttu-id="ee256-110">Le  _paramètre lpPropTagArray ne_ peut pas être définie sur NULL ; chaque table doit avoir au moins une colonne.</span><span class="sxs-lookup"><span data-stu-id="ee256-110">The  _lpPropTagArray_ parameter cannot be set to NULL; every table must have at least one column.</span></span> 
    
 <span data-ttu-id="ee256-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ee256-111">_ulFlags_</span></span>
  
> <span data-ttu-id="ee256-112">[in] Masque de bits d’indicateurs qui contrôle le retour d’un appel asynchrone à **SetColumns,** par exemple lorsque **SetColumns** est utilisé dans la notification.</span><span class="sxs-lookup"><span data-stu-id="ee256-112">[in] Bitmask of flags that controls the return of an asynchronous call to **SetColumns**, for example when **SetColumns** is used in notification.</span></span> <span data-ttu-id="ee256-113">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="ee256-113">The following flags can be set:</span></span> 
    
<span data-ttu-id="ee256-114">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="ee256-114">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="ee256-115">Demande que l’opération de paramètre de colonne soit effectuée de manière asynchrone, ce qui peut entraîner le retour de **SetColumns** avant que l’opération soit entièrement terminée.</span><span class="sxs-lookup"><span data-stu-id="ee256-115">Requests that the column setting operation be performed asynchronously causing **SetColumns** to potentially return before the operation has fully completed.</span></span> 
    
<span data-ttu-id="ee256-116">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="ee256-116">TBL_BATCH</span></span> 
  
> <span data-ttu-id="ee256-117">Permet au tableau de différer l’opération de définition de colonne jusqu’à ce que les données soient réellement requises.</span><span class="sxs-lookup"><span data-stu-id="ee256-117">Permits the table to postpone the column setting operation until the data is actually required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ee256-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ee256-118">Return value</span></span>

<span data-ttu-id="ee256-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="ee256-119">S_OK</span></span> 
  
> <span data-ttu-id="ee256-120">L’opération de paramètre de colonne a réussi.</span><span class="sxs-lookup"><span data-stu-id="ee256-120">The column setting operation was successful.</span></span>
    
<span data-ttu-id="ee256-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="ee256-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="ee256-122">Une autre opération est en cours qui empêche le démarrage de l’opération de paramètre de colonne.</span><span class="sxs-lookup"><span data-stu-id="ee256-122">Another operation is in progress that prevents the column setting operation from starting.</span></span> <span data-ttu-id="ee256-123">L’opération en cours doit être autorisée ou arrêtée.</span><span class="sxs-lookup"><span data-stu-id="ee256-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ee256-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="ee256-124">Remarks</span></span>

<span data-ttu-id="ee256-125">L’ensemble de colonnes d’un tableau est le groupe de propriétés qui constitue les colonnes des lignes du tableau.</span><span class="sxs-lookup"><span data-stu-id="ee256-125">The column set of a table is the group of properties that make up the columns for the rows in the table.</span></span> <span data-ttu-id="ee256-126">Il existe un jeu de colonnes par défaut pour chaque type de tableau.</span><span class="sxs-lookup"><span data-stu-id="ee256-126">There is a default column set for each type of table.</span></span> <span data-ttu-id="ee256-127">L’ensemble de colonnes par défaut est composé des propriétés que l’implémenteur de table inclut automatiquement.</span><span class="sxs-lookup"><span data-stu-id="ee256-127">The default column set is made up of the properties that the table implementer automatically includes.</span></span> <span data-ttu-id="ee256-128">Les utilisateurs du tableau peuvent modifier ce jeu par défaut en appelant la **méthode IMAPITable::SetColumns.**</span><span class="sxs-lookup"><span data-stu-id="ee256-128">Table users can alter this default set by calling the **IMAPITable::SetColumns** method.</span></span> <span data-ttu-id="ee256-129">Ils peuvent demander que d’autres colonnes soient ajoutées à l’ensemble par défaut si l’implémenteur de tableau les prend en charge, que les colonnes soient supprimées ou que l’ordre des colonnes soit modifié.</span><span class="sxs-lookup"><span data-stu-id="ee256-129">They can request that other columns be added to the default set if the table implementer supports them that columns be removed, or that the order of columns be changed.</span></span> <span data-ttu-id="ee256-130">**SetColumns** spécifie les colonnes qui sont renvoyées avec chaque ligne et l’ordre de ces colonnes dans la ligne.</span><span class="sxs-lookup"><span data-stu-id="ee256-130">**SetColumns** specifies the columns that are returned with each row and the order of these columns within the row.</span></span> 
  
<span data-ttu-id="ee256-131">La réussite de **l’opération SetColumns** n’apparaît qu’après qu’un appel ultérieur a été effectué pour récupérer les données de la table.</span><span class="sxs-lookup"><span data-stu-id="ee256-131">The success of the **SetColumns** operation is apparent only after a subsequent call has been made to retrieve the data of the table.</span></span> <span data-ttu-id="ee256-132">C’est alors que les erreurs sont signalées.</span><span class="sxs-lookup"><span data-stu-id="ee256-132">It is then that any errors are reported.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ee256-133">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="ee256-133">Notes to implementers</span></span>

<span data-ttu-id="ee256-134">Certains fournisseurs autorisent un appel **SetColumns** à commander uniquement les colonnes de tableau qui font partie des colonnes disponibles pour un affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="ee256-134">Some providers allow a **SetColumns** call to order only table columns that are part of the available columns for a table view.</span></span> <span data-ttu-id="ee256-135">D’autres fournisseurs autorisent un appel **SetColumns** pour commander toutes les colonnes de table, y compris celles qui contiennent des propriétés qui ne sont pas dans le jeu de colonnes d’origine.</span><span class="sxs-lookup"><span data-stu-id="ee256-135">Other providers allow a **SetColumns** call to order all table columns, including those containing properties not in the original column set.</span></span> 
  
<span data-ttu-id="ee256-136">Lorsque TBL_BATCH est définie pour les opérations asynchrones, les fournisseurs doivent renvoyer un type de propriété de PT_ERROR et une valeur de propriété NULL pour les colonnes qui ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ee256-136">When TBL_BATCH is set for asynchronous operations, providers should return a property type of PT_ERROR and a property value of NULL for columns that are not supported.</span></span>
  
<span data-ttu-id="ee256-137">Vous n’avez pas besoin de répondre à l’indicateur TBL_ASYNC demande que l’opération soit asynchrone.</span><span class="sxs-lookup"><span data-stu-id="ee256-137">You do not need to respond to the TBL_ASYNC flag requesting that the operation be asynchronous.</span></span> <span data-ttu-id="ee256-138">Si vous ne prisez pas en charge la définition de jeu de colonnes asynchrone, effectuez l’opération de manière synchrone.</span><span class="sxs-lookup"><span data-stu-id="ee256-138">If you do not support asynchronous column set definition, perform the operation synchronously.</span></span> <span data-ttu-id="ee256-139">Si vous pouvez prendre en charge l’indicateur TBL_ASYNC et qu’une autre opération asynchrone est toujours en cours, renvoyez MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="ee256-139">If you can support the TBL_ASYNC flag and another asynchronous operation is still in progress, return MAPI_E_BUSY.</span></span> <span data-ttu-id="ee256-140">Sinon, renvoyez S_OK indépendamment de la prise en charge ou non de toutes les propriétés incluses dans le tableau de balises de propriétés.</span><span class="sxs-lookup"><span data-stu-id="ee256-140">Otherwise, return S_OK regardless of whether or not you support all of the properties included in the property tag array.</span></span> <span data-ttu-id="ee256-141">Les erreurs résultant de propriétés nonupportées doivent être renvoyées à partir des méthodes **IMAPITable** qui récupèrent des données, telles que **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="ee256-141">Errors resulting from unsupported properties should be returned from **IMAPITable** methods that retrieve data, such as **QueryRows**.</span></span> 
  
<span data-ttu-id="ee256-142">Ne générez pas de notifications pour les lignes de tableau qui sont masquées par les appels à **Restreindre**.</span><span class="sxs-lookup"><span data-stu-id="ee256-142">Do not generate notifications for table rows that are hidden from view by calls to **Restrict**.</span></span> 
  
<span data-ttu-id="ee256-143">Lors de l’envoi de notifications  de table, l’ordre des propriétés dans le membre de ligne de la structure TABLE_NOTIFICATION et l’ordre spécifié par l’appel **SetColumns** le plus récent doivent être identiques au moment où la demande de notification [a](table_notification.md) été envoyée.</span><span class="sxs-lookup"><span data-stu-id="ee256-143">When sending table notifications, the order of the properties in the **row** member of the [TABLE_NOTIFICATION](table_notification.md) structure and the order specified by the most recent **SetColumns** call must be the same as of the time that the notification request was sent.</span></span> 
  
<span data-ttu-id="ee256-144">Un autre indicateur, TBL_BATCH, permet aux appelants de spécifier que l’implémenteur de table peut différer l’évaluation des résultats de l’opération jusqu’à une date ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ee256-144">Another flag, TBL_BATCH, allows callers to specify that the table implementer can defer evaluating the results of the operation until a later time.</span></span> <span data-ttu-id="ee256-145">Dans la mesure du possible, les appelants doivent définir cet indicateur car l’opération par lot améliore les performances.</span><span class="sxs-lookup"><span data-stu-id="ee256-145">Whenever possible, callers should set this flag because batched operation improves performance.</span></span>
  
<span data-ttu-id="ee256-146">Il est souvent pratique pour les appelants de réserver certaines colonnes dans le jeu de lignes récupéré pour que les valeurs soient ajoutées ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="ee256-146">It is often convenient for callers to reserve some columns in the retrieved row set for values to be added later.</span></span> <span data-ttu-id="ee256-147">Pour ce faire, les appelants placent **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) aux positions souhaitées dans le tableau de balises de propriétés transmis à **SetColumns**; La table est ensuite resserré **PR_NULL** à ces positions dans toutes les lignes récupérées avec **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="ee256-147">Callers do this by placing **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) at the desired positions in the property tag array passed to **SetColumns**; the table will then pass back **PR_NULL** at those positions in all rows retrieved with **QueryRows**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="ee256-148">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="ee256-148">Notes to callers</span></span>

<span data-ttu-id="ee256-149">Lors de la création du tableau de balises de propriétés pour le paramètre  _lpPropTagArray,_ commandez les balises dans l’ordre dans le sens où les colonnes apparaissent dans l’affichage Tableau.</span><span class="sxs-lookup"><span data-stu-id="ee256-149">When building the property tag array for the  _lpPropTagArray_ parameter, order the tags in the order that you want the columns to appear in the table view.</span></span> 
  
<span data-ttu-id="ee256-150">Vous pouvez spécifier des propriétés à valeurs multiples à inclure dans l’ensemble de colonnes en appliquant l’indicateur d’instance à valeurs multiples, ou MVI_FLAG constante, à la balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="ee256-150">You can specify multivalued properties to be included in the column set by applying the multivalued instance flag, or MVI_FLAG constant, to the property tag.</span></span> <span data-ttu-id="ee256-151">Définissez cet indicateur en passant la balise de propriété pour la version à valeur unique de la propriété en tant que paramètre à la macro MVI_PROP comme suit :</span><span class="sxs-lookup"><span data-stu-id="ee256-151">Set this flag by passing the property tag for the single-valued version of the property as a parameter to the MVI_PROP macro as follows:</span></span>
  
```
MVI_PROP(ulPropTag)

```

<span data-ttu-id="ee256-152">La macro MVI_PROP définira MVI_FLAG pour la propriété, ce qui transformera la balise en balise à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="ee256-152">The MVI_PROP macro will set MVI_FLAG for the property, turning the tag into a multivalued tag.</span></span> <span data-ttu-id="ee256-153">Si vous essayez par erreur d’appeler MVI_PROP sur une propriété à valeur unique, MAPI ignore l’appel et laisse la balise de propriété inchangée.</span><span class="sxs-lookup"><span data-stu-id="ee256-153">If you erroneously try to call MVI_PROP on a single-valued property, MAPI will ignore the call and leave the property tag unchanged.</span></span> 
  
<span data-ttu-id="ee256-154">Vous pouvez inclure des balises de propriété définies **PR_NULL** dans le tableau de balises de propriétés pour réserver de l’espace dans le jeu de colonnes.</span><span class="sxs-lookup"><span data-stu-id="ee256-154">You can include property tags set to **PR_NULL** in the property tag array to reserve space in the column set.</span></span> <span data-ttu-id="ee256-155">La réservation d’espace vous permet d’ajouter un jeu de colonnes sans devoir allouer un nouveau tableau de balises de propriétés.</span><span class="sxs-lookup"><span data-stu-id="ee256-155">Reserving space allows you to add to a column set without having to allocate a new property tag array.</span></span> 
  
<span data-ttu-id="ee256-156">Lorsque votre appel à **SetColumns** modifie l’ordre des colonnes d’un tableau et qu’une ou plusieurs de ces colonnes représentent une propriété à valeurs multiples, il est possible d’augmenter le nombre de lignes du tableau.</span><span class="sxs-lookup"><span data-stu-id="ee256-156">When your call to **SetColumns** causes a change to the order of a table's columns and one or more of these columns represent a multivalued property, it is possible for the number of rows in the table to increase.</span></span> <span data-ttu-id="ee256-157">Si cela se produit, tous les signets du tableau sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="ee256-157">If this occurs, all of the bookmarks for the table are discarded.</span></span> <span data-ttu-id="ee256-158">Pour plus d’informations sur l’impact des colonnes à valeurs multiples sur les tableaux, voir [Working with Multivalued Columns](working-with-multivalued-columns.md).</span><span class="sxs-lookup"><span data-stu-id="ee256-158">For more information about how multivalued columns affect tables, see [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
<span data-ttu-id="ee256-159">La définition de colonnes est une opération synchrone par défaut.</span><span class="sxs-lookup"><span data-stu-id="ee256-159">Setting columns is by default a synchronous operation.</span></span> <span data-ttu-id="ee256-160">Toutefois, vous pouvez autoriser la table à reporter l’opération jusqu’à ce que les données soient nécessaires en TBL_BATCH’indicateur.</span><span class="sxs-lookup"><span data-stu-id="ee256-160">However, you can allow the table to postpone the operation until such time as the data is needed by setting the TBL_BATCH flag.</span></span> <span data-ttu-id="ee256-161">La définition de cet indicateur peut améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="ee256-161">Setting this flag can improve performance.</span></span> <span data-ttu-id="ee256-162">Un autre indicateur, TBL_ASYNC, rend l’opération asynchrone, ce qui permet à **SetColumns** de revenir avant la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="ee256-162">Another flag, TBL_ASYNC, makes the operation asynchronous, allowing **SetColumns** to return before the operation is complete.</span></span> <span data-ttu-id="ee256-163">Pour déterminer quand l’achèvement se produit, appelez [IMAPITable::GetStatus](imapitable-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="ee256-163">To determine when completion occurs, call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span>
  
<span data-ttu-id="ee256-164">Si un appel à **SetColumns** renvoie MAPI_E_BUSY, indiquant qu’une autre opération empêche le démarrage de votre opération, vous pouvez appeler [IMAPITable::Abort](imapitable-abort.md) pour arrêter l’opération en cours.</span><span class="sxs-lookup"><span data-stu-id="ee256-164">If a call to **SetColumns** returns MAPI_E_BUSY, indicating that another operation is preventing your operation from starting, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the operation in progress.</span></span> 
  
<span data-ttu-id="ee256-165">Vous pouvez également appeler [HrAddColumnsEx](hraddcolumnsex.md) pour modifier un jeu de colonnes.</span><span class="sxs-lookup"><span data-stu-id="ee256-165">You can also call [HrAddColumnsEx](hraddcolumnsex.md) to change a column set.</span></span> <span data-ttu-id="ee256-166">La différence entre **HrAddColumnsEx** et **IMAPITable::SetColumns** est que **HrAddColumnsEx** est moins flexible ; il ne peut ajouter que des colonnes.</span><span class="sxs-lookup"><span data-stu-id="ee256-166">The difference between **HrAddColumnsEx** and **IMAPITable::SetColumns** is that **HrAddColumnsEx** is less flexible; it can only add columns.</span></span> <span data-ttu-id="ee256-167">Les colonnes supplémentaires sont placées au début du jeu de colonnes ; Toutes les colonnes existantes apparaissent après ces colonnes.</span><span class="sxs-lookup"><span data-stu-id="ee256-167">The additional columns are placed at the beginning of the column set; all existing columns appear following these columns.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ee256-168">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ee256-168">MFCMAPI reference</span></span>

<span data-ttu-id="ee256-169">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ee256-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ee256-170">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="ee256-170">**File**</span></span>|<span data-ttu-id="ee256-171">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="ee256-171">**Function**</span></span>|<span data-ttu-id="ee256-172">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="ee256-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ee256-173">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="ee256-173">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="ee256-174">CContentsTableListCtrl::D oSetColumns</span><span class="sxs-lookup"><span data-stu-id="ee256-174">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="ee256-175">MFCMAPI utilise la **méthode IMAPITable::SetColumns** pour définir les colonnes souhaitées pour le tableau.</span><span class="sxs-lookup"><span data-stu-id="ee256-175">MFCMAPI uses the **IMAPITable::SetColumns** method to set the desired columns for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ee256-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee256-176">See also</span></span>



[<span data-ttu-id="ee256-177">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="ee256-177">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="ee256-178">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="ee256-178">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="ee256-179">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="ee256-179">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="ee256-180">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="ee256-180">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="ee256-181">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="ee256-181">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="ee256-182">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="ee256-182">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="ee256-183">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="ee256-183">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="ee256-184">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="ee256-184">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="ee256-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="ee256-185">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="ee256-186">SRowSet</span><span class="sxs-lookup"><span data-stu-id="ee256-186">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="ee256-187">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="ee256-187">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="ee256-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ee256-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="ee256-189">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="ee256-189">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

