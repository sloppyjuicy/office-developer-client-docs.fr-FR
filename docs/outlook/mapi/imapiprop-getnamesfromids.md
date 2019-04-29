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
# <a name="imapipropgetnamesfromids"></a><span data-ttu-id="b061d-103">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="b061d-103">IMAPIProp::GetNamesFromIDs</span></span>

  
  
<span data-ttu-id="b061d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b061d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b061d-105">Fournit les noms de propriétés qui correspondent à un ou plusieurs identificateurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="b061d-105">Provides the property names that correspond to one or more property identifiers.</span></span>
  
```cpp
HRESULT GetNamesFromIDs(
  LPSPropTagArray FAR * lppPropTags,
  LPGUID lpPropSetGuid,
  ULONG ulFlags,
  ULONG FAR * lpcPropNames,
  LPMAPINAMEID FAR * FAR * lpppPropNames
);
```

## <a name="parameters"></a><span data-ttu-id="b061d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b061d-106">Parameters</span></span>

 <span data-ttu-id="b061d-107">_lppPropTags_</span><span class="sxs-lookup"><span data-stu-id="b061d-107">_lppPropTags_</span></span>
  
> <span data-ttu-id="b061d-108">[in, out] Lors de l'entrée, pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété; Sinon, NULL, ce qui indique que tous les noms doivent être renvoyés.</span><span class="sxs-lookup"><span data-stu-id="b061d-108">[in, out] On input, a pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags; otherwise, NULL, indicating that all names should be returned.</span></span> <span data-ttu-id="b061d-109">Le membre **cValues** pour le tableau de la balise de propriété ne peut pas être 0.</span><span class="sxs-lookup"><span data-stu-id="b061d-109">The **cValues** member for the property tag array cannot be 0.</span></span> <span data-ttu-id="b061d-110">Si _lppPropTags_ est un pointeur valide sur l'entrée, **GetNamesFromIDs** renvoie les noms de chaque identificateur de propriété inclus dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="b061d-110">If  _lppPropTags_ is a valid pointer on input, **GetNamesFromIDs** returns names for each property identifier included in the array.</span></span> 
    
 <span data-ttu-id="b061d-111">_lpPropSetGuid_</span><span class="sxs-lookup"><span data-stu-id="b061d-111">_lpPropSetGuid_</span></span>
  
> <span data-ttu-id="b061d-112">dans Pointeur vers un GUID, ou une structure de [GUID](guid.md) , qui identifie un jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="b061d-112">[in] A pointer to a GUID, or [GUID](guid.md) structure, that identifies a property set.</span></span> <span data-ttu-id="b061d-113">Le paramètre _lpPropSetGuid_ peut pointer vers un jeu de propriétés valide ou peut être null.</span><span class="sxs-lookup"><span data-stu-id="b061d-113">The  _lpPropSetGuid_ parameter can point to a valid property set or can be NULL.</span></span> 
    
 <span data-ttu-id="b061d-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b061d-114">_ulFlags_</span></span>
  
