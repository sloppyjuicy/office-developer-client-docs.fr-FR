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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345506"
---
# <a name="imapipropcopyprops"></a><span data-ttu-id="f62a3-103">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="f62a3-103">IMAPIProp::CopyProps</span></span>

  
  
<span data-ttu-id="f62a3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f62a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f62a3-105">Copie ou déplace les propriétés sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="f62a3-105">Copies or moves selected properties.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="f62a3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f62a3-106">Parameters</span></span>

 <span data-ttu-id="f62a3-107">_lpIncludeProps_</span><span class="sxs-lookup"><span data-stu-id="f62a3-107">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="f62a3-108">[in] Pointeur vers un tableau de balises de propriétés qui spécifie les propriétés à copier ou déplacer.</span><span class="sxs-lookup"><span data-stu-id="f62a3-108">[in] A pointer to a property tag array that specifies the properties to copy or move.</span></span> <span data-ttu-id="f62a3-109">**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) ne peut pas être inclus dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="f62a3-109">**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) cannot be included in the array.</span></span> <span data-ttu-id="f62a3-110">Le  _paramètre lpIncludeProps ne_ peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="f62a3-110">The  _lpIncludeProps_ parameter cannot be **null**.</span></span>
    
 <span data-ttu-id="f62a3-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f62a3-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="f62a3-112">[in] Handle vers la fenêtre parent de l’indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="f62a3-112">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="f62a3-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="f62a3-113">_lpProgress_</span></span>
  
> <span data-ttu-id="f62a3-114">[in] Pointeur vers une implémentation d’un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="f62a3-114">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="f62a3-115">Si **null** est transmis dans  _le paramètre lpProgress,_ l’indicateur de progression s’affiche à l’aide de l’implémentation MAPI.</span><span class="sxs-lookup"><span data-stu-id="f62a3-115">If **null** is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="f62a3-116">Le _paramètre lpProgress est_ ignoré, sauf si l’MAPI_DIALOG est définie dans le paramètre _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="f62a3-116">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="f62a3-117">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="f62a3-117">_lpInterface_</span></span>
  
> <span data-ttu-id="f62a3-118">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface qui doit être utilisée pour accéder à l’objet pointé par le paramètre _lpDestObj._</span><span class="sxs-lookup"><span data-stu-id="f62a3-118">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="f62a3-119">Le  _paramètre lpInterface_ ne doit pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="f62a3-119">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="f62a3-120">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="f62a3-120">_lpDestObj_</span></span>
  
> <span data-ttu-id="f62a3-121">[in] Pointeur vers l’objet pour recevoir les propriétés copiées ou déplacées.</span><span class="sxs-lookup"><span data-stu-id="f62a3-121">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="f62a3-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f62a3-122">_ulFlags_</span></span>
  
> <span data-ttu-id="f62a3-123">[in] Masque de bits d’indicateurs qui contrôle l’opération de copie ou de déplacement.</span><span class="sxs-lookup"><span data-stu-id="f62a3-123">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="f62a3-124">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="f62a3-124">The following flags can be set:</span></span>
    
