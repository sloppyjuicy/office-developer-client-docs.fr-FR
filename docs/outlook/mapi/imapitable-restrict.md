---
title: IMAPITableRestrict
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Restrict
api_type:
- COM
ms.assetid: a5bfc190-b58f-44c3-893c-8727df14ee58
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6cca6bc12fa6f100885b7bf705d79fa24a2e2f91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414619"
---
# <a name="imapitablerestrict"></a><span data-ttu-id="f3bfe-103">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="f3bfe-103">IMAPITable::Restrict</span></span>

  
  
<span data-ttu-id="f3bfe-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3bfe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3bfe-105">Applique un filtre à un tableau, en réduisant le jeu de lignes uniquement aux lignes correspondant aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-105">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f3bfe-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3bfe-106">Parameters</span></span>

 <span data-ttu-id="f3bfe-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="f3bfe-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="f3bfe-108">[in] Pointeur vers une structure [SRestriction](srestriction.md) définissant les conditions du filtre.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-108">[in] Pointer to an [SRestriction](srestriction.md) structure defining the conditions of the filter.</span></span> <span data-ttu-id="f3bfe-109">La transmission de null dans  _le paramètre lpRestriction_ supprime le filtre actuel.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-109">Passing NULL in the  _lpRestriction_ parameter removes the current filter.</span></span> 
    
 <span data-ttu-id="f3bfe-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f3bfe-110">_ulFlags_</span></span>
  
> <span data-ttu-id="f3bfe-111">[in] Masque de bits d’indicateurs qui contrôle le minutage de l’opération de restriction.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-111">[in] Bitmask of flags that controls the timing of the restriction operation.</span></span> <span data-ttu-id="f3bfe-112">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="f3bfe-112">The following flags can be set:</span></span>
    
<span data-ttu-id="f3bfe-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="f3bfe-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="f3bfe-114">Démarre l’opération de manière asynchrone et renvoie avant la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-114">Starts the operation asynchronously and returns before the operation completes.</span></span>
    
<span data-ttu-id="f3bfe-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="f3bfe-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="f3bfe-116">Reporte l’évaluation du filtre jusqu’à ce que les données de la table soient requises.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-116">Defers evaluation of the filter until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f3bfe-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f3bfe-117">Return value</span></span>

<span data-ttu-id="f3bfe-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3bfe-118">S_OK</span></span> 
  
> <span data-ttu-id="f3bfe-119">Le filtre a été appliqué avec succès.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-119">The filter was successfully applied.</span></span>
    
<span data-ttu-id="f3bfe-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="f3bfe-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="f3bfe-121">Une autre opération est en cours qui empêche le démarrage de l’opération de restriction.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-121">Another operation is in progress that prevents the restriction operation from starting.</span></span> <span data-ttu-id="f3bfe-122">L’opération en cours doit être autorisée ou arrêtée.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="f3bfe-123">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="f3bfe-123">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="f3bfe-124">La table ne peut pas effectuer l’opération, car le filtre spécifique pointé par  _le paramètre lpRestriction_ est trop compliqué.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-124">The table cannot perform the operation because the particular filter pointed to by the  _lpRestriction_ parameter is too complicated.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f3bfe-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="f3bfe-125">Remarks</span></span>

<span data-ttu-id="f3bfe-126">La **méthode IMAPITable::Restrict** établit une restriction ou un filtre sur une table.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-126">The **IMAPITable::Restrict** method establishes a restriction, or filter, on a table.</span></span> <span data-ttu-id="f3bfe-127">S’il existe une restriction précédente, elle est ignorée et la nouvelle est appliquée.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-127">If there is a previous restriction, it is discarded and the new one applied.</span></span> <span data-ttu-id="f3bfe-128">L’application d’une restriction n’a aucune incidence sur les données sous-jacentes d’une table . Il modifie simplement l’affichage en limitant les lignes qui peuvent être récupérées aux lignes contenant des données qui répondent à la restriction.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-128">Applying a restriction has no affect on the underlying data of a table; it simply alters the view by limiting the rows that can be retrieved to rows containing data that satisfy the restriction.</span></span> 
  
