---
title: IMAPIPropCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyProps
api_type:
- COM
ms.assetid: f65da1c8-d49b-44e8-8c66-9c53d088d334
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7319f1abb4a74ee17b0a4a1220215c29434d256b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398401"
---
# <a name="imapipropcopyprops"></a><span data-ttu-id="8e180-103">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="8e180-103">IMAPIProp::CopyProps</span></span>

  
  
<span data-ttu-id="8e180-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e180-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e180-105">Copie ou déplace des propriétés sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="8e180-105">Copies or moves selected properties.</span></span> 
  
```cpp
HRESULT CopyProps(
  LPSPropTagArray lpIncludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="8e180-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e180-106">Parameters</span></span>

 <span data-ttu-id="8e180-107">_lpIncludeProps_</span><span class="sxs-lookup"><span data-stu-id="8e180-107">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="8e180-108">[in] Pointeur vers un tableau de balise de propriété qui spécifie les propriétés pour copier ou déplacer.</span><span class="sxs-lookup"><span data-stu-id="8e180-108">[in] A pointer to a property tag array that specifies the properties to copy or move.</span></span> <span data-ttu-id="8e180-109">**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) ne peut pas être incluse dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="8e180-109">**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) cannot be included in the array.</span></span> <span data-ttu-id="8e180-110">Le paramètre _lpIncludeProps_ ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="8e180-110">The  _lpIncludeProps_ parameter cannot be **null**.</span></span>
    
 <span data-ttu-id="8e180-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="8e180-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="8e180-112">[in] Un handle vers la fenêtre parent de l’indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="8e180-112">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="8e180-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="8e180-113">_lpProgress_</span></span>
  
> <span data-ttu-id="8e180-114">[in] Pointeur vers une implémentation d’un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="8e180-114">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="8e180-115">Si **null** est passé dans le paramètre _lpProgress_ , l’indicateur de progression est affichée à l’aide de l’implémentation de MAPI.</span><span class="sxs-lookup"><span data-stu-id="8e180-115">If **null** is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="8e180-116">Le paramètre _lpProgress_ est ignoré à moins que l’indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="8e180-116">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="8e180-117">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="8e180-117">_lpInterface_</span></span>
  
> <span data-ttu-id="8e180-118">[in] Un pointeur vers l’identificateur d’interface (IID) qui représente l’interface qui doit être utilisé pour accéder à l’objet indiqué par le paramètre _lpDestObj_ .</span><span class="sxs-lookup"><span data-stu-id="8e180-118">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="8e180-119">Le paramètre _lpInterface_ ne doit pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="8e180-119">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="8e180-120">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="8e180-120">_lpDestObj_</span></span>
  
> <span data-ttu-id="8e180-121">[in] Pointeur vers l’objet à recevoir les propriétés copiées ou déplacées.</span><span class="sxs-lookup"><span data-stu-id="8e180-121">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="8e180-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8e180-122">_ulFlags_</span></span>
  
> <span data-ttu-id="8e180-123">[in] Masque de bits d’indicateurs qui contrôle l’opération de copie ou de déplacement.</span><span class="sxs-lookup"><span data-stu-id="8e180-123">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="8e180-124">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="8e180-124">The following flags can be set:</span></span>
    
<span data-ttu-id="8e180-125">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="8e180-125">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="8e180-126">Si **CopyProps** appelle la méthode [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) pour gérer la copie ou l’opération de déplacement, il doit renvoyer immédiatement avec la valeur d’erreur MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="8e180-126">If **CopyProps** calls the [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="8e180-127">L’indicateur MAPI_DECLINE_OK est défini par MAPI pour limiter la récurrence.</span><span class="sxs-lookup"><span data-stu-id="8e180-127">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="8e180-128">Les clients ne définissez pas cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="8e180-128">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="8e180-129">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="8e180-129">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="8e180-130">Affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="8e180-130">Displays a progress indicator.</span></span>
    
<span data-ttu-id="8e180-131">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="8e180-131">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="8e180-132">**CopyProps** doit effectuer une opération de déplacement au lieu d’une opération de copie.</span><span class="sxs-lookup"><span data-stu-id="8e180-132">**CopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="8e180-133">Lorsque cet indicateur n’est pas défini, **CopyProps** effectue une opération de copie.</span><span class="sxs-lookup"><span data-stu-id="8e180-133">When this flag is not set, **CopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="8e180-134">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="8e180-134">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="8e180-135">Propriétés existantes dans l’objet de destination ne doivent pas être remplacées.</span><span class="sxs-lookup"><span data-stu-id="8e180-135">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="8e180-136">Lorsque cet indicateur n’est pas défini, **CopyProps** remplace les propriétés existantes.</span><span class="sxs-lookup"><span data-stu-id="8e180-136">When this flag is not set, **CopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="8e180-137">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="8e180-137">_lppProblems_</span></span>
  
> <span data-ttu-id="8e180-138">[entrée, sortie] À l’entrée, un pointeur vers un pointeur vers une structure [SPropProblemArray](spropproblemarray.md) ; Sinon, **valeur null**, indiquant qu’il n’a pas besoin d’informations sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="8e180-138">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, **null**, indicating that there is no need for error information.</span></span> <span data-ttu-id="8e180-139">Si _lppProblems_ est un pointeur valid en entrée, **CopyProps** renvoie des informations détaillées sur les erreurs lors de la copie d’une ou plusieurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="8e180-139">If  _lppProblems_ is a valid pointer on input, **CopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8e180-140">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8e180-140">Return value</span></span>

<span data-ttu-id="8e180-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="8e180-141">S_OK</span></span> 
  
> <span data-ttu-id="8e180-142">Les propriétés ont été copiées ou déplacées.</span><span class="sxs-lookup"><span data-stu-id="8e180-142">Properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="8e180-143">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="8e180-143">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="8e180-144">Un sous-objet ne peut pas être copié, car il existe déjà un sous-objet portant le même nom complet, défini par la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), dans l’objet de destination.</span><span class="sxs-lookup"><span data-stu-id="8e180-144">A subobject cannot be copied because a subobject with the same display name, defined by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, already exists in the destination object.</span></span> 
    
<span data-ttu-id="8e180-145">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="8e180-145">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="8e180-146">Le fournisseur de services n’implémente pas l’opération de copie.</span><span class="sxs-lookup"><span data-stu-id="8e180-146">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="8e180-147">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="8e180-147">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="8e180-148">L’objet source de l’opération de copie ou déplacement directement ou indirectement contient l’objet de destination.</span><span class="sxs-lookup"><span data-stu-id="8e180-148">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="8e180-149">Travail significatifs peut-être avoir été effectué avant cette condition a été détectée, et les objets source et de destination peuvent être modifiées partiellement.</span><span class="sxs-lookup"><span data-stu-id="8e180-149">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="8e180-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="8e180-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="8e180-151">L’interface identifié par le paramètre _lpInterface_ n’est pas pris en charge par l’objet de destination.</span><span class="sxs-lookup"><span data-stu-id="8e180-151">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="8e180-152">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="8e180-152">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="8e180-153">Une tentative a été effectuée pour accéder à un objet pour lequel l’appelant dispose d’autorisations insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="8e180-153">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="8e180-154">Cette erreur est renvoyée si l’objet de destination est identique à l’objet source.</span><span class="sxs-lookup"><span data-stu-id="8e180-154">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="8e180-155">Les valeurs suivantes peuvent être renvoyées dans la structure **SPropProblemArray** , mais pas en tant que valeurs de retour pour **CopyProps**.</span><span class="sxs-lookup"><span data-stu-id="8e180-155">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyProps**.</span></span> <span data-ttu-id="8e180-156">Ces erreurs s’appliquent à une propriété unique.</span><span class="sxs-lookup"><span data-stu-id="8e180-156">These errors apply to a single property.</span></span>
  
<span data-ttu-id="8e180-157">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="8e180-157">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="8e180-158">Soit l’indicateur MAPI_UNICODE a été défini et **CopyProps** ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et **CopyProps** prend en charge Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="8e180-158">Either the MAPI_UNICODE flag was set and **CopyProps** does not support Unicode, or MAPI_UNICODE was not set and **CopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="8e180-159">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="8e180-159">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="8e180-160">La propriété ne peut pas être modifiée par l’appelant car il s’agit d’une propriété en lecture seule, calculée par le propriétaire de l’objet de destination.</span><span class="sxs-lookup"><span data-stu-id="8e180-160">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="8e180-161">Cette erreur n’est pas lourde ; l’appelant doit autoriser l’opération de copie continuer.</span><span class="sxs-lookup"><span data-stu-id="8e180-161">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="8e180-162">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="8e180-162">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="8e180-163">Le type de propriété n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="8e180-163">The property type is invalid.</span></span>
    
<span data-ttu-id="8e180-164">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="8e180-164">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="8e180-165">Le type de propriété n’est pas le type attendu par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="8e180-165">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8e180-166">Remarques</span><span class="sxs-lookup"><span data-stu-id="8e180-166">Remarks</span></span>

<span data-ttu-id="8e180-167">La méthode **IMAPIProp::CopyProps** copie ou déplace les propriétés sélectionnées à partir de l’objet actif à un objet de destination.</span><span class="sxs-lookup"><span data-stu-id="8e180-167">The **IMAPIProp::CopyProps** method copies or moves selected properties from the current object to a destination object.</span></span> <span data-ttu-id="8e180-168">**CopyProps** est utilisé essentiellement pour répondre à et transférer des messages, où uniquement certaines des propriétés à partir du message d’origine se déplacent avec la réponse ou transférés copie.</span><span class="sxs-lookup"><span data-stu-id="8e180-168">**CopyProps** is used mainly for replying to and forwarding messages, where only some of the properties from the original message travel with the reply or forwarded copy.</span></span> 
  
<span data-ttu-id="8e180-169">Les sous-objets de l’objet source sont automatiquement inclus dans l’opération et copiés ou déplacés dans son intégralité, indépendamment de l’utilisation des propriétés indiqués par la structure [SPropTagArray](sproptagarray.md) .</span><span class="sxs-lookup"><span data-stu-id="8e180-169">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety, regardless of the use of properties indicated by the [SPropTagArray](sproptagarray.md) structure.</span></span> <span data-ttu-id="8e180-170">Par défaut, **CopyProps** remplace toutes les propriétés de l’objet cible qui correspondent aux propriétés de l’objet source.</span><span class="sxs-lookup"><span data-stu-id="8e180-170">By default, **CopyProps** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="8e180-171">Si les propriétés copiées ou déplacées existent déjà dans l’objet de destination, les propriétés existantes sont remplacées par les nouvelles propriétés, sauf si l’indicateur MAPI_NOREPLACE est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="8e180-171">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="8e180-172">Les informations existantes dans l’objet de destination n’est pas remplacé sont conservées.</span><span class="sxs-lookup"><span data-stu-id="8e180-172">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8e180-173">Remarques à l’attention des responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="8e180-173">Notes to implementers</span></span>

<span data-ttu-id="8e180-174">Vous pouvez fournir une implémentation complète de **CopyProps** ou reposer sur l’implémentation MAPI fournit de l’objet de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8e180-174">You can provide a full implementation of **CopyProps** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="8e180-175">Si vous souhaitez utiliser l’implémentation MAPI, appelez la méthode **IMAPISupport::DoCopyProps** .</span><span class="sxs-lookup"><span data-stu-id="8e180-175">If you want to use the MAPI implementation, call the **IMAPISupport::DoCopyProps** method.</span></span> <span data-ttu-id="8e180-176">Toutefois, si vous procédez comme déléguer le traitement de **DoCopyProps** et vous sont transmis à l’indicateur MAPI_DECLINE_OK, évitez l’appel de la prise en charge et renvoyer MAPI_E_DECLINE_COPY au lieu de cela.</span><span class="sxs-lookup"><span data-stu-id="8e180-176">However, if you do delegate processing to **DoCopyProps** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="8e180-177">Vous sera appelée avec cet indicateur par MAPI pour éviter la récurrence possible qui peut se produire lorsque vous copiez les dossiers.</span><span class="sxs-lookup"><span data-stu-id="8e180-177">You will be called with this flag by MAPI to avoid the possible recursion that can occur when you copy folders.</span></span> 
  
<span data-ttu-id="8e180-178">Étant donné que l’opération de copie peut être longue, vous devez afficher un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="8e180-178">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="8e180-179">Utilisez l’implémentation [IMAPIProgress](imapiprogressiunknown.md) qui est passée dans le paramètre _lpProgress_ , le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="8e180-179">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation that is passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="8e180-180">Si _lpProgress_ est **null**, appelez la méthode [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) pour utiliser l’implémentation MAPI.</span><span class="sxs-lookup"><span data-stu-id="8e180-180">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8e180-181">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="8e180-181">Notes to callers</span></span>

<span data-ttu-id="8e180-182">Ne définissez pas l’indicateur MAPI_DECLINE_OK ; Il est utilisé par MAPI dans ses appels vers le message implémentations de **CopyProps** fournisseur de banque d’informations.</span><span class="sxs-lookup"><span data-stu-id="8e180-182">Do not set the MAPI_DECLINE_OK flag; it is used by MAPI in its calls to message store provider **CopyProps** implementations.</span></span> 
  
<span data-ttu-id="8e180-183">Étant donné que les opérations de déplacement et de copie peuvent prendre le temps, il est judicieux de demander l’affichage d’un indicateur de progression en définissant l’indicateur MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="8e180-183">Because copy and move operations can take time, it is wise to request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="8e180-184">Vous pouvez définir le paramètre _lpProgress_ votre implémentation **IMAPIProgress**, si vous en avez un, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="8e180-184">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="8e180-185">Si _lpProgress_ est **null**, **CopyProps** utilisera l’indicateur de progression par défaut fourni par MAPI.</span><span class="sxs-lookup"><span data-stu-id="8e180-185">If  _lpProgress_ is **null**, **CopyProps** will use the default progress indicator provided by MAPI.</span></span> 
  
<span data-ttu-id="8e180-186">Vous pouvez supprimer l’affichage d’un indicateur de progression en définissant ne pas l’indicateur MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="8e180-186">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="8e180-187">**CopyProps** ignorera les paramètres _ulUIParam_ et _lpProgress_ et éviter l’affichage de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="8e180-187">**CopyProps** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and avoid displaying the indicator.</span></span> 
  
 <span data-ttu-id="8e180-188">**CopyProps** peuvent signaler des erreurs globaux et individuels ou des erreurs qui se produisent avec un ou plusieurs des propriétés.</span><span class="sxs-lookup"><span data-stu-id="8e180-188">**CopyProps** can report global and individual errors, or errors that occur with one or more of the properties.</span></span> <span data-ttu-id="8e180-189">Ces erreurs individuels sont placés dans une structure **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="8e180-189">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="8e180-190">Vous pouvez supprimer le rapport d’erreurs au niveau de la propriété en passant **null**, au lieu d’un pointeur valide, pour le paramètre property problème tableau structure.</span><span class="sxs-lookup"><span data-stu-id="8e180-190">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="8e180-191">Si vous souhaitez recevoir des informations sur les erreurs, passez un pointeur de structure **SPropProblemArray** valid dans le paramètre _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="8e180-191">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="8e180-192">Lorsque **CopyProps** renvoie S_OK, vérifiez les erreurs possibles avec des propriétés individuelles dans la structure.</span><span class="sxs-lookup"><span data-stu-id="8e180-192">When **CopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="8e180-193">**CopyProps** retourne une erreur, aucune information n’est retournée dans la structure **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="8e180-193">When **CopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="8e180-194">Au lieu de cela, appelez la méthode [IMAPIProp::GetLastError](imapiprop-getlasterror.md) pour récupérer des informations d’erreur détaillé.</span><span class="sxs-lookup"><span data-stu-id="8e180-194">Instead, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="8e180-195">Si **CopyProps** renvoie S_OK, libérer la structure **SPropProblemArray** retournée en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="8e180-195">If **CopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="8e180-196">Si vous copiez les propriétés qui sont uniques pour le type d’objet source, assurez-vous que l’objet de destination est du même type.</span><span class="sxs-lookup"><span data-stu-id="8e180-196">If you are copying properties that are unique to the source object type, you must make sure that the destination object is of the same type.</span></span> <span data-ttu-id="8e180-197">**CopyProps** ne vous empêche pas d’associant des propriétés qui appartiennent généralement à un type d’objet avec un autre type d’objet.</span><span class="sxs-lookup"><span data-stu-id="8e180-197">**CopyProps** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="8e180-198">C’est à vous pour copier des propriétés qui sont pertinents pour l’objet de destination.</span><span class="sxs-lookup"><span data-stu-id="8e180-198">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="8e180-199">Par exemple, vous devez copier pas les propriétés de message à un conteneur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="8e180-199">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="8e180-200">Pour vous assurer que vous copiez entre les objets du même type, vérifiez que l’objet source et de destination sont le même type, par comparaison des pointeurs d’objet ou d’appeler la méthode [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8e180-200">To ensure that you are copying between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="8e180-201">Définir l’identificateur d’interface désigné par _lpInterface_ à l’interface standard pour l’objet source.</span><span class="sxs-lookup"><span data-stu-id="8e180-201">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="8e180-202">Vérifiez également que le type d’objet ou la propriété **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) est la même pour les deux objets.</span><span class="sxs-lookup"><span data-stu-id="8e180-202">Also, ensure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="8e180-203">Par exemple, si vous copiez à partir d’un message, définissez _lpInterface_ IID_IMessage et le **PR_OBJECT_TYPE** pour les deux objets MAPI_MESSAGE.</span><span class="sxs-lookup"><span data-stu-id="8e180-203">For example, if you are copying from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="8e180-204">Si un pointeur non valide est passé dans le paramètre _lpDestObj_ , le résultat est imprévisible.</span><span class="sxs-lookup"><span data-stu-id="8e180-204">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="8e180-205">Pour copier la liste des destinataires d’un message, appelez la méthode **CopyProps** du message et inclure la propriété **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) dans le tableau de balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="8e180-205">To copy a message's recipient list, call the message's **CopyProps** method and include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array.</span></span> <span data-ttu-id="8e180-206">Pour copier les pièces jointes du message, inclure la propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8e180-206">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="8e180-207">Pour copier un dossier une hiérarchie de conteneur de carnet adresses ou table des matières, incluez la **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou des propriétés de **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) dans le tableau de balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="8e180-207">To copy a folder or address book container's hierarchy or contents table, include the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) properties in the property tag array.</span></span> <span data-ttu-id="8e180-208">Pour inclure la table du contenu associé d’un dossier, inclure la propriété **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="8e180-208">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8e180-209">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="8e180-209">MFCMAPI reference</span></span>

<span data-ttu-id="8e180-210">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8e180-210">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8e180-211">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="8e180-211">**File**</span></span>|<span data-ttu-id="8e180-212">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="8e180-212">**Function**</span></span>|<span data-ttu-id="8e180-213">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="8e180-213">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8e180-214">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="8e180-214">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="8e180-215">CopyNamedProps</span><span class="sxs-lookup"><span data-stu-id="8e180-215">CopyNamedProps</span></span>  <br/> |<span data-ttu-id="8e180-216">MFCMAPI utilise la méthode **IMAPIProp::CopyProps** pour copier des propriétés nommées à partir d’un message à un autre.</span><span class="sxs-lookup"><span data-stu-id="8e180-216">MFCMAPI uses the **IMAPIProp::CopyProps** method to copy named properties from one message to another.</span></span>  <br/> |
|<span data-ttu-id="8e180-217">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="8e180-217">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="8e180-218">CSingleMAPIPropListCtrl::OnPasteProperty</span><span class="sxs-lookup"><span data-stu-id="8e180-218">CSingleMAPIPropListCtrl::OnPasteProperty</span></span>  <br/> |<span data-ttu-id="8e180-219">MFCMAPI utilise la méthode **IMAPIProp::CopyProps** pour coller une propriété qui a été copiée à partir d’un autre objet.</span><span class="sxs-lookup"><span data-stu-id="8e180-219">MFCMAPI uses the **IMAPIProp::CopyProps** method to paste a property that has been copied from another object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8e180-220">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e180-220">See also</span></span>



[<span data-ttu-id="8e180-221">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="8e180-221">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="8e180-222">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8e180-222">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="8e180-223">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="8e180-223">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="8e180-224">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="8e180-224">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="8e180-225">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="8e180-225">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
  
[<span data-ttu-id="8e180-226">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="8e180-226">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="8e180-227">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="8e180-227">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="8e180-228">Propriété canonique PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="8e180-228">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="8e180-229">Propriété canonique PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="8e180-229">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="8e180-230">Propriété canonique PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="8e180-230">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="8e180-231">Propriété canonique PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="8e180-231">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="8e180-232">Propriété canonique PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="8e180-232">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="8e180-233">Propriété canonique PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="8e180-233">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="8e180-234">Propriété canonique PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="8e180-234">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="8e180-235">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="8e180-235">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="8e180-236">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="8e180-236">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="8e180-237">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8e180-237">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="8e180-238">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="8e180-238">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

