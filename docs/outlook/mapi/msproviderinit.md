---
title: MSProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MSProviderInit
api_type:
- HeaderDef
ms.assetid: 230c66c4-ab04-4fa6-946f-9f4b704f2842
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9a5f8b44f9d795282ccfd61fd32a306c5478ed21
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416236"
---
# <a name="msproviderinit"></a><span data-ttu-id="79003-103">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="79003-103">MSProviderInit</span></span>

  
  
<span data-ttu-id="79003-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79003-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79003-105">Initialise un fournisseur de magasins de messages pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="79003-105">Initializes a message store provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="79003-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="79003-106">Header file:</span></span>  <br/> |<span data-ttu-id="79003-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="79003-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="79003-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="79003-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="79003-109">Fournisseurs de magasins de messages</span><span class="sxs-lookup"><span data-stu-id="79003-109">Message store providers</span></span>  <br/> |
|<span data-ttu-id="79003-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="79003-110">Called by:</span></span>  <br/> |<span data-ttu-id="79003-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="79003-111">MAPI</span></span>  <br/> |
   
```cpp
HRESULT MSProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPMSPROVIDER FAR * lppMSProvider
);
```

## <a name="parameters"></a><span data-ttu-id="79003-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79003-112">Parameters</span></span>

 <span data-ttu-id="79003-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="79003-113">_hInstance_</span></span>
  
> <span data-ttu-id="79003-114">[in] Instance de la bibliothèque de liens dynamiques (DLL) du fournisseur de magasins de messages que MAPI a utilisée lors de sa liaison.</span><span class="sxs-lookup"><span data-stu-id="79003-114">[in] The instance of the message store provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="79003-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="79003-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="79003-116">[in] Pointeur vers un objet d’allocation de mémoire exposant l’interface OLE **IMalloc.**</span><span class="sxs-lookup"><span data-stu-id="79003-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="79003-117">Le fournisseur de magasin de messages peut avoir besoin d’utiliser cette méthode d’allocation lors de l’utilisation de certaines interfaces telles que **IStream**.</span><span class="sxs-lookup"><span data-stu-id="79003-117">The message store provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="79003-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="79003-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="79003-119">[in] Pointeur vers la [fonction MAPIAllocateBuffer,](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="79003-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="79003-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="79003-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="79003-121">[in] Pointeur vers la [fonction MAPIAllocateMore,](mapiallocatemore.md) à utiliser pour allouer de la mémoire supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="79003-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="79003-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="79003-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="79003-123">[in] Pointeur vers la [fonction MAPIFreeBuffer,](mapifreebuffer.md) à utiliser pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="79003-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="79003-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="79003-124">_ulFlags_</span></span>
  
> <span data-ttu-id="79003-125">[in] Masque de bits d’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="79003-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="79003-126">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="79003-126">The following flag can be set:</span></span>
    
<span data-ttu-id="79003-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="79003-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="79003-128">Le fournisseur est chargé dans le contexte d’un service Windows, un type spécial de processus sans accès à une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="79003-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="79003-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="79003-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="79003-130">[in] Numéro de version de l’interface de fournisseur de services (SPI) que MAPI utilise.</span><span class="sxs-lookup"><span data-stu-id="79003-130">[in] Version number of the service provider interface (SPI) that MAPI uses.</span></span> <span data-ttu-id="79003-131">Pour le numéro de version actuel, voir le fichier d’en-tête Mapispi.h.</span><span class="sxs-lookup"><span data-stu-id="79003-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="79003-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="79003-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="79003-133">[out] Pointeur vers le numéro de version du spi utilisé par ce fournisseur de magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="79003-133">[out] Pointer to the version number of the SPI that this message store provider uses.</span></span> 
    
 <span data-ttu-id="79003-134">_lppMSProvider_</span><span class="sxs-lookup"><span data-stu-id="79003-134">_lppMSProvider_</span></span>
  
> <span data-ttu-id="79003-135">[out] Pointeur vers un pointeur vers l’objet fournisseur de magasin de messages initialisé.</span><span class="sxs-lookup"><span data-stu-id="79003-135">[out] Pointer to a pointer to the initialized message store provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="79003-136">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="79003-136">Return value</span></span>

<span data-ttu-id="79003-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="79003-137">S_OK</span></span> 
  
