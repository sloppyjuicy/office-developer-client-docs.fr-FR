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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3ab069728f872d82246e8925c5ad35c07f41f02e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784101"
---
# <a name="imapitablerestrict"></a><span data-ttu-id="f36f5-103">IMAPITable</span><span class="sxs-lookup"><span data-stu-id="f36f5-103">IMAPITable::Restrict</span></span>

  
  
<span data-ttu-id="f36f5-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f36f5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f36f5-105">Applique un filtre à une table, réduisant la ligne valeur uniquement les lignes correspondant aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="f36f5-105">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f36f5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f36f5-106">Parameters</span></span>

 <span data-ttu-id="f36f5-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="f36f5-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="f36f5-108">[in] Pointeur vers une structure [SRestriction](srestriction.md) définissant les conditions du filtre.</span><span class="sxs-lookup"><span data-stu-id="f36f5-108">[in] Pointer to an [SRestriction](srestriction.md) structure defining the conditions of the filter.</span></span> <span data-ttu-id="f36f5-109">Passage de NULL dans le paramètre _lpRestriction_ supprime le filtre actif.</span><span class="sxs-lookup"><span data-stu-id="f36f5-109">Passing NULL in the  _lpRestriction_ parameter removes the current filter.</span></span> 
    
 <span data-ttu-id="f36f5-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f36f5-110">_ulFlags_</span></span>
  
> <span data-ttu-id="f36f5-111">[in] Masque de bits d’indicateurs qui contrôle le minutage de l’opération de restriction.</span><span class="sxs-lookup"><span data-stu-id="f36f5-111">[in] Bitmask of flags that controls the timing of the restriction operation.</span></span> <span data-ttu-id="f36f5-112">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="f36f5-112">The following flags can be set:</span></span>
    
<span data-ttu-id="f36f5-113">TBL_ASYNC</span><span class="sxs-lookup"><span data-stu-id="f36f5-113">TBL_ASYNC</span></span> 
  
> <span data-ttu-id="f36f5-114">Démarre l’opération asynchrone et renvoie avant la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="f36f5-114">Starts the operation asynchronously and returns before the operation completes.</span></span>
    
<span data-ttu-id="f36f5-115">TBL_BATCH</span><span class="sxs-lookup"><span data-stu-id="f36f5-115">TBL_BATCH</span></span> 
  
> <span data-ttu-id="f36f5-116">Diffère l’évaluation du filtre jusqu'à ce que les données dans le tableau sont requises.</span><span class="sxs-lookup"><span data-stu-id="f36f5-116">Defers evaluation of the filter until the data in the table is required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f36f5-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="f36f5-117">Return value</span></span>

<span data-ttu-id="f36f5-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="f36f5-118">S_OK</span></span> 
  
> <span data-ttu-id="f36f5-119">Le filtre a été appliqué.</span><span class="sxs-lookup"><span data-stu-id="f36f5-119">The filter was successfully applied.</span></span>
    
<span data-ttu-id="f36f5-120">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="f36f5-120">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="f36f5-121">Une autre opération est en cours qui empêche l’opération de restriction de démarrage.</span><span class="sxs-lookup"><span data-stu-id="f36f5-121">Another operation is in progress that prevents the restriction operation from starting.</span></span> <span data-ttu-id="f36f5-122">L’opération en cours doit être autorisée à effectuer ou il doit être arrêté.</span><span class="sxs-lookup"><span data-stu-id="f36f5-122">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="f36f5-123">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="f36f5-123">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="f36f5-124">Le tableau ne peut pas effectuer l’opération car le filtre particulier indiqué par le paramètre _lpRestriction_ est trop compliqué.</span><span class="sxs-lookup"><span data-stu-id="f36f5-124">The table cannot perform the operation because the particular filter pointed to by the  _lpRestriction_ parameter is too complicated.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f36f5-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="f36f5-125">Remarks</span></span>

<span data-ttu-id="f36f5-126">La méthode **IMAPITable** établit une restriction ou le filtre sur une table.</span><span class="sxs-lookup"><span data-stu-id="f36f5-126">The **IMAPITable::Restrict** method establishes a restriction, or filter, on a table.</span></span> <span data-ttu-id="f36f5-127">S’il existe une restriction précédente, elle est ignorée et la nouvelle stratégie appliquée.</span><span class="sxs-lookup"><span data-stu-id="f36f5-127">If there is a previous restriction, it is discarded and the new one applied.</span></span> <span data-ttu-id="f36f5-128">Appliquer une restriction n’a aucun effet sur les données sous-jacentes d’un tableau ; Il modifie simplement l’affichage en limitant les lignes qui peuvent être récupérées aux lignes contenant des données qui répondent à la restriction.</span><span class="sxs-lookup"><span data-stu-id="f36f5-128">Applying a restriction has no affect on the underlying data of a table; it simply alters the view by limiting the rows that can be retrieved to rows containing data that satisfy the restriction.</span></span> 
  
