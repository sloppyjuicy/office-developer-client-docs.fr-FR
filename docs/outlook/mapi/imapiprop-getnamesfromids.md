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
ms.openlocfilehash: 186afd6a80d0ae3ae0a767456e60b2ebaaa579b9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574383"
---
# <a name="imapipropgetnamesfromids"></a><span data-ttu-id="98ef5-103">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="98ef5-103">IMAPIProp::GetNamesFromIDs</span></span>

  
  
<span data-ttu-id="98ef5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98ef5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98ef5-105">Fournit les noms des propriétés qui correspondent à un ou plusieurs identificateurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="98ef5-105">Provides the property names that correspond to one or more property identifiers.</span></span>
  
```cpp
HRESULT GetNamesFromIDs(
  LPSPropTagArray FAR * lppPropTags,
  LPGUID lpPropSetGuid,
  ULONG ulFlags,
  ULONG FAR * lpcPropNames,
  LPMAPINAMEID FAR * FAR * lpppPropNames
);
```

## <a name="parameters"></a><span data-ttu-id="98ef5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98ef5-106">Parameters</span></span>

 <span data-ttu-id="98ef5-107">_lppPropTags_</span><span class="sxs-lookup"><span data-stu-id="98ef5-107">_lppPropTags_</span></span>
  
> <span data-ttu-id="98ef5-108">[entrée, sortie] À l’entrée, un pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété ; dans le cas contraire, la valeur NULL, indiquant que tous les noms doivent être retournées.</span><span class="sxs-lookup"><span data-stu-id="98ef5-108">[in, out] On input, a pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags; otherwise, NULL, indicating that all names should be returned.</span></span> <span data-ttu-id="98ef5-109">Le membre **cValues** pour le tableau de balise de propriété ne peut pas être 0.</span><span class="sxs-lookup"><span data-stu-id="98ef5-109">The **cValues** member for the property tag array cannot be 0.</span></span> <span data-ttu-id="98ef5-110">Si _lppPropTags_ est un pointeur valid en entrée, **GetNamesFromIDs** renvoie les noms pour chaque identificateur de la propriété incluse dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="98ef5-110">If  _lppPropTags_ is a valid pointer on input, **GetNamesFromIDs** returns names for each property identifier included in the array.</span></span> 
    
 <span data-ttu-id="98ef5-111">_lpPropSetGuid_</span><span class="sxs-lookup"><span data-stu-id="98ef5-111">_lpPropSetGuid_</span></span>
  
> <span data-ttu-id="98ef5-112">[in] Un pointeur vers un GUID ou le [GUID](guid.md) structure, qui identifie un jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="98ef5-112">[in] A pointer to a GUID, or [GUID](guid.md) structure, that identifies a property set.</span></span> <span data-ttu-id="98ef5-113">Le paramètre _lpPropSetGuid_ peut pointer vers un jeu de propriétés valide ou peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="98ef5-113">The  _lpPropSetGuid_ parameter can point to a valid property set or can be NULL.</span></span> 
    
 <span data-ttu-id="98ef5-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="98ef5-114">_ulFlags_</span></span>
  
> <span data-ttu-id="98ef5-115">[in] Masque de bits d’indicateurs qui indique le type de noms à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="98ef5-115">[in] A bitmask of flags that indicates the type of names to be returned.</span></span> <span data-ttu-id="98ef5-116">Les indicateurs suivants peuvent être utilisés (si les deux indicateurs sont définis, aucun nom n’est retournées) :</span><span class="sxs-lookup"><span data-stu-id="98ef5-116">The following flags can be used (if both flags are set, no names will be returned):</span></span>
    
<span data-ttu-id="98ef5-117">MAPI_NO_IDS</span><span class="sxs-lookup"><span data-stu-id="98ef5-117">MAPI_NO_IDS</span></span> 
  
> <span data-ttu-id="98ef5-118">Demandes de renvoyer uniquement les noms stockés en tant que chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="98ef5-118">Requests that only names stored as Unicode strings be returned.</span></span> 
    
<span data-ttu-id="98ef5-119">MAPI_NO_STRINGS</span><span class="sxs-lookup"><span data-stu-id="98ef5-119">MAPI_NO_STRINGS</span></span> 
  
> <span data-ttu-id="98ef5-120">Demandes de renvoyer uniquement les noms enregistrés comme des identificateurs numériques.</span><span class="sxs-lookup"><span data-stu-id="98ef5-120">Requests that only names stored as numeric identifiers be returned.</span></span> 
    
 <span data-ttu-id="98ef5-121">_lpcPropNames_</span><span class="sxs-lookup"><span data-stu-id="98ef5-121">_lpcPropNames_</span></span>
  