<span data-ttu-id="f62a3-125">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="f62a3-125">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="f62a3-126">Si **CopyProps** appelle la méthode [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md) pour gérer l’opération de copie ou de déplacement, elle doit à la place renvoyer immédiatement avec la valeur d’erreur MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="f62a3-126">If **CopyProps** calls the [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="f62a3-127">L MAPI_DECLINE_OK est définie par MAPI pour limiter la récursion.</span><span class="sxs-lookup"><span data-stu-id="f62a3-127">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="f62a3-128">Les clients ne définissent pas cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="f62a3-128">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="f62a3-129">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="f62a3-129">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="f62a3-130">Affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="f62a3-130">Displays a progress indicator.</span></span>
    
<span data-ttu-id="f62a3-131">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="f62a3-131">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="f62a3-132">**CopyProps doit** effectuer une opération de déplacement au lieu d’une opération de copie.</span><span class="sxs-lookup"><span data-stu-id="f62a3-132">**CopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="f62a3-133">Lorsque cet indicateur n’est pas définie, **CopyProps** effectue une opération de copie.</span><span class="sxs-lookup"><span data-stu-id="f62a3-133">When this flag is not set, **CopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="f62a3-134">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="f62a3-134">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="f62a3-135">Les propriétés existantes dans l’objet de destination ne doivent pas être écrasées.</span><span class="sxs-lookup"><span data-stu-id="f62a3-135">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="f62a3-136">Lorsque cet indicateur n’est pas définie, **CopyProps** a la valeur par-dessus les propriétés existantes.</span><span class="sxs-lookup"><span data-stu-id="f62a3-136">When this flag is not set, **CopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="f62a3-137">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="f62a3-137">_lppProblems_</span></span>
  
> <span data-ttu-id="f62a3-138">[in, out] Lors de l’entrée, un pointeur vers un pointeur vers une structure [SPropProblemArray](spropproblemarray.md) ; sinon, **null**, indiquant qu’il n’est pas nécessaire d’obtenir des informations sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="f62a3-138">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, **null**, indicating that there is no need for error information.</span></span> <span data-ttu-id="f62a3-139">Si  _lppProblems est_ un pointeur valide sur l’entrée, **CopyProps** renvoie des informations détaillées sur les erreurs de copie d’une ou plusieurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="f62a3-139">If  _lppProblems_ is a valid pointer on input, **CopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f62a3-140">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f62a3-140">Return value</span></span>

<span data-ttu-id="f62a3-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="f62a3-141">S_OK</span></span> 
  
> <span data-ttu-id="f62a3-142">Les propriétés ont été correctement copiées ou déplacées.</span><span class="sxs-lookup"><span data-stu-id="f62a3-142">Properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="f62a3-143">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="f62a3-143">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="f62a3-144">Un sous-objet ne peut pas être copié car un sous-objet du même nom d’affichage, défini par la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), existe déjà dans l’objet de destination.</span><span class="sxs-lookup"><span data-stu-id="f62a3-144">A subobject cannot be copied because a subobject with the same display name, defined by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, already exists in the destination object.</span></span> 
    
<span data-ttu-id="f62a3-145">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="f62a3-145">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="f62a3-146">Le fournisseur de services n’implémente pas l’opération de copie.</span><span class="sxs-lookup"><span data-stu-id="f62a3-146">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="f62a3-147">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="f62a3-147">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="f62a3-148">L’objet source qui effectue l’opération de copie ou de déplacement directement ou indirectement contient l’objet de destination.</span><span class="sxs-lookup"><span data-stu-id="f62a3-148">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="f62a3-149">Des travaux importants ont peut-être été effectués avant la découverte de cette condition, de sorte que les objets source et de destination peuvent être partiellement modifiés.</span><span class="sxs-lookup"><span data-stu-id="f62a3-149">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="f62a3-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="f62a3-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="f62a3-151">L’interface identifiée par  _le paramètre lpInterface_ n’est pas prise en charge par l’objet de destination.</span><span class="sxs-lookup"><span data-stu-id="f62a3-151">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="f62a3-152">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="f62a3-152">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="f62a3-153">Une tentative d’accès à un objet pour lequel l’appelant dispose d’autorisations insuffisantes a été tentée.</span><span class="sxs-lookup"><span data-stu-id="f62a3-153">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="f62a3-154">Cette erreur est renvoyée si l’objet de destination est identique à l’objet source.</span><span class="sxs-lookup"><span data-stu-id="f62a3-154">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="f62a3-155">Les valeurs suivantes peuvent être renvoyées dans la structure **SPropProblemArray,** mais pas en tant que valeurs de retour **pour CopyProps**.</span><span class="sxs-lookup"><span data-stu-id="f62a3-155">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyProps**.</span></span> <span data-ttu-id="f62a3-156">Ces erreurs s’appliquent à une seule propriété.</span><span class="sxs-lookup"><span data-stu-id="f62a3-156">These errors apply to a single property.</span></span>
  
<span data-ttu-id="f62a3-157">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="f62a3-157">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="f62a3-158">L’MAPI_UNICODE a été définie et **CopyProps** ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et **CopyProps** prend uniquement en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="f62a3-158">Either the MAPI_UNICODE flag was set and **CopyProps** does not support Unicode, or MAPI_UNICODE was not set and **CopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="f62a3-159">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="f62a3-159">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="f62a3-160">La propriété ne peut pas être modifiée par l’appelant, car il s’agit d’une propriété en lecture seule, calculée par le propriétaire de l’objet de destination.</span><span class="sxs-lookup"><span data-stu-id="f62a3-160">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="f62a3-161">Cette erreur n’est pas grave ; L’appelant doit autoriser la continuer l’opération de copie.</span><span class="sxs-lookup"><span data-stu-id="f62a3-161">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="f62a3-162">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="f62a3-162">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="f62a3-163">Le type de propriété n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f62a3-163">The property type is invalid.</span></span>
    