<span data-ttu-id="f36f5-129">Il existe plusieurs types de restrictions, chacun décrit avec une structure différente.</span><span class="sxs-lookup"><span data-stu-id="f36f5-129">There are several different types of restrictions, each described with a different structure.</span></span> <span data-ttu-id="f36f5-130">La structure [SRestriction](srestriction.md) contient deux membres : une valeur qui indique le type de restriction et la structure spécifique applicable pour ce type.</span><span class="sxs-lookup"><span data-stu-id="f36f5-130">The [SRestriction](srestriction.md) structure contains two members: a value that indicates the type of restriction and the specific structure applicable for that type.</span></span> 
  
<span data-ttu-id="f36f5-131">Notifications pour les lignes de tableau qui sont masqués par les appels à **restreindre** ne sont jamais générées.</span><span class="sxs-lookup"><span data-stu-id="f36f5-131">Notifications for table rows that are hidden from view by calls to **Restrict** are never generated.</span></span> 
  
<span data-ttu-id="f36f5-132">Une restriction de propriété sur une propriété à valeurs multiples fonctionne comme une restriction sur une propriété à valeur unique.</span><span class="sxs-lookup"><span data-stu-id="f36f5-132">A property restriction on a multivalued property works like a restriction on a single-valued property.</span></span> <span data-ttu-id="f36f5-133">Une propriété à valeurs multiples à être utilisé dans une restriction de propriété doit avoir l’indicateur MVI_FLAG.</span><span class="sxs-lookup"><span data-stu-id="f36f5-133">A multivalued property to be used in a property restriction must have the MVI_FLAG flag set.</span></span> <span data-ttu-id="f36f5-134">Si elle ne possède pas cet indicateur est défini, il est traité comme un tuple totalement triée.</span><span class="sxs-lookup"><span data-stu-id="f36f5-134">If it doesn't have this flag set, it is treated as a totally ordered tuple.</span></span> <span data-ttu-id="f36f5-135">Une comparaison de deux colonnes à valeurs multiples compare les éléments de la colonne dans l’ordre, la relation entre les colonnes de la première inégalité de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="f36f5-135">A comparison of two multivalued columns compares the column elements in order, reporting the relation of the columns at the first inequality.</span></span> <span data-ttu-id="f36f5-136">Égalité est renvoyée uniquement si les colonnes comparées contiennent les mêmes valeurs dans le même ordre.</span><span class="sxs-lookup"><span data-stu-id="f36f5-136">Equality is returned only if the columns compared contain the same values in the same order.</span></span> <span data-ttu-id="f36f5-137">Si une colonne a moins de valeurs à l’autre, la relation signalée est celui d’une valeur null à l’autre valeur.</span><span class="sxs-lookup"><span data-stu-id="f36f5-137">If one column has fewer values than the other, the reported relation is that of a null value to the other value.</span></span>
  
