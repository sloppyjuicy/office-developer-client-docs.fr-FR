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
# <a name="imapitablesetcolumns"></a><span data-ttu-id="e269c-103">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="e269c-103">IMAPITable::SetColumns</span></span>

  
  
<span data-ttu-id="e269c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e269c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e269c-105">Définit les propriétés et l'ordre des propriétés spécifiques à afficher sous la forme de colonnes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="e269c-105">Defines the particular properties and order of properties to appear as columns in the table.</span></span>
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e269c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e269c-106">Parameters</span></span>

 <span data-ttu-id="e269c-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="e269c-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="e269c-108">dans Pointeur vers un tableau de balises de propriété qui identifient les propriétés à inclure en tant que colonnes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="e269c-108">[in] Pointer to an array of property tags identifying properties to be included as columns in the table.</span></span> <span data-ttu-id="e269c-109">La partie type de propriété de chaque balise peut être définie sur un type valide ou sur **PR_NULL** pour réserver de l'espace pour les ajouts suivants.</span><span class="sxs-lookup"><span data-stu-id="e269c-109">The property type portion of each tag can be set to a valid type or to **PR_NULL** to reserve space for subsequent additions.</span></span> <span data-ttu-id="e269c-110">Le paramètre _lpPropTagArray_ ne peut pas avoir la valeur null; chaque tableau doit comporter au moins une colonne.</span><span class="sxs-lookup"><span data-stu-id="e269c-110">The  _lpPropTagArray_ parameter cannot be set to NULL; every table must have at least one column.</span></span> 
    
 <span data-ttu-id="e269c-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e269c-111">_ulFlags_</span></span>
  
> <span data-ttu-id="e269c-112">dans Masque de des indicateurs qui contrôle le renvoi d'un appel asynchrone à **SetColumns**, par exemple lorsque la **SetColumns** est utilisée dans la notification.</span><span class="sxs-lookup"><span data-stu-id="e269c-112">[in] Bitmask of flags that controls the return of an asynchronous call to **SetColumns**, for example when **SetColumns** is used in notification.</span></span> <span data-ttu-id="e269c-113">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="e269c-113">The following flags can be set:</span></span> 
    
<span data-ttu-id="e269c-114">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="e269c-114">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="e269c-115">Demande que l'opération de définition de colonne soit effectuée de manière asynchrone, ce qui entraîne le renvoi éventuel de **SetColumns** avant la fin de l'opération.</span><span class="sxs-lookup"><span data-stu-id="e269c-115">Requests that the column setting operation be performed asynchronously causing **SetColumns** to potentially return before the operation has fully completed.</span></span> 
    
<span data-ttu-id="e269c-116">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="e269c-116">TBL_BATCH</span></span> 
  
> <span data-ttu-id="e269c-117">Permet à la table de reporter l'opération de définition de colonne jusqu'à ce que les données soient réellement requises.</span><span class="sxs-lookup"><span data-stu-id="e269c-117">Permits the table to postpone the column setting operation until the data is actually required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e269c-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e269c-118">Return value</span></span>

<span data-ttu-id="e269c-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="e269c-119">S_OK</span></span> 
  
> <span data-ttu-id="e269c-120">L'opération de définition de la colonne a réussi.</span><span class="sxs-lookup"><span data-stu-id="e269c-120">The column setting operation was successful.</span></span>
    
<span data-ttu-id="e269c-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="e269c-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="e269c-122">Une autre opération est en cours, ce qui empêche le démarrage de l'opération de définition de colonne.</span><span class="sxs-lookup"><span data-stu-id="e269c-122">Another operation is in progress that prevents the column setting operation from starting.</span></span> <span data-ttu-id="e269c-123">L'opération en cours doit être autorisée ou elle doit être arrêtée.</span><span class="sxs-lookup"><span data-stu-id="e269c-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e269c-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="e269c-124">Remarks</span></span>

