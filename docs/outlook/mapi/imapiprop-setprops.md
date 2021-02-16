---
title: IMAPIPropSetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.SetProps
api_type:
- COM
ms.assetid: 49f007c9-42e5-4391-8b83-988c9b0ebdba
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 87709f8a77471637d7652982669bcba93ca2e1dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412617"
---
# <a name="imapipropsetprops"></a><span data-ttu-id="dfdb7-103">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="dfdb7-103">IMAPIProp::SetProps</span></span>

  
  
<span data-ttu-id="dfdb7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dfdb7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dfdb7-105">Met à jour une ou plusieurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-105">Updates one or more properties.</span></span>
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="dfdb7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dfdb7-106">Parameters</span></span>

 <span data-ttu-id="dfdb7-107">_cValues_</span><span class="sxs-lookup"><span data-stu-id="dfdb7-107">_cValues_</span></span>
  
> <span data-ttu-id="dfdb7-108">[in] Nombre de valeurs de propriétés pointées par _le paramètre lpPropArray._</span><span class="sxs-lookup"><span data-stu-id="dfdb7-108">[in] The count of property values pointed to by the  _lpPropArray_ parameter.</span></span> <span data-ttu-id="dfdb7-109">Le  _paramètre cValues_ ne doit pas être 0.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-109">The  _cValues_ parameter must not be 0.</span></span> 
    
 <span data-ttu-id="dfdb7-110">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="dfdb7-110">_lpPropArray_</span></span>
  
> <span data-ttu-id="dfdb7-111">[in] Pointeur vers un tableau de structures [SPropValue](spropvalue.md) qui contiennent des valeurs de propriété à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-111">[in] A pointer to an array of [SPropValue](spropvalue.md) structures that contain property values to be updated.</span></span> 
    
 <span data-ttu-id="dfdb7-112">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="dfdb7-112">_lppProblems_</span></span>
  
> <span data-ttu-id="dfdb7-113">[in, out] Lors de l’entrée, un pointeur vers un pointeur vers une structure [SPropProblemArray](spropproblemarray.md) ; Dans le cas contraire, NULL, indiquant qu’il n’est pas nécessaire d’obtenir des informations sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-113">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, indicating no need for error information.</span></span> <span data-ttu-id="dfdb7-114">Si  _lppProblems est_ un pointeur valide sur l’entrée, **SetProps** renvoie des informations détaillées sur les erreurs de mise à jour d’une ou plusieurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-114">If  _lppProblems_ is a valid pointer on input, **SetProps** returns detailed information about errors in updating one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dfdb7-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dfdb7-115">Return value</span></span>

<span data-ttu-id="dfdb7-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="dfdb7-116">S_OK</span></span> 
  
> <span data-ttu-id="dfdb7-117">Les propriétés ont été correctement mises à jour.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-117">The properties were successfully updated.</span></span>
    
<span data-ttu-id="dfdb7-118">Les valeurs suivantes peuvent être renvoyées dans la structure **SPropProblemArray,** mais pas en tant que valeurs de retour **pour SetProps**:</span><span class="sxs-lookup"><span data-stu-id="dfdb7-118">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **SetProps**:</span></span>
  
<span data-ttu-id="dfdb7-119">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="dfdb7-119">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="dfdb7-120">L’indicateur MAPI_UNICODE a été définie et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et l’implémentation prend uniquement en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-120">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="dfdb7-121">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="dfdb7-121">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="dfdb7-122">La propriété ne peut pas être mise à jour, car elle est en lecture seule, calculée par le fournisseur de services responsable de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-122">The property cannot be updated because it is read-only, computed by the service provider that is responsible for the object.</span></span>
    
<span data-ttu-id="dfdb7-123">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="dfdb7-123">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="dfdb7-124">Le type de propriété n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-124">The property type is invalid.</span></span>
    
