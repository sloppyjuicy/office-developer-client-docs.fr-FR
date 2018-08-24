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
ms.openlocfilehash: b6a27231c8dd2c0796b2dcba268de54fcd93e38d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587907"
---
# <a name="imapitablesetcolumns"></a><span data-ttu-id="3e7ff-103">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="3e7ff-103">IMAPITable::SetColumns</span></span>

  
  
<span data-ttu-id="3e7ff-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e7ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e7ff-105">Définit les propriétés et l’ordre des propriétés apparaissent sous forme de colonnes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-105">Defines the particular properties and order of properties to appear as columns in the table.</span></span>
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="3e7ff-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="3e7ff-106">Parameters</span></span>

 <span data-ttu-id="3e7ff-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="3e7ff-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="3e7ff-108">[in] Pointeur vers un tableau de balises de propriété identification des propriétés pour être inclus en tant que colonnes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-108">[in] Pointer to an array of property tags identifying properties to be included as columns in the table.</span></span> <span data-ttu-id="3e7ff-109">La partie du type de propriété de chaque balise peut avoir un type valide ou **PR_NULL** à réserver un espace pour les ajouts suivants.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-109">The property type portion of each tag can be set to a valid type or to **PR_NULL** to reserve space for subsequent additions.</span></span> <span data-ttu-id="3e7ff-110">Le paramètre _lpPropTagArray_ ne peut pas être défini sur NULL ; chaque table doit comporter au moins une colonne.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-110">The  _lpPropTagArray_ parameter cannot be set to NULL; every table must have at least one column.</span></span> 
    
 <span data-ttu-id="3e7ff-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3e7ff-111">_ulFlags_</span></span>
  
> <span data-ttu-id="3e7ff-112">[in] Masque de bits d’indicateurs qui contrôle le retour d’un appel asynchrone au **SetColumns**, par exemple lorsque **SetColumns** est utilisé dans la notification.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-112">[in] Bitmask of flags that controls the return of an asynchronous call to **SetColumns**, for example when **SetColumns** is used in notification.</span></span> <span data-ttu-id="3e7ff-113">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="3e7ff-113">The following flags can be set:</span></span> 
    
<span data-ttu-id="3e7ff-114">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="3e7ff-114">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="3e7ff-115">Demandes l’opération de définition de colonne est effectuée en mode asynchrone à l’origine de **SetColumns** potentiellement retourner avant que l’opération est entièrement terminée.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-115">Requests that the column setting operation be performed asynchronously causing **SetColumns** to potentially return before the operation has fully completed.</span></span> 
    
<span data-ttu-id="3e7ff-116">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="3e7ff-116">TBL_BATCH</span></span> 
  
> <span data-ttu-id="3e7ff-117">Permet à la table de différer l’opération de définition de colonne jusqu'à ce que les données sont réellement nécessaires.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-117">Permits the table to postpone the column setting operation until the data is actually required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3e7ff-118">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="3e7ff-118">Return value</span></span>

<span data-ttu-id="3e7ff-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="3e7ff-119">S_OK</span></span> 
  
> <span data-ttu-id="3e7ff-120">Le paramètre colonne a réussi.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-120">The column setting operation was successful.</span></span>
    
<span data-ttu-id="3e7ff-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="3e7ff-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="3e7ff-122">Une autre opération est en cours qui empêche la colonne définissant l’opération de démarrage.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-122">Another operation is in progress that prevents the column setting operation from starting.</span></span> <span data-ttu-id="3e7ff-123">L’opération en cours doit être autorisée à effectuer ou il doit être arrêté.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3e7ff-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="3e7ff-124">Remarks</span></span>

<span data-ttu-id="3e7ff-125">L’ensemble de colonnes d’une table est le groupe de propriétés qui constituent les colonnes des lignes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-125">The column set of a table is the group of properties that make up the columns for the rows in the table.</span></span> <span data-ttu-id="3e7ff-126">Il est une colonne par défaut pour chaque type de table.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-126">There is a default column set for each type of table.</span></span> <span data-ttu-id="3e7ff-127">L’ensemble de colonnes par défaut est composée des propriétés qui inclut automatiquement de l’implémentation de la table.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-127">The default column set is made up of the properties that the table implementer automatically includes.</span></span> <span data-ttu-id="3e7ff-128">Les utilisateurs de tableau peuvent modifier cette valeur par défaut définie en appelant la méthode **IMAPITable::SetColumns** .</span><span class="sxs-lookup"><span data-stu-id="3e7ff-128">Table users can alter this default set by calling the **IMAPITable::SetColumns** method.</span></span> <span data-ttu-id="3e7ff-129">Ils peuvent demander que les autres colonnes ajoutées à la valeur par défaut si l’implémentation de la table prend en charge les colonnes supprimées ou modifier l’ordre de colonnes que la valeur.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-129">They can request that other columns be added to the default set if the table implementer supports them that columns be removed, or that the order of columns be changed.</span></span> <span data-ttu-id="3e7ff-130">**SetColumns** spécifie les colonnes qui sont retournées avec chaque ligne et l’ordre de ces colonnes dans la ligne.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-130">**SetColumns** specifies the columns that are returned with each row and the order of these columns within the row.</span></span> 
  
