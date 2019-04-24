---
title: XPProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.XPProviderInit
api_type:
- COM
ms.assetid: df6eacf4-1cf9-4c25-806f-f87c38dad597
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ee0ff8d32436f71020be2cdc91d6677bd4ec8e43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325654"
---
# <a name="xpproviderinit"></a><span data-ttu-id="8827d-103">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="8827d-103">XPProviderInit</span></span>

  
  
<span data-ttu-id="8827d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8827d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8827d-105">Initialise un fournisseur de transport pour l'opération.</span><span class="sxs-lookup"><span data-stu-id="8827d-105">Initializes a transport provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8827d-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="8827d-106">Header file:</span></span>  <br/> |<span data-ttu-id="8827d-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="8827d-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="8827d-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="8827d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8827d-109">Fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="8827d-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="8827d-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="8827d-110">Called by:</span></span>  <br/> |<span data-ttu-id="8827d-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="8827d-111">MAPI</span></span>  <br/> |
   
```cpp
HRESULT XPProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPXPPROVIDER FAR * lppXPProvider
);
```

## <a name="parameters"></a><span data-ttu-id="8827d-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8827d-112">Parameters</span></span>

 <span data-ttu-id="8827d-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="8827d-113">_hInstance_</span></span>
  
> <span data-ttu-id="8827d-114">dans Instance de la bibliothèque de liens dynamiques (DLL) du fournisseur de transport utilisée par MAPI lors de la chargement de la DLL.</span><span class="sxs-lookup"><span data-stu-id="8827d-114">[in] The instance of the transport provider's dynamic-link library (DLL) that MAPI used when it loaded the DLL.</span></span>
    
 <span data-ttu-id="8827d-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="8827d-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="8827d-116">dans Pointeur vers un objet de l'allocation de mémoire qui expose \*\*\*\* l'interface OLE imalloc.</span><span class="sxs-lookup"><span data-stu-id="8827d-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="8827d-117">Le fournisseur de transport peut avoir besoin d'utiliser cette méthode d'allocation lorsque vous travaillez avec certaines interfaces telles que **IStream**.</span><span class="sxs-lookup"><span data-stu-id="8827d-117">The transport provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="8827d-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="8827d-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="8827d-119">dans Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="8827d-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="8827d-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="8827d-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="8827d-121">dans Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) à utiliser pour allouer de la mémoire supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="8827d-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="8827d-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="8827d-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="8827d-123">dans Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) à utiliser pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="8827d-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="8827d-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8827d-124">_ulFlags_</span></span>
  
> <span data-ttu-id="8827d-125">dans Masque de réindicateur des indicateurs.</span><span class="sxs-lookup"><span data-stu-id="8827d-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="8827d-126">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="8827d-126">The following flag can be set:</span></span>
    
<span data-ttu-id="8827d-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="8827d-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="8827d-128">Le fournisseur est en cours de chargement dans le contexte d'un service Windows, un type spécial de processus sans accès à une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8827d-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="8827d-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="8827d-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="8827d-130">dans Numéro de version de l'interface du fournisseur de services (SPI) utilisée par MAPI. dll.</span><span class="sxs-lookup"><span data-stu-id="8827d-130">[in] Version number of the service provider interface (SPI) that Mapi.dll uses.</span></span> <span data-ttu-id="8827d-131">Pour le numéro de version actuel, consultez le fichier d'en-tête Mapispi. h.</span><span class="sxs-lookup"><span data-stu-id="8827d-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="8827d-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="8827d-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="8827d-133">remarquer Pointeur vers le numéro de version du SPI utilisé par ce fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="8827d-133">[out] Pointer to the version number of the SPI that this transport provider uses.</span></span> 
    
 <span data-ttu-id="8827d-134">_lppXPProvider_</span><span class="sxs-lookup"><span data-stu-id="8827d-134">_lppXPProvider_</span></span>
  
> <span data-ttu-id="8827d-135">remarquer Pointeur vers un pointeur vers l'objet fournisseur de transport initialisé.</span><span class="sxs-lookup"><span data-stu-id="8827d-135">[out] Pointer to a pointer to the initialized transport provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8827d-136">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8827d-136">Return value</span></span>

<span data-ttu-id="8827d-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="8827d-137">S_OK</span></span> 
  