<span data-ttu-id="dfdb7-125">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="dfdb7-125">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="dfdb7-126">Une tentative de modification d’un objet en lecture seule ou d’accès à un objet pour lequel l’utilisateur dispose d’autorisations insuffisantes a été tentée.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-126">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="dfdb7-127">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="dfdb7-127">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="dfdb7-128">La propriété ne peut pas être mise à jour car elle est supérieure à la taille de la mémoire tampon d’appel de procédure distante (RPC).</span><span class="sxs-lookup"><span data-stu-id="dfdb7-128">The property cannot be updated because it is larger than the remote procedure call (RPC) buffer size.</span></span>
    
<span data-ttu-id="dfdb7-129">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="dfdb7-129">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="dfdb7-130">Le type de propriété n’est pas le type attendu par l’implémentation d’appel.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-130">The property type is not the type expected by the calling implementation.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="dfdb7-131">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="dfdb7-131">Notes to implementers</span></span>

<span data-ttu-id="dfdb7-132">Ignorez **la PR_NULL** de propriété ([PidTagNull](pidtagnull-canonical-property.md)) et toutes les propriétés avec un type de **PT_ERROR**.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-132">Ignore the **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag and all properties with a type of **PT_ERROR**.</span></span> <span data-ttu-id="dfdb7-133">Ne pas apporter de modifications ni signaler de problèmes dans la structure **SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="dfdb7-133">Do not make changes or report problems in the **SPropProblemArray** structure.</span></span> 
  
<span data-ttu-id="dfdb7-134">Renvoyer MAPI_E_INVALID_PARAMETER si une propriété de type **PT_OBJECT** est incluse dans le tableau de valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-134">Return MAPI_E_INVALID_PARAMETER if a property of type **PT_OBJECT** is included in the property value array.</span></span> <span data-ttu-id="dfdb7-135">Renvoyer également cette erreur si une propriété à valeurs multiples est incluse dans le tableau et que son membre **cValues** est définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-135">Also return this error if a multiple-value property is included in the array and its **cValues** member is set to 0.</span></span> 
  
<span data-ttu-id="dfdb7-136">Si l’appel réussit globalement mais qu’il y a des problèmes avec la définition de certaines propriétés, renvoyez S_OK et placez des informations sur les problèmes dans l’entrée appropriée de la structure **SPropProblemArray** vers qui pointe le paramètre _lppProblems._</span><span class="sxs-lookup"><span data-stu-id="dfdb7-136">If the call succeeds overall but there are problems with setting some of the properties, return S_OK and put information about the problems in the appropriate entry of the **SPropProblemArray** structure that the  _lppProblems_ parameter points to.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="dfdb7-137">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="dfdb7-137">Notes to callers</span></span>

<span data-ttu-id="dfdb7-138">Selon le fournisseur de services, vous pouvez également modifier le type de propriété en passant une balise de propriété qui contient un type différent de celui précédemment utilisé avec un identificateur de propriété donné.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-138">Depending on the service provider, you might also be able to change the property type by passing a property tag that contains a different type than was previously used with a given property identifier.</span></span>
  
<span data-ttu-id="dfdb7-139">Si vous incluez une balise de propriété pour une propriété qui n’est pas pris en compte par l’objet et que l’implémentation de **SetProps** permet la création de nouvelles propriétés, la propriété est ajoutée à l’objet.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-139">If you include a property tag for a property that is unsupported by the object and the implementation of **SetProps** allows the creation of new properties, the property is added to the object.</span></span> <span data-ttu-id="dfdb7-140">Toute valeur précédente stockée avec l’identificateur de propriété utilisé pour la nouvelle propriété est ignorée.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-140">Any previous value stored with the property identifier that was used for the new property is discarded.</span></span> 
  