> <span data-ttu-id="b061d-115">dans Masque de des indicateurs qui indique le type de nom à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="b061d-115">[in] A bitmask of flags that indicates the type of names to be returned.</span></span> <span data-ttu-id="b061d-116">Les indicateurs suivants peuvent être utilisés (si les deux indicateurs sont définis, aucun nom n'est renvoyé):</span><span class="sxs-lookup"><span data-stu-id="b061d-116">The following flags can be used (if both flags are set, no names will be returned):</span></span>
    
<span data-ttu-id="b061d-117">MAPI_NO_IDS</span><span class="sxs-lookup"><span data-stu-id="b061d-117">MAPI_NO_IDS</span></span> 
  
> <span data-ttu-id="b061d-118">Demande que seuls les noms stockés sous forme de chaînes Unicode soient renvoyés.</span><span class="sxs-lookup"><span data-stu-id="b061d-118">Requests that only names stored as Unicode strings be returned.</span></span> 
    
<span data-ttu-id="b061d-119">MAPI_NO_STRINGS</span><span class="sxs-lookup"><span data-stu-id="b061d-119">MAPI_NO_STRINGS</span></span> 
  
> <span data-ttu-id="b061d-120">Demande que seuls les noms stockés en tant qu'identificateurs numériques soient renvoyés.</span><span class="sxs-lookup"><span data-stu-id="b061d-120">Requests that only names stored as numeric identifiers be returned.</span></span> 
    
 <span data-ttu-id="b061d-121">_lpcPropNames_</span><span class="sxs-lookup"><span data-stu-id="b061d-121">_lpcPropNames_</span></span>
  
> <span data-ttu-id="b061d-122">remarquer Pointeur vers le nombre de pointeurs de nom de propriété dans le tableau vers lequel pointe le paramètre _lppPropNames_ .</span><span class="sxs-lookup"><span data-stu-id="b061d-122">[out] A pointer to a count of the property name pointers in the array pointed to by the  _lppPropNames_ parameter.</span></span> 
    
 <span data-ttu-id="b061d-123">_lpppPropNames_</span><span class="sxs-lookup"><span data-stu-id="b061d-123">_lpppPropNames_</span></span>
  
> <span data-ttu-id="b061d-124">remarquer Pointeur vers un tableau de pointeurs vers des structures [MAPINAMEID](mapinameid.md) contenant des noms de propriétés.</span><span class="sxs-lookup"><span data-stu-id="b061d-124">[out] A pointer to an array of pointers to [MAPINAMEID](mapinameid.md) structures that contains property names.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b061d-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b061d-125">Return value</span></span>

<span data-ttu-id="b061d-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="b061d-126">S_OK</span></span> 
  
> <span data-ttu-id="b061d-127">Les noms des propriétés ont été renvoyés.</span><span class="sxs-lookup"><span data-stu-id="b061d-127">The property names were successfully returned.</span></span> 
    
<span data-ttu-id="b061d-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="b061d-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="b061d-129">L'objet ne prend pas en charge les propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="b061d-129">The object does not support named properties.</span></span> 
    
<span data-ttu-id="b061d-130">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="b061d-130">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="b061d-131">L'appel a réussi globalement, mais les noms d'une ou plusieurs propriétés n'ont pas pu être renvoyés.</span><span class="sxs-lookup"><span data-stu-id="b061d-131">The call succeeded overall, but names for one or more properties could not be returned.</span></span> <span data-ttu-id="b061d-132">Les balises de propriété pour les propriétés ayant échoué ont un type de propriété **PT_ERROR**.</span><span class="sxs-lookup"><span data-stu-id="b061d-132">The property tags for the failing properties have a property type of **PT_ERROR**.</span></span> <span data-ttu-id="b061d-133">Lorsque cet avertissement est renvoyé, l'appel doit être géré comme réussi.</span><span class="sxs-lookup"><span data-stu-id="b061d-133">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="b061d-134">Pour tester cet avertissement, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="b061d-134">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="b061d-135">Pour plus d'informations, consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="b061d-135">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> 
    
<span data-ttu-id="b061d-136">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b061d-136">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="b061d-137">Le membre **cValues** d'une ou plusieurs des entrées du tableau de balises de propriété pointé par _lppPropTags_ est défini sur 0.</span><span class="sxs-lookup"><span data-stu-id="b061d-137">The **cValues** member of one or more of the entries in the property tag array pointed to by  _lppPropTags_ is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b061d-138">Remarques</span><span class="sxs-lookup"><span data-stu-id="b061d-138">Remarks</span></span>

<span data-ttu-id="b061d-139">Bien qu'il soit possible d'accéder à la plupart des propriétés à l'aide d'un identificateur de propriété, certaines propriétés sont accessibles par nom.</span><span class="sxs-lookup"><span data-stu-id="b061d-139">While access to most properties is by property identifier, some properties can be accessed by name.</span></span> <span data-ttu-id="b061d-140">La méthode **IMAPIProp:: GetNamesFromIDs** peut être appelée pour effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="b061d-140">The **IMAPIProp::GetNamesFromIDs** method can be called to do the following:</span></span> 
  
- <span data-ttu-id="b061d-141">Récupérez des noms pour des identificateurs de propriétés spécifiques dans un jeu de propriétés spécifique.</span><span class="sxs-lookup"><span data-stu-id="b061d-141">Retrieve names for specific property identifiers in a specific property set.</span></span>
    
- <span data-ttu-id="b061d-142">Récupérez des noms pour des identificateurs de propriétés spécifiques dans n'importe quel jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="b061d-142">Retrieve names for specific property identifiers in any property set.</span></span>
    
- <span data-ttu-id="b061d-143">Récupérez les noms de toutes les propriétés nommées incluses dans le mappage de l'objet.</span><span class="sxs-lookup"><span data-stu-id="b061d-143">Retrieve names for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="b061d-144">Si _lppPropTags_ pointe vers un tableau de balises de propriété valide avec un ou plusieurs identificateurs de propriété et _lpPropSetGuid_ pointe sur un jeu de propriétés valide, **GetNamesFromIDs** ignore le jeu de propriétés et les types de propriété et renvoie tous les noms qui mappent aux identificateurs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="b061d-144">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers, and  _lpPropSetGuid_ points to a valid property set, **GetNamesFromIDs** ignores the property set and the property types and returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="b061d-145">Si _lppPropTags_ pointe vers un tableau de balises de propriété valide avec un ou plusieurs identificateurs de propriété et _LPPROPSETGUID_ a la valeur null, **GetNamesFromIDs** renvoie tous les noms mappés aux identificateurs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="b061d-145">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers and  _lpPropSetGuid_ is NULL, **GetNamesFromIDs** returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="b061d-146">Si un identificateur spécifié ne possède pas de nom, **GetNamesFromIDs** renvoie la valeur null à la place de cet identificateur dans la structure renvoyée dans _lpppPropNames_ et renvoie également MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="b061d-146">If a specified identifier does not have a name, **GetNamesFromIDs** returns NULL in that identifier's place in the structure returned in  _lpppPropNames_ and also returns MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="b061d-147">Si _lpPropSetGuid_ et _lppPropTags_ sont tous deux null, **GetNamesFromIDs** alloue un nouveau tableau de balises de propriété et renvoie tous les noms de toutes les propriétés nommées pour l'objet.</span><span class="sxs-lookup"><span data-stu-id="b061d-147">If both  _lpPropSetGuid_ and  _lppPropTags_ are NULL, **GetNamesFromIDs** allocates a new property tag array and returns all of the names for all of the named properties for the object.</span></span> 
  
<span data-ttu-id="b061d-148">Lorsqu'il n'y a aucun nom à renvoyer, par exemple s'il n'y a pas de propriétés dans le jeu de propriétés demandé ou si toutes les propriétés sont d'un type exclu par les indicateurs, **GetNamesFromIDs** effectue les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="b061d-148">When there are no names to be returned, perhaps because there are no properties in the requested property set or all of the properties are of a type excluded by the flags, **GetNamesFromIDs** does the following:</span></span> 
  
- <span data-ttu-id="b061d-149">Renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="b061d-149">Returns S_OK.</span></span>
    
- <span data-ttu-id="b061d-150">Alloue une nouvelle structure **SPropTagArray** en définissant le membre **cValues** sur 0.</span><span class="sxs-lookup"><span data-stu-id="b061d-150">Allocates a new **SPropTagArray** structure, setting the **cValues** member to 0.</span></span> 
    
- <span data-ttu-id="b061d-151">Définit le contenu de _lpcPropNames_ sur 0.</span><span class="sxs-lookup"><span data-stu-id="b061d-151">Sets the contents of  _lpcPropNames_ to 0.</span></span> 
    
- <span data-ttu-id="b061d-152">Définit le contenu de _lpppPropNames_ sur null.</span><span class="sxs-lookup"><span data-stu-id="b061d-152">Sets the contents of  _lpppPropNames_ to NULL.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="b061d-153">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="b061d-153">Notes to implementers</span></span>

<span data-ttu-id="b061d-154">Si _lpPropSetGuid_ pointe vers un jeu de propriétés valide et _LPPPROPTAGS_ a la valeur null, le résultat n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="b061d-154">If  _lpPropSetGuid_ points to a valid property set and  _lppPropTags_ is NULL, the result is undefined.</span></span> <span data-ttu-id="b061d-155">Vous pouvez utiliser l'une des stratégies suivantes:</span><span class="sxs-lookup"><span data-stu-id="b061d-155">You can use one of the following strategies:</span></span> 
  
- <span data-ttu-id="b061d-156">Ignorez le jeu de propriétés et renvoyez les noms pour les identificateurs dans le tableau de balises de propriété.</span><span class="sxs-lookup"><span data-stu-id="b061d-156">Ignore the property set and return the names for the identifiers in the property tag array.</span></span>
    
- <span data-ttu-id="b061d-157">Renvoyer uniquement les noms pour les identificateurs du tableau de balises de propriété qui appartiennent au jeu de propriétés spécifié.</span><span class="sxs-lookup"><span data-stu-id="b061d-157">Return the names for only the identifiers in the property tag array that belong to the specified property set.</span></span>
    
- <span data-ttu-id="b061d-158">Échec de l'appel, en renvoyant MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="b061d-158">Fail the call, returning MAPI_E_INVALID_PARAMETER.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="b061d-159">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="b061d-159">Notes to callers</span></span>

<span data-ttu-id="b061d-160">Pour récupérer toutes les propriétés nommées d'un objet, vous devez d'abord appeler la méthode [IMAPIProp:: GetPropList](imapiprop-getproplist.md) de l'objet, puis transmettre les identificateurs renvoyés situés au-dessus de la plage 0X8000 à **GetNamesFromIDs**.</span><span class="sxs-lookup"><span data-stu-id="b061d-160">To retrieve all of the named properties for an object, you must first call the object's [IMAPIProp::GetPropList](imapiprop-getproplist.md) method and then pass the returned identifiers that are above the 0x8000 range to **GetNamesFromIDs**.</span></span>
  
<span data-ttu-id="b061d-161">Si vous transmettez un jeu de propriétés valide, mais pas un tableau de balises de propriété valide, soyez prêt à obtenir des résultats imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="b061d-161">If you pass a valid property set but not a valid property tag array, be prepared for unpredictable results.</span></span> <span data-ttu-id="b061d-162">Certaines implémentations de **GetNamesFromIDs** ignorent le jeu de propriétés et renvoient les noms des identificateurs dans le tableau de balises de propriété.</span><span class="sxs-lookup"><span data-stu-id="b061d-162">Some implementations of **GetNamesFromIDs** ignore the property set and return the names for the identifiers in the property tag array.</span></span> <span data-ttu-id="b061d-163">Certaines implémentations renvoient MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="b061d-163">Some implementations return MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="b061d-164">D'autres implémentations renvoient les noms des identificateurs de toutes les propriétés dans le jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="b061d-164">Still other implementations return names for identifiers of all properties in the property set.</span></span> <span data-ttu-id="b061d-165">Si le jeu de propriétés est PS_PUBLIC_STRINGS, **GetNamesFromIDs** peut renvoyer tous les noms qui ont été créés.</span><span class="sxs-lookup"><span data-stu-id="b061d-165">If the property set is PS_PUBLIC_STRINGS, **GetNamesFromIDs** can return all names that were ever created.</span></span> <span data-ttu-id="b061d-166">Si le fournisseur de services stocke une propriété sous les identificateurs associés aux chaînes publiques est immatérielle.</span><span class="sxs-lookup"><span data-stu-id="b061d-166">Whether the service provider stores a property under the identifiers associated with the public strings is immaterial.</span></span> 
  
<span data-ttu-id="b061d-167">Lorsque vous avez terminé d'utiliser les noms de propriété, vérifiez le contenu du paramètre _lpcPropNames_ pour déterminer si des noms ont été renvoyés.</span><span class="sxs-lookup"><span data-stu-id="b061d-167">When you are finished with the property names, check the contents of the  _lpcPropNames_ parameter to determine whether any names were returned.</span></span> <span data-ttu-id="b061d-168">Si c'est le cas, appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer la mémoire désignée par _lppPropTags_ et _lpppPropNames_ lorsqu'un résultat réussi est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="b061d-168">If so, call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory pointed to by  _lppPropTags_ and  _lpppPropNames_ when a successful result is returned.</span></span> <span data-ttu-id="b061d-169">Un appel à **MAPIFreeBuffer** est suffisant pour chaque paramètre; vous n'avez pas besoin de parcourir le tableau de pointeurs et de libérer chaque structure **MAPINAMEID** individuellement.</span><span class="sxs-lookup"><span data-stu-id="b061d-169">One call to **MAPIFreeBuffer** is sufficient for each parameter; you do not have to traverse the array of pointers and free each **MAPINAMEID** structure individually.</span></span> 
  
<span data-ttu-id="b061d-170">Pour plus d'informations sur les propriétés nommées, voir [MAPI named Properties](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="b061d-170">For more information about named properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b061d-171">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b061d-171">MFCMAPI reference</span></span>

<span data-ttu-id="b061d-172">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b061d-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b061d-173">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="b061d-173">**File**</span></span>|<span data-ttu-id="b061d-174">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="b061d-174">**Function**</span></span>|<span data-ttu-id="b061d-175">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="b061d-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b061d-176">SingleMAPIPropListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="b061d-176">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="b061d-177">CSingleMAPIPropListCtrl:: FindAllNamedProps</span><span class="sxs-lookup"><span data-stu-id="b061d-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span></span>  <br/> |<span data-ttu-id="b061d-178">MFCMAPI utilise la méthode **IMAPIProp:: GetNamesFromIDs** pour rechercher des propriétés nommées qui ont été précédemment mappées.</span><span class="sxs-lookup"><span data-stu-id="b061d-178">MFCMAPI uses the **IMAPIProp::GetNamesFromIDs** method to look up named properties that have previously been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b061d-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b061d-179">See also</span></span>



[<span data-ttu-id="b061d-180">GUID</span><span class="sxs-lookup"><span data-stu-id="b061d-180">GUID</span></span>](guid.md)
  
[<span data-ttu-id="b061d-181">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="b061d-181">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)
  
[<span data-ttu-id="b061d-182">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="b061d-182">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="b061d-183">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b061d-183">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="b061d-184">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="b061d-184">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="b061d-185">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="b061d-185">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="b061d-186">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b061d-186">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="b061d-187">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="b061d-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="b061d-188">MAPI des propri�t�s nomm�e</span><span class="sxs-lookup"><span data-stu-id="b061d-188">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="b061d-189">Utilisation de macros pour la gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="b061d-189">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