<span data-ttu-id="f62a3-164">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="f62a3-164">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="f62a3-165">Le type de propriété n’est pas le type attendu par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="f62a3-165">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f62a3-166">Remarques</span><span class="sxs-lookup"><span data-stu-id="f62a3-166">Remarks</span></span>

<span data-ttu-id="f62a3-167">La **méthode IMAPIProp::CopyProps** copie ou déplace les propriétés sélectionnées de l’objet actuel vers un objet de destination.</span><span class="sxs-lookup"><span data-stu-id="f62a3-167">The **IMAPIProp::CopyProps** method copies or moves selected properties from the current object to a destination object.</span></span> <span data-ttu-id="f62a3-168">**CopyProps est** principalement utilisé pour répondre aux messages et les transmettre, où seules certaines des propriétés du message d’origine se déplacent avec la réponse ou la copie recopiée.</span><span class="sxs-lookup"><span data-stu-id="f62a3-168">**CopyProps** is used mainly for replying to and forwarding messages, where only some of the properties from the original message travel with the reply or forwarded copy.</span></span> 
  
<span data-ttu-id="f62a3-169">Tous les sous-objets de l’objet source sont automatiquement inclus dans l’opération et copiés ou déplacés dans leur intégralité, quelle que soit l’utilisation des propriétés indiquées par la structure [SPropTagArray.](sproptagarray.md)</span><span class="sxs-lookup"><span data-stu-id="f62a3-169">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety, regardless of the use of properties indicated by the [SPropTagArray](sproptagarray.md) structure.</span></span> <span data-ttu-id="f62a3-170">Par défaut, **CopyProps** a la valeur par défaut pour toutes les propriétés de l’objet de destination qui correspondent aux propriétés de l’objet source.</span><span class="sxs-lookup"><span data-stu-id="f62a3-170">By default, **CopyProps** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="f62a3-171">Si l’une des propriétés copiées ou déplacées existe déjà dans l’objet de destination, les propriétés existantes sont écrasées par les nouvelles propriétés, sauf si l’indicateur MAPI_NOREPLACE est définie dans le paramètre _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="f62a3-171">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="f62a3-172">Les informations existantes dans l’objet de destination qui ne sont pas écrasées restent intactes.</span><span class="sxs-lookup"><span data-stu-id="f62a3-172">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f62a3-173">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="f62a3-173">Notes to implementers</span></span>

<span data-ttu-id="f62a3-174">Vous pouvez fournir une implémentation complète de **CopyProps** ou vous appuyer sur l’implémentation fournie par MAPI dans son objet de support.</span><span class="sxs-lookup"><span data-stu-id="f62a3-174">You can provide a full implementation of **CopyProps** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="f62a3-175">Si vous souhaitez utiliser l’implémentation MAPI, appelez la méthode **IMAPISupport::D oCopyProps.**</span><span class="sxs-lookup"><span data-stu-id="f62a3-175">If you want to use the MAPI implementation, call the **IMAPISupport::DoCopyProps** method.</span></span> <span data-ttu-id="f62a3-176">Toutefois, si vous délèguez le traitement à **DoCopyProps** et que vous avez reçu l’indicateur MAPI_DECLINE_OK, évitez l’appel de support et renvoyez-MAPI_E_DECLINE_COPY à la place.</span><span class="sxs-lookup"><span data-stu-id="f62a3-176">However, if you do delegate processing to **DoCopyProps** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="f62a3-177">MapI vous appelle avec cet indicateur pour éviter toute récursion possible lorsque vous copiez des dossiers.</span><span class="sxs-lookup"><span data-stu-id="f62a3-177">You will be called with this flag by MAPI to avoid the possible recursion that can occur when you copy folders.</span></span> 
  
<span data-ttu-id="f62a3-178">Étant donné que l’opération de copie peut être longue, vous devez afficher un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="f62a3-178">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="f62a3-179">Utilisez [l’implémentation IMAPIProgress](imapiprogressiunknown.md) qui est passée dans le  _paramètre lpProgress,_ s’il en existe un.</span><span class="sxs-lookup"><span data-stu-id="f62a3-179">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation that is passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="f62a3-180">Si  _lpProgress_ est **null,** appelez la méthode [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) pour utiliser l’implémentation MAPI.</span><span class="sxs-lookup"><span data-stu-id="f62a3-180">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f62a3-181">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="f62a3-181">Notes to callers</span></span>

