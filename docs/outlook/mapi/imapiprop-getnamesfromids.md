---
title: IMAPIPropGetNamesFromIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetNamesFromIDs
api_type:
- COM
ms.assetid: 3efa4731-cf32-4a6c-9ba8-d059e58b0d98
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f6688afde9b36a7722eaaf768f091481c15b7308
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423572"
---
# <a name="imapipropgetnamesfromids"></a><span data-ttu-id="fd079-103">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="fd079-103">IMAPIProp::GetNamesFromIDs</span></span>

  
  
<span data-ttu-id="fd079-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd079-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd079-105">Fournit les noms de propriété qui correspondent à un ou plusieurs identificateurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="fd079-105">Provides the property names that correspond to one or more property identifiers.</span></span>
  
```cpp
HRESULT GetNamesFromIDs(
  LPSPropTagArray FAR * lppPropTags,
  LPGUID lpPropSetGuid,
  ULONG ulFlags,
  ULONG FAR * lpcPropNames,
  LPMAPINAMEID FAR * FAR * lpppPropNames
);
```

## <a name="parameters"></a><span data-ttu-id="fd079-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="fd079-106">Parameters</span></span>

 <span data-ttu-id="fd079-107">_lppPropTags_</span><span class="sxs-lookup"><span data-stu-id="fd079-107">_lppPropTags_</span></span>
  
> <span data-ttu-id="fd079-108">[in, out] Lors de l’entrée, un pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété ; Sinon, NULL, indiquant que tous les noms doivent être renvoyés.</span><span class="sxs-lookup"><span data-stu-id="fd079-108">[in, out] On input, a pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags; otherwise, NULL, indicating that all names should be returned.</span></span> <span data-ttu-id="fd079-109">Le **membre cValues** du tableau de balises de propriétés ne peut pas être 0.</span><span class="sxs-lookup"><span data-stu-id="fd079-109">The **cValues** member for the property tag array cannot be 0.</span></span> <span data-ttu-id="fd079-110">Si  _lppPropTags est_ un pointeur valide lors de l’entrée, **GetNamesFromIDs** renvoie les noms de chaque identificateur de propriété inclus dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="fd079-110">If  _lppPropTags_ is a valid pointer on input, **GetNamesFromIDs** returns names for each property identifier included in the array.</span></span> 
    
 <span data-ttu-id="fd079-111">_lpPropSetGuid_</span><span class="sxs-lookup"><span data-stu-id="fd079-111">_lpPropSetGuid_</span></span>
  
> <span data-ttu-id="fd079-112">[in] Pointeur vers un GUID ou une structure [GUID](guid.md) qui identifie un jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="fd079-112">[in] A pointer to a GUID, or [GUID](guid.md) structure, that identifies a property set.</span></span> <span data-ttu-id="fd079-113">Le  _paramètre lpPropSetGuid_ peut pointer vers un jeu de propriétés valide ou peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="fd079-113">The  _lpPropSetGuid_ parameter can point to a valid property set or can be NULL.</span></span> 
    
 <span data-ttu-id="fd079-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fd079-114">_ulFlags_</span></span>
  
> <span data-ttu-id="fd079-115">[in] Masque de bits d’indicateurs qui indique le type de noms à retourner.</span><span class="sxs-lookup"><span data-stu-id="fd079-115">[in] A bitmask of flags that indicates the type of names to be returned.</span></span> <span data-ttu-id="fd079-116">Les indicateurs suivants peuvent être utilisés (si les deux indicateurs sont définies, aucun nom ne sera renvoyé) :</span><span class="sxs-lookup"><span data-stu-id="fd079-116">The following flags can be used (if both flags are set, no names will be returned):</span></span>
    
<span data-ttu-id="fd079-117">MAPI_NO_IDS</span><span class="sxs-lookup"><span data-stu-id="fd079-117">MAPI_NO_IDS</span></span> 
  
> <span data-ttu-id="fd079-118">Demande que seuls les noms stockés en tant que chaînes Unicode soient renvoyés.</span><span class="sxs-lookup"><span data-stu-id="fd079-118">Requests that only names stored as Unicode strings be returned.</span></span> 
    
<span data-ttu-id="fd079-119">MAPI_NO_STRINGS</span><span class="sxs-lookup"><span data-stu-id="fd079-119">MAPI_NO_STRINGS</span></span> 
  
> <span data-ttu-id="fd079-120">Demande que seuls les noms stockés en tant qu’identificateurs numériques soient renvoyés.</span><span class="sxs-lookup"><span data-stu-id="fd079-120">Requests that only names stored as numeric identifiers be returned.</span></span> 
    
 <span data-ttu-id="fd079-121">_lpcPropNames_</span><span class="sxs-lookup"><span data-stu-id="fd079-121">_lpcPropNames_</span></span>
  