<span data-ttu-id="e269c-125">Le jeu de colonnes d'un tableau est le groupe de propriétés qui composent les colonnes des lignes du tableau.</span><span class="sxs-lookup"><span data-stu-id="e269c-125">The column set of a table is the group of properties that make up the columns for the rows in the table.</span></span> <span data-ttu-id="e269c-126">Il existe un jeu de colonnes par défaut pour chaque type de tableau.</span><span class="sxs-lookup"><span data-stu-id="e269c-126">There is a default column set for each type of table.</span></span> <span data-ttu-id="e269c-127">L'ensemble de colonnes par défaut est composé des propriétés que le programme d'implémentation du tableau inclut automatiquement.</span><span class="sxs-lookup"><span data-stu-id="e269c-127">The default column set is made up of the properties that the table implementer automatically includes.</span></span> <span data-ttu-id="e269c-128">Les utilisateurs de tableau peuvent modifier cet ensemble par défaut en appelant la méthode **IMAPITable:: SetColumns** .</span><span class="sxs-lookup"><span data-stu-id="e269c-128">Table users can alter this default set by calling the **IMAPITable::SetColumns** method.</span></span> <span data-ttu-id="e269c-129">Ils peuvent demander à ce que d'autres colonnes soient ajoutées à l'ensemble par défaut si l'implémenteur de table les prend en charge, ou que l'ordre des colonnes doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="e269c-129">They can request that other columns be added to the default set if the table implementer supports them that columns be removed, or that the order of columns be changed.</span></span> <span data-ttu-id="e269c-130">**SetColumns** spécifie les colonnes renvoyées avec chaque ligne et l'ordre de ces colonnes dans la ligne.</span><span class="sxs-lookup"><span data-stu-id="e269c-130">**SetColumns** specifies the columns that are returned with each row and the order of these columns within the row.</span></span> 
  
<span data-ttu-id="e269c-131">La réussite de l'opération **SetColumns** n'est apparente qu'après qu'un appel a été effectué pour extraire les données de la table.</span><span class="sxs-lookup"><span data-stu-id="e269c-131">The success of the **SetColumns** operation is apparent only after a subsequent call has been made to retrieve the data of the table.</span></span> <span data-ttu-id="e269c-132">Cela signifie que toutes les erreurs sont signalées.</span><span class="sxs-lookup"><span data-stu-id="e269c-132">It is then that any errors are reported.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e269c-133">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="e269c-133">Notes to implementers</span></span>

<span data-ttu-id="e269c-134">Certains fournisseurs permettent à un appel **SetColumns** de trier uniquement les colonnes de table qui font partie des colonnes disponibles pour un affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="e269c-134">Some providers allow a **SetColumns** call to order only table columns that are part of the available columns for a table view.</span></span> <span data-ttu-id="e269c-135">D'autres fournisseurs autorisent un appel **SetColumns** à trier toutes les colonnes de table, y compris celles contenant des propriétés qui ne figurent pas dans l'ensemble de colonnes d'origine.</span><span class="sxs-lookup"><span data-stu-id="e269c-135">Other providers allow a **SetColumns** call to order all table columns, including those containing properties not in the original column set.</span></span> 
  
<span data-ttu-id="e269c-136">Lorsque TBL_BATCH est défini pour des opérations asynchrones, les fournisseurs doivent renvoyer un type de propriété PT_ERROR et une valeur de propriété NULL pour les colonnes qui ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="e269c-136">When TBL_BATCH is set for asynchronous operations, providers should return a property type of PT_ERROR and a property value of NULL for columns that are not supported.</span></span>
  
