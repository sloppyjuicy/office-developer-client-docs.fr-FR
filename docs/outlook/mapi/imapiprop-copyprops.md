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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7319f1abb4a74ee17b0a4a1220215c29434d256b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345506"
---
# <a name="imapipropcopyprops"></a><span data-ttu-id="1f8b1-103">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="1f8b1-103">IMAPIProp::CopyProps</span></span>

  
  
<span data-ttu-id="1f8b1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f8b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f8b1-105">Copie ou déplace les propriétés sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-105">Copies or moves selected properties.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="1f8b1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f8b1-106">Parameters</span></span>

 <span data-ttu-id="1f8b1-107">_lpIncludeProps_</span><span class="sxs-lookup"><span data-stu-id="1f8b1-107">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="1f8b1-108">dans Pointeur vers un tableau de balises de propriété qui spécifie les propriétés à copier ou déplacer.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-108">[in] A pointer to a property tag array that specifies the properties to copy or move.</span></span> <span data-ttu-id="1f8b1-109">**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) ne peut pas être inclus dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-109">**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) cannot be included in the array.</span></span> <span data-ttu-id="1f8b1-110">Le paramètre _lpIncludeProps_ ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-110">The  _lpIncludeProps_ parameter cannot be **null**.</span></span>
    
 <span data-ttu-id="1f8b1-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1f8b1-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="1f8b1-112">dans Handle de la fenêtre parent de l'indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-112">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="1f8b1-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="1f8b1-113">_lpProgress_</span></span>
  
> <span data-ttu-id="1f8b1-114">dans Pointeur vers une implémentation d'un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-114">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="1f8b1-115">Si la **valeur null** est transmise au paramètre _lpProgress_ , l'indicateur de progression est affiché à l'aide de l'implémentation MAPI.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-115">If **null** is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="1f8b1-116">Le paramètre _lpProgress_ est ignoré sauf si l'indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="1f8b1-116">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="1f8b1-117">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="1f8b1-117">_lpInterface_</span></span>
  
> <span data-ttu-id="1f8b1-118">dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface qui doit être utilisée pour accéder à l'objet pointé par le paramètre _lpDestObj_ .</span><span class="sxs-lookup"><span data-stu-id="1f8b1-118">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="1f8b1-119">Le paramètre _lpInterface_ ne doit pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-119">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="1f8b1-120">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="1f8b1-120">_lpDestObj_</span></span>
  
> <span data-ttu-id="1f8b1-121">dans Pointeur vers l'objet pour recevoir les propriétés copiées ou déplacées.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-121">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="1f8b1-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1f8b1-122">_ulFlags_</span></span>
  
> <span data-ttu-id="1f8b1-123">dans Masque de des indicateurs qui contrôle l'opération de copie ou de déplacement.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-123">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="1f8b1-124">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="1f8b1-124">The following flags can be set:</span></span>
    
<span data-ttu-id="1f8b1-125">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="1f8b1-125">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="1f8b1-126">Si **CopyProps** appelle la méthode [IMAPISupport::D ocopyprops](imapisupport-docopyprops.md) pour gérer l'opération de copie ou de déplacement, il doit renvoyer immédiatement immédiatement la valeur d'erreur MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-126">If **CopyProps** calls the [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="1f8b1-127">L'indicateur MAPI_DECLINE_OK est défini par MAPI pour limiter la récursivité.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-127">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="1f8b1-128">Les clients ne définissent pas cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-128">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="1f8b1-129">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="1f8b1-129">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="1f8b1-130">Affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-130">Displays a progress indicator.</span></span>
    
<span data-ttu-id="1f8b1-131">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="1f8b1-131">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="1f8b1-132">**CopyProps** doit effectuer une opération de déplacement au lieu d'une opération de copie.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-132">**CopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="1f8b1-133">Lorsque cet indicateur n'est pas défini, **CopyProps** effectue une opération de copie.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-133">When this flag is not set, **CopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="1f8b1-134">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="1f8b1-134">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="1f8b1-135">Les propriétés existantes dans l'objet de destination ne doivent pas être remplacées.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-135">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="1f8b1-136">Lorsque cet indicateur n'est pas défini, **CopyProps** remplace les propriétés existantes.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-136">When this flag is not set, **CopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="1f8b1-137">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="1f8b1-137">_lppProblems_</span></span>
  