> <span data-ttu-id="fd079-122">[out] Pointeur vers un nombre de pointeurs de nom de propriété dans le tableau pointé par _le paramètre lppPropNames._</span><span class="sxs-lookup"><span data-stu-id="fd079-122">[out] A pointer to a count of the property name pointers in the array pointed to by the  _lppPropNames_ parameter.</span></span> 
    
 <span data-ttu-id="fd079-123">_lpppPropNames_</span><span class="sxs-lookup"><span data-stu-id="fd079-123">_lpppPropNames_</span></span>
  
> <span data-ttu-id="fd079-124">[out] Pointeur vers un tableau de pointeurs vers des structures [MAPINAMEID](mapinameid.md) qui contiennent des noms de propriétés.</span><span class="sxs-lookup"><span data-stu-id="fd079-124">[out] A pointer to an array of pointers to [MAPINAMEID](mapinameid.md) structures that contains property names.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fd079-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fd079-125">Return value</span></span>

<span data-ttu-id="fd079-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="fd079-126">S_OK</span></span> 
  
> <span data-ttu-id="fd079-127">Les noms des propriétés ont été renvoyés avec succès.</span><span class="sxs-lookup"><span data-stu-id="fd079-127">The property names were successfully returned.</span></span> 
    
<span data-ttu-id="fd079-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="fd079-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="fd079-129">L’objet ne prend pas en charge les propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="fd079-129">The object does not support named properties.</span></span> 
    
<span data-ttu-id="fd079-130">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="fd079-130">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="fd079-131">L’appel a réussi globalement, mais les noms d’une ou plusieurs propriétés n’ont pas pu être renvoyés.</span><span class="sxs-lookup"><span data-stu-id="fd079-131">The call succeeded overall, but names for one or more properties could not be returned.</span></span> <span data-ttu-id="fd079-132">Les balises de propriété pour les propriétés défaillantes ont un type de propriété **PT_ERROR**.</span><span class="sxs-lookup"><span data-stu-id="fd079-132">The property tags for the failing properties have a property type of **PT_ERROR**.</span></span> <span data-ttu-id="fd079-133">Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi.</span><span class="sxs-lookup"><span data-stu-id="fd079-133">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="fd079-134">Pour tester cet avertissement, utilisez la macro **HR_FAILED.**</span><span class="sxs-lookup"><span data-stu-id="fd079-134">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="fd079-135">Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="fd079-135">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> 
    
<span data-ttu-id="fd079-136">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fd079-136">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="fd079-137">Le **membre cValues** d’une ou plusieurs des entrées du tableau de balises de propriétés pointées par  _lppPropTags_ est définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="fd079-137">The **cValues** member of one or more of the entries in the property tag array pointed to by  _lppPropTags_ is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fd079-138">Remarques</span><span class="sxs-lookup"><span data-stu-id="fd079-138">Remarks</span></span>

<span data-ttu-id="fd079-139">Bien que l’accès à la plupart des propriétés se fait par identificateur de propriété, certaines propriétés sont accessibles par nom.</span><span class="sxs-lookup"><span data-stu-id="fd079-139">While access to most properties is by property identifier, some properties can be accessed by name.</span></span> <span data-ttu-id="fd079-140">La **méthode IMAPIProp::GetNamesFromIDs** peut être appelée pour :</span><span class="sxs-lookup"><span data-stu-id="fd079-140">The **IMAPIProp::GetNamesFromIDs** method can be called to do the following:</span></span> 
  
- <span data-ttu-id="fd079-141">Récupérer les noms des identificateurs de propriété spécifiques dans un jeu de propriétés spécifique.</span><span class="sxs-lookup"><span data-stu-id="fd079-141">Retrieve names for specific property identifiers in a specific property set.</span></span>
    
- <span data-ttu-id="fd079-142">Récupérer des noms pour des identificateurs de propriété spécifiques dans n’importe quel jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="fd079-142">Retrieve names for specific property identifiers in any property set.</span></span>
    