<span data-ttu-id="3e7ff-131">La réussite de l’opération **SetColumns** n’apparaît qu’après qu’un appel suivant a été effectué pour récupérer les données de la table.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-131">The success of the **SetColumns** operation is apparent only after a subsequent call has been made to retrieve the data of the table.</span></span> <span data-ttu-id="3e7ff-132">Il est alors que les erreurs détectées.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-132">It is then that any errors are reported.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3e7ff-133">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="3e7ff-133">Notes to implementers</span></span>

<span data-ttu-id="3e7ff-134">Certains fournisseurs permettent à un appel **SetColumns** trier uniquement les colonnes de tableau qui font partie des colonnes disponibles pour un affichage de tableau.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-134">Some providers allow a **SetColumns** call to order only table columns that are part of the available columns for a table view.</span></span> <span data-ttu-id="3e7ff-135">Autres fournisseurs d’autorisent un appel **SetColumns** trier toutes les colonnes du tableau, y compris ceux qui contiennent des propriétés pas dans l’ensemble de colonnes d’origine.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-135">Other providers allow a **SetColumns** call to order all table columns, including those containing properties not in the original column set.</span></span> 
  
<span data-ttu-id="3e7ff-136">Lorsque TBL_BATCH est défini pour les opérations asynchrones, fournisseurs doivent renvoyer un type de propriété de PT_ERROR et une valeur de la propriété Null pour les colonnes qui ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-136">When TBL_BATCH is set for asynchronous operations, providers should return a property type of PT_ERROR and a property value of NULL for columns that are not supported.</span></span>
  
<span data-ttu-id="3e7ff-137">Il est inutile de répondre à le TBL_ASYNC indicateur qui sollicitent que l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-137">You do not need to respond to the TBL_ASYNC flag requesting that the operation be asynchronous.</span></span> <span data-ttu-id="3e7ff-138">Si vous ne prennent pas en charge colonne asynchrone définition, effectuer l’opération de manière synchrone.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-138">If you do not support asynchronous column set definition, perform the operation synchronously.</span></span> <span data-ttu-id="3e7ff-139">Si vous pouvez prendre en charge l’indicateur TBL_ASYNC et l’autre asynchrone opération est toujours en cours, renvoyée MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-139">If you can support the TBL_ASYNC flag and another asynchronous operation is still in progress, return MAPI_E_BUSY.</span></span> <span data-ttu-id="3e7ff-140">Sinon, renvoie S_OK quel que soit ou non toutes les propriétés incluses dans le tableau de la propriété tag prend en charge.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-140">Otherwise, return S_OK regardless of whether or not you support all of the properties included in the property tag array.</span></span> <span data-ttu-id="3e7ff-141">Erreurs résultant des propriétés non prises en charge doivent être renvoyées à partir de méthodes **IMAPITable** qui récupèrent des données, telles que **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-141">Errors resulting from unsupported properties should be returned from **IMAPITable** methods that retrieve data, such as **QueryRows**.</span></span> 
  
<span data-ttu-id="3e7ff-142">Ne génèrent pas de notifications pour les lignes de tableau sont masquées à partir de la vue par les appels à **restreindre**.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-142">Do not generate notifications for table rows that are hidden from view by calls to **Restrict**.</span></span> 
  
<span data-ttu-id="3e7ff-143">Lors de l’envoi des notifications de table, l’ordre des propriétés de membre de la **ligne** de la structure [TABLE_NOTIFICATION](table_notification.md) et l’ordre spécifié par l’appel le plus récent **SetColumns** doit être identique à compter de l’heure de la notification de demande a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-143">When sending table notifications, the order of the properties in the **row** member of the [TABLE_NOTIFICATION](table_notification.md) structure and the order specified by the most recent **SetColumns** call must be the same as of the time that the notification request was sent.</span></span> 
  