> <span data-ttu-id="1f8b1-138">[in, out] Lors de l'entrée, pointeur vers un pointeur vers une structure [SPropProblemArray](spropproblemarray.md) ; Sinon, **null**, ce qui indique qu'il n'est pas nécessaire d'obtenir des informations sur l'erreur.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-138">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, **null**, indicating that there is no need for error information.</span></span> <span data-ttu-id="1f8b1-139">Si _lppProblems_ est un pointeur valide sur l'entrée, **CopyProps** renvoie des informations détaillées sur les erreurs lors de la copie d'une ou de plusieurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-139">If  _lppProblems_ is a valid pointer on input, **CopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1f8b1-140">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1f8b1-140">Return value</span></span>

<span data-ttu-id="1f8b1-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="1f8b1-141">S_OK</span></span> 
  
> <span data-ttu-id="1f8b1-142">Les propriétés ont été correctement copiées ou déplacées.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-142">Properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="1f8b1-143">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="1f8b1-143">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="1f8b1-144">Un sous-objet ne peut pas être copié, car un sous-objet portant le même nom d'affichage, défini par la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), existe déjà dans l'objet de destination.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-144">A subobject cannot be copied because a subobject with the same display name, defined by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, already exists in the destination object.</span></span> 
    
<span data-ttu-id="1f8b1-145">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="1f8b1-145">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="1f8b1-146">Le fournisseur de services n'implémente pas l'opération de copie.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-146">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="1f8b1-147">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="1f8b1-147">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="1f8b1-148">Objet source effectuant l'opération de copie ou de déplacement, directement ou indirectement, contenant l'objet de destination.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-148">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="1f8b1-149">Un travail significatif a pu être effectué avant la découverte de cette condition, de sorte que les objets source et de destination puissent être partiellement modifiés.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-149">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="1f8b1-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="1f8b1-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="1f8b1-151">L'interface identifiée par le paramètre _lpInterface_ n'est pas prise en charge par l'objet de destination.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-151">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="1f8b1-152">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="1f8b1-152">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="1f8b1-153">Une tentative d'accès à un objet pour lequel l'appelant ne dispose pas des autorisations suffisantes a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-153">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="1f8b1-154">Cette erreur est renvoyée si l'objet de destination est identique à l'objet source.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-154">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="1f8b1-155">Les valeurs suivantes peuvent être renvoyées dans la structure **SPropProblemArray** , mais pas comme valeurs de retour pour **CopyProps**.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-155">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyProps**.</span></span> <span data-ttu-id="1f8b1-156">Ces erreurs s'appliquent à une seule propriété.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-156">These errors apply to a single property.</span></span>
  
<span data-ttu-id="1f8b1-157">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="1f8b1-157">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="1f8b1-158">L'indicateur MAPI_UNICODE a été défini et **CopyProps** ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et **CopyProps** prend en charge uniquement Unicode.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-158">Either the MAPI_UNICODE flag was set and **CopyProps** does not support Unicode, or MAPI_UNICODE was not set and **CopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="1f8b1-159">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="1f8b1-159">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="1f8b1-160">La propriété ne peut pas être modifiée par l'appelant car il s'agit d'une propriété en lecture seule, calculée par le propriétaire de l'objet de destination.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-160">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="1f8b1-161">Cette erreur n'est pas grave; l'appelant doit autoriser la poursuite de l'opération de copie.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-161">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="1f8b1-162">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="1f8b1-162">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="1f8b1-163">Le type de propriété n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-163">The property type is invalid.</span></span>
    
<span data-ttu-id="1f8b1-164">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="1f8b1-164">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="1f8b1-165">Le type de propriété n'est pas le type attendu par l'appelant.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-165">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1f8b1-166">Remarques</span><span class="sxs-lookup"><span data-stu-id="1f8b1-166">Remarks</span></span>