- <span data-ttu-id="fd079-143">Récupérer les noms de toutes les propriétés nommées incluses dans le mappage de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fd079-143">Retrieve names for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="fd079-144">Si  _lppPropTags_ pointe vers un tableau de balises de propriétés valide avec un ou plusieurs identificateurs de propriété et  _que lpPropSetGuid_ pointe vers un jeu de propriétés valide, **GetNamesFromIDs** ignore le jeu de propriétés et les types de propriétés et renvoie tous les noms qui sont mappés aux identificateurs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="fd079-144">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers, and  _lpPropSetGuid_ points to a valid property set, **GetNamesFromIDs** ignores the property set and the property types and returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="fd079-145">Si  _lppPropTags_ pointe vers un tableau de balises de propriétés valide avec un ou plusieurs identificateurs de propriété et  _que lpPropSetGuid_ a la valeur NULL, **GetNamesFromIDs** renvoie tous les noms mappés aux identificateurs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="fd079-145">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers and  _lpPropSetGuid_ is NULL, **GetNamesFromIDs** returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="fd079-146">Si un identificateur spécifié n’a pas de nom, **GetNamesFromIDs** renvoie la valeur NULL à la place de cet identificateur dans la structure renvoyée dans  _lpppPropNames_ et renvoie également MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="fd079-146">If a specified identifier does not have a name, **GetNamesFromIDs** returns NULL in that identifier's place in the structure returned in  _lpppPropNames_ and also returns MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="fd079-147">Si  _lpPropSetGuid_ et  _lppPropTags_ ont la valeur NULL, **GetNamesFromIDs** alloue un nouveau tableau de balises de propriétés et renvoie tous les noms de toutes les propriétés nommées de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fd079-147">If both  _lpPropSetGuid_ and  _lppPropTags_ are NULL, **GetNamesFromIDs** allocates a new property tag array and returns all of the names for all of the named properties for the object.</span></span> 
  
<span data-ttu-id="fd079-148">Lorsqu’il n’y a aucun nom à retourner, peut-être parce qu’il n’y a aucune propriété dans le jeu de propriétés demandé ou que toutes les propriétés sont d’un type exclu par les indicateurs, **GetNamesFromIDs** :</span><span class="sxs-lookup"><span data-stu-id="fd079-148">When there are no names to be returned, perhaps because there are no properties in the requested property set or all of the properties are of a type excluded by the flags, **GetNamesFromIDs** does the following:</span></span> 
  
- <span data-ttu-id="fd079-149">Renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="fd079-149">Returns S_OK.</span></span>
    
- <span data-ttu-id="fd079-150">Alloue une nouvelle structure **SPropTagArray,** en fixant le membre **cValues** sur 0.</span><span class="sxs-lookup"><span data-stu-id="fd079-150">Allocates a new **SPropTagArray** structure, setting the **cValues** member to 0.</span></span> 
    
- <span data-ttu-id="fd079-151">Définit le contenu de  _lpcPropNames_ sur 0.</span><span class="sxs-lookup"><span data-stu-id="fd079-151">Sets the contents of  _lpcPropNames_ to 0.</span></span> 
    
- <span data-ttu-id="fd079-152">Définit le contenu de  _lpppPropNames_ sur NULL.</span><span class="sxs-lookup"><span data-stu-id="fd079-152">Sets the contents of  _lpppPropNames_ to NULL.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="fd079-153">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="fd079-153">Notes to implementers</span></span>

<span data-ttu-id="fd079-154">Si  _lpPropSetGuid_ pointe vers un jeu de propriétés valide et  _que lppPropTags_ est NULL, le résultat n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="fd079-154">If  _lpPropSetGuid_ points to a valid property set and  _lppPropTags_ is NULL, the result is undefined.</span></span> <span data-ttu-id="fd079-155">Vous pouvez utiliser l’une des stratégies suivantes :</span><span class="sxs-lookup"><span data-stu-id="fd079-155">You can use one of the following strategies:</span></span> 
  
- <span data-ttu-id="fd079-156">Ignorez le jeu de propriétés et renvoyer les noms des identificateurs dans le tableau de balises de propriétés.</span><span class="sxs-lookup"><span data-stu-id="fd079-156">Ignore the property set and return the names for the identifiers in the property tag array.</span></span>
    
- <span data-ttu-id="fd079-157">Renvoyer les noms des identificateurs du tableau de balises de propriétés qui appartiennent au jeu de propriétés spécifié.</span><span class="sxs-lookup"><span data-stu-id="fd079-157">Return the names for only the identifiers in the property tag array that belong to the specified property set.</span></span>
    
- <span data-ttu-id="fd079-158">Échec de l’appel, renvoyant MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="fd079-158">Fail the call, returning MAPI_E_INVALID_PARAMETER.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="fd079-159">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="fd079-159">Notes to callers</span></span>

<span data-ttu-id="fd079-160">Pour récupérer toutes les propriétés nommées d’un objet, vous devez d’abord appeler la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) de l’objet, puis transmettre les identificateurs renvoyés au-dessus de la plage 0x8000 à **GetNamesFromIDs**.</span><span class="sxs-lookup"><span data-stu-id="fd079-160">To retrieve all of the named properties for an object, you must first call the object's [IMAPIProp::GetPropList](imapiprop-getproplist.md) method and then pass the returned identifiers that are above the 0x8000 range to **GetNamesFromIDs**.</span></span>
  