<span data-ttu-id="f62a3-182">Ne définissez pas l’MAPI_DECLINE_OK de l’indicateur . Il est utilisé par MAPI dans ses appels aux implémentations **CopyProps** du fournisseur de magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="f62a3-182">Do not set the MAPI_DECLINE_OK flag; it is used by MAPI in its calls to message store provider **CopyProps** implementations.</span></span> 
  
<span data-ttu-id="f62a3-183">Étant donné que les opérations de copie et de déplacement peuvent prendre du temps, il est judicieux de demander l’affichage d’un indicateur de progression en MAPI_DIALOG’indicateur.</span><span class="sxs-lookup"><span data-stu-id="f62a3-183">Because copy and move operations can take time, it is wise to request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="f62a3-184">Vous pouvez définir le  _paramètre lpProgress_ sur votre implémentation de **IMAPIProgress,** si vous en avez un, ou sur **null**.</span><span class="sxs-lookup"><span data-stu-id="f62a3-184">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="f62a3-185">Si  _lpProgress est_ **null,** **CopyProps** utilise l’indicateur de progression par défaut fourni par MAPI.</span><span class="sxs-lookup"><span data-stu-id="f62a3-185">If  _lpProgress_ is **null**, **CopyProps** will use the default progress indicator provided by MAPI.</span></span> 
  
