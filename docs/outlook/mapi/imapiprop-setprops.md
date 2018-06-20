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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 304295e3ac77fb67ec5875620a7a269377b542c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783904"
---
# <a name="imapipropsetprops"></a><span data-ttu-id="00985-103">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="00985-103">IMAPIProp::SetProps</span></span>

  
  
<span data-ttu-id="00985-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="00985-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="00985-105">Met à jour une ou plusieurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="00985-105">Updates one or more properties.</span></span>
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="00985-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00985-106">Parameters</span></span>

 <span data-ttu-id="00985-107">_cValues_</span><span class="sxs-lookup"><span data-stu-id="00985-107">_cValues_</span></span>
  
> <span data-ttu-id="00985-108">[in] Le nombre de valeurs de propriété indiqué par le paramètre _lpPropArray_ .</span><span class="sxs-lookup"><span data-stu-id="00985-108">[in] The count of property values pointed to by the  _lpPropArray_ parameter.</span></span> <span data-ttu-id="00985-109">Le paramètre _cValues_ ne doit pas être 0.</span><span class="sxs-lookup"><span data-stu-id="00985-109">The  _cValues_ parameter must not be 0.</span></span> 
    
 <span data-ttu-id="00985-110">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="00985-110">_lpPropArray_</span></span>
  
> <span data-ttu-id="00985-111">[in] Pointeur vers un tableau de structures [SPropValue](spropvalue.md) qui contiennent des valeurs de propriété à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="00985-111">[in] A pointer to an array of [SPropValue](spropvalue.md) structures that contain property values to be updated.</span></span> 
    
 <span data-ttu-id="00985-112">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="00985-112">_lppProblems_</span></span>
  
> <span data-ttu-id="00985-113">[entrée, sortie] À l’entrée, un pointeur vers un pointeur vers une structure [SPropProblemArray](spropproblemarray.md) ; dans le cas contraire, NULL, indiquant ainsi pas besoin d’informations sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="00985-113">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, indicating no need for error information.</span></span> <span data-ttu-id="00985-114">Si _lppProblems_ est un pointeur valid en entrée, **SetProps** renvoie des informations détaillées sur les erreurs dans une ou plusieurs propriétés de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="00985-114">If  _lppProblems_ is a valid pointer on input, **SetProps** returns detailed information about errors in updating one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="00985-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="00985-115">Return value</span></span>

<span data-ttu-id="00985-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="00985-116">S_OK</span></span> 
  
> <span data-ttu-id="00985-117">Les propriétés ont été correctement mis à jour.</span><span class="sxs-lookup"><span data-stu-id="00985-117">The properties were successfully updated.</span></span>
    
<span data-ttu-id="00985-118">Les valeurs suivantes peuvent être renvoyées dans la structure **SPropProblemArray** , mais pas en tant que valeurs de retour pour **SetProps**:</span><span class="sxs-lookup"><span data-stu-id="00985-118">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **SetProps**:</span></span>
  
<span data-ttu-id="00985-119">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="00985-119">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="00985-120">Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="00985-120">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="00985-121">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="00985-121">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="00985-122">La propriété ne peut pas être mis à jour, car elle est en lecture seule, calculé par le fournisseur de services qui est responsable de l’objet.</span><span class="sxs-lookup"><span data-stu-id="00985-122">The property cannot be updated because it is read-only, computed by the service provider that is responsible for the object.</span></span>
    
<span data-ttu-id="00985-123">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="00985-123">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="00985-124">Le type de propriété n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="00985-124">The property type is invalid.</span></span>
    
<span data-ttu-id="00985-125">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="00985-125">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="00985-126">Une tentative a été effectuée pour modifier un objet en lecture seule ou pour accéder à un objet pour lequel l’utilisateur dispose d’autorisations insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="00985-126">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="00985-127">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="00985-127">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="00985-128">La propriété ne peut pas être mis à jour, car elle est supérieure à la taille de mémoire tampon de procédure distante (RPC) d’appel.</span><span class="sxs-lookup"><span data-stu-id="00985-128">The property cannot be updated because it is larger than the remote procedure call (RPC) buffer size.</span></span>
    
<span data-ttu-id="00985-129">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="00985-129">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="00985-130">Le type de propriété n’est pas le type attendu par l’implémentation d’appel.</span><span class="sxs-lookup"><span data-stu-id="00985-130">The property type is not the type expected by the calling implementation.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="00985-131">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="00985-131">Notes to implementers</span></span>

<span data-ttu-id="00985-132">Ignorer la balise de propriété **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) et toutes les propriétés de type **PT_ERROR**.</span><span class="sxs-lookup"><span data-stu-id="00985-132">Ignore the **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag and all properties with a type of **PT_ERROR**.</span></span> <span data-ttu-id="00985-133">N’apportez les modifications ou signaler les problèmes dans la structure **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="00985-133">Do not make changes or report problems in the **SPropProblemArray** structure.</span></span> 
  
<span data-ttu-id="00985-134">Retourner MAPI_E_INVALID_PARAMETER si une propriété de type **PT_OBJECT** est incluse dans le tableau de valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="00985-134">Return MAPI_E_INVALID_PARAMETER if a property of type **PT_OBJECT** is included in the property value array.</span></span> <span data-ttu-id="00985-135">Aussi renvoyer cette erreur si une propriété à valeurs multiples est incluse dans le tableau et ses membres **cValues** est définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="00985-135">Also return this error if a multiple-value property is included in the array and its **cValues** member is set to 0.</span></span> 
  
