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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7bf1d6912e44319c36e288cd3870218e8c4e45ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319809"
---
# <a name="imapipropopenproperty"></a><span data-ttu-id="07e34-103">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="07e34-103">IMAPIProp::OpenProperty</span></span>

<span data-ttu-id="07e34-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07e34-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07e34-105">Renvoie un pointeur vers une interface qui peut être utilisée pour accéder à une propriété.</span><span class="sxs-lookup"><span data-stu-id="07e34-105">Returns a pointer to an interface that can be used to access a property.</span></span>
  
```cpp
HRESULT OpenProperty(
  ULONG ulPropTag,
  LPCIID lpiid,
  ULONG ulInterfaceOptions,
  ULONG ulFlags,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="07e34-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="07e34-106">Parameters</span></span>

 <span data-ttu-id="07e34-107">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="07e34-107">_ulPropTag_</span></span>
  
> <span data-ttu-id="07e34-108">[in] Balise de propriété de la propriété à accéder.</span><span class="sxs-lookup"><span data-stu-id="07e34-108">[in] The property tag for the property to be accessed.</span></span> <span data-ttu-id="07e34-109">L’identificateur et le type doivent être inclus dans la balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="07e34-109">Both the identifier and the type must be included in the property tag.</span></span>
    
 <span data-ttu-id="07e34-110">_lpiid_</span><span class="sxs-lookup"><span data-stu-id="07e34-110">_lpiid_</span></span>
  
> <span data-ttu-id="07e34-111">[in] Pointeur vers l’identificateur de l’interface à utiliser pour accéder à la propriété.</span><span class="sxs-lookup"><span data-stu-id="07e34-111">[in] A pointer to the identifier for the interface to be used to access the property.</span></span> <span data-ttu-id="07e34-112">Le  _paramètre lpiid_ ne doit pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="07e34-112">The  _lpiid_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="07e34-113">_ulInterfaceOptions_</span><span class="sxs-lookup"><span data-stu-id="07e34-113">_ulInterfaceOptions_</span></span>
  
> <span data-ttu-id="07e34-114">[in] Données liées à l’interface identifiée par _le paramètre lpiid._</span><span class="sxs-lookup"><span data-stu-id="07e34-114">[in] Data that relates to the interface identified by the  _lpiid_ parameter.</span></span> 
    
 <span data-ttu-id="07e34-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="07e34-115">_ulFlags_</span></span>
  
> <span data-ttu-id="07e34-116">[in] Masque de bits d’indicateurs qui contrôle l’accès à la propriété.</span><span class="sxs-lookup"><span data-stu-id="07e34-116">[in] A bitmask of flags that controls access to the property.</span></span> <span data-ttu-id="07e34-117">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="07e34-117">The following flags can be set:</span></span>
    
<span data-ttu-id="07e34-118">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="07e34-118">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="07e34-119">Si la propriété n’existe pas, elle doit être créée.</span><span class="sxs-lookup"><span data-stu-id="07e34-119">If the property does not exist, it should be created.</span></span> <span data-ttu-id="07e34-120">Si la propriété existe, la valeur actuelle de la propriété doit être ignorée.</span><span class="sxs-lookup"><span data-stu-id="07e34-120">If the property does exist, the current value of the property should be discarded.</span></span> <span data-ttu-id="07e34-121">Lorsqu’un appelant définit l’MAPI_CREATE, il doit également définir l’MAPI_MODIFY’indicateur.</span><span class="sxs-lookup"><span data-stu-id="07e34-121">When a caller sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="07e34-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="07e34-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="07e34-123">Permet à **OpenProperty de** renvoyer correctement, éventuellement avant que l’objet soit entièrement disponible pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="07e34-123">Allows **OpenProperty** to return successfully, possibly before the object is fully available to the caller.</span></span> <span data-ttu-id="07e34-124">Si l’objet n’est pas disponible, effectuer un appel d’objet ultérieur peut occasioner une erreur.</span><span class="sxs-lookup"><span data-stu-id="07e34-124">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="07e34-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="07e34-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="07e34-126">MAPI_MODIFY est nécessaire dans les situations ci-après :</span><span class="sxs-lookup"><span data-stu-id="07e34-126">MAPI_MODIFY is required in these situations:</span></span>
    
  - <span data-ttu-id="07e34-127">Lors de l’ouverture d’une propriété de **flux, IID_IStream**, pour la modifier.</span><span class="sxs-lookup"><span data-stu-id="07e34-127">When opening a stream property, such as **IID_IStream**, to modify it.</span></span>
    
  - <span data-ttu-id="07e34-128">Lors de l’ouverture d’une pièce jointe de message incorporée, [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) ouverte avec **IID_IMessage,** pour la modifier.</span><span class="sxs-lookup"><span data-stu-id="07e34-128">When opening an embedded message attachment, such as [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) opened with **IID_IMessage**, to modify it.</span></span>
    
 <span data-ttu-id="07e34-129">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="07e34-129">_lppUnk_</span></span>
  
> <span data-ttu-id="07e34-130">[out] Pointeur vers l’interface demandée à utiliser pour l’accès aux propriétés.</span><span class="sxs-lookup"><span data-stu-id="07e34-130">[out] A pointer to the requested interface to be used for property access.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="07e34-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="07e34-131">Return value</span></span>

<span data-ttu-id="07e34-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="07e34-132">S_OK</span></span> 
  
> <span data-ttu-id="07e34-133">Le pointeur d’interface demandé a été renvoyé avec succès.</span><span class="sxs-lookup"><span data-stu-id="07e34-133">The requested interface pointer was successfully returned.</span></span>
    
<span data-ttu-id="07e34-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="07e34-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="07e34-135">L’interface demandée n’est pas prise en charge pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="07e34-135">The requested interface is not supported for this property.</span></span>
    
<span data-ttu-id="07e34-136">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="07e34-136">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="07e34-137">L’appelant ne dispose pas des autorisations suffisantes pour accéder à la propriété.</span><span class="sxs-lookup"><span data-stu-id="07e34-137">The caller has insufficient permissions to access the property.</span></span>
    
<span data-ttu-id="07e34-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="07e34-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="07e34-139">L’objet ne peut pas fournir l’accès à cette propriété via l’interface demandée.</span><span class="sxs-lookup"><span data-stu-id="07e34-139">The object cannot provide access to this property through the requested interface.</span></span>
    
<span data-ttu-id="07e34-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="07e34-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="07e34-141">La propriété demandée n’existe pas et MAPI_CREATE n’a pas été définie dans le _paramètre ulFlags._</span><span class="sxs-lookup"><span data-stu-id="07e34-141">The requested property does not exist and MAPI_CREATE was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="07e34-142">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="07e34-142">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="07e34-143">Le type de propriété dans la balise est PT_UNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="07e34-143">The property type in the tag is set to PT_UNSPECIFIED.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="07e34-144">Remarques</span><span class="sxs-lookup"><span data-stu-id="07e34-144">Remarks</span></span>

<span data-ttu-id="07e34-145">La **méthode IMAPIProp::OpenProperty** permet d’accéder à une propriété via une interface particulière.</span><span class="sxs-lookup"><span data-stu-id="07e34-145">The **IMAPIProp::OpenProperty** method provides access to a property through a particular interface.</span></span> <span data-ttu-id="07e34-146">**OpenProperty** est une alternative aux méthodes [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPIProp::SetProps.](imapiprop-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="07e34-146">**OpenProperty** is an alternative to the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="07e34-147">Lorsque **GetProps ou** **SetProps échoue** parce que la propriété est trop grande ou trop complexe, appelez **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="07e34-147">When either **GetProps** or **SetProps** fails because the property is too large or too complex, call **OpenProperty**.</span></span> <span data-ttu-id="07e34-148">**OpenProperty est** généralement utilisé pour accéder aux propriétés de type PT_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="07e34-148">**OpenProperty** is typically used to access properties of type PT_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="07e34-149">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="07e34-149">Notes to callers</span></span>

<span data-ttu-id="07e34-150">Pour accéder aux pièces jointes des messages, ouvrez la propriété **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) avec un identificateur d’interface différent, en fonction du type de pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="07e34-150">To access message attachments, open the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property with a different interface identifier, depending on the type of attachment.</span></span> <span data-ttu-id="07e34-151">Le tableau suivant décrit comment appeler **OpenProperty** pour les différents types de pièces jointes :</span><span class="sxs-lookup"><span data-stu-id="07e34-151">The following table describes how to call **OpenProperty** for the different types of attachments:</span></span> 
  
|<span data-ttu-id="07e34-152">**Type de pièce jointe**</span><span class="sxs-lookup"><span data-stu-id="07e34-152">**Type of attachment**</span></span>|<span data-ttu-id="07e34-153">**Identificateur d’interface à utiliser**</span><span class="sxs-lookup"><span data-stu-id="07e34-153">**Interface identifier to use**</span></span>|
|:-----|:-----|
|<span data-ttu-id="07e34-154">Binaire</span><span class="sxs-lookup"><span data-stu-id="07e34-154">Binary</span></span>  <br/> |<span data-ttu-id="07e34-155">IID_IStream</span><span class="sxs-lookup"><span data-stu-id="07e34-155">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="07e34-156">String</span><span class="sxs-lookup"><span data-stu-id="07e34-156">String</span></span>  <br/> |<span data-ttu-id="07e34-157">IID_IStream</span><span class="sxs-lookup"><span data-stu-id="07e34-157">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="07e34-158">Message</span><span class="sxs-lookup"><span data-stu-id="07e34-158">Message</span></span>  <br/> |<span data-ttu-id="07e34-159">IID_IMessage</span><span class="sxs-lookup"><span data-stu-id="07e34-159">IID_IMessage</span></span>  <br/> |
|<span data-ttu-id="07e34-160">OLE 2.0</span><span class="sxs-lookup"><span data-stu-id="07e34-160">OLE 2.0</span></span>  <br/> |<span data-ttu-id="07e34-161">IID_IStreamDocfile</span><span class="sxs-lookup"><span data-stu-id="07e34-161">IID_IStreamDocfile</span></span>  <br/> |
   
<span data-ttu-id="07e34-162">**IStreamDocfile** est une dérivée de l’interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) basée sur un fichier composé OLE 2.0.</span><span class="sxs-lookup"><span data-stu-id="07e34-162">**IStreamDocfile** is a derivative of the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface that is based on an OLE 2.0 compound file.</span></span> <span data-ttu-id="07e34-163">**IStreamDocfile** est le meilleur choix pour accéder aux pièces jointes OLE 2.0, car il implique la charge de travail la moins importante.</span><span class="sxs-lookup"><span data-stu-id="07e34-163">**IStreamDocfile** is the best choice for accessing OLE 2.0 attachments because it involves the least amount of overhead.</span></span> <span data-ttu-id="07e34-164">Vous pouvez utiliser IID_IStreamDocFile pour les propriétés qui contiennent des données stockées dans un stockage structuré disponible via l’interface [IStorage.](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07e34-164">You can use IID_IStreamDocFile for those properties that contain data stored in structured storage available through the [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="07e34-165">Pour plus d’informations sur l’utilisation **d’OpenProperty** avec des pièces jointes, voir la **propriété PR_ATTACH_DATA_OBJ** et [l’ouverture d’une pièce jointe.](opening-an-attachment.md)</span><span class="sxs-lookup"><span data-stu-id="07e34-165">For more information about how to use **OpenProperty** with attachments, see the **PR_ATTACH_DATA_OBJ** property and [Opening an Attachment](opening-an-attachment.md).</span></span>
  
<span data-ttu-id="07e34-166">N’utilisez pas le pointeur **IStream** que vous recevez pour appeler sa méthode [Seek](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) ou [SetSize,](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) sauf si vous utilisez une variable de position ou de taille nulle.</span><span class="sxs-lookup"><span data-stu-id="07e34-166">Do not use the **IStream** pointer that you receive to call either its [Seek](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) or [SetSize](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) method unless you use a zero position or size variable.</span></span> <span data-ttu-id="07e34-167">En outre, ne vous appuyez pas sur la valeur du paramètre de sortie _plibNewPosition_ renvoyée par **l’appel Seek.**</span><span class="sxs-lookup"><span data-stu-id="07e34-167">Also, do not rely on the value of the  _plibNewPosition_ output parameter returned from the **Seek** call.</span></span> 
  
<span data-ttu-id="07e34-168">Si vous appelez **OpenProperty** pour accéder à une propriété avec l’interface **IStream,** utilisez uniquement cette interface pour y apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="07e34-168">If you call **OpenProperty** to access a property with the **IStream** interface, use only that interface to make changes to it.</span></span> <span data-ttu-id="07e34-169">N’essayez pas de mettre à jour la propriété avec les autres méthodes [IMAPIProp : IUnknown,](imapipropiunknown.md) telles que **SetProps** ou [IMAPIProp::D eleteProps](imapiprop-deleteprops.md).</span><span class="sxs-lookup"><span data-stu-id="07e34-169">Do not attempt to update the property with any of the other [IMAPIProp : IUnknown](imapipropiunknown.md) methods, such as **SetProps** or [IMAPIProp::DeleteProps](imapiprop-deleteprops.md).</span></span> 
  
<span data-ttu-id="07e34-170">N’essayez pas d’ouvrir une propriété avec **OpenProperty** plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="07e34-170">Do not try to open a property with **OpenProperty** more than once.</span></span> <span data-ttu-id="07e34-171">Les résultats ne sont pas indéfinis, car ils peuvent varier d’un fournisseur à l’autre.</span><span class="sxs-lookup"><span data-stu-id="07e34-171">The results are undefined because they can vary from provider to provider.</span></span> 
  
<span data-ttu-id="07e34-172">Si vous avez besoin de modifier la propriété à ouvrir, définissez l’MAPI_MODIFY’indicateur.</span><span class="sxs-lookup"><span data-stu-id="07e34-172">If you need to modify the property to be opened, set the MAPI_MODIFY flag.</span></span> <span data-ttu-id="07e34-173">Si vous ne savez pas si l’objet prend en charge la propriété, mais vous pensez qu’elle le devrait, définissez les MAPI_CREATE et MAPI_MODIFY indicateurs.</span><span class="sxs-lookup"><span data-stu-id="07e34-173">If you are not sure whether the object supports the property but you think it should, set the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="07e34-174">Chaque MAPI_CREATE est définie, MAPI_MODIFY doit également être définie.</span><span class="sxs-lookup"><span data-stu-id="07e34-174">Whenever MAPI_CREATE is set, MAPI_MODIFY must also be set.</span></span>
  
<span data-ttu-id="07e34-175">Vous êtes responsable de la rediffusion du pointeur d’interface renvoyé dans le paramètre _lppUnk_ sur un point approprié pour l’interface spécifiée dans le _paramètre lpiid._</span><span class="sxs-lookup"><span data-stu-id="07e34-175">You are responsible for recasting the interface pointer returned in the  _lppUnk_ parameter to one that is appropriate for the interface specified in the  _lpiid_ parameter.</span></span> <span data-ttu-id="07e34-176">Vous devez également utiliser le pointeur renvoyé pour appeler sa méthode [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) lorsque vous en avez terminé.</span><span class="sxs-lookup"><span data-stu-id="07e34-176">You must also use the returned pointer to call its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method when you are finished with it.</span></span> 
  
<span data-ttu-id="07e34-177">Parfois, la définition des indicateurs dans le  _paramètre ulFlags_ n’est pas suffisante pour indiquer le type d’accès à la propriété qui est requis.</span><span class="sxs-lookup"><span data-stu-id="07e34-177">Sometimes setting the flags in the  _ulFlags_ parameter is not enough to indicate the type of access to the property that is required.</span></span> <span data-ttu-id="07e34-178">Vous pouvez placer des données supplémentaires, telles que des indicateurs, dans le _paramètre ulInterfaceOptions._</span><span class="sxs-lookup"><span data-stu-id="07e34-178">You can put additional data, such as flags, in the  _ulInterfaceOptions_ parameter.</span></span> <span data-ttu-id="07e34-179">Ces données dépendent de l’interface.</span><span class="sxs-lookup"><span data-stu-id="07e34-179">This data is interface dependent.</span></span> <span data-ttu-id="07e34-180">Certaines interfaces (telles que **IStream)** l’utilisent, tandis que d’autres ne l’utilisent pas.</span><span class="sxs-lookup"><span data-stu-id="07e34-180">Some interfaces (such as **IStream**) use it, and others do not.</span></span> <span data-ttu-id="07e34-181">Par exemple, lorsque vous ouvrez une propriété à modifier avec **IStream,** définissez l’indicateur STGM_WRITE dans le paramètre  _ulInterfaceOptions_ en plus de MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="07e34-181">For example, when you open a property to be modified with **IStream**, set the STGM_WRITE flag in the  _ulInterfaceOptions_ parameter in addition to MAPI_MODIFY.</span></span> <span data-ttu-id="07e34-182">Lorsque vous ouvrez un tableau à l’aide de l’interface [IMAPITable,](imapitableiunknown.md) vous pouvez définir  _ulInterfaceOptions_ sur MAPI_UNICODE pour indiquer si les colonnes du tableau qui détiennent des propriétés de chaîne doivent être au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="07e34-182">When you open a table by using the [IMAPITable](imapitableiunknown.md) interface, you can set  _ulInterfaceOptions_ to MAPI_UNICODE to indicate whether the columns in the table that hold string properties should be in Unicode format.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="07e34-183">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="07e34-183">MFCMAPI reference</span></span>

<span data-ttu-id="07e34-184">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="07e34-184">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="07e34-185">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="07e34-185">**File**</span></span>|<span data-ttu-id="07e34-186">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="07e34-186">**Function**</span></span>|<span data-ttu-id="07e34-187">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="07e34-187">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="07e34-188">StreamEditor.cpp</span><span class="sxs-lookup"><span data-stu-id="07e34-188">StreamEditor.cpp</span></span>  <br/> |<span data-ttu-id="07e34-189">CStreamEditor::ReadTextStreamFromProperty</span><span class="sxs-lookup"><span data-stu-id="07e34-189">CStreamEditor::ReadTextStreamFromProperty</span></span>  <br/> |<span data-ttu-id="07e34-190">MFCMAPI utilise **la méthode IMAPIProp::OpenProperty** pour récupérer une interface de flux pour les propriétés binaires et de texte de grande taille.</span><span class="sxs-lookup"><span data-stu-id="07e34-190">MFCMAPI uses the **IMAPIProp::OpenProperty** method to retrieve a stream interface for large text and binary properties.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="07e34-191">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07e34-191">See also</span></span>

- [<span data-ttu-id="07e34-192">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="07e34-192">HrIStorageFromStream</span></span>](hristoragefromstream.md) 
- [<span data-ttu-id="07e34-193">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="07e34-193">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md) 
- [<span data-ttu-id="07e34-194">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="07e34-194">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="07e34-195">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="07e34-195">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
- [<span data-ttu-id="07e34-196">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="07e34-196">IMAPISupport::IStorageFromStream</span></span>](imapisupport-istoragefromstream.md)
- [<span data-ttu-id="07e34-197">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="07e34-197">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
- [<span data-ttu-id="07e34-198">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="07e34-198">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
- [<span data-ttu-id="07e34-199">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="07e34-199">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
- [<span data-ttu-id="07e34-200">Ouverture d’une pièce jointe</span><span class="sxs-lookup"><span data-stu-id="07e34-200">Opening an Attachment</span></span>](opening-an-attachment.md)

