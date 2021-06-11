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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ee0ff8d32436f71020be2cdc91d6677bd4ec8e43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428535"
---
# <a name="xpproviderinit"></a><span data-ttu-id="d940d-103">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="d940d-103">XPProviderInit</span></span>

  
  
<span data-ttu-id="d940d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d940d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d940d-105">Initialise un fournisseur de transport pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="d940d-105">Initializes a transport provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d940d-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="d940d-106">Header file:</span></span>  <br/> |<span data-ttu-id="d940d-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="d940d-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="d940d-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="d940d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d940d-109">Fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="d940d-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="d940d-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="d940d-110">Called by:</span></span>  <br/> |<span data-ttu-id="d940d-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="d940d-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="d940d-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="d940d-112">Parameters</span></span>

 <span data-ttu-id="d940d-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="d940d-113">_hInstance_</span></span>
  
> <span data-ttu-id="d940d-114">[in] Instance de la bibliothèque de liens dynamiques (DLL) du fournisseur de transport que MAPI a utilisée lors du chargement de la DLL.</span><span class="sxs-lookup"><span data-stu-id="d940d-114">[in] The instance of the transport provider's dynamic-link library (DLL) that MAPI used when it loaded the DLL.</span></span>
    
 <span data-ttu-id="d940d-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="d940d-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="d940d-116">[in] Pointeur vers un objet d’allocation de mémoire exposant l’interface OLE **IMalloc.**</span><span class="sxs-lookup"><span data-stu-id="d940d-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="d940d-117">Le fournisseur de transport peut avoir besoin d’utiliser cette méthode d’allocation lors de l’utilisation de certaines interfaces telles que **IStream**.</span><span class="sxs-lookup"><span data-stu-id="d940d-117">The transport provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="d940d-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="d940d-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="d940d-119">[in] Pointeur vers la [fonction MAPIAllocateBuffer,](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="d940d-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="d940d-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="d940d-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="d940d-121">[in] Pointeur vers la [fonction MAPIAllocateMore,](mapiallocatemore.md) à utiliser pour allouer de la mémoire supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="d940d-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="d940d-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="d940d-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="d940d-123">[in] Pointeur vers la [fonction MAPIFreeBuffer,](mapifreebuffer.md) à utiliser pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="d940d-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="d940d-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d940d-124">_ulFlags_</span></span>
  
> <span data-ttu-id="d940d-125">[in] Masque de bits d’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="d940d-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="d940d-126">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="d940d-126">The following flag can be set:</span></span>
    
<span data-ttu-id="d940d-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="d940d-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="d940d-128">Le fournisseur est chargé dans le contexte d’un service Windows, un type spécial de processus sans accès à une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d940d-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="d940d-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="d940d-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="d940d-130">[in] Numéro de version de l’interface du fournisseur de services (SPI) que Mapi.dll utilise.</span><span class="sxs-lookup"><span data-stu-id="d940d-130">[in] Version number of the service provider interface (SPI) that Mapi.dll uses.</span></span> <span data-ttu-id="d940d-131">Pour le numéro de version actuel, voir le fichier d’en-tête Mapispi.h.</span><span class="sxs-lookup"><span data-stu-id="d940d-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="d940d-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="d940d-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="d940d-133">[out] Pointeur vers le numéro de version du SPI utilisé par ce fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="d940d-133">[out] Pointer to the version number of the SPI that this transport provider uses.</span></span> 
    
 <span data-ttu-id="d940d-134">_lppXPProvider_</span><span class="sxs-lookup"><span data-stu-id="d940d-134">_lppXPProvider_</span></span>
  
> <span data-ttu-id="d940d-135">[out] Pointeur vers un pointeur vers l’objet fournisseur de transport initialisé.</span><span class="sxs-lookup"><span data-stu-id="d940d-135">[out] Pointer to a pointer to the initialized transport provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d940d-136">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d940d-136">Return value</span></span>

<span data-ttu-id="d940d-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="d940d-137">S_OK</span></span> 
  
> <span data-ttu-id="d940d-138">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="d940d-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="d940d-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="d940d-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="d940d-140">La version SPI utilisée par MAPI n’est pas compatible avec la spi utilisée par ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d940d-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d940d-141">Remarques</span><span class="sxs-lookup"><span data-stu-id="d940d-141">Remarks</span></span>