<span data-ttu-id="00985-136">Si l’appel réussit globale, mais il existe des problèmes liés à la définition de certaines des propriétés, qu’elles retournent S_OK et placer les informations sur les problèmes dans l’entrée appropriée de la structure **SPropProblemArray** vers laquelle pointe le paramètre _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="00985-136">If the call succeeds overall but there are problems with setting some of the properties, return S_OK and put information about the problems in the appropriate entry of the **SPropProblemArray** structure that the  _lppProblems_ parameter points to.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="00985-137">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="00985-137">Notes to callers</span></span>

<span data-ttu-id="00985-138">Selon le fournisseur de services, vous pourrez également modifier le type de propriété en transmettant une balise de propriété qui contient un type autre que celui utilisé précédemment avec un identificateur de propriété donné.</span><span class="sxs-lookup"><span data-stu-id="00985-138">Depending on the service provider, you might also be able to change the property type by passing a property tag that contains a different type than was previously used with a given property identifier.</span></span>
  
<span data-ttu-id="00985-139">Si vous incluez une balise de propriété pour une propriété qui est pris en charge par l’objet et l’implémentation de **SetProps** permet la création de nouvelles propriétés, la propriété est ajoutée à l’objet.</span><span class="sxs-lookup"><span data-stu-id="00985-139">If you include a property tag for a property that is unsupported by the object and the implementation of **SetProps** allows the creation of new properties, the property is added to the object.</span></span> <span data-ttu-id="00985-140">Toute valeur stockée avec l’identificateur de la propriété qui a été utilisé pour la nouvelle propriété est ignorée.</span><span class="sxs-lookup"><span data-stu-id="00985-140">Any previous value stored with the property identifier that was used for the new property is discarded.</span></span> 
  
<span data-ttu-id="00985-141">Notez que la valeur de retour de S_OK ne garantit pas que toutes les propriétés ont été correctement mis à jour.</span><span class="sxs-lookup"><span data-stu-id="00985-141">Note that the S_OK return value does not guarantee that all of the properties were successfully updated.</span></span> <span data-ttu-id="00985-142">Certains fournisseurs de mettre en cache les appels **SetProps** jusqu'à ce qu’ils reçoivent un appel qui nécessite une intervention fournisseur, telles que [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ou [IMAPIProp::GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="00985-142">Some providers cache **SetProps** calls until they receive a call that requires provider intervention, such as [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span> <span data-ttu-id="00985-143">Par conséquent, il est possible de recevoir des valeurs d’erreur qui sont associées à l’appel **SetProps** avec les appels ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="00985-143">Therefore, it is possible to receive error values that relate to the **SetProps** call with the later calls.</span></span> 
  
<span data-ttu-id="00985-144">Si **SetProps** renvoie S_OK, vérifiez la structure **SPropProblemArray** désignée par _lppProblems_ les problèmes de mise à jour des propriétés individuelles.</span><span class="sxs-lookup"><span data-stu-id="00985-144">If **SetProps** returns S_OK, check the **SPropProblemArray** structure pointed to by  _lppProblems_ for problems updating individual properties.</span></span> <span data-ttu-id="00985-145">Si **SetProps** renvoie une erreur, n’activez pas le tableau de problème de propriétés.</span><span class="sxs-lookup"><span data-stu-id="00985-145">If **SetProps** returns an error, do not check the property problem array.</span></span> <span data-ttu-id="00985-146">Au lieu de cela, appelez la méthode l’objet [IMAPIProp::GetLastError](imapiprop-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="00985-146">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
  
<span data-ttu-id="00985-147">Lors de la mise à jour des propriétés de grande taille, **SetProps** peut échouer et renvoyer MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="00985-147">When updating large properties, **SetProps** can fail and return MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="00985-148">Il n’existe pas de taille maximale des propriétés et objets différents peuvent avoir différentes limites.</span><span class="sxs-lookup"><span data-stu-id="00985-148">There is no maximum size for properties, and different objects can have different limits.</span></span> <span data-ttu-id="00985-149">Si vous travaillez avec des propriétés potentiellement volumineux, être prêt à appeler la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) avec IID_IStream l’identificateur d’interface si **SetProps** renvoie cette valeur d’erreur.</span><span class="sxs-lookup"><span data-stu-id="00985-149">If you deal with potentially large properties, be prepared to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with IID_IStream as the interface identifier if **SetProps** returns this error value.</span></span> 
  
<span data-ttu-id="00985-150">Appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer de la structure **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="00985-150">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the **SPropProblemArray** structure.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="00985-151">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="00985-151">MFCMAPI reference</span></span>

<span data-ttu-id="00985-152">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="00985-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="00985-153">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="00985-153">**File**</span></span>|<span data-ttu-id="00985-154">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="00985-154">**Function**</span></span>|<span data-ttu-id="00985-155">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="00985-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="00985-156">PropertyEditor.cpp</span><span class="sxs-lookup"><span data-stu-id="00985-156">PropertyEditor.cpp</span></span>  <br/> |<span data-ttu-id="00985-157">CPropertyEditor::WriteSPropValueToObject</span><span class="sxs-lookup"><span data-stu-id="00985-157">CPropertyEditor::WriteSPropValueToObject</span></span>  <br/> |<span data-ttu-id="00985-158">MFCMAPI utilise la méthode **IMAPIProp::SetProps** pour écrire dans une propriété à un objet une fois que la propriété a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="00985-158">MFCMAPI uses the **IMAPIProp::SetProps** method to write a property back to an object after the property has been edited.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="00985-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00985-159">See also</span></span>



[<span data-ttu-id="00985-160">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="00985-160">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="00985-161">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="00985-161">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="00985-162">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="00985-162">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="00985-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="00985-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="00985-164">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="00985-164">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="00985-165">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="00985-165">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="00985-166">SPropValue</span><span class="sxs-lookup"><span data-stu-id="00985-166">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="00985-167">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="00985-167">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)