<span data-ttu-id="e269c-137">Vous n'avez pas besoin de répondre à l'indicateur TBL_ASYNC demandant que l'opération soit asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e269c-137">You do not need to respond to the TBL_ASYNC flag requesting that the operation be asynchronous.</span></span> <span data-ttu-id="e269c-138">Si vous ne prenez pas en charge la définition de jeu de colonnes asynchrone, effectuez l'opération de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="e269c-138">If you do not support asynchronous column set definition, perform the operation synchronously.</span></span> <span data-ttu-id="e269c-139">Si vous pouvez prendre en charge l'indicateur TBL_ASYNC et qu'une autre opération asynchrone est toujours en cours, renvoyez MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="e269c-139">If you can support the TBL_ASYNC flag and another asynchronous operation is still in progress, return MAPI_E_BUSY.</span></span> <span data-ttu-id="e269c-140">Sinon, renvoie S_OK, que vous soyez ou non en prise en charge de toutes les propriétés incluses dans le tableau de balises de propriété.</span><span class="sxs-lookup"><span data-stu-id="e269c-140">Otherwise, return S_OK regardless of whether or not you support all of the properties included in the property tag array.</span></span> <span data-ttu-id="e269c-141">Les erreurs résultant de propriétés non prises en charge doivent être renvoyées par les méthodes **IMAPITable** qui extraient des données, telles que **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="e269c-141">Errors resulting from unsupported properties should be returned from **IMAPITable** methods that retrieve data, such as **QueryRows**.</span></span> 
  
<span data-ttu-id="e269c-142">Ne générez pas de notifications pour les lignes de tableau masquées en vue par les appels à **limiter**.</span><span class="sxs-lookup"><span data-stu-id="e269c-142">Do not generate notifications for table rows that are hidden from view by calls to **Restrict**.</span></span> 
  
<span data-ttu-id="e269c-143">Lors de l'envoi de notifications de table, l'ordre des propriétés dans le membre de **ligne** de la structure [TABLE_NOTIFICATION](table_notification.md) et l'ordre spécifié par le dernier appel **SetColumns** doivent être les mêmes que ceux de la demande de notification. a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="e269c-143">When sending table notifications, the order of the properties in the **row** member of the [TABLE_NOTIFICATION](table_notification.md) structure and the order specified by the most recent **SetColumns** call must be the same as of the time that the notification request was sent.</span></span> 
  
<span data-ttu-id="e269c-144">Un autre indicateur, TBL_BATCH, permet aux appelants de spécifier que l'implémenteur de table peut différer l'évaluation des résultats de l'opération jusqu'à une date ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e269c-144">Another flag, TBL_BATCH, allows callers to specify that the table implementer can defer evaluating the results of the operation until a later time.</span></span> <span data-ttu-id="e269c-145">Dans la mesure du possible, les appelants doivent définir cet indicateur car l'opération par lot améliore les performances.</span><span class="sxs-lookup"><span data-stu-id="e269c-145">Whenever possible, callers should set this flag because batched operation improves performance.</span></span>
  
<span data-ttu-id="e269c-146">Il est souvent commode pour les appelants de réserver certaines colonnes dans l'ensemble de lignes récupérés pour que les valeurs soient ajoutées ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="e269c-146">It is often convenient for callers to reserve some columns in the retrieved row set for values to be added later.</span></span> <span data-ttu-id="e269c-147">Pour cela, les appelants placent **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) aux positions souhaitées dans le tableau des balises de propriété transmises à **SetColumns**; le tableau transmet ensuite **PR_NULL** à ces positions dans toutes les lignes récupérées avec **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="e269c-147">Callers do this by placing **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) at the desired positions in the property tag array passed to **SetColumns**; the table will then pass back **PR_NULL** at those positions in all rows retrieved with **QueryRows**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="e269c-148">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="e269c-148">Notes to callers</span></span>

<span data-ttu-id="e269c-149">Lors de la création du tableau de balises de propriété pour le paramètre _lpPropTagArray_ , organisez les balises dans l'ordre dans lequel vous souhaitez que les colonnes apparaissent dans l'affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="e269c-149">When building the property tag array for the  _lpPropTagArray_ parameter, order the tags in the order that you want the columns to appear in the table view.</span></span> 
  