<span data-ttu-id="1f8b1-167">La méthode **IMAPIProp:: CopyProps** copie ou déplace les propriétés sélectionnées de l'objet actif vers un objet de destination.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-167">The **IMAPIProp::CopyProps** method copies or moves selected properties from the current object to a destination object.</span></span> <span data-ttu-id="1f8b1-168">**CopyProps** est principalement utilisé pour répondre à des messages et les transférer, où seules quelques-unes des propriétés du message d'origine sont transférées avec la copie de réponse ou de transfert.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-168">**CopyProps** is used mainly for replying to and forwarding messages, where only some of the properties from the original message travel with the reply or forwarded copy.</span></span> 
  
<span data-ttu-id="1f8b1-169">Tous les sous-objets de l'objet source sont inclus automatiquement dans l'opération et copiés ou déplacés dans leur intégralité, indépendamment de l'utilisation des propriétés indiquées par la structure [SPropTagArray](sproptagarray.md) .</span><span class="sxs-lookup"><span data-stu-id="1f8b1-169">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety, regardless of the use of properties indicated by the [SPropTagArray](sproptagarray.md) structure.</span></span> <span data-ttu-id="1f8b1-170">Par défaut, **CopyProps** remplace toutes les propriétés de l'objet de destination qui correspondent aux propriétés de l'objet source.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-170">By default, **CopyProps** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="1f8b1-171">Si une des propriétés copiées ou déplacées existe déjà dans l'objet de destination, les propriétés existantes sont remplacées par les nouvelles propriétés, sauf si l'indicateur MAPI_NOREPLACE est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="1f8b1-171">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="1f8b1-172">Les informations existantes de l'objet de destination qui ne sont pas remplacées restent intactes.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-172">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1f8b1-173">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="1f8b1-173">Notes to implementers</span></span>

<span data-ttu-id="1f8b1-174">Vous pouvez fournir une implémentation complète de **CopyProps** ou vous reposer sur l'implémentation fournie par MAPI dans son objet support.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-174">You can provide a full implementation of **CopyProps** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="1f8b1-175">Si vous souhaitez utiliser l'implémentation MAPI, appelez la méthode **IMAPISupport::D ocopyprops** .</span><span class="sxs-lookup"><span data-stu-id="1f8b1-175">If you want to use the MAPI implementation, call the **IMAPISupport::DoCopyProps** method.</span></span> <span data-ttu-id="1f8b1-176">Toutefois, si vous déléguez le traitement à **DoCopyProps** et que vous avez passé l'indicateur MAPI_DECLINE_OK, évitez d'utiliser l'appel de prise en charge et de retourner MAPI_E_DECLINE_COPY à la place.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-176">However, if you do delegate processing to **DoCopyProps** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="1f8b1-177">Vous serez appelé avec cet indicateur par MAPI pour éviter la récursivité possible qui peut se produire lorsque vous copiez des dossiers.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-177">You will be called with this flag by MAPI to avoid the possible recursion that can occur when you copy folders.</span></span> 
  
<span data-ttu-id="1f8b1-178">Étant donné que l'opération de copie peut être longue, vous devez afficher un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-178">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="1f8b1-179">Utilisez l'implémentation [méthode imapiprogress](imapiprogressiunknown.md) qui est transmise dans le paramètre _lpProgress_ , le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-179">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation that is passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="1f8b1-180">Si _lpProgress_ est **null**, appelez la méthode [IMAPISupport::D OPROGRESSDIALOG](imapisupport-doprogressdialog.md) pour utiliser l'implémentation MAPI.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-180">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1f8b1-181">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="1f8b1-181">Notes to callers</span></span>

<span data-ttu-id="1f8b1-182">Ne définissez pas l'indicateur MAPI_DECLINE_OK; Il est utilisé par MAPI dans ses appels aux implémentations du fournisseur de banque de **CopyProps** .</span><span class="sxs-lookup"><span data-stu-id="1f8b1-182">Do not set the MAPI_DECLINE_OK flag; it is used by MAPI in its calls to message store provider **CopyProps** implementations.</span></span> 
  