> <span data-ttu-id="98ef5-122">[out] Un pointeur vers un décompte des pointeurs de nom de propriété dans le tableau indiqué par le paramètre _lppPropNames_ .</span><span class="sxs-lookup"><span data-stu-id="98ef5-122">[out] A pointer to a count of the property name pointers in the array pointed to by the  _lppPropNames_ parameter.</span></span> 
    
 <span data-ttu-id="98ef5-123">_lpppPropNames_</span><span class="sxs-lookup"><span data-stu-id="98ef5-123">_lpppPropNames_</span></span>
  
> <span data-ttu-id="98ef5-124">[out] Pointeur vers un tableau de pointeurs vers des structures [MAPINAMEID](mapinameid.md) qui contient les noms de propriété.</span><span class="sxs-lookup"><span data-stu-id="98ef5-124">[out] A pointer to an array of pointers to [MAPINAMEID](mapinameid.md) structures that contains property names.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="98ef5-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="98ef5-125">Return value</span></span>

<span data-ttu-id="98ef5-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="98ef5-126">S_OK</span></span> 
  
> <span data-ttu-id="98ef5-127">Les noms de propriété ont été renvoyées avec succès.</span><span class="sxs-lookup"><span data-stu-id="98ef5-127">The property names were successfully returned.</span></span> 
    
<span data-ttu-id="98ef5-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="98ef5-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="98ef5-129">L’objet ne gère pas les propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="98ef5-129">The object does not support named properties.</span></span> 
    
<span data-ttu-id="98ef5-130">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="98ef5-130">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="98ef5-131">L’appel a réussi, mais les noms pour une ou plusieurs propriétés n’a pas peuvent être retournés.</span><span class="sxs-lookup"><span data-stu-id="98ef5-131">The call succeeded overall, but names for one or more properties could not be returned.</span></span> <span data-ttu-id="98ef5-132">Les balises de propriété pour les propriétés défectueux ont un type de propriété de **PT_ERROR**.</span><span class="sxs-lookup"><span data-stu-id="98ef5-132">The property tags for the failing properties have a property type of **PT_ERROR**.</span></span> <span data-ttu-id="98ef5-133">Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi.</span><span class="sxs-lookup"><span data-stu-id="98ef5-133">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="98ef5-134">Pour tester cet avertissement, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="98ef5-134">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="98ef5-135">Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="98ef5-135">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> 
    
<span data-ttu-id="98ef5-136">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="98ef5-136">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="98ef5-137">Membre d’une ou plusieurs des entrées du tableau de la propriété tag désignés par _lppPropTags_ **cValues** est défini sur 0.</span><span class="sxs-lookup"><span data-stu-id="98ef5-137">The **cValues** member of one or more of the entries in the property tag array pointed to by  _lppPropTags_ is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="98ef5-138">Remarques</span><span class="sxs-lookup"><span data-stu-id="98ef5-138">Remarks</span></span>

<span data-ttu-id="98ef5-139">Accès à la plupart des propriétés est par identificateur de la propriété, certaines propriétés accessibles par un nom.</span><span class="sxs-lookup"><span data-stu-id="98ef5-139">While access to most properties is by property identifier, some properties can be accessed by name.</span></span> <span data-ttu-id="98ef5-140">La méthode **IMAPIProp::GetNamesFromIDs** peut être appelée pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="98ef5-140">The **IMAPIProp::GetNamesFromIDs** method can be called to do the following:</span></span> 
  
- <span data-ttu-id="98ef5-141">Récupérer les noms des identificateurs de propriété spécifique dans un jeu de propriétés spécifique.</span><span class="sxs-lookup"><span data-stu-id="98ef5-141">Retrieve names for specific property identifiers in a specific property set.</span></span>
    
- <span data-ttu-id="98ef5-142">Récupérer les noms des identificateurs de propriété spécifique dans n’importe quel jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="98ef5-142">Retrieve names for specific property identifiers in any property set.</span></span>
    
