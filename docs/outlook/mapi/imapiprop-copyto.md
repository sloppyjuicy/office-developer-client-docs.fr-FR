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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f76b0a5482647fe3e181a36d7dcd8cb60ffc8985
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356391"
---
# <a name="imapipropcopyto"></a><span data-ttu-id="f131e-103">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="f131e-103">IMAPIProp::CopyTo</span></span>

  
  
<span data-ttu-id="f131e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f131e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f131e-105">Copie ou déplace toutes les propriétés, à l'exception des propriétés spécifiquement exclues.</span><span class="sxs-lookup"><span data-stu-id="f131e-105">Copies or moves all properties, except for specifically excluded properties.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="f131e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f131e-106">Parameters</span></span>

 <span data-ttu-id="f131e-107">_ciidExclude_</span><span class="sxs-lookup"><span data-stu-id="f131e-107">_ciidExclude_</span></span>
  
> <span data-ttu-id="f131e-108">dans Nombre d'interfaces à exclure lorsque les propriétés sont copiées ou déplacées.</span><span class="sxs-lookup"><span data-stu-id="f131e-108">[in] The count of interfaces to exclude when properties are copied or moved.</span></span>
    
 <span data-ttu-id="f131e-109">_rgiidExclude_</span><span class="sxs-lookup"><span data-stu-id="f131e-109">_rgiidExclude_</span></span>
  