> <span data-ttu-id="8827d-138">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="8827d-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="8827d-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="8827d-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="8827d-140">La version SPI utilisée par MAPI n'est pas compatible avec le SPI utilisé par ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="8827d-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8827d-141">Remarques</span><span class="sxs-lookup"><span data-stu-id="8827d-141">Remarks</span></span>

<span data-ttu-id="8827d-142">MAPI appelle la fonction de point d'entrée **XPProviderInit** pour initialiser un fournisseur de transport à la suite d'une ouverture de session client.</span><span class="sxs-lookup"><span data-stu-id="8827d-142">MAPI calls the entry point function **XPProviderInit** to initialize a transport provider following a client logon.</span></span> <span data-ttu-id="8827d-143">**XPProviderInit** est appelé une fois pour chaque fournisseur de transport spécifié dans le profil du client.</span><span class="sxs-lookup"><span data-stu-id="8827d-143">**XPProviderInit** is called once for each transport provider specified in the client's profile.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8827d-144">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="8827d-144">Notes to implementers</span></span>

<span data-ttu-id="8827d-145">Un fournisseur de transport doit implémenter **XPProviderInit** en tant que fonction de point d'entrée dans la dll du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="8827d-145">A transport provider must implement **XPProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="8827d-146">L'implémentation doit être basée sur le prototype de fonction **XPPROVIDERINIT** , également spécifié dans Mapispi. h.</span><span class="sxs-lookup"><span data-stu-id="8827d-146">The implementation must be based on the **XPPROVIDERINIT** function prototype, also specified in Mapispi.h.</span></span> <span data-ttu-id="8827d-147">MAPI définit **XPPROVIDERINIT** pour utiliser le type d'appel d'initialisation MAPI standard, STDMAPIINITCALLTYPE, qui force **XPPROVIDERINIT** à suivre la Convention d'appel CDECL.</span><span class="sxs-lookup"><span data-stu-id="8827d-147">MAPI defines **XPPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **XPProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="8827d-148">L'un des avantages de CDECL est que les appels peuvent être tentés même si le nombre de paramètres d'appel ne correspond pas au nombre de paramètres définis.</span><span class="sxs-lookup"><span data-stu-id="8827d-148">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="8827d-149">Un fournisseur peut être initialisé plusieurs fois à la suite de l'affichage simultané de plusieurs profils ou de plusieurs fois dans le même profil.</span><span class="sxs-lookup"><span data-stu-id="8827d-149">A provider can be initialized multiple times as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="8827d-150">Étant donné que l'objet fournisseur contient le contexte, **XPProviderInit** doit renvoyer un objet fournisseur différent dans _lppXPProvider_ pour chaque initialisation, même pour plusieurs initialisations dans le même processus.</span><span class="sxs-lookup"><span data-stu-id="8827d-150">Because the provider object contains context, **XPProviderInit** must return a different provider object in  _lppXPProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="8827d-151">Le fournisseur de transport doit utiliser les fonctions pointées par _lpAllocateBuffer_, _lpAllocateMore_et _lpFreeBuffer_ pour la plupart de l'allocation et de la libération de mémoire.</span><span class="sxs-lookup"><span data-stu-id="8827d-151">The transport provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="8827d-152">En particulier, le fournisseur doit utiliser ces fonctions pour allouer de la mémoire à utiliser par les applications clientes lors de l'appel d'interfaces d'objets telles que [IMAPIProp:: GetProps](imapiprop-getprops.md) et [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="8827d-152">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="8827d-153">Si le fournisseur s'attend également à utiliser l'allocateur de mémoire OLE, il doit appeler la méthode **IUnknown:: AddRef** de l'objet allocater pointé par le paramètre _lpMalloc_ .</span><span class="sxs-lookup"><span data-stu-id="8827d-153">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="8827d-154">Pour plus d'informations sur l'écriture de **XPProviderInit**, consultez [la rubrique initialisation du fournisseur de transport](initializing-the-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8827d-154">For more information about writing **XPProviderInit**, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span> <span data-ttu-id="8827d-155">Pour plus d'informations sur les fonctions de point d'entrée, consultez [la rubrique implémentation d'une fonction de point d'entrée du fournisseur de services](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="8827d-155">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8827d-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8827d-156">See also</span></span>



[<span data-ttu-id="8827d-157">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="8827d-157">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="8827d-158">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8827d-158">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)
  
[<span data-ttu-id="8827d-159">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="8827d-159">MSProviderInit</span></span>](msproviderinit.md)