- <span data-ttu-id="98ef5-143">Récupérer les noms de toutes les propriétés nommées qui sont incluses dans le mappage de l’objet.</span><span class="sxs-lookup"><span data-stu-id="98ef5-143">Retrieve names for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="98ef5-144">Si la valeur _lppPropTags_ points dans un tableau de balise de propriété valide avec un ou plusieurs identificateurs de propriété et _lpPropSetGuid_ sur une propriété valide, **GetNamesFromIDs** ignore le jeu de propriétés et les types de propriétés et renvoie tous les noms qui correspondent aux identificateurs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="98ef5-144">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers, and  _lpPropSetGuid_ points to a valid property set, **GetNamesFromIDs** ignores the property set and the property types and returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="98ef5-145">Si _lppPropTags_ pointe vers un tableau de balise de propriété valide avec un ou plusieurs identificateurs de propriété et _lpPropSetGuid_ est NULL, **GetNamesFromIDs** renvoie tous les noms qui correspondent aux identificateurs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="98ef5-145">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers and  _lpPropSetGuid_ is NULL, **GetNamesFromIDs** returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="98ef5-146">Si un identificateur spécifié ne dispose pas d’un nom, **GetNamesFromIDs** renvoie la valeur NULL en place de cet identificateur dans la structure retournée dans _lpppPropNames_ et retourne également MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="98ef5-146">If a specified identifier does not have a name, **GetNamesFromIDs** returns NULL in that identifier's place in the structure returned in  _lpppPropNames_ and also returns MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="98ef5-147">Si _lpPropSetGuid_ et _lppPropTags_ sont NULL, **GetNamesFromIDs** alloue un nouveau tableau de balise de propriété et retourne tous les noms de toutes les propriétés de l’objet nommées.</span><span class="sxs-lookup"><span data-stu-id="98ef5-147">If both  _lpPropSetGuid_ and  _lppPropTags_ are NULL, **GetNamesFromIDs** allocates a new property tag array and returns all of the names for all of the named properties for the object.</span></span> 
  
<span data-ttu-id="98ef5-148">Lorsqu’il n’y a aucun nom à renvoyer, par exemple, car il n’existe aucune propriété dans le jeu de propriétés demandé ou toutes les propriétés sont de type exclu par le paramètre flags, **GetNamesFromIDs** effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="98ef5-148">When there are no names to be returned, perhaps because there are no properties in the requested property set or all of the properties are of a type excluded by the flags, **GetNamesFromIDs** does the following:</span></span> 
  
- <span data-ttu-id="98ef5-149">Renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="98ef5-149">Returns S_OK.</span></span>
    
- <span data-ttu-id="98ef5-150">Affecte une nouvelle structure **SPropTagArray** , définissant le membre **cValues** sur 0.</span><span class="sxs-lookup"><span data-stu-id="98ef5-150">Allocates a new **SPropTagArray** structure, setting the **cValues** member to 0.</span></span> 
    
- <span data-ttu-id="98ef5-151">Définit le contenu de _lpcPropNames_ à 0.</span><span class="sxs-lookup"><span data-stu-id="98ef5-151">Sets the contents of  _lpcPropNames_ to 0.</span></span> 
    
- <span data-ttu-id="98ef5-152">Définit le contenu de _lpppPropNames_ sur NULL.</span><span class="sxs-lookup"><span data-stu-id="98ef5-152">Sets the contents of  _lpppPropNames_ to NULL.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="98ef5-153">Remarques à l’attention des responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="98ef5-153">Notes to implementers</span></span>

<span data-ttu-id="98ef5-154">Si _lpPropSetGuid_ points à un jeu de propriétés valide et un _lppPropTags_ est NULL, le résultat est indéfini.</span><span class="sxs-lookup"><span data-stu-id="98ef5-154">If  _lpPropSetGuid_ points to a valid property set and  _lppPropTags_ is NULL, the result is undefined.</span></span> <span data-ttu-id="98ef5-155">Vous pouvez utiliser une des stratégies suivantes :</span><span class="sxs-lookup"><span data-stu-id="98ef5-155">You can use one of the following strategies:</span></span> 
  
- <span data-ttu-id="98ef5-156">Ignorer le jeu de propriétés et renvoyer les noms pour les identificateurs de tableau de la propriété tag.</span><span class="sxs-lookup"><span data-stu-id="98ef5-156">Ignore the property set and return the names for the identifiers in the property tag array.</span></span>
    
- <span data-ttu-id="98ef5-157">Renvoyer les noms pour seulement les identificateurs de tableau de la propriété tag qui appartiennent au jeu de propriétés spécifié.</span><span class="sxs-lookup"><span data-stu-id="98ef5-157">Return the names for only the identifiers in the property tag array that belong to the specified property set.</span></span>
    
- <span data-ttu-id="98ef5-158">Échec de l’appel, renvoi MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="98ef5-158">Fail the call, returning MAPI_E_INVALID_PARAMETER.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="98ef5-159">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="98ef5-159">Notes to callers</span></span>

<span data-ttu-id="98ef5-160">Pour récupérer toutes les propriétés d’un objet nommées, vous devez d’abord appeler la méthode l’objet [IMAPIProp::GetPropList](imapiprop-getproplist.md) et puis passer les identificateurs au-dessus de la plage 0 x 8000 à **GetNamesFromIDs**renvoyées.</span><span class="sxs-lookup"><span data-stu-id="98ef5-160">To retrieve all of the named properties for an object, you must first call the object's [IMAPIProp::GetPropList](imapiprop-getproplist.md) method and then pass the returned identifiers that are above the 0x8000 range to **GetNamesFromIDs**.</span></span>
  