<span data-ttu-id="1f8b1-183">Étant donné que les opérations de copie et de déplacement peuvent prendre du temps, il est recommandé de demander l'affichage d'un indicateur de progression en définissant l'indicateur MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-183">Because copy and move operations can take time, it is wise to request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="1f8b1-184">Vous pouvez définir le paramètre _lpProgress_ sur votre implémentation de **méthode imapiprogress**, si vous en avez un, ou sur **null**.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-184">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="1f8b1-185">Si _lpProgress_ a la **valeur null**, **CopyProps** utilise l'indicateur de progression par défaut fourni par MAPI.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-185">If  _lpProgress_ is **null**, **CopyProps** will use the default progress indicator provided by MAPI.</span></span> 
  
<span data-ttu-id="1f8b1-186">Vous pouvez supprimer l'affichage d'un indicateur de progression en ne définissant pas l'indicateur MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-186">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="1f8b1-187">**CopyProps** ignorera les paramètres _ulUIParam_ et _lpProgress_ et évitera l'affichage de l'indicateur.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-187">**CopyProps** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and avoid displaying the indicator.</span></span> 
  
 <span data-ttu-id="1f8b1-188">**CopyProps** peut signaler des erreurs globales et individuelles, ou des erreurs qui se produisent avec une ou plusieurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-188">**CopyProps** can report global and individual errors, or errors that occur with one or more of the properties.</span></span> <span data-ttu-id="1f8b1-189">Ces erreurs individuelles sont placées dans une structure **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="1f8b1-189">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="1f8b1-190">Vous pouvez supprimer le rapport d'erreurs au niveau de la propriété en transférant **null**, au lieu d'un pointeur valide, pour le paramètre de structure de tableau de problèmes de propriété.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-190">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="1f8b1-191">Si vous souhaitez recevoir des informations sur les erreurs, transmettez un pointeur de structure **SPropProblemArray** valide dans le paramètre _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="1f8b1-191">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="1f8b1-192">Lorsque **CopyProps** renvoie S_OK, vérifiez la possibilité d'éventuelles erreurs avec des propriétés individuelles dans la structure.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-192">When **CopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="1f8b1-193">Lorsque **CopyProps** renvoie une erreur, aucune information n'est renvoyée dans la structure **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="1f8b1-193">When **CopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="1f8b1-194">À la place, appelez la méthode [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) pour extraire des informations détaillées sur les erreurs.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-194">Instead, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="1f8b1-195">Si **CopyProps** renvoie S_OK, libérez la structure **SPropProblemArray** renvoyée en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="1f8b1-195">If **CopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="1f8b1-196">Si vous copiez des propriétés propres au type d'objet source, vous devez vous assurer que l'objet de destination est du même type.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-196">If you are copying properties that are unique to the source object type, you must make sure that the destination object is of the same type.</span></span> <span data-ttu-id="1f8b1-197">**CopyProps** ne vous empêche pas d'associer des propriétés qui appartiennent généralement à un type d'objet avec un autre type d'objet.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-197">**CopyProps** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="1f8b1-198">Il vous revient de copier les propriétés qui ont un sens pour l'objet de destination.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-198">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="1f8b1-199">Par exemple, vous ne devez pas copier les propriétés de message dans un conteneur de carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-199">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="1f8b1-200">Pour vous assurer que vous effectuez une copie entre des objets du même type, vérifiez que l'objet source et de destination sont du même type, soit en comparant des pointeurs d'objet, soit en appelant la méthode [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="1f8b1-200">To ensure that you are copying between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="1f8b1-201">Définissez l'identificateur d'interface désigné par _lpInterface_ à l'interface standard pour l'objet source.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-201">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="1f8b1-202">Assurez-vous également que le type d'objet ou la propriété **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) est identique pour les deux objets.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-202">Also, ensure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="1f8b1-203">Par exemple, si vous effectuez une copie à partir d'un message, définissez _lpInterface_ sur IID_IMessage et le **PR_OBJECT_TYPE** pour les deux objets sur MAPI_MESSAGE.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-203">For example, if you are copying from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="1f8b1-204">Si un pointeur non valide est transmis dans le paramètre _lpDestObj_ , les résultats sont imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-204">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="1f8b1-205">Pour copier la liste des destinataires d'un message, appelez la méthode **CopyProps** du message et incluez la propriété **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) dans le tableau des balises de propriété.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-205">To copy a message's recipient list, call the message's **CopyProps** method and include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array.</span></span> <span data-ttu-id="1f8b1-206">Pour copier les pièces jointes du message, incluez la propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1f8b1-206">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="1f8b1-207">Pour copier la table de hiérarchie ou de contenu d'un conteneur de carnet d'adresses ou de dossier, incluez les propriétés **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) dans le Tableau de balises de propriété.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-207">To copy a folder or address book container's hierarchy or contents table, include the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) properties in the property tag array.</span></span> <span data-ttu-id="1f8b1-208">Pour inclure le tableau de contenu associé à un dossier, incluez la propriété **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-208">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1f8b1-209">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1f8b1-209">MFCMAPI reference</span></span>