<span data-ttu-id="f36f5-138">Pour plus d’informations sur les restrictions, voir [à propos des Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="f36f5-138">For more information about restrictions, see [About Restrictions](about-restrictions.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="f36f5-139">Si vous créez des requêtes dynamiques pour rechercher des données sur le serveur, utilisez la méthode **FindRow** au lieu d’utiliser la méthode **Restrict** et la méthode **QueryRows** ensemble.</span><span class="sxs-lookup"><span data-stu-id="f36f5-139">If you create dynamic queries to search for data on the server, use the **FindRow** method instead of using the **Restrict** method and the **QueryRows** method together.</span></span> <span data-ttu-id="f36f5-140">La méthode **Restrict** crée un affichage mis en cache qui est utilisé pour analyser tous les messages ajoutés à ou modifiés dans le dossier de base.</span><span class="sxs-lookup"><span data-stu-id="f36f5-140">The **Restrict** method creates a cached view that is used to evaluate all messages added to or modified in the base folder.</span></span> <span data-ttu-id="f36f5-141">Si une application cliente utilise la méthode **Restrict** pour chaque requête dynamique, un affichage mis en cache sera créé pour chaque requête.</span><span class="sxs-lookup"><span data-stu-id="f36f5-141">If a client application uses the **Restrict** method for each dynamic query, a cached view will be created for each query.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f36f5-142">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="f36f5-142">Notes to callers</span></span>

<span data-ttu-id="f36f5-143">Pour supprimer la restriction actuelle sans créer un nouveau, passez la valeur NULL dans _lpRestriction_.</span><span class="sxs-lookup"><span data-stu-id="f36f5-143">To discard the current restriction without creating a new one, pass NULL in  _lpRestriction_.</span></span>
  
<span data-ttu-id="f36f5-144">Si un autre appel asynchrone table est en cours, à l’origine **Restrict** renvoyer MAPI_E_BUSY, vous pouvez appeler [IMAPITable::Abort](imapitable-abort.md) pour arrêter l’appel.</span><span class="sxs-lookup"><span data-stu-id="f36f5-144">If another asynchronous table call is in progress, causing **Restrict** to return MAPI_E_BUSY, you can call [IMAPITable::Abort](imapitable-abort.md) to stop the call.</span></span> 
  
 <span data-ttu-id="f36f5-145">**Restrict** fonctionne de manière synchrone, sauf si vous définissez un des indicateurs.</span><span class="sxs-lookup"><span data-stu-id="f36f5-145">**Restrict** operates synchronously unless you set one of the flags.</span></span> <span data-ttu-id="f36f5-146">Si vous définissez l’indicateur TBL_BATCH, **Restrict** diffère de l’évaluation de la restriction, sauf si vous demandez les données.</span><span class="sxs-lookup"><span data-stu-id="f36f5-146">If you set the TBL_BATCH flag, **Restrict** postpones the evaluation of the restriction unless you request the data.</span></span> <span data-ttu-id="f36f5-147">Si l’indicateur TBL_ASYNC est défini, **Restrict**fonctionne de manière asynchrone, potentiellement renvoi avant la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="f36f5-147">If the TBL_ASYNC flag is set, **Restrict**operates asynchronously, potentially returning before the completion of the operation.</span></span>
  
<span data-ttu-id="f36f5-148">Tous les signets pour une table sont ignorées lorsqu’un appel à **restreindre** et BOOKMARK_CURRENT, l’emplacement du curseur, est définie au début de la table.</span><span class="sxs-lookup"><span data-stu-id="f36f5-148">All bookmarks for a table are discarded when a call to **Restrict** is made, and BOOKMARK_CURRENT, the current cursor position, is set to the beginning of the table.</span></span> 
  
<span data-ttu-id="f36f5-149">Si vous tentez d’imposer une restriction de propriété sur une propriété qui n’est pas dans l’ensemble de colonnes de la table, les résultats ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="f36f5-149">If you attempt to impose a property restriction on a property that is not in the table's column set, the results are undefined.</span></span> <span data-ttu-id="f36f5-150">Chaque fois que vous n’êtes pas certain si une propriété est prise en charge dans un tableau, combiner la restriction de propriété avec une restriction d’existe.</span><span class="sxs-lookup"><span data-stu-id="f36f5-150">Whenever you are unsure as to whether a property is supported in a table, combine the property restriction with an exists restriction.</span></span> <span data-ttu-id="f36f5-151">La restriction vérifie l’existence de la propriété avant d’essayer d’imposer la restriction de propriété d’existe.</span><span class="sxs-lookup"><span data-stu-id="f36f5-151">The exists restriction checks for the existence of the property before attempting to impose the property restriction.</span></span> 
  
<span data-ttu-id="f36f5-152">Ne prévoyez pas de recevoir une notification de tableau sur une ligne qui a été filtrée d’une table en raison d’une restriction.</span><span class="sxs-lookup"><span data-stu-id="f36f5-152">Do not expect to receive a table notification on a row that has been filtered from a table due to a restriction.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f36f5-153">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f36f5-153">MFCMAPI reference</span></span>

<span data-ttu-id="f36f5-154">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f36f5-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f36f5-155">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="f36f5-155">**File**</span></span>|<span data-ttu-id="f36f5-156">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="f36f5-156">**Function**</span></span>|<span data-ttu-id="f36f5-157">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="f36f5-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f36f5-158">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="f36f5-158">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="f36f5-159">CContentsTableListCtrl::ApplyRestriction</span><span class="sxs-lookup"><span data-stu-id="f36f5-159">CContentsTableListCtrl::ApplyRestriction</span></span>  <br/> |<span data-ttu-id="f36f5-160">MFCMAPI utilise la méthode **IMAPITable** pour définir une restriction sur une table.</span><span class="sxs-lookup"><span data-stu-id="f36f5-160">MFCMAPI uses the **IMAPITable::Restrict** method to set a restriction on a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f36f5-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f36f5-161">See also</span></span>



[<span data-ttu-id="f36f5-162">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="f36f5-162">IMAPITable::Abort</span></span>](imapitable-abort.md)
  
[<span data-ttu-id="f36f5-163">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="f36f5-163">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="f36f5-164">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="f36f5-164">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="f36f5-165">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="f36f5-165">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="f36f5-166">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="f36f5-166">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="f36f5-167">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f36f5-167">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="f36f5-168">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="f36f5-168">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