<span data-ttu-id="3e7ff-144">Un autre indicateur, TBL_BATCH, permet aux appelants de spécifier que l’implémentation de la table peut différer l’évaluation des résultats de l’opération jusqu'à une date ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-144">Another flag, TBL_BATCH, allows callers to specify that the table implementer can defer evaluating the results of the operation until a later time.</span></span> <span data-ttu-id="3e7ff-145">La mesure du possible, les appelants doivent définir cet indicateur car une opération par lot améliore les performances.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-145">Whenever possible, callers should set this flag because batched operation improves performance.</span></span>
  
<span data-ttu-id="3e7ff-146">Il est souvent pratique pour les appelants à réserver certaines colonnes dans le jeu de lignes récupérées pour les valeurs d’être ajoutées ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-146">It is often convenient for callers to reserve some columns in the retrieved row set for values to be added later.</span></span> <span data-ttu-id="3e7ff-147">Les appelants cela en plaçant **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) à la position souhaitée dans le tableau de balise de propriété passé à **SetColumns**; le tableau sera puis renvoie **PR_NULL** à ces postes dans toutes les lignes extraites avec **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-147">Callers do this by placing **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) at the desired positions in the property tag array passed to **SetColumns**; the table will then pass back **PR_NULL** at those positions in all rows retrieved with **QueryRows**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="3e7ff-148">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="3e7ff-148">Notes to callers</span></span>

<span data-ttu-id="3e7ff-149">Lors de la création du tableau de balise de propriété pour le paramètre _lpPropTagArray_ , les balises de commande dans l’ordre souhaité les colonnes à afficher dans l’affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-149">When building the property tag array for the  _lpPropTagArray_ parameter, order the tags in the order that you want the columns to appear in the table view.</span></span> 
  
<span data-ttu-id="3e7ff-150">Vous pouvez spécifier les propriétés à valeurs multiples pour être inclus dans la colonne en appliquant l’indicateur d’instance à valeurs multiples, ou une constante MVI_FLAG, à la balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-150">You can specify multivalued properties to be included in the column set by applying the multivalued instance flag, or MVI_FLAG constant, to the property tag.</span></span> <span data-ttu-id="3e7ff-151">Définissez cet indicateur en transmettant la balise de propriété pour la version de la propriété à valeur unique en tant que paramètre à la macro MVI_PROP comme suit :</span><span class="sxs-lookup"><span data-stu-id="3e7ff-151">Set this flag by passing the property tag for the single-valued version of the property as a parameter to the MVI_PROP macro as follows:</span></span>
  
```
MVI_PROP(ulPropTag)

```

<span data-ttu-id="3e7ff-152">La macro MVI_PROP définira MVI_FLAG pour la propriété transformer la balise en une balise à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-152">The MVI_PROP macro will set MVI_FLAG for the property, turning the tag into a multivalued tag.</span></span> <span data-ttu-id="3e7ff-153">Si vous essayez tort d’appeler MVI_PROP sur une propriété à valeur unique, MAPI ignorera l’appel et laissez la balise de propriété inchangée.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-153">If you erroneously try to call MVI_PROP on a single-valued property, MAPI will ignore the call and leave the property tag unchanged.</span></span> 
  
<span data-ttu-id="3e7ff-154">Vous pouvez inclure des balises de propriété **PR_NULL** la valeur dans le tableau de la propriété tag pour réserver un espace dans la colonne.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-154">You can include property tags set to **PR_NULL** in the property tag array to reserve space in the column set.</span></span> <span data-ttu-id="3e7ff-155">Réservation d’espace vous permet d’ajouter à une colonne sans avoir à allouer un nouveau tableau de balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-155">Reserving space allows you to add to a column set without having to allocate a new property tag array.</span></span> 
  
