---
title: IMAPIPropCopyTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyTo
api_type:
- COM
ms.assetid: e56042e9-5bb7-4a99-b6de-1546d4ca07f0
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: bbc9dcf2218907b5d31ce1fc9f904e6ae1da47d9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594011"
---
# <a name="imapipropcopyto"></a><span data-ttu-id="619e0-103">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="619e0-103">IMAPIProp::CopyTo</span></span>

  
  
<span data-ttu-id="619e0-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="619e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="619e0-105">Copie ou déplace toutes les propriétés, à l’exception de spécifiquement des propriétés exclues.</span><span class="sxs-lookup"><span data-stu-id="619e0-105">Copies or moves all properties, except for specifically excluded properties.</span></span>
  
```cpp
HRESULT CopyTo(
 ULONG ciidExclude,
 LPCIID rgiidExclude,
 LPSPropTagArray lpExcludeProps,
 ULONG_PTR ulUIParam,
 LPMAPIPROGRESS lpProgress,
 LPCIID lpInterface,
 LPVOID lpDestObj,
 ULONG ulFlags,
 LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="619e0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="619e0-106">Parameters</span></span>

 <span data-ttu-id="619e0-107">_ciidExclude_</span><span class="sxs-lookup"><span data-stu-id="619e0-107">_ciidExclude_</span></span>
  
> <span data-ttu-id="619e0-108">[in] Le nombre d’interfaces à exclure des propriétés sont copiées ou déplacées.</span><span class="sxs-lookup"><span data-stu-id="619e0-108">[in] The count of interfaces to exclude when properties are copied or moved.</span></span>
    
 <span data-ttu-id="619e0-109">_rgiidExclude_</span><span class="sxs-lookup"><span data-stu-id="619e0-109">_rgiidExclude_</span></span>
  
> <span data-ttu-id="619e0-110">[in] Tableau d’identificateurs d’interface (IID) qui spécifient les interfaces qui ne doivent pas être utilisées lorsque des informations supplémentaires sont copiées ou déplacées à l’objet de destination.</span><span class="sxs-lookup"><span data-stu-id="619e0-110">[in] An array of interface identifiers (IIDs) that specify interfaces that should not be used when supplemental information is copied or moved to the destination object.</span></span>
    
 <span data-ttu-id="619e0-111">_lpExcludeProps_</span><span class="sxs-lookup"><span data-stu-id="619e0-111">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="619e0-112">[in] Pointeur vers un tableau de balise de propriété qui identifie les balises de propriété qui doivent être exclus de la copie ou l’opération de déplacement.</span><span class="sxs-lookup"><span data-stu-id="619e0-112">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="619e0-113">Le passage de **null** dans le paramètre _lpExcludeProps_ indique que toutes les propriétés de l’objet doivent être copiés ou déplacés.</span><span class="sxs-lookup"><span data-stu-id="619e0-113">Passing **null** in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="619e0-114">**CopyTo** renvoie MAPI_E_INVALID_PARAMETER lorsque le membre **cValues** de la structure [SPropProblemArray](spropproblemarray.md) désignés par _lpExcludeProps_ est définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="619e0-114">**CopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropProblemArray](spropproblemarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="619e0-115">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="619e0-115">_ulUIParam_</span></span>
  
> <span data-ttu-id="619e0-116">[in] Un handle vers la fenêtre parent de l’indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="619e0-116">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="619e0-117">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="619e0-117">_lpProgress_</span></span>
  
> <span data-ttu-id="619e0-118">[in] Pointeur vers une implémentation d’indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="619e0-118">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="619e0-119">Si la **valeur null** est passée dans le paramètre _lpProgress_ , MAPI fournit l’implémentation de progression.</span><span class="sxs-lookup"><span data-stu-id="619e0-119">If **null** is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="619e0-120">Le paramètre _lpProgress_ est ignoré à moins que l’indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="619e0-120">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="619e0-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="619e0-121">_lpInterface_</span></span>
  
> <span data-ttu-id="619e0-122">[in] Un pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’objet indiqué par le paramètre _lpDestObj_ .</span><span class="sxs-lookup"><span data-stu-id="619e0-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="619e0-123">Le paramètre _lpInterface_ ne doit pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="619e0-123">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="619e0-124">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="619e0-124">_lpDestObj_</span></span>
  
> <span data-ttu-id="619e0-125">[in] Pointeur vers l’objet à recevoir les propriétés copiées ou déplacées.</span><span class="sxs-lookup"><span data-stu-id="619e0-125">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="619e0-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="619e0-126">_ulFlags_</span></span>
  
> <span data-ttu-id="619e0-127">[in] Masque de bits d’indicateurs qui contrôle l’opération de copie ou de déplacement.</span><span class="sxs-lookup"><span data-stu-id="619e0-127">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="619e0-128">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="619e0-128">The following flags can be set:</span></span>
    
<span data-ttu-id="619e0-129">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="619e0-129">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="619e0-130">Si **CopyTo** appelle la méthode [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) pour gérer la copie ou l’opération de déplacement, il doit renvoyer immédiatement avec la valeur d’erreur MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="619e0-130">If **CopyTo** calls the [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="619e0-131">L’indicateur MAPI_DECLINE_OK est défini par MAPI pour limiter la récurrence.</span><span class="sxs-lookup"><span data-stu-id="619e0-131">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="619e0-132">Les clients ne définissez pas cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="619e0-132">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="619e0-133">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="619e0-133">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="619e0-134">Affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="619e0-134">Displays a progress indicator.</span></span>
    
<span data-ttu-id="619e0-135">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="619e0-135">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="619e0-136">**CopyTo** doit effectuer une opération de déplacement au lieu d’une opération de copie.</span><span class="sxs-lookup"><span data-stu-id="619e0-136">**CopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="619e0-137">Lorsque cet indicateur n’est pas défini, **CopyTo** effectue une opération de copie.</span><span class="sxs-lookup"><span data-stu-id="619e0-137">When this flag is not set, **CopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="619e0-138">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="619e0-138">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="619e0-139">Propriétés existantes dans l’objet de destination ne doivent pas être remplacées.</span><span class="sxs-lookup"><span data-stu-id="619e0-139">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="619e0-140">Lorsque cet indicateur n’est pas défini, **CopyTo** remplace les propriétés existantes.</span><span class="sxs-lookup"><span data-stu-id="619e0-140">When this flag is not set, **CopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="619e0-141">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="619e0-141">_lppProblems_</span></span>
  
> <span data-ttu-id="619e0-142">[entrée, sortie] À l’entrée, un pointeur vers un pointeur vers une structure **SPropProblemArray** ; dans le cas contraire, **null**, indiquant ainsi pas besoin d’informations sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="619e0-142">[in, out] On input, a pointer to a pointer to an **SPropProblemArray** structure; otherwise, **null**, indicating no need for error information.</span></span> <span data-ttu-id="619e0-143">Si _lppProblems_ est un pointeur valid en entrée, **CopyTo** renvoie des informations détaillées sur les erreurs lors de la copie d’une ou plusieurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="619e0-143">If  _lppProblems_ is a valid pointer on input, **CopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="619e0-144">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="619e0-144">Return value</span></span>

<span data-ttu-id="619e0-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="619e0-145">S_OK</span></span> 
  
> <span data-ttu-id="619e0-146">Les propriétés ont été copiées ou déplacées.</span><span class="sxs-lookup"><span data-stu-id="619e0-146">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="619e0-147">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="619e0-147">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="619e0-148">Impossible de copier un sous-objet car un sous-objet ayant le même nom d’affichage, spécifiée par la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) — existe déjà dans l’objet de destination.</span><span class="sxs-lookup"><span data-stu-id="619e0-148">A subobject cannot be copied because a subobject with the same display name — specified by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property — already exists in the destination object.</span></span> 
    
<span data-ttu-id="619e0-149">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="619e0-149">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="619e0-150">Le fournisseur de services n’implémente pas l’opération de copie.</span><span class="sxs-lookup"><span data-stu-id="619e0-150">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="619e0-151">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="619e0-151">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="619e0-152">L’objet source de l’opération de copie ou déplacement directement ou indirectement contient l’objet de destination.</span><span class="sxs-lookup"><span data-stu-id="619e0-152">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="619e0-153">Travail significatifs peut-être avoir été effectué avant cette condition a été détectée, et les objets source et de destination peuvent être modifiées partiellement.</span><span class="sxs-lookup"><span data-stu-id="619e0-153">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="619e0-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="619e0-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="619e0-155">L’interface identifié par le paramètre _lpInterface_ n’est pas pris en charge par l’objet de destination.</span><span class="sxs-lookup"><span data-stu-id="619e0-155">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="619e0-156">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="619e0-156">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="619e0-157">Une tentative a été effectuée pour accéder à un objet pour lequel l’appelant dispose d’autorisations insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="619e0-157">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="619e0-158">Cette erreur est renvoyée si l’objet de destination est identique à l’objet source.</span><span class="sxs-lookup"><span data-stu-id="619e0-158">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="619e0-159">Les valeurs suivantes peuvent être renvoyées dans la structure **SPropProblemArray** , mais pas en tant que valeurs de retour pour **CopyTo**.</span><span class="sxs-lookup"><span data-stu-id="619e0-159">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyTo**.</span></span> <span data-ttu-id="619e0-160">Les erreurs suivantes s’appliquent à une seule propriété :</span><span class="sxs-lookup"><span data-stu-id="619e0-160">The following errors apply to a single property:</span></span>
  
<span data-ttu-id="619e0-161">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="619e0-161">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="619e0-162">Soit l’indicateur MAPI_UNICODE a été défini et **CopyTo** ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et **CopyTo** prend en charge Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="619e0-162">Either the MAPI_UNICODE flag was set and **CopyTo** does not support Unicode, or MAPI_UNICODE was not set and **CopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="619e0-163">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="619e0-163">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="619e0-164">La propriété ne peut pas être modifiée par l’appelant car il s’agit d’une propriété en lecture seule, calculée par le propriétaire de l’objet de destination.</span><span class="sxs-lookup"><span data-stu-id="619e0-164">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="619e0-165">Cette erreur n’est pas lourde ; l’appelant doit autoriser l’opération de copie continuer.</span><span class="sxs-lookup"><span data-stu-id="619e0-165">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="619e0-166">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="619e0-166">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="619e0-167">Le type de propriété n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="619e0-167">The property type is invalid.</span></span>
    
<span data-ttu-id="619e0-168">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="619e0-168">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="619e0-169">Le type de propriété n’est pas le type attendu par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="619e0-169">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="619e0-170">Remarques</span><span class="sxs-lookup"><span data-stu-id="619e0-170">Remarks</span></span>

<span data-ttu-id="619e0-171">Par défaut, la méthode **IMAPIProp::CopyTo** copie ou déplace toutes les propriétés de l’objet en cours à un objet de destination.</span><span class="sxs-lookup"><span data-stu-id="619e0-171">By default, the **IMAPIProp::CopyTo** method copies or moves all of the current object's properties to a destination object.</span></span> <span data-ttu-id="619e0-172">**CopyTo** est utilisée lorsqu’un objet doit être copié ou déplacé exactement, avec tout ou partie de ses propriétés intactes.</span><span class="sxs-lookup"><span data-stu-id="619e0-172">**CopyTo** is used when an object should be copied or moved exactly, with all or most of its properties intact.</span></span> 
  
<span data-ttu-id="619e0-173">Les sous-objets de l’objet source sont automatiquement inclus dans l’opération et sont copiés ou déplacés dans leur intégralité.</span><span class="sxs-lookup"><span data-stu-id="619e0-173">Any subobjects in the source object are automatically included in the operation and are copied or moved in their entirety.</span></span> <span data-ttu-id="619e0-174">Par défaut, **CopyTo** remplace toutes les propriétés de l’objet cible qui correspondent aux propriétés de l’objet source.</span><span class="sxs-lookup"><span data-stu-id="619e0-174">By default, **CopyTo** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="619e0-175">Si les propriétés copiées ou déplacées existent déjà dans l’objet de destination, les propriétés existantes sont remplacées par les nouvelles propriétés, sauf si l’indicateur MAPI_NOREPLACE est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="619e0-175">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="619e0-176">Les informations existantes dans l’objet de destination n’est pas remplacé sont conservées.</span><span class="sxs-lookup"><span data-stu-id="619e0-176">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="619e0-177">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="619e0-177">Notes to implementers</span></span>

<span data-ttu-id="619e0-178">Vous pouvez fournir une implémentation complète de **CopyTo** ou reposer sur l’implémentation MAPI fournit de l’objet de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="619e0-178">You can provide a full implementation of **CopyTo** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="619e0-179">Si vous souhaitez utiliser l’implémentation MAPI, appelez **IMAPISupport::DoCopyTo**.</span><span class="sxs-lookup"><span data-stu-id="619e0-179">If you want to use the MAPI implementation, call **IMAPISupport::DoCopyTo**.</span></span> <span data-ttu-id="619e0-180">Toutefois, si vous procédez comme déléguer le traitement de **DoCopyTo** et vous sont transmis à l’indicateur MAPI_DECLINE_OK, évitez l’appel de la prise en charge et renvoyer MAPI_E_DECLINE_COPY au lieu de cela.</span><span class="sxs-lookup"><span data-stu-id="619e0-180">However, if you do delegate processing to **DoCopyTo** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="619e0-181">MAPI appellera avec cet indicateur pour éviter la récurrence possible qui peut se produire lorsque les dossiers sont copiés.</span><span class="sxs-lookup"><span data-stu-id="619e0-181">MAPI will call with this flag to avoid the possible recursion that can happen when folders are copied.</span></span> 
  
<span data-ttu-id="619e0-182">Étant donné que l’opération de copie peut être longue, vous devez afficher un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="619e0-182">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="619e0-183">Utilisez l’implémentation de [IMAPIProgress](imapiprogressiunknown.md) transmise dans le paramètre _lpProgress_ , le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="619e0-183">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="619e0-184">Si _lpProgress_ est **null**, appelez la méthode [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) pour utiliser l’implémentation MAPI.</span><span class="sxs-lookup"><span data-stu-id="619e0-184">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
<span data-ttu-id="619e0-185">N’essayez pas de définir des propriétés en lecture seule connues dans l’objet de destination ; Retournez à la place MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="619e0-185">Do not attempt to set any known read-only properties in the destination object; return MAPI_E_NO_ACCESS instead.</span></span>
  
<span data-ttu-id="619e0-186">Les objets source et de destination doivent utiliser les mêmes interfaces.</span><span class="sxs-lookup"><span data-stu-id="619e0-186">The source and destination objects should use the same interfaces.</span></span> <span data-ttu-id="619e0-187">Retourner MAPI_E_INVALID_PARAMETER si _lpInterface_ n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="619e0-187">Return MAPI_E_INVALID_PARAMETER if  _lpInterface_ is not set.</span></span> 
  
<span data-ttu-id="619e0-188">Retourner MAPI_E_INTERFACE_NOT_SUPPORTED si toutes les interfaces connus sont exclus.</span><span class="sxs-lookup"><span data-stu-id="619e0-188">Return MAPI_E_INTERFACE_NOT_SUPPORTED if all known interfaces are excluded.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="619e0-189">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="619e0-189">Notes to callers</span></span>

<span data-ttu-id="619e0-190">Ne définissez pas l’indicateur MAPI_DECLINE_OK ; MAPI utilise dans ses appels pour les implémentations de **CopyTo** de fournisseur de banque d’informations du message.</span><span class="sxs-lookup"><span data-stu-id="619e0-190">Do not set the MAPI_DECLINE_OK flag; MAPI uses it in its calls to message store provider **CopyTo** implementations.</span></span> 
  
<span data-ttu-id="619e0-191">Étant donné que les opérations de déplacement et de copie peuvent prendre un temps, vous devez demander l’affichage d’un indicateur de progression en définissant l’indicateur MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="619e0-191">Because copy and move operations can take time, you should request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="619e0-192">Vous pouvez définir le paramètre _lpProgress_ votre implémentation **IMAPIProgress**, si vous en avez un, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="619e0-192">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="619e0-193">Si _lpProgress_ est **null**, **CopyTo** utilisera l’indicateur de progression par défaut offertes par MAPI.</span><span class="sxs-lookup"><span data-stu-id="619e0-193">If  _lpProgress_ is **null**, **CopyTo** will use the default progress indicator that MAPI provides.</span></span> 
  
<span data-ttu-id="619e0-194">Vous pouvez supprimer l’affichage d’un indicateur de progression en définissant ne pas l’indicateur MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="619e0-194">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="619e0-195">**CopyTo** ignorera les paramètres _ulUIParam_ et _lpProgress_ et n’affiche pas l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="619e0-195">**CopyTo** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and will not display the indicator.</span></span> 
  
 <span data-ttu-id="619e0-196">**CopyTo** peuvent signaler des erreurs globaux et individuels ou des erreurs qui se produisent avec une ou plusieurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="619e0-196">**CopyTo** can report global and individual errors, or errors that occur with one or more properties.</span></span> <span data-ttu-id="619e0-197">Ces erreurs individuels sont placés dans une structure **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="619e0-197">These individual errors are placed in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="619e0-198">Vous pouvez supprimer le rapport d’erreurs au niveau de la propriété en passant **null**, au lieu d’un pointeur valide, pour le paramètre property problème tableau structure.</span><span class="sxs-lookup"><span data-stu-id="619e0-198">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="619e0-199">Si vous souhaitez recevoir des informations sur les erreurs, passez un pointeur de structure **SPropProblemArray** valid dans le paramètre _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="619e0-199">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="619e0-200">Lorsque **CopyTo** renvoie S_OK, vérifiez les erreurs possibles avec des propriétés individuelles dans la structure.</span><span class="sxs-lookup"><span data-stu-id="619e0-200">When **CopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="619e0-201">**CopyTo** retourne une erreur, aucune information n’est retournée dans la structure **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="619e0-201">When **CopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="619e0-202">Au lieu de cela, appelez [IMAPIProp::GetLastError](imapiprop-getlasterror.md) pour récupérer des informations d’erreur détaillé.</span><span class="sxs-lookup"><span data-stu-id="619e0-202">Instead, call [IMAPIProp::GetLastError](imapiprop-getlasterror.md) to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="619e0-203">Si **CopyTo** renvoie S_OK, libérer la structure **SPropProblemArray** retournée en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="619e0-203">If **CopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="619e0-204">Si vous copiez les propriétés qui sont uniques pour le type d’objet source, vous devez vous assurer que l’objet de destination est du même type.</span><span class="sxs-lookup"><span data-stu-id="619e0-204">If you copy properties that are unique to the source object type, you must ensure that the destination object is of the same type.</span></span> <span data-ttu-id="619e0-205">**CopyTo** ne vous empêche pas d’associant des propriétés qui appartiennent généralement à un type d’objet avec un autre type d’objet.</span><span class="sxs-lookup"><span data-stu-id="619e0-205">**CopyTo** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="619e0-206">C’est à vous pour copier des propriétés qui sont pertinents pour l’objet de destination.</span><span class="sxs-lookup"><span data-stu-id="619e0-206">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="619e0-207">Par exemple, vous devez copier pas les propriétés de message à un conteneur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="619e0-207">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="619e0-208">Pour vous assurer que vous copiez entre les objets du même type, vérifiez que l’objet source et de destination sont le même type, soit en comparaison des pointeurs d’objet ou en appelant [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="619e0-208">To ensure that you copy between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="619e0-209">Définir l’identificateur d’interface désigné par _lpInterface_ à l’interface standard pour l’objet source.</span><span class="sxs-lookup"><span data-stu-id="619e0-209">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="619e0-210">En outre, n’oubliez pas que le type d’objet ou la propriété **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) est la même pour les deux objets.</span><span class="sxs-lookup"><span data-stu-id="619e0-210">Also, be sure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="619e0-211">Par exemple, si vous copiez à partir d’un message, définissez _lpInterface_ IID_IMessage et le **PR_OBJECT_TYPE** pour les deux objets MAPI_MESSAGE.</span><span class="sxs-lookup"><span data-stu-id="619e0-211">For example, if you copy from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="619e0-212">Si un pointeur non valide est passé dans le paramètre _lpDestObj_ , le résultat est imprévisible.</span><span class="sxs-lookup"><span data-stu-id="619e0-212">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="619e0-213">Exclusion des propriétés sur un appel **CopyTo** peuvent être utile.</span><span class="sxs-lookup"><span data-stu-id="619e0-213">Excluding properties on a **CopyTo** call can be useful.</span></span> <span data-ttu-id="619e0-214">Par exemple, certains objets ont des propriétés qui sont spécifiques à une seule instance de l’objet, telles que la date et l’heure de remise du message.</span><span class="sxs-lookup"><span data-stu-id="619e0-214">For example, some objects have properties that are specific to a single instance of the object, such as the date and time of message delivery.</span></span> <span data-ttu-id="619e0-215">Pour éviter de copier l’heure de remise d’un message lorsque vous copiez le message vers un autre dossier, spécifiez **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) dans la propriété tag exclure le tableau.</span><span class="sxs-lookup"><span data-stu-id="619e0-215">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="619e0-216">Pour exclure la liste des destinataires d’un message, ajoutez la propriété **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) dans le tableau exclure.</span><span class="sxs-lookup"><span data-stu-id="619e0-216">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="619e0-217">Pour exclure les pièces jointes d’un message, ajoutez la propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="619e0-217">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="619e0-218">De même, empêcher la copie ou le déplacement d’un dossier ou une table de hiérarchie ou le contenu du conteneur de carnet d’adresses en incluant **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) dans la propriété tag exclure tableau.</span><span class="sxs-lookup"><span data-stu-id="619e0-218">Similarly, prevent the copying or moving of a folder or address book container's hierarchy or contents table by including **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="619e0-219">Pour exclure les propriétés de la copie ou l’opération de déplacement, inclut les balises de propriété dans le paramètre _lpExcludeProps_ .</span><span class="sxs-lookup"><span data-stu-id="619e0-219">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="619e0-220">Si vous passez les résultats de la macro **PROP_TAG** pour créer une balise de propriété à partir d’un identificateur spécifique dans le tableau de balise de propriété, toutes les propriétés de cet identificateur seront exclues.</span><span class="sxs-lookup"><span data-stu-id="619e0-220">If you pass the results of the **PROP_TAG** macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="619e0-221">Par exemple, l’entrée suivante dans le tableau de la propriété tag, toutes les propriétés d’un identificateur de 0x8002 à exclure, quel que soit le type :</span><span class="sxs-lookup"><span data-stu-id="619e0-221">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="619e0-222">La balise de propriété **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) ne peut pas être incluse dans le tableau _lpExcludeProps_ .</span><span class="sxs-lookup"><span data-stu-id="619e0-222">The **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag cannot be included in the  _lpExcludeProps_ array.</span></span> 
  
<span data-ttu-id="619e0-223">L’utilité de la fonctionnalité **CopyTo** pour exclure des interfaces n’est peut-être pas comme évidente comme l’utilité de l’exclusion des propriétés.</span><span class="sxs-lookup"><span data-stu-id="619e0-223">The usefulness of the **CopyTo** feature for excluding interfaces is perhaps not as obvious as the usefulness of excluding properties.</span></span> <span data-ttu-id="619e0-224">Vous pouvez exclure une interface lors de la copie à un objet qui n’a pas connaissance d’un groupe de propriétés.</span><span class="sxs-lookup"><span data-stu-id="619e0-224">You can exclude an interface when you copy to an object that has no knowledge of a group of properties.</span></span> <span data-ttu-id="619e0-225">Par exemple, si vous copiez les propriétés d’un dossier à une pièce jointe, les seules propriétés fonctionnant avec la pièce jointe sont les propriétés génériques disponibles avec n’importe quelle implémentation [IMAPIProp](imapipropiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="619e0-225">For example, if you copy properties from a folder to an attachment, the only properties that the attachment can work with are the generic properties available with any [IMAPIProp](imapipropiunknown.md) implementation.</span></span> <span data-ttu-id="619e0-226">En excluant [IMAPIFolder](imapifolderimapicontainer.md) à partir de l’opération de copie, la pièce jointe ne reçoit pas toutes les propriétés de dossier plus spécifiques.</span><span class="sxs-lookup"><span data-stu-id="619e0-226">By excluding [IMAPIFolder](imapifolderimapicontainer.md) from the copy operation, the attachment will not receive any of the more specific folder properties.</span></span> 
  
<span data-ttu-id="619e0-227">Lorsque vous utilisez le paramètre _rgiidExclude_ pour exclure une interface, il exclut également toutes les interfaces dérivées de cette interface.</span><span class="sxs-lookup"><span data-stu-id="619e0-227">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="619e0-228">Par exemple, à l’exclusion de [IMAPIContainer](imapicontainerimapiprop.md) , dossiers ou conteneurs de carnet d’adresses à exclure, selon le type de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="619e0-228">For example, excluding [IMAPIContainer](imapicontainerimapiprop.md) causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="619e0-229">N’excluent pas **IMAPIProp** ou [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) , car les interfaces autant dérivent de ces derniers.</span><span class="sxs-lookup"><span data-stu-id="619e0-229">Do not exclude **IMAPIProp** or [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) because so many interfaces derive from them.</span></span> 
  
<span data-ttu-id="619e0-230">MAPI_E_COMPUTED ignorer les erreurs renvoyées dans la structure **SPropProblemArray** dans le paramètre _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="619e0-230">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="619e0-231">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="619e0-231">MFCMAPI reference</span></span>

<span data-ttu-id="619e0-232">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="619e0-232">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="619e0-233">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="619e0-233">**File**</span></span>|<span data-ttu-id="619e0-234">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="619e0-234">**Function**</span></span>|<span data-ttu-id="619e0-235">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="619e0-235">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="619e0-236">File.cpp</span><span class="sxs-lookup"><span data-stu-id="619e0-236">File.cpp</span></span>  <br/> |<span data-ttu-id="619e0-237">LoadFromMSG</span><span class="sxs-lookup"><span data-stu-id="619e0-237">LoadFromMSG</span></span>  <br/> |<span data-ttu-id="619e0-238">MFCMAPI utilise la méthode **IMAPIProp::CopyTo** pour copier les propriétés d’un fichier .msg à un objet [IMAPIMessageSite](imapimessagesiteiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="619e0-238">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a .msg file to an [IMAPIMessageSite](imapimessagesiteiunknown.md) object.</span></span>  <br/> |
|<span data-ttu-id="619e0-239">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="619e0-239">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="619e0-240">CFolderDlg::HandlePaste</span><span class="sxs-lookup"><span data-stu-id="619e0-240">CFolderDlg::HandlePaste</span></span>  <br/> |<span data-ttu-id="619e0-241">MFCMAPI utilise la méthode **IMAPIProp::CopyTo** pour copier les propriétés d’un message source vers un message cible pendant une opération de collage.</span><span class="sxs-lookup"><span data-stu-id="619e0-241">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a source message to a target message during a paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="619e0-242">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="619e0-242">See also</span></span>



[<span data-ttu-id="619e0-243">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="619e0-243">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="619e0-244">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="619e0-244">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="619e0-245">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="619e0-245">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="619e0-246">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="619e0-246">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="619e0-247">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="619e0-247">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="619e0-248">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="619e0-248">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="619e0-249">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="619e0-249">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="619e0-250">Propriété canonique PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="619e0-250">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="619e0-251">Propriété canonique PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="619e0-251">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="619e0-252">Propriété canonique PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="619e0-252">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="619e0-253">Propriété canonique PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="619e0-253">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="619e0-254">Propriété canonique PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="619e0-254">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="619e0-255">Propriété canonique PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="619e0-255">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="619e0-256">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="619e0-256">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="619e0-257">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="619e0-257">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="619e0-258">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="619e0-258">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="619e0-259">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="619e0-259">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