<span data-ttu-id="d940d-142">MAPI appelle la fonction de point d’entrée **XPProviderInit** pour initialiser un fournisseur de transport à la suite d’une logon client.</span><span class="sxs-lookup"><span data-stu-id="d940d-142">MAPI calls the entry point function **XPProviderInit** to initialize a transport provider following a client logon.</span></span> <span data-ttu-id="d940d-143">**XPProviderInit est** appelé une fois pour chaque fournisseur de transport spécifié dans le profil du client.</span><span class="sxs-lookup"><span data-stu-id="d940d-143">**XPProviderInit** is called once for each transport provider specified in the client's profile.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d940d-144">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="d940d-144">Notes to implementers</span></span>

<span data-ttu-id="d940d-145">Un fournisseur de transport doit implémenter **XPProviderInit** en tant que fonction de point d’entrée dans la DLL du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d940d-145">A transport provider must implement **XPProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="d940d-146">L’implémentation doit être basée sur le prototype de fonction **XPPROVIDERINIT,** également spécifié dans Mapispi.h.</span><span class="sxs-lookup"><span data-stu-id="d940d-146">The implementation must be based on the **XPPROVIDERINIT** function prototype, also specified in Mapispi.h.</span></span> <span data-ttu-id="d940d-147">MAPI définit **XPPROVIDERINIT** pour utiliser le type d’appel d’initialisation MAPI standard, STDMAPIINITCALLTYPE, qui entraîne **XPProviderInit** à respecter la convention d’appel CDECL.</span><span class="sxs-lookup"><span data-stu-id="d940d-147">MAPI defines **XPPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **XPProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="d940d-148">Un avantage de CDECL est que les appels peuvent être tentés même si le nombre de paramètres d’appel ne correspond pas au nombre de paramètres définis.</span><span class="sxs-lookup"><span data-stu-id="d940d-148">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="d940d-149">Un fournisseur peut être initialisé plusieurs fois suite à l’apparition de plusieurs profils dans une utilisation simultanée ou de l’apparition de plusieurs fois dans le même profil.</span><span class="sxs-lookup"><span data-stu-id="d940d-149">A provider can be initialized multiple times as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="d940d-150">Étant donné que l’objet fournisseur contient du contexte, **XPProviderInit** doit retourner un autre objet fournisseur dans  _lppXPProvider_ pour chaque initialisation, même pour plusieurs initialisations dans le même processus.</span><span class="sxs-lookup"><span data-stu-id="d940d-150">Because the provider object contains context, **XPProviderInit** must return a different provider object in  _lppXPProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="d940d-151">Le fournisseur de transport doit utiliser les fonctions pointées par  _lpAllocateBuffer,_  _lpAllocateMore_ et  _lpFreeBuffer_ pour la plupart des allocations de mémoire et de la déallocation.</span><span class="sxs-lookup"><span data-stu-id="d940d-151">The transport provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="d940d-152">En particulier, le fournisseur doit utiliser ces fonctions pour allouer de la mémoire pour une utilisation par les applications clientes lors de l’appel d’interfaces d’objet telles que [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="d940d-152">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="d940d-153">Si le fournisseur s’attend également à utiliser l’allocation de mémoire OLE, il doit appeler la méthode **IUnknown::AddRef** de l’objet d’allocation pointé par le paramètre _lpMalloc._</span><span class="sxs-lookup"><span data-stu-id="d940d-153">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="d940d-154">Pour plus d’informations **sur l’écriture de XPProviderInit,** voir [Initialisation du fournisseur de transport.](initializing-the-transport-provider.md)</span><span class="sxs-lookup"><span data-stu-id="d940d-154">For more information about writing **XPProviderInit**, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span> <span data-ttu-id="d940d-155">Pour plus d’informations sur les fonctions de point d’entrée, voir [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="d940d-155">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d940d-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d940d-156">See also</span></span>



[<span data-ttu-id="d940d-157">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="d940d-157">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="d940d-158">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d940d-158">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)
  
[<span data-ttu-id="d940d-159">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="d940d-159">MSProviderInit</span></span>](msproviderinit.md)