<span data-ttu-id="1f8b1-210">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-210">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1f8b1-211">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="1f8b1-211">**File**</span></span>|<span data-ttu-id="1f8b1-212">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="1f8b1-212">**Function**</span></span>|<span data-ttu-id="1f8b1-213">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="1f8b1-213">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1f8b1-214">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="1f8b1-214">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="1f8b1-215">CopyNamedProps</span><span class="sxs-lookup"><span data-stu-id="1f8b1-215">CopyNamedProps</span></span>  <br/> |<span data-ttu-id="1f8b1-216">MFCMAPI utilise la méthode **IMAPIProp:: CopyProps** pour copier les propriétés nommées d'un message à un autre.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-216">MFCMAPI uses the **IMAPIProp::CopyProps** method to copy named properties from one message to another.</span></span>  <br/> |
|<span data-ttu-id="1f8b1-217">SingleMAPIPropListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="1f8b1-217">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="1f8b1-218">CSingleMAPIPropListCtrl:: OnPasteProperty</span><span class="sxs-lookup"><span data-stu-id="1f8b1-218">CSingleMAPIPropListCtrl::OnPasteProperty</span></span>  <br/> |<span data-ttu-id="1f8b1-219">MFCMAPI utilise la méthode **IMAPIProp:: CopyProps** pour coller une propriété qui a été copiée à partir d'un autre objet.</span><span class="sxs-lookup"><span data-stu-id="1f8b1-219">MFCMAPI uses the **IMAPIProp::CopyProps** method to paste a property that has been copied from another object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1f8b1-220">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f8b1-220">See also</span></span>



[<span data-ttu-id="1f8b1-221">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="1f8b1-221">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="1f8b1-222">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1f8b1-222">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="1f8b1-223">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="1f8b1-223">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="1f8b1-224">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="1f8b1-224">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="1f8b1-225">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="1f8b1-225">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
  
[<span data-ttu-id="1f8b1-226">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="1f8b1-226">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="1f8b1-227">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="1f8b1-227">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="1f8b1-228">Propriété canonique PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="1f8b1-228">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="1f8b1-229">Propriété canonique PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="1f8b1-229">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="1f8b1-230">Propriété canonique PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="1f8b1-230">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="1f8b1-231">Propriété canonique PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="1f8b1-231">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="1f8b1-232">Propriété canonique PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="1f8b1-232">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="1f8b1-233">Propriété canonique PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="1f8b1-233">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="1f8b1-234">Propriété canonique PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="1f8b1-234">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="1f8b1-235">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="1f8b1-235">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="1f8b1-236">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="1f8b1-236">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="1f8b1-237">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1f8b1-237">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="1f8b1-238">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="1f8b1-238">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