<span data-ttu-id="98ef5-161">Si vous passez d’un jeu de propriétés valide, mais pas un tableau de balise de propriété valide, être préparé pour des résultats imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="98ef5-161">If you pass a valid property set but not a valid property tag array, be prepared for unpredictable results.</span></span> <span data-ttu-id="98ef5-162">Certaines implémentations de **GetNamesFromIDs** ignorer le jeu de propriétés et renvoyer les noms pour les identificateurs de tableau de la propriété tag.</span><span class="sxs-lookup"><span data-stu-id="98ef5-162">Some implementations of **GetNamesFromIDs** ignore the property set and return the names for the identifiers in the property tag array.</span></span> <span data-ttu-id="98ef5-163">Certaines implémentations retourner MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="98ef5-163">Some implementations return MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="98ef5-164">Toujours implémentations renvoient des noms pour les identificateurs de toutes les propriétés dans le jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="98ef5-164">Still other implementations return names for identifiers of all properties in the property set.</span></span> <span data-ttu-id="98ef5-165">Si le jeu de propriétés est PS_PUBLIC_STRINGS, **GetNamesFromIDs** peut renvoyer tous les noms qui ont été créées jamais.</span><span class="sxs-lookup"><span data-stu-id="98ef5-165">If the property set is PS_PUBLIC_STRINGS, **GetNamesFromIDs** can return all names that were ever created.</span></span> <span data-ttu-id="98ef5-166">Si le fournisseur de services stocke une propriété sous les identificateurs de chaînes publics est indifférent.</span><span class="sxs-lookup"><span data-stu-id="98ef5-166">Whether the service provider stores a property under the identifiers associated with the public strings is immaterial.</span></span> 
  
<span data-ttu-id="98ef5-167">Lorsque vous avez terminé avec les noms de propriété, vérifiez le contenu du paramètre _lpcPropNames_ pour déterminer si des noms ont été retournés.</span><span class="sxs-lookup"><span data-stu-id="98ef5-167">When you are finished with the property names, check the contents of the  _lpcPropNames_ parameter to determine whether any names were returned.</span></span> <span data-ttu-id="98ef5-168">Dans ce cas, appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer de la mémoire vers lequel pointée _lppPropTags_ et _lpppPropNames_ lorsqu’un résultat réussi est retourné.</span><span class="sxs-lookup"><span data-stu-id="98ef5-168">If so, call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory pointed to by  _lppPropTags_ and  _lpppPropNames_ when a successful result is returned.</span></span> <span data-ttu-id="98ef5-169">Un appel à **MAPIFreeBuffer** est suffisant pour chaque paramètre ; Il est inutile de parcourir le tableau des pointeurs et de libérer chaque structure **MAPINAMEID** individuellement.</span><span class="sxs-lookup"><span data-stu-id="98ef5-169">One call to **MAPIFreeBuffer** is sufficient for each parameter; you do not have to traverse the array of pointers and free each **MAPINAMEID** structure individually.</span></span> 
  
<span data-ttu-id="98ef5-170">Pour plus d’informations sur les propriétés nommées, voir [Les propriétés MAPI nommée](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="98ef5-170">For more information about named properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="98ef5-171">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="98ef5-171">MFCMAPI reference</span></span>

<span data-ttu-id="98ef5-172">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="98ef5-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="98ef5-173">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="98ef5-173">**File**</span></span>|<span data-ttu-id="98ef5-174">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="98ef5-174">**Function**</span></span>|<span data-ttu-id="98ef5-175">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="98ef5-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="98ef5-176">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="98ef5-176">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="98ef5-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span><span class="sxs-lookup"><span data-stu-id="98ef5-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span></span>  <br/> |<span data-ttu-id="98ef5-178">MFCMAPI utilise la méthode **IMAPIProp::GetNamesFromIDs** pour rechercher des propriétés nommées qui ont déjà été mappées.</span><span class="sxs-lookup"><span data-stu-id="98ef5-178">MFCMAPI uses the **IMAPIProp::GetNamesFromIDs** method to look up named properties that have previously been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="98ef5-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98ef5-179">See also</span></span>



[<span data-ttu-id="98ef5-180">GUID</span><span class="sxs-lookup"><span data-stu-id="98ef5-180">GUID</span></span>](guid.md)
  
[<span data-ttu-id="98ef5-181">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="98ef5-181">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)
  
[<span data-ttu-id="98ef5-182">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="98ef5-182">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="98ef5-183">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="98ef5-183">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="98ef5-184">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="98ef5-184">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="98ef5-185">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="98ef5-185">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="98ef5-186">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="98ef5-186">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="98ef5-187">MFCMAPI en tant qu’exemple de code</span><span class="sxs-lookup"><span data-stu-id="98ef5-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="98ef5-188">MAPI des propri�t�s nomm�e</span><span class="sxs-lookup"><span data-stu-id="98ef5-188">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="98ef5-189">Utilisation de Macros pour la gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="98ef5-189">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