<span data-ttu-id="dfdb7-141">Notez que la S_OK valeur de retour ne garantit pas que toutes les propriétés ont été correctement mises à jour.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-141">Note that the S_OK return value does not guarantee that all of the properties were successfully updated.</span></span> <span data-ttu-id="dfdb7-142">Some providers cache **SetProps** calls until they receive a call that requires provider intervention, such as [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMAPIProp::GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="dfdb7-142">Some providers cache **SetProps** calls until they receive a call that requires provider intervention, such as [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span> <span data-ttu-id="dfdb7-143">Par conséquent, il est possible de recevoir des valeurs d’erreur liées à l’appel **SetProps** avec les appels ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-143">Therefore, it is possible to receive error values that relate to the **SetProps** call with the later calls.</span></span> 
  
<span data-ttu-id="dfdb7-144">Si **SetProps renvoie** S_OK, vérifiez la structure **SPropProblemArray** pointée par  _lppProblems_ pour les problèmes de mise à jour des propriétés individuelles.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-144">If **SetProps** returns S_OK, check the **SPropProblemArray** structure pointed to by  _lppProblems_ for problems updating individual properties.</span></span> <span data-ttu-id="dfdb7-145">Si **SetProps renvoie** une erreur, ne vérifiez pas le tableau des problèmes de propriété.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-145">If **SetProps** returns an error, do not check the property problem array.</span></span> <span data-ttu-id="dfdb7-146">Appelez plutôt la méthode [IMAPIProp::GetLastError](imapiprop-getlasterror.md) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-146">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
  
<span data-ttu-id="dfdb7-147">Lors de la mise à jour de propriétés de grande taille, **SetProps** peut échouer et renvoyer des MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-147">When updating large properties, **SetProps** can fail and return MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="dfdb7-148">Il n’existe aucune taille maximale pour les propriétés, et différents objets peuvent avoir des limites différentes.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-148">There is no maximum size for properties, and different objects can have different limits.</span></span> <span data-ttu-id="dfdb7-149">Si vous traitez des propriétés potentiellement importantes, soyez prêt à appeler la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) avec IID_IStream comme identificateur d’interface si **SetProps** renvoie cette valeur d’erreur.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-149">If you deal with potentially large properties, be prepared to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with IID_IStream as the interface identifier if **SetProps** returns this error value.</span></span> 
  
<span data-ttu-id="dfdb7-150">Appelez la [fonction MAPIFreeBuffer](mapifreebuffer.md) pour libérer la structure **SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="dfdb7-150">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the **SPropProblemArray** structure.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="dfdb7-151">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="dfdb7-151">MFCMAPI reference</span></span>

<span data-ttu-id="dfdb7-152">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dfdb7-153">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="dfdb7-153">**File**</span></span>|<span data-ttu-id="dfdb7-154">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="dfdb7-154">**Function**</span></span>|<span data-ttu-id="dfdb7-155">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="dfdb7-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dfdb7-156">PropertyEditor.cpp</span><span class="sxs-lookup"><span data-stu-id="dfdb7-156">PropertyEditor.cpp</span></span>  <br/> |<span data-ttu-id="dfdb7-157">CPropertyEditor::WriteSPropValueToObject</span><span class="sxs-lookup"><span data-stu-id="dfdb7-157">CPropertyEditor::WriteSPropValueToObject</span></span>  <br/> |<span data-ttu-id="dfdb7-158">MFCMAPI utilise la méthode **IMAPIProp::SetProps** pour écrire une propriété dans un objet une fois la propriété modifiée.</span><span class="sxs-lookup"><span data-stu-id="dfdb7-158">MFCMAPI uses the **IMAPIProp::SetProps** method to write a property back to an object after the property has been edited.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dfdb7-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfdb7-159">See also</span></span>



[<span data-ttu-id="dfdb7-160">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="dfdb7-160">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="dfdb7-161">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="dfdb7-161">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="dfdb7-162">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="dfdb7-162">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="dfdb7-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="dfdb7-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="dfdb7-164">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="dfdb7-164">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="dfdb7-165">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="dfdb7-165">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="dfdb7-166">SPropValue</span><span class="sxs-lookup"><span data-stu-id="dfdb7-166">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="dfdb7-167">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dfdb7-167">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)