<span data-ttu-id="fd079-161">Si vous passez un jeu de propriétés valide mais pas un tableau de balises de propriétés valide, soyez préparé pour des résultats imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="fd079-161">If you pass a valid property set but not a valid property tag array, be prepared for unpredictable results.</span></span> <span data-ttu-id="fd079-162">Certaines implémentations **de GetNamesFromIDs** ignorent le jeu de propriétés et retournent les noms des identificateurs dans le tableau de balises de propriétés.</span><span class="sxs-lookup"><span data-stu-id="fd079-162">Some implementations of **GetNamesFromIDs** ignore the property set and return the names for the identifiers in the property tag array.</span></span> <span data-ttu-id="fd079-163">Certaines implémentations retournent des MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="fd079-163">Some implementations return MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="fd079-164">D’autres implémentations retournent des noms pour les identificateurs de toutes les propriétés du jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="fd079-164">Still other implementations return names for identifiers of all properties in the property set.</span></span> <span data-ttu-id="fd079-165">Si le jeu de propriétés PS_PUBLIC_STRINGS, **GetNamesFromIDs** peut renvoyer tous les noms qui ont été créés.</span><span class="sxs-lookup"><span data-stu-id="fd079-165">If the property set is PS_PUBLIC_STRINGS, **GetNamesFromIDs** can return all names that were ever created.</span></span> <span data-ttu-id="fd079-166">Le fait que le fournisseur de services stocke une propriété sous les identificateurs associés aux chaînes publiques est immérial.</span><span class="sxs-lookup"><span data-stu-id="fd079-166">Whether the service provider stores a property under the identifiers associated with the public strings is immaterial.</span></span> 
  
<span data-ttu-id="fd079-167">Lorsque vous avez terminé avec les noms des propriétés, vérifiez le contenu du paramètre  _lpcPropNames_ pour déterminer si des noms ont été renvoyés.</span><span class="sxs-lookup"><span data-stu-id="fd079-167">When you are finished with the property names, check the contents of the  _lpcPropNames_ parameter to determine whether any names were returned.</span></span> <span data-ttu-id="fd079-168">Si c’est le cas, appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer la mémoire pointée par  _lppPropTags_ et  _lpppPropNames_ lorsqu’un résultat réussi est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="fd079-168">If so, call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory pointed to by  _lppPropTags_ and  _lpppPropNames_ when a successful result is returned.</span></span> <span data-ttu-id="fd079-169">Un appel à **MAPIFreeBuffer est** suffisant pour chaque paramètre ; vous n’avez pas besoin de parcourir le tableau de pointeurs et de libérer chaque structure **MAPINAMEID** individuellement.</span><span class="sxs-lookup"><span data-stu-id="fd079-169">One call to **MAPIFreeBuffer** is sufficient for each parameter; you do not have to traverse the array of pointers and free each **MAPINAMEID** structure individually.</span></span> 
  
<span data-ttu-id="fd079-170">Pour plus d’informations sur les propriétés nommées, voir [MAPI Named Properties](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="fd079-170">For more information about named properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fd079-171">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="fd079-171">MFCMAPI reference</span></span>

<span data-ttu-id="fd079-172">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fd079-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fd079-173">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="fd079-173">**File**</span></span>|<span data-ttu-id="fd079-174">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="fd079-174">**Function**</span></span>|<span data-ttu-id="fd079-175">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="fd079-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fd079-176">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="fd079-176">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="fd079-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span><span class="sxs-lookup"><span data-stu-id="fd079-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span></span>  <br/> |<span data-ttu-id="fd079-178">MFCMAPI utilise la méthode **IMAPIProp::GetNamesFromIDs** pour rechercher les propriétés nommées qui ont été précédemment mappées.</span><span class="sxs-lookup"><span data-stu-id="fd079-178">MFCMAPI uses the **IMAPIProp::GetNamesFromIDs** method to look up named properties that have previously been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fd079-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd079-179">See also</span></span>



[<span data-ttu-id="fd079-180">GUID</span><span class="sxs-lookup"><span data-stu-id="fd079-180">GUID</span></span>](guid.md)
  
[<span data-ttu-id="fd079-181">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="fd079-181">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)
  
[<span data-ttu-id="fd079-182">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="fd079-182">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="fd079-183">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="fd079-183">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="fd079-184">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="fd079-184">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="fd079-185">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="fd079-185">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="fd079-186">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fd079-186">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="fd079-187">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="fd079-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="fd079-188">MAPI des propri�t�s nomm�e</span><span class="sxs-lookup"><span data-stu-id="fd079-188">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="fd079-189">Utilisation de macros pour la gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="fd079-189">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

