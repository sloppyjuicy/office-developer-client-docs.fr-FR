---
title: IMAPISupportDoCopyTo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyTo
api_type:
- COM
ms.assetid: 84019475-5176-4fc5-a3ee-871095077498
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6f6c802f1d5ead1750c05fafc54533487fe3732a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331807"
---
# <a name="imapisupportdocopyto"></a><span data-ttu-id="151bd-103">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="151bd-103">IMAPISupport::DoCopyTo</span></span>

  
  
<span data-ttu-id="151bd-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="151bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="151bd-105">Copie ou déplace toutes les propriétés d’un objet, à l’exception des propriétés spécifiquement exclues, vers un autre objet.</span><span class="sxs-lookup"><span data-stu-id="151bd-105">Copies or moves all properties of one object, except for specifically excluded properties, to another object.</span></span>
  
```cpp
HRESULT DoCopyTo(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  ULONG ciidExclude,
  LPCIID rgiidExclude,
  LPSPropTagArray lpExcludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpDestInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="151bd-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="151bd-106">Parameters</span></span>

 <span data-ttu-id="151bd-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="151bd-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="151bd-108">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’objet qui possède les propriétés à copier ou à déplacer.</span><span class="sxs-lookup"><span data-stu-id="151bd-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="151bd-109">_lpSrcObj_</span><span class="sxs-lookup"><span data-stu-id="151bd-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="151bd-110">[in] Pointeur vers l’objet qui possède les propriétés à copier ou déplacer.</span><span class="sxs-lookup"><span data-stu-id="151bd-110">[in] A pointer to the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="151bd-111">_ciidExclude_</span><span class="sxs-lookup"><span data-stu-id="151bd-111">_ciidExclude_</span></span>
  
> <span data-ttu-id="151bd-112">[in] Nombre d’interfaces à exclure lorsque vous copiez ou déplacez des propriétés.</span><span class="sxs-lookup"><span data-stu-id="151bd-112">[in] The count of interfaces to exclude when you copy or move properties.</span></span>
    
 <span data-ttu-id="151bd-113">_tricidExclude_</span><span class="sxs-lookup"><span data-stu-id="151bd-113">_rgiidExclude_</span></span>
  
> <span data-ttu-id="151bd-114">[in] Tableau d’identificateurs d’interface qui indique les interfaces qui ne doivent pas être utilisées lorsque vous copiez ou déplacez des informations supplémentaires vers l’objet de destination.</span><span class="sxs-lookup"><span data-stu-id="151bd-114">[in] An array of interface identifiers that indicates interfaces that should not be used when you copy or move supplemental information to the destination object.</span></span>
    
 <span data-ttu-id="151bd-115">_lpExcludeProps_</span><span class="sxs-lookup"><span data-stu-id="151bd-115">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="151bd-116">[in] Pointeur vers un tableau de balises de propriétés qui identifie les balises de propriété qui doivent être exclues de l’opération de copie ou de déplacement.</span><span class="sxs-lookup"><span data-stu-id="151bd-116">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="151bd-117">La transmission de null dans  _le paramètre lpExcludeProps_ indique que toutes les propriétés de l’objet doivent être copiées ou déplacées.</span><span class="sxs-lookup"><span data-stu-id="151bd-117">Passing NULL in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="151bd-118">**DoCopyTo** renvoie MAPI_E_INVALID_PARAMETER lorsque le membre **cValues** de la structure [SPropTagArray](sproptagarray.md) pointée par  _lpExcludeProps_ est définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="151bd-118">**DoCopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="151bd-119">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="151bd-119">_ulUIParam_</span></span>
  
> <span data-ttu-id="151bd-120">[in] Handle vers la fenêtre parent de l’indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="151bd-120">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="151bd-121">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="151bd-121">_lpProgress_</span></span>
  
> <span data-ttu-id="151bd-122">[in] Pointeur vers une implémentation d’indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="151bd-122">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="151bd-123">Si NULL est transmis dans  _le paramètre lpProgress,_ MAPI fournit l’implémentation de progression.</span><span class="sxs-lookup"><span data-stu-id="151bd-123">If NULL is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="151bd-124">Le _paramètre lpProgress est_ ignoré, sauf si l’MAPI_DIALOG est définie dans le paramètre _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="151bd-124">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="151bd-125">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="151bd-125">_lpDestInterface_</span></span>
  
> <span data-ttu-id="151bd-126">[in] Pointeur vers l’identificateur d’interface qui représente l’interface à utiliser pour accéder à l’objet afin de recevoir les propriétés copiées ou déplacées.</span><span class="sxs-lookup"><span data-stu-id="151bd-126">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="151bd-127">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="151bd-127">_lpDestObj_</span></span>
  
> <span data-ttu-id="151bd-128">[in] Pointeur vers l’objet pour recevoir les propriétés copiées ou déplacées.</span><span class="sxs-lookup"><span data-stu-id="151bd-128">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="151bd-129">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="151bd-129">_ulFlags_</span></span>
  
> <span data-ttu-id="151bd-130">[in] Masque de bits d’indicateurs qui contrôle l’opération de copie ou de déplacement.</span><span class="sxs-lookup"><span data-stu-id="151bd-130">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="151bd-131">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="151bd-131">The following flags can be set:</span></span>
    
<span data-ttu-id="151bd-132">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="151bd-132">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="151bd-133">Affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="151bd-133">Displays a progress indicator.</span></span> 
    
<span data-ttu-id="151bd-134">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="151bd-134">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="151bd-135">**DoCopyTo doit** effectuer une opération de déplacement au lieu d’une opération de copie.</span><span class="sxs-lookup"><span data-stu-id="151bd-135">**DoCopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="151bd-136">Lorsque cet indicateur n’est pas définie, **DoCopyTo** effectue une opération de copie.</span><span class="sxs-lookup"><span data-stu-id="151bd-136">When this flag is not set, **DoCopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="151bd-137">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="151bd-137">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="151bd-138">Les propriétés existantes dans l’objet de destination ne doivent pas être écrasées.</span><span class="sxs-lookup"><span data-stu-id="151bd-138">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="151bd-139">Lorsque cet indicateur n’est pas définie, **DoCopyTo** se place sur les propriétés existantes.</span><span class="sxs-lookup"><span data-stu-id="151bd-139">When this flag is not set, **DoCopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="151bd-140">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="151bd-140">_lppProblems_</span></span>
  
> <span data-ttu-id="151bd-141">[out] Lors de l’entrée, un pointeur vers un pointeur vers une structure [SPropProblemArray](spropproblemarray.md) ; dans le cas contraire, NULL, qui indique qu’il n’est pas nécessaire d’obtenir des informations sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="151bd-141">[out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="151bd-142">Si  _lppProblems est_ un pointeur valide sur l’entrée, **DoCopyTo** renvoie des informations détaillées sur les erreurs de copie d’une ou plusieurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="151bd-142">If  _lppProblems_ is a valid pointer on input, **DoCopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="151bd-143">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="151bd-143">Return value</span></span>

<span data-ttu-id="151bd-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="151bd-144">S_OK</span></span> 
  
> <span data-ttu-id="151bd-145">Les propriétés ont été correctement copiées ou déplacées.</span><span class="sxs-lookup"><span data-stu-id="151bd-145">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="151bd-146">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="151bd-146">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="151bd-147">Une propriété à copier ou à déplacer existe déjà dans l’objet de destination et l’MAPI_NOREPLACE est définie.</span><span class="sxs-lookup"><span data-stu-id="151bd-147">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="151bd-148">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="151bd-148">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="151bd-149">L’objet source contient directement ou indirectement l’objet de destination.</span><span class="sxs-lookup"><span data-stu-id="151bd-149">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="151bd-150">Des travaux importants ont peut-être été effectués avant la découverte de cette condition, de sorte que les objets source et de destination peuvent être partiellement modifiés.</span><span class="sxs-lookup"><span data-stu-id="151bd-150">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="151bd-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="151bd-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="151bd-152">L’interface identifiée par le paramètre  _lpSrcInterface_ n’est pas prise en charge par l’objet pointé par  _lpSrcObj_ ou l’interface identifiée par le paramètre  _lpDestInterface_ n’est pas prise en charge par l’objet pointé par  _lpDestObj_.</span><span class="sxs-lookup"><span data-stu-id="151bd-152">The interface identified by the  _lpSrcInterface_ parameter is not supported by the object pointed to by  _lpSrcObj_, or the interface identified by the  _lpDestInterface_ parameter is not supported by the object pointed to by  _lpDestObj_.</span></span> 
    
<span data-ttu-id="151bd-153">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="151bd-153">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="151bd-154">Une tentative d’accès à un objet pour lequel l’appelant ne dispose pas des autorisations suffisantes a été tentée.</span><span class="sxs-lookup"><span data-stu-id="151bd-154">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="151bd-155">Cette erreur est renvoyée si l’objet de destination est identique à l’objet source.</span><span class="sxs-lookup"><span data-stu-id="151bd-155">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="151bd-156">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="151bd-156">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="151bd-157">Le  _paramètre lpSrcInterface_ est NULL.</span><span class="sxs-lookup"><span data-stu-id="151bd-157">The  _lpSrcInterface_ parameter is NULL.</span></span> 
    
<span data-ttu-id="151bd-158">Les valeurs suivantes peuvent être renvoyées dans la structure **SPropProblemArray,** mais pas en tant que valeurs de retour **pour DoCopyTo**.</span><span class="sxs-lookup"><span data-stu-id="151bd-158">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyTo**.</span></span> <span data-ttu-id="151bd-159">Ces erreurs s’appliquent à une seule propriété.</span><span class="sxs-lookup"><span data-stu-id="151bd-159">These errors apply to a single property.</span></span>
  
<span data-ttu-id="151bd-160">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="151bd-160">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="151bd-161">L’MAPI_UNICODE a été définie et **DoCopyTo** ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et **DoCopyTo** prend uniquement en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="151bd-161">Either the MAPI_UNICODE flag was set and **DoCopyTo** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="151bd-162">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="151bd-162">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="151bd-163">La propriété ne peut pas être modifiée par l’appelant, car il s’agit d’une propriété en lecture seule, calculée par le propriétaire de l’objet de destination.</span><span class="sxs-lookup"><span data-stu-id="151bd-163">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="151bd-164">Cette erreur n’est pas grave ; L’appelant doit autoriser la continuer l’opération de copie.</span><span class="sxs-lookup"><span data-stu-id="151bd-164">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="151bd-165">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="151bd-165">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="151bd-166">Le type de propriété n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="151bd-166">The property type is invalid.</span></span>
    
<span data-ttu-id="151bd-167">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="151bd-167">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="151bd-168">Le type de propriété n’est pas le type attendu par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="151bd-168">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="151bd-169">Remarques</span><span class="sxs-lookup"><span data-stu-id="151bd-169">Remarks</span></span>

<span data-ttu-id="151bd-170">La **méthode IMAPISupport::D oCopyTo** est implémentée pour les objets de prise en charge du fournisseur de magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="151bd-170">The **IMAPISupport::DoCopyTo** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="151bd-171">Les fournisseurs de magasins de messages peuvent appeler **DoCopyTo** pour implémenter la méthode [IMAPIProp::CopyTo](imapiprop-copyto.md) pour leurs dossiers et messages.</span><span class="sxs-lookup"><span data-stu-id="151bd-171">Message store providers can call **DoCopyTo** to implement the [IMAPIProp::CopyTo](imapiprop-copyto.md) method for their folders and messages.</span></span> 
  
<span data-ttu-id="151bd-172">Par défaut, **DoCopyTo** copie ou déplace toutes les propriétés d’un objet vers un autre objet.</span><span class="sxs-lookup"><span data-stu-id="151bd-172">By default, **DoCopyTo** copies or moves all of the properties of one object to another object.</span></span> <span data-ttu-id="151bd-173">Tous les sous-objets de l’objet source sont automatiquement inclus dans l’opération et copiés ou déplacés dans leur intégralité.</span><span class="sxs-lookup"><span data-stu-id="151bd-173">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety.</span></span> 
  
<span data-ttu-id="151bd-174">Si l’une des propriétés copiées ou déplacées existe déjà dans l’objet de destination, les propriétés existantes sont écrasées par les nouvelles propriétés, sauf si l’indicateur MAPI_NOREPLACE est définie dans le paramètre _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="151bd-174">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="151bd-175">Les informations existantes dans l’objet de destination qui ne sont pas écrasées restent intactes.</span><span class="sxs-lookup"><span data-stu-id="151bd-175">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="151bd-176">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="151bd-176">Notes to callers</span></span>

<span data-ttu-id="151bd-177">Pour exclure des propriétés de l’opération de copie ou de déplacement, incluez leurs balises de propriété dans le paramètre _lpExcludeProps._</span><span class="sxs-lookup"><span data-stu-id="151bd-177">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="151bd-178">Si vous passez les résultats de l’utilisation de la macro [PROP_TAG](prop_tag.md) pour créer une balise de propriété à partir d’un identificateur spécifique dans le tableau de balises de propriétés, toutes les propriétés avec cet identificateur seront exclues.</span><span class="sxs-lookup"><span data-stu-id="151bd-178">If you pass the results of using the [PROP_TAG](prop_tag.md) macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="151bd-179">Par exemple, l’entrée suivante dans le tableau de balises de propriétés exclut toutes les propriétés dont l’identificateur est 0x8002, quel que soit le type :</span><span class="sxs-lookup"><span data-stu-id="151bd-179">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="151bd-180">Pour éviter de copier le temps de remise d’un message lorsque vous copiez le message dans un autre dossier, spécifiez **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) dans le tableau d’exclusion de balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="151bd-180">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="151bd-181">Pour exclure la liste des destinataires d’un message, ajoutez la propriété **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) au tableau d’exclusion.</span><span class="sxs-lookup"><span data-stu-id="151bd-181">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="151bd-182">Pour exclure les pièces jointes d’un message, ajoutez la propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) au tableau.</span><span class="sxs-lookup"><span data-stu-id="151bd-182">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="151bd-183">De même, pour empêcher la copie ou le déplacement de la hiérarchie ou de la table des matières d’un conteneur de dossier ou de carnet d’adresses, incluez **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) dans le tableau d’exclusion de balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="151bd-183">Similarly, to prevent the copying or moving of a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="151bd-184">Ignorez MAPI_E_COMPUTED erreurs renvoyées dans la structure **SPropProblemArray** dans le paramètre _lppProblems._</span><span class="sxs-lookup"><span data-stu-id="151bd-184">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
<span data-ttu-id="151bd-185">L’identificateur d’interface vers qui _pointe lpSrcInterface_ est généralement identique à l’identificateur d’interface vers qui _pointe lpDestInterface._</span><span class="sxs-lookup"><span data-stu-id="151bd-185">The interface identifier that  _lpSrcInterface_ points to is usually the same as the interface identifier that  _lpDestInterface_ points to.</span></span> 
  
<span data-ttu-id="151bd-186">Si vous passez un identificateur d’interface acceptable dans  _lpDestInterface_ mais un pointeur non valide dans  _lpDestObj,_ les résultats sont imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="151bd-186">If you pass an acceptable interface identifier in  _lpDestInterface_ but an invalid pointer in  _lpDestObj_, the results are unpredictable.</span></span> <span data-ttu-id="151bd-187">Il est très probable que cela entraîne l’échec de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="151bd-187">Most likely this will cause your provider to fail.</span></span> 
  
<span data-ttu-id="151bd-188">À l’inverse, si vous avez connaissance d’informations supplémentaires qui ne doivent pas être copiées ou déplacées, ajoutez les identificateurs d’interface pour les interfaces à exclure dans le tableau transmis dans le paramètre _converseidExclude._</span><span class="sxs-lookup"><span data-stu-id="151bd-188">Conversely, if you are aware of supplemental information that should not be copied or moved, add the interface identifiers for the interfaces to be excluded in the array passed in the  _rgiidExclude_ parameter.</span></span> <span data-ttu-id="151bd-189">Par exemple, si vous copiez des messages, mais pas leurs pièces jointes, passez IID_IMessage dans le tableau _eaidExclude._</span><span class="sxs-lookup"><span data-stu-id="151bd-189">For example, if you are copying messages, but not any of their message attachments, pass IID_IMessage in the  _rgiidExclude_ array.</span></span> <span data-ttu-id="151bd-190">**DoCopyTo** ignore les interfaces répertoriées dans  _rgidExclude_ qu’il ne reconnaît pas.</span><span class="sxs-lookup"><span data-stu-id="151bd-190">**DoCopyTo** ignores any interfaces listed in  _rgiidExclude_ that it does not recognize.</span></span> 
  
<span data-ttu-id="151bd-191">Lorsque vous utilisez le  _paramètre autantidExclude_ que pour exclure une interface, il exclut également toutes les interfaces dérivées de cette interface.</span><span class="sxs-lookup"><span data-stu-id="151bd-191">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="151bd-192">Par exemple, l’exclusion de l’interface [IMAPIContainer](imapicontainerimapiprop.md) entraîne l’exclusion des dossiers ou des conteneurs de carnet d’adresses, selon le type de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="151bd-192">For example, excluding the [IMAPIContainer](imapicontainerimapiprop.md) interface causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="151bd-193">N’excluez [pas IMAPIProp](imapipropiunknown.md) ou [IUnknown,](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) car de nombreuses interfaces en dérivent.</span><span class="sxs-lookup"><span data-stu-id="151bd-193">Do not exclude [IMAPIProp](imapipropiunknown.md) or [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) because so many interfaces derive from them.</span></span> 
  
 <span data-ttu-id="151bd-194">**DoCopyTo signale les** erreurs globales qui s’appliquent à l’opération dans son ensemble et les erreurs individuelles qui s’appliquent à des propriétés individuelles.</span><span class="sxs-lookup"><span data-stu-id="151bd-194">**DoCopyTo** reports global errors that apply to the operation as a whole, and individual errors that apply to individual properties.</span></span> <span data-ttu-id="151bd-195">Ces erreurs individuelles sont mises dans une structure **SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="151bd-195">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="151bd-196">Vous pouvez supprimer le rapport d’erreurs au niveau de la propriété en passant NULL, plutôt qu’un pointeur valide, pour le paramètre de structure de tableau de problème de propriété.</span><span class="sxs-lookup"><span data-stu-id="151bd-196">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="151bd-197">Si vous souhaitez recevoir des informations sur les erreurs, passez un pointeur de structure **SPropProblemArray** valide dans le paramètre _lppProblems._</span><span class="sxs-lookup"><span data-stu-id="151bd-197">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="151bd-198">Lorsque **DoCopyTo renvoie** S_OK, recherchez les erreurs possibles avec des propriétés individuelles dans la structure.</span><span class="sxs-lookup"><span data-stu-id="151bd-198">When **DoCopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="151bd-199">Lorsque **DoCopyTo renvoie** une erreur, aucune information n’est renvoyée dans la structure **SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="151bd-199">When **DoCopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="151bd-200">Appelez plutôt la [méthode IMAPISupport::GetLastError](imapisupport-getlasterror.md) pour récupérer des informations détaillées sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="151bd-200">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="151bd-201">Si **DoCopyTo renvoie** S_OK, libérez la structure **SPropProblemArray** renvoyée en appelant la [fonction MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="151bd-201">If **DoCopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="151bd-202">Si une erreur globale se produit lors de l’appel **DoCopyTo,** n’utilisez pas ou ne llibérez pas la structure **SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="151bd-202">If a global error occurs on the **DoCopyTo** call, do not use or free the **SPropProblemArray** structure.</span></span> <span data-ttu-id="151bd-203">Les fournisseurs doivent ignorer le  _membre ulIndex_ dans les structures **SPropProblemArray** renvoyées par **DoCopyTo**.</span><span class="sxs-lookup"><span data-stu-id="151bd-203">Providers should ignore the  _ulIndex_ member in **SPropProblemArray** structures returned by **DoCopyTo**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="151bd-204">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="151bd-204">See also</span></span>



[<span data-ttu-id="151bd-205">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="151bd-205">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="151bd-206">IMAPISupport::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="151bd-206">IMAPISupport::CopyFolder</span></span>](imapisupport-copyfolder.md)
  
[<span data-ttu-id="151bd-207">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="151bd-207">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="151bd-208">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="151bd-208">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="151bd-209">Propriété canonique PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="151bd-209">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="151bd-210">Propriété canonique PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="151bd-210">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="151bd-211">Propriété canonique PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="151bd-211">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="151bd-212">Propriété canonique PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="151bd-212">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="151bd-213">Propriété canonique PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="151bd-213">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="151bd-214">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="151bd-214">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="151bd-215">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="151bd-215">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="151bd-216">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="151bd-216">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