<span data-ttu-id="e269c-150">Vous pouvez spécifier que les propriétés à valeurs multiples doivent être incluses dans le jeu de colonnes en appliquant l'indicateur d'instance à valeurs multiples ou une constante MVI_FLAG à la balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="e269c-150">You can specify multivalued properties to be included in the column set by applying the multivalued instance flag, or MVI_FLAG constant, to the property tag.</span></span> <span data-ttu-id="e269c-151">Définissez cet indicateur en transmettant la balise de propriété de la version à valeur unique de la propriété en tant que paramètre à la macro MVI_PROP comme suit:</span><span class="sxs-lookup"><span data-stu-id="e269c-151">Set this flag by passing the property tag for the single-valued version of the property as a parameter to the MVI_PROP macro as follows:</span></span>
  
```
MVI_PROP(ulPropTag)

```

<span data-ttu-id="e269c-152">La macro MVI_PROP définit MVI_FLAG pour la propriété, transformant la balise en balise à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="e269c-152">The MVI_PROP macro will set MVI_FLAG for the property, turning the tag into a multivalued tag.</span></span> <span data-ttu-id="e269c-153">Si vous essayez d'appeler MVI_PROP à tort sur une propriété à valeur unique, MAPI ignore l'appel et laisse la balise de propriété inchangée.</span><span class="sxs-lookup"><span data-stu-id="e269c-153">If you erroneously try to call MVI_PROP on a single-valued property, MAPI will ignore the call and leave the property tag unchanged.</span></span> 
  
<span data-ttu-id="e269c-154">Vous pouvez inclure des balises de propriété définies sur **PR_NULL** dans le tableau des balises de propriété pour réserver de l'espace dans le jeu de colonnes.</span><span class="sxs-lookup"><span data-stu-id="e269c-154">You can include property tags set to **PR_NULL** in the property tag array to reserve space in the column set.</span></span> <span data-ttu-id="e269c-155">L'espace réservé vous permet d'ajouter à un jeu de colonnes sans devoir allouer un nouveau tableau de balises de propriété.</span><span class="sxs-lookup"><span data-stu-id="e269c-155">Reserving space allows you to add to a column set without having to allocate a new property tag array.</span></span> 
  