<span data-ttu-id="f3bfe-129">Il existe plusieurs types de restrictions, chacune étant décrite avec une structure différente.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-129">There are several different types of restrictions, each described with a different structure.</span></span> <span data-ttu-id="f3bfe-130">La structure [SRestriction](srestriction.md) contient deux membres : une valeur qui indique le type de restriction et la structure spécifique applicable à ce type.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-130">The [SRestriction](srestriction.md) structure contains two members: a value that indicates the type of restriction and the specific structure applicable for that type.</span></span> 
  
<span data-ttu-id="f3bfe-131">Les notifications pour les lignes de tableau masquées par les appels à **Restreindre** ne sont jamais générées.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-131">Notifications for table rows that are hidden from view by calls to **Restrict** are never generated.</span></span> 
  
<span data-ttu-id="f3bfe-132">Une restriction de propriété sur une propriété à valeurs multiples fonctionne comme une restriction sur une propriété à valeur unique.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-132">A property restriction on a multivalued property works like a restriction on a single-valued property.</span></span> <span data-ttu-id="f3bfe-133">Une propriété à valeurs multiples à utiliser dans une restriction de propriété doit avoir l’indicateur MVI_FLAG définie.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-133">A multivalued property to be used in a property restriction must have the MVI_FLAG flag set.</span></span> <span data-ttu-id="f3bfe-134">S’il n’a pas cet indicateur, il est traité comme un tuple totalement ordonné.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-134">If it doesn't have this flag set, it is treated as a totally ordered tuple.</span></span> <span data-ttu-id="f3bfe-135">Une comparaison de deux colonnes à valeurs multiples compare les éléments de colonne dans l’ordre, en signalant la relation des colonnes à la première indiquité.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-135">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality.</span></span> <span data-ttu-id="f3bfe-136">L’égalité est renvoyée uniquement si les colonnes comparées contiennent les mêmes valeurs dans le même ordre.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-136">Equality is returned only if the columns compared contain the same values in the same order.</span></span> <span data-ttu-id="f3bfe-137">Si une colonne a moins de valeurs que l’autre, la relation signalée est celle d’une valeur null par rapport à l’autre valeur.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-137">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
<span data-ttu-id="f3bfe-138">Pour plus d’informations sur les restrictions, voir [À propos des restrictions.](about-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="f3bfe-138">For more information about restrictions, see [About Restrictions](about-restrictions.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="f3bfe-139">Si vous créez des requêtes dynamiques pour rechercher des données sur le serveur, utilisez la méthode **FindRow** au lieu d’utiliser les méthodes **Restrict** et **QueryRows** ensemble.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-139">If you create dynamic queries to search for data on the server, use the **FindRow** method instead of using the **Restrict** method and the **QueryRows** method together.</span></span> <span data-ttu-id="f3bfe-140">La **méthode Restrict** crée une vue mise en cache qui est utilisée pour évaluer tous les messages ajoutés ou modifiés dans le dossier de base.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-140">The **Restrict** method creates a cached view that is used to evaluate all messages added to or modified in the base folder.</span></span> <span data-ttu-id="f3bfe-141">Si une application cliente utilise **la méthode Restrict** pour chaque requête dynamique, une vue mise en cache est créée pour chaque requête.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-141">If a client application uses the **Restrict** method for each dynamic query, a cached view will be created for each query.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f3bfe-142">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="f3bfe-142">Notes to callers</span></span>

<span data-ttu-id="f3bfe-143">Pour ignorer la restriction actuelle sans en créer une, passez NULL dans  _lpRestriction_.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-143">To discard the current restriction without creating a new one, pass NULL in  _lpRestriction_.</span></span>
  
<span data-ttu-id="f3bfe-144">Si un autre appel de table asynchrone est en cours, ce qui a pour effet de restreindre le retour de MAPI_E_BUSY, vous pouvez appeler [IMAPITable::Abort](imapitable-abort.md) pour arrêter l’appel. </span><span class="sxs-lookup"><span data-stu-id="f3bfe-144">If another asynchronous table call is in progress, causing **Restrict** to return MAPI_E_BUSY, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the call.</span></span> 
  
 <span data-ttu-id="f3bfe-145">**La** restriction fonctionne de manière synchrone, sauf si vous définissez l’un des indicateurs.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-145">**Restrict** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="f3bfe-146">Si vous définissez l’TBL_BATCH, **Restrict** reporte l’évaluation de la restriction, sauf si vous demandez les données.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-146">If you set the TBL_BATCH flag, **Restrict** postpones the evaluation of the restriction unless you request the data.</span></span> <span data-ttu-id="f3bfe-147">Si l TBL_ASYNC est définie, **Restrict** fonctionne de manière asynchrone, ce qui peut renvoyer le résultat avant la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-147">If the TBL_ASYNC flag is set, **Restrict** operates asynchronously, potentially returning before the completion of the operation.</span></span>
  
<span data-ttu-id="f3bfe-148">Tous les signets d’une table  sont ignorés lorsqu’un appel à Restreindre est effectué et BOOKMARK_CURRENT, la position actuelle du curseur, est définie au début du tableau.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-148">All bookmarks for a table are discarded when a call to **Restrict** is made, and BOOKMARK_CURRENT, the current cursor position, is set to the beginning of the table.</span></span> 
  
<span data-ttu-id="f3bfe-149">Si vous tentez d’imposer une restriction de propriété à une propriété qui ne se trouve pas dans le jeu de colonnes du tableau, les résultats ne sont pas définies.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-149">If you attempt to impose a property restriction on a property that is not in the table's column set, the results are undefined.</span></span> <span data-ttu-id="f3bfe-150">Chaque fois que vous ne savez pas si une propriété est prise en charge dans une table, combinez la restriction de propriété avec une restriction qui existe.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-150">Whenever you are unsure as to whether a property is supported in a table, combine the property restriction with an exists restriction.</span></span> <span data-ttu-id="f3bfe-151">La restriction existe vérifie l’existence de la propriété avant d’essayer d’imposer la restriction de propriété.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-151">The exists restriction checks for the existence of the property before attempting to impose the property restriction.</span></span> 
  
<span data-ttu-id="f3bfe-152">Ne vous attendez pas à recevoir une notification de tableau sur une ligne qui a été filtrée à partir d’une table en raison d’une restriction.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-152">Do not expect to receive a table notification on a row that has been filtered from a table due to a restriction.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f3bfe-153">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f3bfe-153">MFCMAPI reference</span></span>

<span data-ttu-id="f3bfe-154">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f3bfe-155">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="f3bfe-155">**File**</span></span>|<span data-ttu-id="f3bfe-156">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="f3bfe-156">**Function**</span></span>|<span data-ttu-id="f3bfe-157">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="f3bfe-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f3bfe-158">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="f3bfe-158">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="f3bfe-159">CContentsTableListCtrl::ApplyRestriction</span><span class="sxs-lookup"><span data-stu-id="f3bfe-159">CContentsTableListCtrl::ApplyRestriction</span></span>  <br/> |<span data-ttu-id="f3bfe-160">MFCMAPI utilise la **méthode IMAPITable::Restrict** pour définir une restriction sur une table.</span><span class="sxs-lookup"><span data-stu-id="f3bfe-160">MFCMAPI uses the **IMAPITable::Restrict** method to set a restriction on a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f3bfe-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3bfe-161">See also</span></span>



[<span data-ttu-id="f3bfe-162">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="f3bfe-162">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="f3bfe-163">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="f3bfe-163">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="f3bfe-164">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="f3bfe-164">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="f3bfe-165">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="f3bfe-165">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="f3bfe-166">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="f3bfe-166">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="f3bfe-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f3bfe-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="f3bfe-168">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="f3bfe-168">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

