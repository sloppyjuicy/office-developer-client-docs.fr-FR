---
title: IMAPIPropOpenProperty
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.OpenProperty
api_type:
- COM
ms.assetid: e400e6cc-4e36-43fc-9304-b688a0a7fd77
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 656e5c5532edfc6c791ca30aa30f4c4d96847295
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783907"
---
# <a name="imapipropopenproperty"></a><span data-ttu-id="c95ae-103">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="c95ae-103">IMAPIProp::OpenProperty</span></span>

<span data-ttu-id="c95ae-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c95ae-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c95ae-105">Retourne un pointeur vers une interface qui peut être utilisée pour accéder à une propriété.</span><span class="sxs-lookup"><span data-stu-id="c95ae-105">Returns a pointer to an interface that can be used to access a property.</span></span>
  
```cpp
HRESULT OpenProperty(
  ULONG ulPropTag,
  LPCIID lpiid,
  ULONG ulInterfaceOptions,
  ULONG ulFlags,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="c95ae-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c95ae-106">Parameters</span></span>

 <span data-ttu-id="c95ae-107">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="c95ae-107">_ulPropTag_</span></span>
  
> <span data-ttu-id="c95ae-108">[in] La balise de propriété pour la propriété auquel accéder.</span><span class="sxs-lookup"><span data-stu-id="c95ae-108">[in] The property tag for the property to be accessed.</span></span> <span data-ttu-id="c95ae-109">L’identificateur et le type doivent être inclus dans la balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="c95ae-109">Both the identifier and the type must be included in the property tag.</span></span>
    
 <span data-ttu-id="c95ae-110">_lpiid_</span><span class="sxs-lookup"><span data-stu-id="c95ae-110">_lpiid_</span></span>
  
> <span data-ttu-id="c95ae-111">[in] Pointeur vers l’identificateur de l’interface à utiliser pour accéder à la propriété.</span><span class="sxs-lookup"><span data-stu-id="c95ae-111">[in] A pointer to the identifier for the interface to be used to access the property.</span></span> <span data-ttu-id="c95ae-112">Le paramètre _lpiid_ ne doit pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="c95ae-112">The  _lpiid_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="c95ae-113">_ulInterfaceOptions_</span><span class="sxs-lookup"><span data-stu-id="c95ae-113">_ulInterfaceOptions_</span></span>
  
> <span data-ttu-id="c95ae-114">[in] Données relatives à l’interface identifié par le paramètre _lpiid_ .</span><span class="sxs-lookup"><span data-stu-id="c95ae-114">[in] Data that relates to the interface identified by the  _lpiid_ parameter.</span></span> 
    
 <span data-ttu-id="c95ae-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c95ae-115">_ulFlags_</span></span>
  
> <span data-ttu-id="c95ae-116">[in] Masque de bits d’indicateurs qui contrôle l’accès à la propriété.</span><span class="sxs-lookup"><span data-stu-id="c95ae-116">[in] A bitmask of flags that controls access to the property.</span></span> <span data-ttu-id="c95ae-117">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="c95ae-117">The following flags can be set:</span></span>
    
<span data-ttu-id="c95ae-118">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="c95ae-118">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="c95ae-119">Si la propriété n’existe pas, il doit être créé.</span><span class="sxs-lookup"><span data-stu-id="c95ae-119">If the property does not exist, it should be created.</span></span> <span data-ttu-id="c95ae-120">Si la propriété n’existe pas, la valeur actuelle de la propriété doit être ignorée.</span><span class="sxs-lookup"><span data-stu-id="c95ae-120">If the property does exist, the current value of the property should be discarded.</span></span> <span data-ttu-id="c95ae-121">Lorsqu’un appelant définit l’indicateur MAPI_CREATE, il doit également affecter l’indicateur ne.</span><span class="sxs-lookup"><span data-stu-id="c95ae-121">When a caller sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="c95ae-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="c95ae-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="c95ae-123">Permet **OpenProperty** retournée correctement, éventuellement, avant de l’objet est entièrement disponible à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="c95ae-123">Allows **OpenProperty** to return successfully, possibly before the object is fully available to the caller.</span></span> <span data-ttu-id="c95ae-124">Si l’objet n’est pas disponible, l’émission d’un appel d’objet suivantes peut déclencher une erreur.</span><span class="sxs-lookup"><span data-stu-id="c95ae-124">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="c95ae-125">N'</span><span class="sxs-lookup"><span data-stu-id="c95ae-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="c95ae-126">Dans ce cas, n’est requise :</span><span class="sxs-lookup"><span data-stu-id="c95ae-126">MAPI_MODIFY is required in these situations:</span></span>
    
  - <span data-ttu-id="c95ae-127">Lors de l’ouverture d’une propriété de flux, tels **IID_IStream**, afin de le modifier.</span><span class="sxs-lookup"><span data-stu-id="c95ae-127">When opening a stream property, such as **IID_IStream**, to modify it.</span></span>
    
  - <span data-ttu-id="c95ae-128">Lorsque l’ouverture d’une pièce jointe du message incorporé, tel que [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) ouvert avec **IID_IMessage**, afin de le modifier.</span><span class="sxs-lookup"><span data-stu-id="c95ae-128">When opening an embedded message attachment, such as [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) opened with **IID_IMessage**, to modify it.</span></span>
    
 <span data-ttu-id="c95ae-129">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="c95ae-129">_lppUnk_</span></span>
  
> <span data-ttu-id="c95ae-130">[out] Pointeur vers l’interface à utiliser pour l’accès à la propriété demandée.</span><span class="sxs-lookup"><span data-stu-id="c95ae-130">[out] A pointer to the requested interface to be used for property access.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c95ae-131">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="c95ae-131">Return value</span></span>

<span data-ttu-id="c95ae-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="c95ae-132">S_OK</span></span> 
  
> <span data-ttu-id="c95ae-133">Le pointeur d’interface demandé a été renvoyé avec succès.</span><span class="sxs-lookup"><span data-stu-id="c95ae-133">The requested interface pointer was successfully returned.</span></span>
    
<span data-ttu-id="c95ae-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="c95ae-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="c95ae-135">L’interface demandée n’est pas pris en charge pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="c95ae-135">The requested interface is not supported for this property.</span></span>
    
<span data-ttu-id="c95ae-136">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="c95ae-136">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="c95ae-137">L’appelant a des autorisations suffisantes pour accéder à la propriété.</span><span class="sxs-lookup"><span data-stu-id="c95ae-137">The caller has insufficient permissions to access the property.</span></span>
    
<span data-ttu-id="c95ae-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="c95ae-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="c95ae-139">L’objet ne peut pas fournir l’accès à cette propriété par le biais de l’interface demandée.</span><span class="sxs-lookup"><span data-stu-id="c95ae-139">The object cannot provide access to this property through the requested interface.</span></span>
    
<span data-ttu-id="c95ae-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c95ae-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="c95ae-141">La propriété demandée n’existe pas et MAPI_CREATE n’a pas été défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="c95ae-141">The requested property does not exist and MAPI_CREATE was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="c95ae-142">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c95ae-142">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="c95ae-143">Le type de propriété dans la balise est défini sur PT_UNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="c95ae-143">The property type in the tag is set to PT_UNSPECIFIED.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c95ae-144">Remarques</span><span class="sxs-lookup"><span data-stu-id="c95ae-144">Remarks</span></span>

<span data-ttu-id="c95ae-145">La méthode **IMAPIProp::OpenProperty** permet d’accéder à une propriété via une interface particulière.</span><span class="sxs-lookup"><span data-stu-id="c95ae-145">The **IMAPIProp::OpenProperty** method provides access to a property through a particular interface.</span></span> <span data-ttu-id="c95ae-146">**OpenProperty** est une alternative aux méthodes [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPIProp::SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="c95ae-146">**OpenProperty** is an alternative to the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="c95ae-147">Lorsque vous **GetProps** ou **SetProps** échoue parce que la propriété est trop grande ou trop complexe, appelez **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="c95ae-147">When either **GetProps** or **SetProps** fails because the property is too large or too complex, call **OpenProperty**.</span></span> <span data-ttu-id="c95ae-148">**OpenProperty** est généralement utilisé pour accéder aux propriétés de type PT_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="c95ae-148">**OpenProperty** is typically used to access properties of type PT_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c95ae-149">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="c95ae-149">Notes to callers</span></span>

<span data-ttu-id="c95ae-150">Pour accéder aux pièces jointes des messages, ouvrez la propriété **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) avec un identificateur d’interface différents, en fonction du type de pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="c95ae-150">To access message attachments, open the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property with a different interface identifier, depending on the type of attachment.</span></span> <span data-ttu-id="c95ae-151">Le tableau suivant indique comment appeler **OpenProperty** pour les différents types de pièces jointes :</span><span class="sxs-lookup"><span data-stu-id="c95ae-151">The following table describes how to call **OpenProperty** for the different types of attachments:</span></span> 
  
|<span data-ttu-id="c95ae-152">**Type de pièce jointe**</span><span class="sxs-lookup"><span data-stu-id="c95ae-152">**Type of attachment**</span></span>|<span data-ttu-id="c95ae-153">**Identificateur de l’interface à utiliser**</span><span class="sxs-lookup"><span data-stu-id="c95ae-153">**Interface identifier to use**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c95ae-154">Binaire</span><span class="sxs-lookup"><span data-stu-id="c95ae-154">Binary</span></span>  <br/> |<span data-ttu-id="c95ae-155">IID_IStream</span><span class="sxs-lookup"><span data-stu-id="c95ae-155">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="c95ae-156">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c95ae-156">String</span></span>  <br/> |<span data-ttu-id="c95ae-157">IID_IStream</span><span class="sxs-lookup"><span data-stu-id="c95ae-157">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="c95ae-158">Message</span><span class="sxs-lookup"><span data-stu-id="c95ae-158">Message</span></span>  <br/> |<span data-ttu-id="c95ae-159">IID_IMessage</span><span class="sxs-lookup"><span data-stu-id="c95ae-159">IID_IMessage</span></span>  <br/> |
|<span data-ttu-id="c95ae-160">OLE 2.0</span><span class="sxs-lookup"><span data-stu-id="c95ae-160">OLE 2.0</span></span>  <br/> |<span data-ttu-id="c95ae-161">IID_IStreamDocfile</span><span class="sxs-lookup"><span data-stu-id="c95ae-161">IID_IStreamDocfile</span></span>  <br/> |
   
<span data-ttu-id="c95ae-162">**IStreamDocfile** est un dérivé de l’interface [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) basé sur un fichier composé OLE 2.0.</span><span class="sxs-lookup"><span data-stu-id="c95ae-162">**IStreamDocfile** is a derivative of the [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface that is based on an OLE 2.0 compound file.</span></span> <span data-ttu-id="c95ae-163">**IStreamDocfile** est la meilleure solution pour l’accès aux pièces jointes OLE 2.0 car elle implique le moins de surcharge.</span><span class="sxs-lookup"><span data-stu-id="c95ae-163">**IStreamDocfile** is the best choice for accessing OLE 2.0 attachments because it involves the least amount of overhead.</span></span> <span data-ttu-id="c95ae-164">Vous pouvez utiliser IID_IStreamDocFile pour ces propriétés qui contiennent des données stockées dans le stockage structuré disponible par le biais de l’interface [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c95ae-164">You can use IID_IStreamDocFile for those properties that contain data stored in structured storage available through the [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="c95ae-165">Pour plus d’informations sur l’utilisation de **OpenProperty** avec les pièces jointes, voir la propriété **PR_ATTACH_DATA_OBJ** et [l’ouverture d’une pièce jointe](opening-an-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="c95ae-165">For more information about how to use **OpenProperty** with attachments, see the **PR_ATTACH_DATA_OBJ** property and [Opening an Attachment](opening-an-attachment.md).</span></span>
  
<span data-ttu-id="c95ae-166">N’utilisez pas le pointeur **IStream** que vous recevez pour appeler la méthode son [Seek](http://msdn.microsoft.com/en-us/library/aa380043%28v=VS.85%29.aspx) ou [SetSize](http://msdn.microsoft.com/en-us/library/aa380044%28v=VS.85%29.aspx) sauf si vous utilisez une variable zéro position ou la taille.</span><span class="sxs-lookup"><span data-stu-id="c95ae-166">Do not use the **IStream** pointer that you receive to call either its [Seek](http://msdn.microsoft.com/en-us/library/aa380043%28v=VS.85%29.aspx) or [SetSize](http://msdn.microsoft.com/en-us/library/aa380044%28v=VS.85%29.aspx) method unless you use a zero position or size variable.</span></span> <span data-ttu-id="c95ae-167">En outre, ne comptez pas sur la valeur du paramètre de sortie _plibNewPosition_ renvoyé à partir de l’appel de la **méthode Seek** .</span><span class="sxs-lookup"><span data-stu-id="c95ae-167">Also, do not rely on the value of the  _plibNewPosition_ output parameter returned from the **Seek** call.</span></span> 
  
<span data-ttu-id="c95ae-168">Si vous appelez **OpenProperty** pour accéder à une propriété de l’interface **IStream** , utilisez uniquement cette interface pour apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="c95ae-168">If you call **OpenProperty** to access a property with the **IStream** interface, use only that interface to make changes to it.</span></span> <span data-ttu-id="c95ae-169">N’essayez pas de mettre à jour de la propriété avec les autres [IMAPIProp : IUnknown](imapipropiunknown.md) méthodes, telles que **SetProps** ou [IMAPIProp::DeleteProps](imapiprop-deleteprops.md).</span><span class="sxs-lookup"><span data-stu-id="c95ae-169">Do not attempt to update the property with any of the other [IMAPIProp : IUnknown](imapipropiunknown.md) methods, such as **SetProps** or [IMAPIProp::DeleteProps](imapiprop-deleteprops.md).</span></span> 
  
<span data-ttu-id="c95ae-170">N’essayez pas d’ouvrir une propriété avec **OpenProperty** plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="c95ae-170">Do not try to open a property with **OpenProperty** more than once.</span></span> <span data-ttu-id="c95ae-171">Les résultats ne sont pas définis, car ils peuvent varier d’un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c95ae-171">The results are undefined because they can vary from provider to provider.</span></span> 
  
<span data-ttu-id="c95ae-172">Si vous devez modifier la propriété ouverture, définissez l’indicateur ne.</span><span class="sxs-lookup"><span data-stu-id="c95ae-172">If you need to modify the property to be opened, set the MAPI_MODIFY flag.</span></span> <span data-ttu-id="c95ae-173">Si vous n’êtes pas certain que l’objet prend en charge la propriété, mais il devrait, définissez les indicateurs MAPI_CREATE et ne.</span><span class="sxs-lookup"><span data-stu-id="c95ae-173">If you are not sure whether the object supports the property but you think it should, set the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="c95ae-174">Chaque fois que MAPI_CREATE est défini, ne doit également être définie.</span><span class="sxs-lookup"><span data-stu-id="c95ae-174">Whenever MAPI_CREATE is set, MAPI_MODIFY must also be set.</span></span>
  
<span data-ttu-id="c95ae-175">Vous êtes responsable de refonte le pointeur d’interface retourné dans le paramètre _lppUnk_ à celui qui est approprié pour l’interface spécifiée dans le paramètre _lpiid_ .</span><span class="sxs-lookup"><span data-stu-id="c95ae-175">You are responsible for recasting the interface pointer returned in the  _lppUnk_ parameter to one that is appropriate for the interface specified in the  _lpiid_ parameter.</span></span> <span data-ttu-id="c95ae-176">Vous devez également utiliser le pointeur retourné pour appeler la méthode [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) lorsque vous avez terminé avec lui.</span><span class="sxs-lookup"><span data-stu-id="c95ae-176">You must also use the returned pointer to call its [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method when you are finished with it.</span></span> 
  
<span data-ttu-id="c95ae-177">Parfois, les indicateurs de la configuration dans le paramètre _ulFlags_ n’est pas suffisant pour indiquer le type d’accès à la propriété est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="c95ae-177">Sometimes setting the flags in the  _ulFlags_ parameter is not enough to indicate the type of access to the property that is required.</span></span> <span data-ttu-id="c95ae-178">Vous pouvez placer des données supplémentaires, telles que les indicateurs, dans le paramètre _ulInterfaceOptions_ .</span><span class="sxs-lookup"><span data-stu-id="c95ae-178">You can put additional data, such as flags, in the  _ulInterfaceOptions_ parameter.</span></span> <span data-ttu-id="c95ae-179">Ces données sont selon l’interface.</span><span class="sxs-lookup"><span data-stu-id="c95ae-179">This data is interface dependent.</span></span> <span data-ttu-id="c95ae-180">Utilisent des interfaces (par exemple, **IStream**) et d’autres pas.</span><span class="sxs-lookup"><span data-stu-id="c95ae-180">Some interfaces (such as **IStream**) use it, and others do not.</span></span> <span data-ttu-id="c95ae-181">Par exemple, lorsque vous ouvrez une propriété modifiée avec **IStream**, définir l’indicateur STGM_WRITE dans le paramètre _ulInterfaceOptions_ outre ne.</span><span class="sxs-lookup"><span data-stu-id="c95ae-181">For example, when you open a property to be modified with **IStream**, set the STGM_WRITE flag in the  _ulInterfaceOptions_ parameter in addition to MAPI_MODIFY.</span></span> <span data-ttu-id="c95ae-182">Lorsque vous ouvrez un tableau à l’aide de l’interface [IMAPITable](imapitableiunknown.md) , vous pouvez définir _ulInterfaceOptions_ sur MAPI_UNICODE pour indiquer si les colonnes de la table contenant les propriétés de type chaîne doivent être au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="c95ae-182">When you open a table by using the [IMAPITable](imapitableiunknown.md) interface, you can set  _ulInterfaceOptions_ to MAPI_UNICODE to indicate whether the columns in the table that hold string properties should be in Unicode format.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c95ae-183">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c95ae-183">MFCMAPI reference</span></span>

<span data-ttu-id="c95ae-184">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c95ae-184">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c95ae-185">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="c95ae-185">**File**</span></span>|<span data-ttu-id="c95ae-186">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="c95ae-186">**Function**</span></span>|<span data-ttu-id="c95ae-187">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="c95ae-187">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c95ae-188">StreamEditor.cpp</span><span class="sxs-lookup"><span data-stu-id="c95ae-188">StreamEditor.cpp</span></span>  <br/> |<span data-ttu-id="c95ae-189">CStreamEditor::ReadTextStreamFromProperty</span><span class="sxs-lookup"><span data-stu-id="c95ae-189">CStreamEditor::ReadTextStreamFromProperty</span></span>  <br/> |<span data-ttu-id="c95ae-190">MFCMAPI utilise la méthode **IMAPIProp::OpenProperty** pour récupérer une interface de flux de texte de grande taille et propriétés binaires.</span><span class="sxs-lookup"><span data-stu-id="c95ae-190">MFCMAPI uses the **IMAPIProp::OpenProperty** method to retrieve a stream interface for large text and binary properties.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c95ae-191">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c95ae-191">See also</span></span>

- [<span data-ttu-id="c95ae-192">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="c95ae-192">HrIStorageFromStream</span></span>](hristoragefromstream.md) 
- [<span data-ttu-id="c95ae-193">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="c95ae-193">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md) 
- [<span data-ttu-id="c95ae-194">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="c95ae-194">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="c95ae-195">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="c95ae-195">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
- [<span data-ttu-id="c95ae-196">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="c95ae-196">IMAPISupport::IStorageFromStream</span></span>](imapisupport-istoragefromstream.md)
- [<span data-ttu-id="c95ae-197">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c95ae-197">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
- [<span data-ttu-id="c95ae-198">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c95ae-198">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
- [<span data-ttu-id="c95ae-199">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="c95ae-199">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
- [<span data-ttu-id="c95ae-200">L’ouverture d’une pièce jointe</span><span class="sxs-lookup"><span data-stu-id="c95ae-200">Opening an Attachment</span></span>](opening-an-attachment.md)