<span data-ttu-id="e269c-156">Lorsque votre appel à **SetColumns** entraîne une modification de l'ordre des colonnes d'une table et qu'une ou plusieurs de ces colonnes représentent une propriété à valeurs multiples, il est possible que le nombre de lignes de la table augmente.</span><span class="sxs-lookup"><span data-stu-id="e269c-156">When your call to **SetColumns** causes a change to the order of a table's columns and one or more of these columns represent a multivalued property, it is possible for the number of rows in the table to increase.</span></span> <span data-ttu-id="e269c-157">Dans ce cas, tous les signets de la table sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="e269c-157">If this occurs, all of the bookmarks for the table are discarded.</span></span> <span data-ttu-id="e269c-158">Pour plus d'informations sur l'impact des colonnes à valeurs multiples sur [les](working-with-multivalued-columns.md)tableaux, voir Working with multiValued Columns.</span><span class="sxs-lookup"><span data-stu-id="e269c-158">For more information about how multivalued columns affect tables, see [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
<span data-ttu-id="e269c-159">La définition de colonnes est par défaut une opération synchrone.</span><span class="sxs-lookup"><span data-stu-id="e269c-159">Setting columns is by default a synchronous operation.</span></span> <span data-ttu-id="e269c-160">Toutefois, vous pouvez autoriser la table à reporter l'opération jusqu'à ce que les données soient nécessaires en définissant l'indicateur TBL_BATCH.</span><span class="sxs-lookup"><span data-stu-id="e269c-160">However, you can allow the table to postpone the operation until such time as the data is needed by setting the TBL_BATCH flag.</span></span> <span data-ttu-id="e269c-161">La définition de cet indicateur peut améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="e269c-161">Setting this flag can improve performance.</span></span> <span data-ttu-id="e269c-162">Un autre indicateur, TBL_ASYNC, rend l'opération asynchrone, ce qui permet le renvoi de **SetColumns** avant la fin de l'opération.</span><span class="sxs-lookup"><span data-stu-id="e269c-162">Another flag, TBL_ASYNC, makes the operation asynchronous, allowing **SetColumns** to return before the operation is complete.</span></span> <span data-ttu-id="e269c-163">Pour déterminer à quel moment l'opération se termine, appelez [IMAPITable:: GetStatus](imapitable-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="e269c-163">To determine when completion occurs, call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span>
  
<span data-ttu-id="e269c-164">Si un appel à **SetColumns** renvoie MAPI_E_BUSY, indiquant qu'une autre opération empêche le démarrage de votre opération, vous pouvez appeler la méthode [IMAPITable:: Abort](imapitable-abort.md) pour arrêter l'opération en cours.</span><span class="sxs-lookup"><span data-stu-id="e269c-164">If a call to **SetColumns** returns MAPI_E_BUSY, indicating that another operation is preventing your operation from starting, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the operation in progress.</span></span> 
  
<span data-ttu-id="e269c-165">Vous pouvez également appeler [HrAddColumnsEx](hraddcolumnsex.md) pour modifier un jeu de colonnes.</span><span class="sxs-lookup"><span data-stu-id="e269c-165">You can also call [HrAddColumnsEx](hraddcolumnsex.md) to change a column set.</span></span> <span data-ttu-id="e269c-166">La différence entre **HrAddColumnsEx** et **IMAPITable:: SetColumns** est que **HrAddColumnsEx** est moins flexible; Il peut uniquement ajouter des colonnes.</span><span class="sxs-lookup"><span data-stu-id="e269c-166">The difference between **HrAddColumnsEx** and **IMAPITable::SetColumns** is that **HrAddColumnsEx** is less flexible; it can only add columns.</span></span> <span data-ttu-id="e269c-167">Les colonnes supplémentaires sont placées au début de l'ensemble de colonnes; toutes les colonnes existantes apparaissent à la suite de ces colonnes.</span><span class="sxs-lookup"><span data-stu-id="e269c-167">The additional columns are placed at the beginning of the column set; all existing columns appear following these columns.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e269c-168">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e269c-168">MFCMAPI reference</span></span>

<span data-ttu-id="e269c-169">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e269c-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e269c-170">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="e269c-170">**File**</span></span>|<span data-ttu-id="e269c-171">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="e269c-171">**Function**</span></span>|<span data-ttu-id="e269c-172">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="e269c-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e269c-173">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="e269c-173">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="e269c-174">CContentsTableListCtrl::D oSetColumns</span><span class="sxs-lookup"><span data-stu-id="e269c-174">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="e269c-175">MFCMAPI utilise la méthode **IMAPITable:: SetColumns** pour définir les colonnes souhaitées pour le tableau.</span><span class="sxs-lookup"><span data-stu-id="e269c-175">MFCMAPI uses the **IMAPITable::SetColumns** method to set the desired columns for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e269c-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e269c-176">See also</span></span>



[<span data-ttu-id="e269c-177">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="e269c-177">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="e269c-178">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="e269c-178">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="e269c-179">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="e269c-179">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="e269c-180">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="e269c-180">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="e269c-181">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="e269c-181">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="e269c-182">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="e269c-182">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="e269c-183">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="e269c-183">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="e269c-184">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="e269c-184">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="e269c-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="e269c-185">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="e269c-186">SRowSet</span><span class="sxs-lookup"><span data-stu-id="e269c-186">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="e269c-187">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e269c-187">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="e269c-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e269c-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="e269c-189">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="e269c-189">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