> <span data-ttu-id="79003-138">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="79003-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="79003-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="79003-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="79003-140">La version SPI utilisée par MAPI n’est pas compatible avec la spi utilisée par ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="79003-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="79003-141">Remarques</span><span class="sxs-lookup"><span data-stu-id="79003-141">Remarks</span></span>

<span data-ttu-id="79003-142">MAPI appelle la fonction de point d’entrée **MSProviderInit** pour initialiser un fournisseur de magasins de messages à la suite d’une ouverture de compte client.</span><span class="sxs-lookup"><span data-stu-id="79003-142">MAPI calls the entry point function **MSProviderInit** to initialize a message store provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="79003-143">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="79003-143">Notes to implementers</span></span>

<span data-ttu-id="79003-144">Un fournisseur de magasins de messages doit implémenter **MSProviderInit** en tant que fonction de point d’entrée dans la DLL du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="79003-144">A message store provider must implement **MSProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="79003-145">L’implémentation doit être basée sur le prototype de fonction **MSPROVIDERINIT,** également spécifié dans MAPISPI.H.</span><span class="sxs-lookup"><span data-stu-id="79003-145">The implementation must be based on the **MSPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="79003-146">MAPI définit **MSPROVIDERINIT** pour utiliser le type d’appel d’initialisation MAPI standard, STDMAPIINITCALLTYPE, qui entraîne **MSProviderInit** à respecter la convention d’appel CDECL.</span><span class="sxs-lookup"><span data-stu-id="79003-146">MAPI defines **MSPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **MSProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="79003-147">Un avantage de CDECL est que les appels peuvent être tentés même si le nombre de paramètres d’appel ne correspond pas au nombre de paramètres définis.</span><span class="sxs-lookup"><span data-stu-id="79003-147">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="79003-148">Un fournisseur peut être initialisé plusieurs fois, suite à l’apparition de plusieurs profils dans une utilisation simultanée ou de l’apparition de plusieurs fois dans le même profil.</span><span class="sxs-lookup"><span data-stu-id="79003-148">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="79003-149">Étant donné que l’objet fournisseur contient du contexte, **MSProviderInit** doit retourner un autre objet fournisseur dans  _lppMSProvider_ pour chaque initialisation, même pour plusieurs initialisations dans le même processus.</span><span class="sxs-lookup"><span data-stu-id="79003-149">Because the provider object contains context, **MSProviderInit** must return a different provider object in  _lppMSProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="79003-150">La DLL du fournisseur ne doit pas être liée à Mapix.dll.</span><span class="sxs-lookup"><span data-stu-id="79003-150">The provider DLL should not be linked with Mapix.dll.</span></span> <span data-ttu-id="79003-151">Au lieu de cela, il doit utiliser ces pointeurs pour l’allocation ou la déallocation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="79003-151">Instead, it should use these pointers for memory allocation or deallocation.</span></span> 
  
<span data-ttu-id="79003-152">Le fournisseur de magasin de messages doit utiliser les fonctions pointées par  _lpAllocateBuffer,_  _lpAllocateMore_ et  _lpFreeBuffer_ pour la plupart des allocations et des déallocations de mémoire.</span><span class="sxs-lookup"><span data-stu-id="79003-152">The message store provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="79003-153">En particulier, le fournisseur doit utiliser ces fonctions pour allouer de la mémoire aux applications clientes lors de l’appel d’interfaces d’objets telles que [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="79003-153">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="79003-154">Si le fournisseur s’attend également à utiliser l’allocation de mémoire OLE, il doit appeler la méthode **IUnknown::AddRef** de l’objet allocateur pointé par le paramètre _lpMalloc._</span><span class="sxs-lookup"><span data-stu-id="79003-154">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="79003-155">Pour plus d’informations sur **l’écriture de MSProviderInit,** voir [Loading Message Store Providers](loading-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="79003-155">For more information about writing **MSProviderInit**, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span> <span data-ttu-id="79003-156">Pour plus d’informations sur les fonctions de point d’entrée, voir [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="79003-156">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="79003-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79003-157">See also</span></span>



[<span data-ttu-id="79003-158">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="79003-158">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="79003-159">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="79003-159">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)
  
[<span data-ttu-id="79003-160">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="79003-160">XPProviderInit</span></span>](xpproviderinit.md)

