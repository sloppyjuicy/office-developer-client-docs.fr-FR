---
title: IMAPISupportDoCopyProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyProps
api_type:
- COM
ms.assetid: 2446ef52-578a-4004-9719-de9b0207ccad
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a30a323874c847d9a08b00512cfd30ff3cf5c5ff
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591127"
---
# <a name="imapisupportdocopyprops"></a><span data-ttu-id="ff6e3-103">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="ff6e3-103">IMAPISupport::DoCopyProps</span></span>

  
  
<span data-ttu-id="ff6e3-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff6e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff6e3-105">Copie ou déplace une ou plusieurs propriétés d’un objet à un autre objet.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-105">Copies or moves one or more properties of an object to another object.</span></span>
  
```cpp
HRESULT DoCopyProps(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  LPSPropTagArray lpIncludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpDestInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="ff6e3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff6e3-106">Parameters</span></span>

 <span data-ttu-id="ff6e3-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="ff6e3-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="ff6e3-108">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’objet avec les propriétés à déplacer ou copier.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object with the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="ff6e3-109">_lpSrcObj_</span><span class="sxs-lookup"><span data-stu-id="ff6e3-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="ff6e3-110">[in] Pointeur vers l’objet qui contient les propriétés pour déplacer ou copier.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-110">[in] A pointer to the object that contains the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="ff6e3-111">_lpIncludeProps_</span><span class="sxs-lookup"><span data-stu-id="ff6e3-111">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="ff6e3-112">[in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau compté de balises de propriétés qui indiquent les propriétés pour copier ou déplacer.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-112">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains a counted array of property tags that indicate the properties to copy or move.</span></span> <span data-ttu-id="ff6e3-113">Le paramètre _lpIncludeProps_ ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-113">The  _lpIncludeProps_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="ff6e3-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="ff6e3-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="ff6e3-115">[in] Un handle vers la fenêtre parent de l’indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-115">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="ff6e3-116">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="ff6e3-116">_lpProgress_</span></span>
  
> <span data-ttu-id="ff6e3-117">[in] Pointeur vers une implémentation d’un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-117">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="ff6e3-118">Si NULL est indiqué dans le paramètre _lpProgress_ , l’indicateur de progression est affichée à l’aide de l’implémentation de MAPI.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-118">If NULL is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="ff6e3-119">Le paramètre _lpProgress_ est ignoré à moins que l’indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="ff6e3-119">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="ff6e3-120">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="ff6e3-120">_lpDestInterface_</span></span>
  
> <span data-ttu-id="ff6e3-121">[in] Pointeur vers l’identificateur d’interface qui représente l’interface à utiliser pour accéder à l’objet pour recevoir les propriétés qui sont copiées ou déplacées.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-121">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the properties that are copied or moved.</span></span>
    
 <span data-ttu-id="ff6e3-122">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="ff6e3-122">_lpDestObj_</span></span>
  
> <span data-ttu-id="ff6e3-123">[in] Pointeur vers l’objet à recevoir les propriétés copiées ou déplacées.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-123">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="ff6e3-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ff6e3-124">_ulFlags_</span></span>
  
> <span data-ttu-id="ff6e3-125">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’opération de copie ou de déplacement est effectuée.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-125">[in] A bitmask of flags that controls how the copy or move operation is performed.</span></span> <span data-ttu-id="ff6e3-126">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="ff6e3-126">The following flags can be set:</span></span>
    
<span data-ttu-id="ff6e3-127">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="ff6e3-127">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="ff6e3-128">Affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-128">Displays a progress indicator.</span></span>
    
<span data-ttu-id="ff6e3-129">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="ff6e3-129">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="ff6e3-130">**DoCopyProps** doit effectuer une opération de déplacement au lieu d’une opération de copie.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-130">**DoCopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="ff6e3-131">Lorsque cet indicateur n’est pas défini, **DoCopyProps** effectue une opération de copie.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-131">When this flag is not set, **DoCopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="ff6e3-132">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="ff6e3-132">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="ff6e3-133">Propriétés existantes dans l’objet de destination ne doivent pas être remplacées.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-133">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="ff6e3-134">Lorsque cet indicateur n’est pas défini, **DoCopyProps** remplace les propriétés existantes.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-134">When this flag is not set, **DoCopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="ff6e3-135">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="ff6e3-135">_lppProblems_</span></span>
  
> <span data-ttu-id="ff6e3-136">[entrée, sortie] À l’entrée, un pointeur vers un pointeur vers une structure [SPropProblemArray](spropproblemarray.md) ; dans le cas contraire, NULL, qui n’indique aucun besoin d’informations sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-136">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="ff6e3-137">Si _lppProblems_ est un pointeur valid en entrée, **DoCopyProps** renvoie des informations détaillées sur les erreurs lors de la copie d’une ou plusieurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-137">If  _lppProblems_ is a valid pointer on input, **DoCopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ff6e3-138">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="ff6e3-138">Return value</span></span>

<span data-ttu-id="ff6e3-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="ff6e3-139">S_OK</span></span> 
  
> <span data-ttu-id="ff6e3-140">Les propriétés ont été correctement copiées ou déplacées.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-140">Properties were successfully copied or moved.</span></span>
    
<span data-ttu-id="ff6e3-141">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="ff6e3-141">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="ff6e3-142">Une propriété à copier ou déplacer déjà existe dans l’objet de destination et l’indicateur MAPI_NOREPLACE est défini.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-142">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="ff6e3-143">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="ff6e3-143">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="ff6e3-144">L’objet source, directement ou indirectement contient l’objet de destination.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-144">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="ff6e3-145">Travail significatifs peut-être avoir été effectué avant cette condition a été détectée, et les objets source et de destination peuvent être modifiées partiellement.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-145">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="ff6e3-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="ff6e3-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="ff6e3-147">L’interface identifié par le paramètre _lpSrcInterface_ n’est pas pris en charge par l’objet source, ou l’interface identifié par le paramètre _lpDestInterface_ n’est pas pris en charge par l’objet de destination.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-147">The interface identified by the  _lpSrcInterface_ parameter is not supported by the source object, or the interface identified by the  _lpDestInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="ff6e3-148">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="ff6e3-148">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="ff6e3-149">Une tentative a été effectuée pour accéder à un objet pour lequel l’appelant dispose d’autorisations insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-149">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="ff6e3-150">Cette erreur est renvoyée si l’objet de destination est identique à l’objet source.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-150">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="ff6e3-151">Les valeurs suivantes peuvent être renvoyées dans la structure **SPropProblemArray** , mais pas en tant que valeurs de retour pour **DoCopyProps**.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-151">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyProps**.</span></span> <span data-ttu-id="ff6e3-152">Ces erreurs s’appliquent à une propriété unique.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-152">These errors apply to a single property.</span></span>
  
<span data-ttu-id="ff6e3-153">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="ff6e3-153">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="ff6e3-154">Soit l’indicateur MAPI_UNICODE a été défini et **DoCopyProps** ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et **DoCopyProps** prend en charge Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-154">Either the MAPI_UNICODE flag was set and **DoCopyProps** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="ff6e3-155">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="ff6e3-155">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="ff6e3-156">La propriété ne peut pas être modifiée par l’appelant car il s’agit d’une propriété en lecture seule, calculée par le propriétaire de l’objet de destination.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-156">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="ff6e3-157">Cette erreur n’est pas lourde ; l’appelant doit autoriser l’opération de copie continuer.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-157">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="ff6e3-158">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="ff6e3-158">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="ff6e3-159">Le type de propriété n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-159">The property type is invalid.</span></span>
    
<span data-ttu-id="ff6e3-160">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="ff6e3-160">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="ff6e3-161">Le type de propriété n’est pas le type attendu par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-161">The property type is not the type that the caller expects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ff6e3-162">Remarques</span><span class="sxs-lookup"><span data-stu-id="ff6e3-162">Remarks</span></span>

<span data-ttu-id="ff6e3-163">La méthode **IMAPISupport::DoCopyProps** est implémentée pour les objets de prise en charge de fournisseur de magasin de message.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-163">The **IMAPISupport::DoCopyProps** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="ff6e3-164">Fournisseurs de banque de messages peuvent appeler **DoCopyProps** pour implémenter la méthode [IMAPIProp::CopyProps](imapiprop-copyprops.md) pour leurs dossiers et des messages.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-164">Message store providers can call **DoCopyProps** to implement the [IMAPIProp::CopyProps](imapiprop-copyprops.md) method for their folders and messages.</span></span> <span data-ttu-id="ff6e3-165">**DoCopyProps** copie ou déplace les propriétés identifiées dans le tableau de balise de propriété désigné par _lpIncludeProps_ et qui sont présentes dans l’objet vers lequel pointé _lpSrcObj_.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-165">**DoCopyProps** copies or moves the properties that are identified in the property tag array pointed to by  _lpIncludeProps_ and that are present in the object pointed to by  _lpSrcObj_.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ff6e3-166">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="ff6e3-166">Notes to callers</span></span>

<span data-ttu-id="ff6e3-167">Lorsque vous copiez des propriétés entre les objets du même type, tels que les deux messages, les paramètres _lpSrcInterface_ et _lpDestInterface_ doivent contenir les mêmes paramètres interface identificateur et _lpSrcObj_ et _lpDestObj_ doit pointer sur les objets du même type.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-167">When you copy properties between objects of the same type, such as two messages, the  _lpSrcInterface_ and  _lpDestInterface_ parameters must contain the same interface identifier, and the  _lpSrcObj_ and  _lpDestObj_ parameters must point to objects of the same type.</span></span> <span data-ttu-id="ff6e3-168">Si _lpDestInterface_ est défini sur NULL, **DoCopyProps** renvoie MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-168">If  _lpDestInterface_ is set to NULL, **DoCopyProps** returns MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="ff6e3-169">Si vous définissez _lpDestInterface_ à un identificateur d’interface acceptable, mais un ensemble _lpDestObj_ à un pointeur non valide, le résultat est imprévisible.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-169">If you set  _lpDestInterface_ to an acceptable interface identifier, but set  _lpDestObj_ to an invalid pointer, the results are unpredictable.</span></span> <span data-ttu-id="ff6e3-170">Votre fournisseur échouera probablement.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-170">Most likely your provider will fail.</span></span> 
  
<span data-ttu-id="ff6e3-171">Définir l’indicateur MAPI_NOREPLACE si vous ne souhaitez pas que les propriétés de l’objet cible pour être remplacé.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-171">Set the MAPI_NOREPLACE flag if you do not want any of the properties in the destination object to be overwritten.</span></span> <span data-ttu-id="ff6e3-172">Propriétés de l’objet cible qui existent dans l’objet source et ne sont pas remplacées ne sont pas supprimées ou modifiées.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-172">Properties in the destination object that exist in the source object and are not overwritten are not deleted or modified.</span></span>
  
<span data-ttu-id="ff6e3-173">Pour copier la liste des destinataires d’un message, inclure la propriété **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) dans le tableau de balise de propriété indiqué par le paramètre _lpIncludeProps_ .</span><span class="sxs-lookup"><span data-stu-id="ff6e3-173">To copy a message's recipient list, include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array pointed to by the  _lpIncludeProps_ parameter.</span></span> <span data-ttu-id="ff6e3-174">Pour copier les pièces jointes du message, inclure la propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ff6e3-174">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="ff6e3-175">Pour copier un dossier ou hiérarchie du conteneur de carnet d’adresses ou table des matières, inclure **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) dans le tableau de balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-175">To copy a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag array.</span></span> <span data-ttu-id="ff6e3-176">Pour inclure la table du contenu associé d’un dossier, inclure la propriété **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-176">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span>
  
<span data-ttu-id="ff6e3-177">Si les sous-dossiers sont copiés ou déplacés, leur contenu est copiés ou déplacés dans son intégralité, indépendamment de l’utilisation des propriétés indiqués par la structure **SPropTagArray** .</span><span class="sxs-lookup"><span data-stu-id="ff6e3-177">If subfolders are copied or moved, their contents are copied or moved in their entirety, regardless of the use of properties indicated by the **SPropTagArray** structure.</span></span> 
  
 <span data-ttu-id="ff6e3-178">Les rapports **DoCopyProps** globales erreurs qui se produisent avec l’opération dans sa globalité et les erreurs qui se produisent avec un ou plusieurs des propriétés individuelles.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-178">**DoCopyProps** reports global errors that occur with the operation as a whole, and individual errors that occur with one or more of the properties.</span></span> <span data-ttu-id="ff6e3-179">Ces erreurs individuels sont placés dans une structure **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="ff6e3-179">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="ff6e3-180">Vous pouvez supprimer le rapport d’erreurs au niveau de la propriété en passant NULL, plutôt qu’un pointeur valid, pour le paramètre property problème tableau structure.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-180">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="ff6e3-181">Si vous souhaitez recevoir des informations sur les erreurs, passez un pointeur de structure **SPropProblemArray** valid dans le paramètre _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="ff6e3-181">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="ff6e3-182">Lorsque **DoCopyProps** renvoie S_OK, vérifiez les erreurs possibles avec des propriétés individuelles dans la structure.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-182">When **DoCopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="ff6e3-183">Lorsque **DoCopyProps** renvoie une erreur, aucune information n’est retournée dans la structure **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="ff6e3-183">When **DoCopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="ff6e3-184">Au lieu de cela, appelez la méthode [IMAPISupport::GetLastError](imapisupport-getlasterror.md) pour récupérer des informations d’erreur détaillé.</span><span class="sxs-lookup"><span data-stu-id="ff6e3-184">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="ff6e3-185">Si **DoCopyProps** renvoie S_OK, libérer la structure **SPropProblemArray** retournée en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="ff6e3-185">If **DoCopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ff6e3-186">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff6e3-186">See also</span></span>



[<span data-ttu-id="ff6e3-187">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="ff6e3-187">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
  
[<span data-ttu-id="ff6e3-188">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="ff6e3-188">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="ff6e3-189">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="ff6e3-189">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="ff6e3-190">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="ff6e3-190">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="ff6e3-191">Propriété canonique PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="ff6e3-191">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="ff6e3-192">Propriété canonique PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="ff6e3-192">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="ff6e3-193">Propriété canonique PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="ff6e3-193">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="ff6e3-194">Propriété canonique PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="ff6e3-194">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="ff6e3-195">Propriété canonique PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="ff6e3-195">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="ff6e3-196">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="ff6e3-196">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="ff6e3-197">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="ff6e3-197">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="ff6e3-198">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ff6e3-198">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