<span data-ttu-id="f62a3-186">Vous pouvez supprimer l’affichage d’un indicateur de progression en ne MAPI_DIALOG indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="f62a3-186">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="f62a3-187">**CopyProps ignore** les paramètres  _ulUIParam_ et  _lpProgress_ et évite d’afficher l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="f62a3-187">**CopyProps** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and avoid displaying the indicator.</span></span> 
  
 <span data-ttu-id="f62a3-188">**CopyProps peut** signaler des erreurs globales et individuelles, ou des erreurs qui se produisent avec une ou plusieurs des propriétés.</span><span class="sxs-lookup"><span data-stu-id="f62a3-188">**CopyProps** can report global and individual errors, or errors that occur with one or more of the properties.</span></span> <span data-ttu-id="f62a3-189">Ces erreurs individuelles sont mises dans une structure **SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="f62a3-189">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="f62a3-190">Vous pouvez supprimer le rapport d’erreurs au niveau de la propriété en passant **null**, au lieu d’un pointeur valide, pour le paramètre de structure de tableau de problème de propriété.</span><span class="sxs-lookup"><span data-stu-id="f62a3-190">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="f62a3-191">Si vous souhaitez recevoir des informations sur les erreurs, passez un pointeur de structure **SPropProblemArray** valide dans le paramètre _lppProblems._</span><span class="sxs-lookup"><span data-stu-id="f62a3-191">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="f62a3-192">Lorsque **CopyProps renvoie** S_OK, recherchez les erreurs possibles avec des propriétés individuelles dans la structure.</span><span class="sxs-lookup"><span data-stu-id="f62a3-192">When **CopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="f62a3-193">Lorsque **CopyProps renvoie** une erreur, aucune information n’est renvoyée dans la structure **SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="f62a3-193">When **CopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="f62a3-194">Appelez plutôt la [méthode IMAPIProp::GetLastError](imapiprop-getlasterror.md) pour récupérer des informations détaillées sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="f62a3-194">Instead, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="f62a3-195">Si **CopyProps renvoie** S_OK, libérez la structure **SPropProblemArray** renvoyée en appelant la [fonction MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="f62a3-195">If **CopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="f62a3-196">Si vous copiez des propriétés propres au type d’objet source, vous devez vous assurer que l’objet de destination est du même type.</span><span class="sxs-lookup"><span data-stu-id="f62a3-196">If you are copying properties that are unique to the source object type, you must make sure that the destination object is of the same type.</span></span> <span data-ttu-id="f62a3-197">**CopyProps ne** vous empêche pas d’associer des propriétés qui appartiennent généralement à un type d’objet à un autre type d’objet.</span><span class="sxs-lookup"><span data-stu-id="f62a3-197">**CopyProps** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="f62a3-198">C’est à vous de copier les propriétés qui ont un sens pour l’objet de destination.</span><span class="sxs-lookup"><span data-stu-id="f62a3-198">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="f62a3-199">Par exemple, vous ne devez pas copier les propriétés de message dans un conteneur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="f62a3-199">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="f62a3-200">Pour vous assurer que vous copiez entre des objets du même type, vérifiez que l’objet source et l’objet de destination sont du même type, soit en comparant des pointeurs d’objet, soit en appelant la méthode [IUnknown::QueryInterface.](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f62a3-200">To ensure that you are copying between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="f62a3-201">Définissez l’identificateur d’interface pointé par  _lpInterface_ sur l’interface standard de l’objet source.</span><span class="sxs-lookup"><span data-stu-id="f62a3-201">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="f62a3-202">Assurez-vous également que le type d’objet **ou PR_OBJECT_TYPE** propriété ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) est identique pour les deux objets.</span><span class="sxs-lookup"><span data-stu-id="f62a3-202">Also, ensure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="f62a3-203">Par exemple, si vous copiez à partir d’un message,  définissez _lpInterface_ sur IID_IMessage et le PR_OBJECT_TYPE pour les deux objets sur MAPI_MESSAGE.</span><span class="sxs-lookup"><span data-stu-id="f62a3-203">For example, if you are copying from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="f62a3-204">Si un pointeur non valide est transmis dans le  _paramètre lpDestObj,_ les résultats sont imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="f62a3-204">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="f62a3-205">Pour copier la liste des destinataires d’un message, appelez la méthode **CopyProps** du message et incluez la propriété **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) dans le tableau de balises de propriétés.</span><span class="sxs-lookup"><span data-stu-id="f62a3-205">To copy a message's recipient list, call the message's **CopyProps** method and include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array.</span></span> <span data-ttu-id="f62a3-206">Pour copier les pièces jointes du message, incluez la **propriété PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f62a3-206">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="f62a3-207">Pour copier la hiérarchie ou la table des matières d’un conteneur de dossier ou de carnet d’adresses, incluez les propriétés **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) dans le tableau de balises de propriétés.</span><span class="sxs-lookup"><span data-stu-id="f62a3-207">To copy a folder or address book container's hierarchy or contents table, include the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) properties in the property tag array.</span></span> <span data-ttu-id="f62a3-208">Pour inclure la table des matières associée d’un dossier, incluez la propriété **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="f62a3-208">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f62a3-209">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f62a3-209">MFCMAPI reference</span></span>

<span data-ttu-id="f62a3-210">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f62a3-210">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f62a3-211">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="f62a3-211">**File**</span></span>|<span data-ttu-id="f62a3-212">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="f62a3-212">**Function**</span></span>|<span data-ttu-id="f62a3-213">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="f62a3-213">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f62a3-214">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="f62a3-214">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="f62a3-215">CopyNamedProps</span><span class="sxs-lookup"><span data-stu-id="f62a3-215">CopyNamedProps</span></span>  <br/> |<span data-ttu-id="f62a3-216">MFCMAPI utilise la **méthode IMAPIProp::CopyProps** pour copier les propriétés nommées d’un message vers un autre.</span><span class="sxs-lookup"><span data-stu-id="f62a3-216">MFCMAPI uses the **IMAPIProp::CopyProps** method to copy named properties from one message to another.</span></span>  <br/> |
|<span data-ttu-id="f62a3-217">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="f62a3-217">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="f62a3-218">CSingleMAPIPropListCtrl::OnPasteProperty</span><span class="sxs-lookup"><span data-stu-id="f62a3-218">CSingleMAPIPropListCtrl::OnPasteProperty</span></span>  <br/> |<span data-ttu-id="f62a3-219">MFCMAPI utilise la **méthode IMAPIProp::CopyProps** pour coller une propriété qui a été copiée à partir d’un autre objet.</span><span class="sxs-lookup"><span data-stu-id="f62a3-219">MFCMAPI uses the **IMAPIProp::CopyProps** method to paste a property that has been copied from another object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f62a3-220">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f62a3-220">See also</span></span>



[<span data-ttu-id="f62a3-221">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="f62a3-221">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="f62a3-222">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f62a3-222">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="f62a3-223">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="f62a3-223">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="f62a3-224">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="f62a3-224">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="f62a3-225">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="f62a3-225">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
  
[<span data-ttu-id="f62a3-226">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="f62a3-226">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="f62a3-227">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f62a3-227">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f62a3-228">Propriété canonique PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="f62a3-228">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="f62a3-229">Propriété canonique PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="f62a3-229">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="f62a3-230">Propriété canonique PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="f62a3-230">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="f62a3-231">Propriété canonique PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="f62a3-231">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="f62a3-232">Propriété canonique PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="f62a3-232">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="f62a3-233">Propriété canonique PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="f62a3-233">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="f62a3-234">Propriété canonique PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="f62a3-234">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="f62a3-235">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="f62a3-235">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="f62a3-236">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="f62a3-236">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="f62a3-237">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f62a3-237">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="f62a3-238">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="f62a3-238">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