> <span data-ttu-id="f131e-110">dans Tableau des identificateurs d'interface (IID) qui spécifient les interfaces qui ne doivent pas être utilisées lorsque des informations supplémentaires sont copiées ou déplacées vers l'objet de destination.</span><span class="sxs-lookup"><span data-stu-id="f131e-110">[in] An array of interface identifiers (IIDs) that specify interfaces that should not be used when supplemental information is copied or moved to the destination object.</span></span>
    
 <span data-ttu-id="f131e-111">_lpExcludeProps_</span><span class="sxs-lookup"><span data-stu-id="f131e-111">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="f131e-112">dans Pointeur vers un tableau de balises de propriété qui identifie les balises de propriété qui doivent être exclues de l'opération de copie ou de déplacement.</span><span class="sxs-lookup"><span data-stu-id="f131e-112">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="f131e-113">Le fait de transmettre **null** dans le paramètre _lpExcludeProps_ indique que toutes les propriétés de l'objet doivent être copiées ou déplacées.</span><span class="sxs-lookup"><span data-stu-id="f131e-113">Passing **null** in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="f131e-114">**CopyTo** renvoie MAPI_E_INVALID_PARAMETER lorsque le membre **cValues** de la structure [SPropProblemArray](spropproblemarray.md) vers laquelle pointe _lpExcludeProps_ est défini sur 0.</span><span class="sxs-lookup"><span data-stu-id="f131e-114">**CopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropProblemArray](spropproblemarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="f131e-115">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f131e-115">_ulUIParam_</span></span>
  
> <span data-ttu-id="f131e-116">dans Handle de la fenêtre parent de l'indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="f131e-116">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="f131e-117">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="f131e-117">_lpProgress_</span></span>
  
> <span data-ttu-id="f131e-118">dans Pointeur vers une implémentation d'indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="f131e-118">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="f131e-119">Si **null** est transmis dans le paramètre _lpProgress_ , MAPI fournit l'implémentation de la progression.</span><span class="sxs-lookup"><span data-stu-id="f131e-119">If **null** is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="f131e-120">Le paramètre _lpProgress_ est ignoré sauf si l'indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="f131e-120">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="f131e-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="f131e-121">_lpInterface_</span></span>
  
> <span data-ttu-id="f131e-122">dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder à l'objet pointé par le paramètre _lpDestObj_ .</span><span class="sxs-lookup"><span data-stu-id="f131e-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="f131e-123">Le paramètre _lpInterface_ ne doit pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="f131e-123">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="f131e-124">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="f131e-124">_lpDestObj_</span></span>
  
> <span data-ttu-id="f131e-125">dans Pointeur vers l'objet pour recevoir les propriétés copiées ou déplacées.</span><span class="sxs-lookup"><span data-stu-id="f131e-125">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="f131e-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f131e-126">_ulFlags_</span></span>
  
> <span data-ttu-id="f131e-127">dans Masque de des indicateurs qui contrôle l'opération de copie ou de déplacement.</span><span class="sxs-lookup"><span data-stu-id="f131e-127">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="f131e-128">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="f131e-128">The following flags can be set:</span></span>
    
<span data-ttu-id="f131e-129">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="f131e-129">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="f131e-130">Si **CopyTo** appelle la méthode [IMAPISupport::D ocopyto](imapisupport-docopyto.md) pour gérer l'opération de copie ou de déplacement, il doit renvoyer immédiatement immédiatement la valeur d'erreur MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="f131e-130">If **CopyTo** calls the [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="f131e-131">L'indicateur MAPI_DECLINE_OK est défini par MAPI pour limiter la récursivité.</span><span class="sxs-lookup"><span data-stu-id="f131e-131">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="f131e-132">Les clients ne définissent pas cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="f131e-132">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="f131e-133">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="f131e-133">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="f131e-134">Affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="f131e-134">Displays a progress indicator.</span></span>
    
<span data-ttu-id="f131e-135">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="f131e-135">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="f131e-136">**CopyTo** doit effectuer une opération Move au lieu d'une opération de copie.</span><span class="sxs-lookup"><span data-stu-id="f131e-136">**CopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="f131e-137">Lorsque cet indicateur n'est pas défini, **CopyTo** effectue une opération de copie.</span><span class="sxs-lookup"><span data-stu-id="f131e-137">When this flag is not set, **CopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="f131e-138">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="f131e-138">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="f131e-139">Les propriétés existantes dans l'objet de destination ne doivent pas être remplacées.</span><span class="sxs-lookup"><span data-stu-id="f131e-139">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="f131e-140">Lorsque cet indicateur n'est pas défini, **CopyTo** remplace les propriétés existantes.</span><span class="sxs-lookup"><span data-stu-id="f131e-140">When this flag is not set, **CopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="f131e-141">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="f131e-141">_lppProblems_</span></span>
  
> <span data-ttu-id="f131e-142">[in, out] Lors de l'entrée, pointeur vers un pointeur vers une structure **SPropProblemArray** ; Sinon, **null**, indiquant qu'aucune information d'erreur n'est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f131e-142">[in, out] On input, a pointer to a pointer to an **SPropProblemArray** structure; otherwise, **null**, indicating no need for error information.</span></span> <span data-ttu-id="f131e-143">Si _lppProblems_ est un pointeur valide sur Input, **CopyTo** renvoie des informations détaillées sur les erreurs lors de la copie d'une ou de plusieurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="f131e-143">If  _lppProblems_ is a valid pointer on input, **CopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f131e-144">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f131e-144">Return value</span></span>

<span data-ttu-id="f131e-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="f131e-145">S_OK</span></span> 
  
> <span data-ttu-id="f131e-146">Les propriétés ont été correctement copiées ou déplacées.</span><span class="sxs-lookup"><span data-stu-id="f131e-146">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="f131e-147">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="f131e-147">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="f131e-148">Un sous-objet ne peut pas être copié, car un sous-objet avec le même nom d'affichage, spécifié par la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), existe déjà dans l'objet de destination.</span><span class="sxs-lookup"><span data-stu-id="f131e-148">A subobject cannot be copied because a subobject with the same display name — specified by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property — already exists in the destination object.</span></span> 
    
<span data-ttu-id="f131e-149">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="f131e-149">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="f131e-150">Le fournisseur de services n'implémente pas l'opération de copie.</span><span class="sxs-lookup"><span data-stu-id="f131e-150">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="f131e-151">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="f131e-151">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="f131e-152">Objet source effectuant l'opération de copie ou de déplacement, directement ou indirectement, contenant l'objet de destination.</span><span class="sxs-lookup"><span data-stu-id="f131e-152">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="f131e-153">Un travail significatif a pu être effectué avant la découverte de cette condition, de sorte que les objets source et de destination puissent être partiellement modifiés.</span><span class="sxs-lookup"><span data-stu-id="f131e-153">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="f131e-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="f131e-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="f131e-155">L'interface identifiée par le paramètre _lpInterface_ n'est pas prise en charge par l'objet de destination.</span><span class="sxs-lookup"><span data-stu-id="f131e-155">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="f131e-156">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="f131e-156">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="f131e-157">Une tentative d'accès à un objet pour lequel l'appelant ne dispose pas des autorisations suffisantes a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="f131e-157">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="f131e-158">Cette erreur est renvoyée si l'objet de destination est identique à l'objet source.</span><span class="sxs-lookup"><span data-stu-id="f131e-158">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="f131e-159">Les valeurs suivantes peuvent être renvoyées dans la structure **SPropProblemArray** , mais pas comme valeurs de retour pour **CopyTo**.</span><span class="sxs-lookup"><span data-stu-id="f131e-159">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyTo**.</span></span> <span data-ttu-id="f131e-160">Les erreurs suivantes s'appliquent à une seule propriété:</span><span class="sxs-lookup"><span data-stu-id="f131e-160">The following errors apply to a single property:</span></span>
  
<span data-ttu-id="f131e-161">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="f131e-161">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="f131e-162">L'indicateur MAPI_UNICODE a été défini et **CopyTo** ne prend pas en charge Unicode, ou MAPI_UNICODE n'est pas défini et **CopyTo** prend en charge uniquement Unicode.</span><span class="sxs-lookup"><span data-stu-id="f131e-162">Either the MAPI_UNICODE flag was set and **CopyTo** does not support Unicode, or MAPI_UNICODE was not set and **CopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="f131e-163">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="f131e-163">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="f131e-164">La propriété ne peut pas être modifiée par l'appelant car il s'agit d'une propriété en lecture seule, calculée par le propriétaire de l'objet de destination.</span><span class="sxs-lookup"><span data-stu-id="f131e-164">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="f131e-165">Cette erreur n'est pas grave; l'appelant doit autoriser la poursuite de l'opération de copie.</span><span class="sxs-lookup"><span data-stu-id="f131e-165">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="f131e-166">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="f131e-166">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="f131e-167">Le type de propriété n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f131e-167">The property type is invalid.</span></span>
    
<span data-ttu-id="f131e-168">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="f131e-168">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="f131e-169">Le type de propriété n'est pas le type attendu par l'appelant.</span><span class="sxs-lookup"><span data-stu-id="f131e-169">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f131e-170">Remarques</span><span class="sxs-lookup"><span data-stu-id="f131e-170">Remarks</span></span>

<span data-ttu-id="f131e-171">Par défaut, la méthode **IMAPIProp:: CopyTo** copie ou déplace toutes les propriétés de l'objet actif vers un objet de destination.</span><span class="sxs-lookup"><span data-stu-id="f131e-171">By default, the **IMAPIProp::CopyTo** method copies or moves all of the current object's properties to a destination object.</span></span> <span data-ttu-id="f131e-172">**CopyTo** est utilisé lorsqu'un objet doit être copié ou déplacé exactement, avec toutes ou la plupart de ses propriétés intactes.</span><span class="sxs-lookup"><span data-stu-id="f131e-172">**CopyTo** is used when an object should be copied or moved exactly, with all or most of its properties intact.</span></span> 
  
<span data-ttu-id="f131e-173">Tous les sous-objets de l'objet source sont inclus automatiquement dans l'opération et sont copiés ou déplacés dans leur intégralité.</span><span class="sxs-lookup"><span data-stu-id="f131e-173">Any subobjects in the source object are automatically included in the operation and are copied or moved in their entirety.</span></span> <span data-ttu-id="f131e-174">Par défaut, **CopyTo** remplace toutes les propriétés de l'objet de destination qui correspondent aux propriétés de l'objet source.</span><span class="sxs-lookup"><span data-stu-id="f131e-174">By default, **CopyTo** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="f131e-175">Si une des propriétés copiées ou déplacées existe déjà dans l'objet de destination, les propriétés existantes sont remplacées par les nouvelles propriétés, sauf si l'indicateur MAPI_NOREPLACE est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="f131e-175">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="f131e-176">Les informations existantes de l'objet de destination qui ne sont pas remplacées restent intactes.</span><span class="sxs-lookup"><span data-stu-id="f131e-176">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f131e-177">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="f131e-177">Notes to implementers</span></span>

<span data-ttu-id="f131e-178">Vous pouvez fournir une implémentation complète de **CopyTo** ou reposer sur l'implémentation fournie par MAPI dans son objet support.</span><span class="sxs-lookup"><span data-stu-id="f131e-178">You can provide a full implementation of **CopyTo** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="f131e-179">Si vous souhaitez utiliser l'implémentation MAPI, appelez **IMAPISupport::D ocopyto**.</span><span class="sxs-lookup"><span data-stu-id="f131e-179">If you want to use the MAPI implementation, call **IMAPISupport::DoCopyTo**.</span></span> <span data-ttu-id="f131e-180">Toutefois, si vous déléguez le traitement à **DoCopyTo** et que vous avez passé l'indicateur MAPI_DECLINE_OK, évitez d'utiliser l'appel de prise en charge et de retourner MAPI_E_DECLINE_COPY à la place.</span><span class="sxs-lookup"><span data-stu-id="f131e-180">However, if you do delegate processing to **DoCopyTo** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="f131e-181">MAPI appellera avec cet indicateur pour éviter la récursivité possible pouvant se produire lorsque les dossiers sont copiés.</span><span class="sxs-lookup"><span data-stu-id="f131e-181">MAPI will call with this flag to avoid the possible recursion that can happen when folders are copied.</span></span> 
  
<span data-ttu-id="f131e-182">Étant donné que l'opération de copie peut être longue, vous devez afficher un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="f131e-182">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="f131e-183">Utilisez l'implémentation [méthode imapiprogress](imapiprogressiunknown.md) passée dans le paramètre _lpProgress_ , le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="f131e-183">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="f131e-184">Si _lpProgress_ est **null**, appelez la méthode [IMAPISupport::D OPROGRESSDIALOG](imapisupport-doprogressdialog.md) pour utiliser l'implémentation MAPI.</span><span class="sxs-lookup"><span data-stu-id="f131e-184">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
<span data-ttu-id="f131e-185">N'essayez pas de définir des propriétés en lecture seule connues dans l'objet de destination; Retournez MAPI_E_NO_ACCESS à la place.</span><span class="sxs-lookup"><span data-stu-id="f131e-185">Do not attempt to set any known read-only properties in the destination object; return MAPI_E_NO_ACCESS instead.</span></span>
  
<span data-ttu-id="f131e-186">Les objets source et de destination doivent utiliser les mêmes interfaces.</span><span class="sxs-lookup"><span data-stu-id="f131e-186">The source and destination objects should use the same interfaces.</span></span> <span data-ttu-id="f131e-187">Renvoie MAPI_E_INVALID_PARAMETER si _lpInterface_ n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="f131e-187">Return MAPI_E_INVALID_PARAMETER if  _lpInterface_ is not set.</span></span> 
  
<span data-ttu-id="f131e-188">Renvoie MAPI_E_INTERFACE_NOT_SUPPORTED si toutes les interfaces connues sont exclues.</span><span class="sxs-lookup"><span data-stu-id="f131e-188">Return MAPI_E_INTERFACE_NOT_SUPPORTED if all known interfaces are excluded.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="f131e-189">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="f131e-189">Notes to callers</span></span>

<span data-ttu-id="f131e-190">Ne définissez pas l'indicateur MAPI_DECLINE_OK; MAPI l'utilise dans ses appels aux implémentations du \*\*\*\* fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="f131e-190">Do not set the MAPI_DECLINE_OK flag; MAPI uses it in its calls to message store provider **CopyTo** implementations.</span></span> 
  
<span data-ttu-id="f131e-191">Étant donné que les opérations de copie et de déplacement peuvent prendre du temps, vous devez demander l'affichage d'un indicateur de progression en définissant l'indicateur MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="f131e-191">Because copy and move operations can take time, you should request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="f131e-192">Vous pouvez définir le paramètre _lpProgress_ sur votre implémentation de **méthode imapiprogress**, si vous en avez un, ou sur **null**.</span><span class="sxs-lookup"><span data-stu-id="f131e-192">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="f131e-193">Si _lpProgress_ a la **valeur null**, **CopyTo** utilise l'indicateur de progression par défaut fourni par MAPI.</span><span class="sxs-lookup"><span data-stu-id="f131e-193">If  _lpProgress_ is **null**, **CopyTo** will use the default progress indicator that MAPI provides.</span></span> 
  
<span data-ttu-id="f131e-194">Vous pouvez supprimer l'affichage d'un indicateur de progression en ne définissant pas l'indicateur MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="f131e-194">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="f131e-195">**CopyTo** ignorera les paramètres _ulUIParam_ et _lpProgress_ et n'affichera pas l'indicateur.</span><span class="sxs-lookup"><span data-stu-id="f131e-195">**CopyTo** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and will not display the indicator.</span></span> 
  
 <span data-ttu-id="f131e-196">**CopyTo** peut signaler des erreurs globales et individuelles, ou des erreurs qui se produisent avec une ou plusieurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="f131e-196">**CopyTo** can report global and individual errors, or errors that occur with one or more properties.</span></span> <span data-ttu-id="f131e-197">Ces erreurs individuelles sont placées dans une structure **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="f131e-197">These individual errors are placed in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="f131e-198">Vous pouvez supprimer le rapport d'erreurs au niveau de la propriété en transférant **null**, au lieu d'un pointeur valide, pour le paramètre de structure de tableau de problèmes de propriété.</span><span class="sxs-lookup"><span data-stu-id="f131e-198">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="f131e-199">Si vous souhaitez recevoir des informations sur les erreurs, transmettez un pointeur de structure **SPropProblemArray** valide dans le paramètre _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="f131e-199">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="f131e-200">Lorsque **CopyTo** renvoie S_OK, vérifiez la possibilité d'éventuelles erreurs avec des propriétés individuelles dans la structure.</span><span class="sxs-lookup"><span data-stu-id="f131e-200">When **CopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="f131e-201">Lorsque **CopyTo** renvoie une erreur, aucune information n'est renvoyée dans la structure **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="f131e-201">When **CopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="f131e-202">Au lieu de cela, appelez [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) pour récupérer des informations détaillées sur l'erreur.</span><span class="sxs-lookup"><span data-stu-id="f131e-202">Instead, call [IMAPIProp::GetLastError](imapiprop-getlasterror.md) to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="f131e-203">Si **CopyTo** renvoie S_OK, libérez la structure **SPropProblemArray** renvoyée en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="f131e-203">If **CopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="f131e-204">Si vous copiez des propriétés propres au type d'objet source, vous devez vous assurer que l'objet de destination est du même type.</span><span class="sxs-lookup"><span data-stu-id="f131e-204">If you copy properties that are unique to the source object type, you must ensure that the destination object is of the same type.</span></span> <span data-ttu-id="f131e-205">**CopyTo** ne vous empêche pas d'associer des propriétés qui appartiennent généralement à un type d'objet avec un autre type d'objet.</span><span class="sxs-lookup"><span data-stu-id="f131e-205">**CopyTo** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="f131e-206">Il vous revient de copier les propriétés qui ont un sens pour l'objet de destination.</span><span class="sxs-lookup"><span data-stu-id="f131e-206">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="f131e-207">Par exemple, vous ne devez pas copier les propriétés de message dans un conteneur de carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="f131e-207">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="f131e-208">Pour vous assurer d'effectuer une copie entre les objets du même type, vérifiez que l'objet source et de destination sont du même type, soit en comparant des pointeurs d'objet, soit en appelant [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f131e-208">To ensure that you copy between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="f131e-209">Définissez l'identificateur d'interface désigné par _lpInterface_ à l'interface standard pour l'objet source.</span><span class="sxs-lookup"><span data-stu-id="f131e-209">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="f131e-210">Assurez-vous également que le type d'objet ou la propriété **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) est identique pour les deux objets.</span><span class="sxs-lookup"><span data-stu-id="f131e-210">Also, be sure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="f131e-211">Par exemple, si vous copiez à partir d'un message, définissez _lpInterface_ sur IID_IMessage et le **PR_OBJECT_TYPE** pour les deux objets sur MAPI_MESSAGE.</span><span class="sxs-lookup"><span data-stu-id="f131e-211">For example, if you copy from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="f131e-212">Si un pointeur non valide est transmis dans le paramètre _lpDestObj_ , les résultats sont imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="f131e-212">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="f131e-213">L'exclusion des propriétés d'un appel **CopyTo** peut être utile.</span><span class="sxs-lookup"><span data-stu-id="f131e-213">Excluding properties on a **CopyTo** call can be useful.</span></span> <span data-ttu-id="f131e-214">Par exemple, certains objets ont des propriétés qui sont spécifiques à une seule instance de l'objet, telles que la date et l'heure de remise du message.</span><span class="sxs-lookup"><span data-stu-id="f131e-214">For example, some objects have properties that are specific to a single instance of the object, such as the date and time of message delivery.</span></span> <span data-ttu-id="f131e-215">Pour éviter de copier le délai de remise d'un message lorsque vous copiez le message dans un autre dossier, spécifiez **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) dans la balise de propriété Exclude Array.</span><span class="sxs-lookup"><span data-stu-id="f131e-215">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="f131e-216">Pour exclure la liste de destinataires d'un message, ajoutez la propriété **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) au tableau d'exclusion.</span><span class="sxs-lookup"><span data-stu-id="f131e-216">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="f131e-217">Pour exclure les pièces jointes d'un message, ajoutez la propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) au tableau.</span><span class="sxs-lookup"><span data-stu-id="f131e-217">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="f131e-218">De même, vous empêchez la copie ou le changement de la table des matières ou de la hiérarchie d'un dossier ou d'un conteneur de carnet d'adresses en incluant **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) dans la balise de propriété Exclude Array.</span><span class="sxs-lookup"><span data-stu-id="f131e-218">Similarly, prevent the copying or moving of a folder or address book container's hierarchy or contents table by including **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="f131e-219">Pour exclure les propriétés de l'opération de copie ou de déplacement, incluez les balises de propriété dans le paramètre _lpExcludeProps_ .</span><span class="sxs-lookup"><span data-stu-id="f131e-219">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="f131e-220">Si vous transmettez les résultats de la macro **PROP_TAG** pour créer une balise de propriété à partir d'un identificateur spécifique dans le tableau de balises de propriété, toutes les propriétés dotées de cet identificateur seront exclues.</span><span class="sxs-lookup"><span data-stu-id="f131e-220">If you pass the results of the **PROP_TAG** macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="f131e-221">Par exemple, l'entrée suivante dans le tableau de la balise de propriété entraîne l'exclusion de toutes les propriétés dotées d'un identificateur 0x8002, quel que soit le type:</span><span class="sxs-lookup"><span data-stu-id="f131e-221">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="f131e-222">La balise de propriété **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) ne peut pas être incluse dans le tableau _lpExcludeProps_ .</span><span class="sxs-lookup"><span data-stu-id="f131e-222">The **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag cannot be included in the  _lpExcludeProps_ array.</span></span> 
  
<span data-ttu-id="f131e-223">L'utilité de la fonctionnalité **CopyTo** pour l'exclusion d'interfaces n'est peut-être pas aussi évidente que l'exclusion des propriétés.</span><span class="sxs-lookup"><span data-stu-id="f131e-223">The usefulness of the **CopyTo** feature for excluding interfaces is perhaps not as obvious as the usefulness of excluding properties.</span></span> <span data-ttu-id="f131e-224">Vous pouvez exclure une interface lorsque vous copiez vers un objet qui n'a aucune connaissance d'un groupe de propriétés.</span><span class="sxs-lookup"><span data-stu-id="f131e-224">You can exclude an interface when you copy to an object that has no knowledge of a group of properties.</span></span> <span data-ttu-id="f131e-225">Par exemple, si vous copiez les propriétés d'un dossier vers une pièce jointe, les seules propriétés que la pièce jointe peut utiliser sont les propriétés génériques disponibles pour toute implémentation [IMAPIProp](imapipropiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="f131e-225">For example, if you copy properties from a folder to an attachment, the only properties that the attachment can work with are the generic properties available with any [IMAPIProp](imapipropiunknown.md) implementation.</span></span> <span data-ttu-id="f131e-226">En excluant [IMAPIFolder](imapifolderimapicontainer.md) de l'opération de copie, la pièce jointe ne reçoit pas les propriétés de dossier les plus spécifiques.</span><span class="sxs-lookup"><span data-stu-id="f131e-226">By excluding [IMAPIFolder](imapifolderimapicontainer.md) from the copy operation, the attachment will not receive any of the more specific folder properties.</span></span> 
  
<span data-ttu-id="f131e-227">Lorsque vous utilisez le paramètre _rgiidExclude_ pour exclure une interface, il exclut également toutes les interfaces dérivées de cette interface.</span><span class="sxs-lookup"><span data-stu-id="f131e-227">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="f131e-228">Par exemple, si vous excluez [IMAPIContainer](imapicontainerimapiprop.md) , les dossiers ou les conteneurs du carnet d'adresses seront exclus, selon le type de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f131e-228">For example, excluding [IMAPIContainer](imapicontainerimapiprop.md) causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="f131e-229">N'excluez pas **IMAPIProp** ou [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) car un grand nombre d'interfaces dérivent de celles-ci.</span><span class="sxs-lookup"><span data-stu-id="f131e-229">Do not exclude **IMAPIProp** or [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) because so many interfaces derive from them.</span></span> 
  
<span data-ttu-id="f131e-230">Ignore les erreurs MAPI_E_COMPUTED renvoyées dans la structure **SPropProblemArray** dans le paramètre _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="f131e-230">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f131e-231">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f131e-231">MFCMAPI reference</span></span>

<span data-ttu-id="f131e-232">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f131e-232">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f131e-233">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="f131e-233">**File**</span></span>|<span data-ttu-id="f131e-234">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="f131e-234">**Function**</span></span>|<span data-ttu-id="f131e-235">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="f131e-235">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f131e-236">File. cpp</span><span class="sxs-lookup"><span data-stu-id="f131e-236">File.cpp</span></span>  <br/> |<span data-ttu-id="f131e-237">LoadFromMSG</span><span class="sxs-lookup"><span data-stu-id="f131e-237">LoadFromMSG</span></span>  <br/> |<span data-ttu-id="f131e-238">MFCMAPI utilise la méthode **IMAPIProp:: CopyTo** pour copier les propriétés d'un fichier. MSG vers un objet [IMAPIMessageSite](imapimessagesiteiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="f131e-238">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a .msg file to an [IMAPIMessageSite](imapimessagesiteiunknown.md) object.</span></span>  <br/> |
|<span data-ttu-id="f131e-239">FolderDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="f131e-239">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="f131e-240">CFolderDlg:: HandlePaste</span><span class="sxs-lookup"><span data-stu-id="f131e-240">CFolderDlg::HandlePaste</span></span>  <br/> |<span data-ttu-id="f131e-241">MFCMAPI utilise la méthode **IMAPIProp:: CopyTo** pour copier les propriétés d'un message source vers un message cible pendant une opération de collage.</span><span class="sxs-lookup"><span data-stu-id="f131e-241">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a source message to a target message during a paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f131e-242">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f131e-242">See also</span></span>



[<span data-ttu-id="f131e-243">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="f131e-243">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="f131e-244">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="f131e-244">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="f131e-245">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f131e-245">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="f131e-246">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f131e-246">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="f131e-247">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="f131e-247">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="f131e-248">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="f131e-248">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="f131e-249">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f131e-249">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f131e-250">Propriété canonique PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="f131e-250">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="f131e-251">Propriété canonique PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="f131e-251">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="f131e-252">Propriété canonique PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="f131e-252">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="f131e-253">Propriété canonique PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="f131e-253">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="f131e-254">Propriété canonique PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="f131e-254">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="f131e-255">Propriété canonique PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="f131e-255">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="f131e-256">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="f131e-256">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="f131e-257">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="f131e-257">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="f131e-258">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f131e-258">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="f131e-259">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="f131e-259">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