<span data-ttu-id="3e7ff-156">Lors de l’appel de **SetColumns** provoque une modification de l’ordre des colonnes d’une table et un ou plusieurs de ces colonnes représentent une propriété à valeurs multiples, il est possible pour le nombre de lignes de la table pour augmenter.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-156">When your call to **SetColumns** causes a change to the order of a table's columns and one or more of these columns represent a multivalued property, it is possible for the number of rows in the table to increase.</span></span> <span data-ttu-id="3e7ff-157">Si cela se produit, tous les signets du tableau sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-157">If this occurs, all of the bookmarks for the table are discarded.</span></span> <span data-ttu-id="3e7ff-158">Pour plus d’informations sur la façon de colonnes à valeurs multiples affectent les tables, voir [utilisation des colonnes à valeurs multiples](working-with-multivalued-columns.md).</span><span class="sxs-lookup"><span data-stu-id="3e7ff-158">For more information about how multivalued columns affect tables, see [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
<span data-ttu-id="3e7ff-159">Définition des colonnes par défaut est une opération synchrone.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-159">Setting columns is by default a synchronous operation.</span></span> <span data-ttu-id="3e7ff-160">Toutefois, vous pouvez autoriser la table à différer l’opération jusqu'à ce que les données sont nécessaires à la définition de l’indicateur TBL_BATCH.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-160">However, you can allow the table to postpone the operation until such time as the data is needed by setting the TBL_BATCH flag.</span></span> <span data-ttu-id="3e7ff-161">Définition de cet indicateur peut améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-161">Setting this flag can improve performance.</span></span> <span data-ttu-id="3e7ff-162">Un autre indicateur, TBL_ASYNC, effectue l’opération asynchrone, ce qui permet de **SetColumns** retourner avant que l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-162">Another flag, TBL_ASYNC, makes the operation asynchronous, allowing **SetColumns** to return before the operation is complete.</span></span> <span data-ttu-id="3e7ff-163">Pour déterminer si l’exécution se produit, appelez [IMAPITable::GetStatus](imapitable-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="3e7ff-163">To determine when completion occurs, call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span>
  
<span data-ttu-id="3e7ff-164">Si un appel à la **méthode SetColumns** renvoie MAPI_E_BUSY, indiquant qu’une autre opération empêche l’opération de démarrage, vous pouvez appeler [IMAPITable::Abort](imapitable-abort.md) pour arrêter l’opération en cours.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-164">If a call to **SetColumns** returns MAPI_E_BUSY, indicating that another operation is preventing your operation from starting, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the operation in progress.</span></span> 
  
<span data-ttu-id="3e7ff-165">Vous pouvez également appeler [HrAddColumnsEx](hraddcolumnsex.md) pour modifier un ensemble de colonnes.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-165">You can also call [HrAddColumnsEx](hraddcolumnsex.md) to change a column set.</span></span> <span data-ttu-id="3e7ff-166">La différence entre **HrAddColumnsEx** et **IMAPITable::SetColumns** est **HrAddColumnsEx** moins de souplesse ; Il ne peut ajouter des colonnes.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-166">The difference between **HrAddColumnsEx** and **IMAPITable::SetColumns** is that **HrAddColumnsEx** is less flexible; it can only add columns.</span></span> <span data-ttu-id="3e7ff-167">Les colonnes supplémentaires sont placés au début de l’ensemble de colonnes ; toutes les colonnes existantes apparaissent après ces colonnes.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-167">The additional columns are placed at the beginning of the column set; all existing columns appear following these columns.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3e7ff-168">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3e7ff-168">MFCMAPI reference</span></span>

<span data-ttu-id="3e7ff-169">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3e7ff-170">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="3e7ff-170">**File**</span></span>|<span data-ttu-id="3e7ff-171">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="3e7ff-171">**Function**</span></span>|<span data-ttu-id="3e7ff-172">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="3e7ff-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3e7ff-173">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="3e7ff-173">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="3e7ff-174">CContentsTableListCtrl::DoSetColumns</span><span class="sxs-lookup"><span data-stu-id="3e7ff-174">CContentsTableListCtrl::DoSetColumns</span></span>  <br/> |<span data-ttu-id="3e7ff-175">MFCMAPI utilise la méthode **IMAPITable::SetColumns** pour définir les colonnes souhaitées pour la table.</span><span class="sxs-lookup"><span data-stu-id="3e7ff-175">MFCMAPI uses the **IMAPITable::SetColumns** method to set the desired columns for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3e7ff-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e7ff-176">See also</span></span>



[<span data-ttu-id="3e7ff-177">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="3e7ff-177">HrQueryAllRows</span></span>](hrqueryallrows.md)
  
[<span data-ttu-id="3e7ff-178">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="3e7ff-178">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="3e7ff-179">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="3e7ff-179">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="3e7ff-180">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="3e7ff-180">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="3e7ff-181">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="3e7ff-181">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="3e7ff-182">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="3e7ff-182">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="3e7ff-183">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="3e7ff-183">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="3e7ff-184">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="3e7ff-184">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="3e7ff-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3e7ff-185">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="3e7ff-186">SRowSet</span><span class="sxs-lookup"><span data-stu-id="3e7ff-186">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="3e7ff-187">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="3e7ff-187">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="3e7ff-188">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3e7ff-188">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="3e7ff-189">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="3e7ff-189">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

