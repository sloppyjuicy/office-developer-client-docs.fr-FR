---
title: ABProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ABProviderInit
api_type:
- HeaderDef
ms.assetid: c3dcd0d4-018a-47b0-b040-227034ed59d8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: acec07df0b72685cf9ec6b21499c730b72f58c59
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428283"
---
# <a name="abproviderinit"></a><span data-ttu-id="f270c-103">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="f270c-103">ABProviderInit</span></span>
 
<span data-ttu-id="f270c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f270c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f270c-105">Initialise un fournisseur de carnet d’adresses pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="f270c-105">Initializes an address book provider for operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f270c-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="f270c-106">Header file:</span></span>  <br/> |<span data-ttu-id="f270c-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="f270c-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="f270c-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="f270c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f270c-109">Fournisseurs de carnets d’adresses</span><span class="sxs-lookup"><span data-stu-id="f270c-109">Address book providers</span></span>  <br/> |
|<span data-ttu-id="f270c-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="f270c-110">Called by:</span></span>  <br/> |<span data-ttu-id="f270c-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="f270c-111">MAPI</span></span>  <br/> |
   
```cpp
HRESULT ABProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPABPROVIDER FAR * lppABProvider
);
```

## <a name="parameters"></a><span data-ttu-id="f270c-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="f270c-112">Parameters</span></span>

 <span data-ttu-id="f270c-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="f270c-113">_hInstance_</span></span>
  
> <span data-ttu-id="f270c-114">[in] Instance de la bibliothèque de liens dynamiques (DLL) du fournisseur de carnet d’adresses que MAPI a utilisée lors de sa liaison.</span><span class="sxs-lookup"><span data-stu-id="f270c-114">[in] The instance of the address book provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="f270c-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="f270c-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="f270c-116">[in] Pointeur vers un objet d’allocation de mémoire exposant l’interface OLE **IMalloc.**</span><span class="sxs-lookup"><span data-stu-id="f270c-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="f270c-117">Le fournisseur de carnet d’adresses peut avoir besoin d’utiliser cette méthode d’allocation lors de l’utilisation de certaines interfaces telles que **IStream**.</span><span class="sxs-lookup"><span data-stu-id="f270c-117">The address book provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="f270c-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="f270c-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="f270c-119">[in] Pointeur vers la [fonction MAPIAllocateBuffer,](mapiallocatebuffer.md) à utiliser lorsque MAPI l’exige pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="f270c-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used where required by MAPI to allocate memory.</span></span> 
    
 <span data-ttu-id="f270c-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="f270c-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="f270c-121">[in] Pointeur vers la [fonction MAPIAllocateMore,](mapiallocatemore.md) à utiliser lorsque MAPI l’exige pour allouer de la mémoire supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="f270c-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used where required by MAPI to allocate additional memory.</span></span> 
    
 <span data-ttu-id="f270c-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="f270c-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="f270c-123">[in] Pointeur vers la [fonction MAPIFreeBuffer,](mapifreebuffer.md) à utiliser lorsque MAPI l’exige pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="f270c-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used where required by MAPI to free memory.</span></span> 
    
 <span data-ttu-id="f270c-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f270c-124">_ulFlags_</span></span>
  
> <span data-ttu-id="f270c-125">[in] Masque de bits d’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="f270c-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="f270c-126">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="f270c-126">The following flag can be set:</span></span>
    
<span data-ttu-id="f270c-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="f270c-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="f270c-128">Le fournisseur est chargé dans le contexte d’un service Windows, un type spécial de processus sans accès à une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f270c-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="f270c-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="f270c-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="f270c-130">[in] Numéro de version de l’interface du fournisseur de services (SPI) que MAPI.DLL utilise.</span><span class="sxs-lookup"><span data-stu-id="f270c-130">[in] Version number of the service provider interface (SPI) that MAPI.DLL uses.</span></span> <span data-ttu-id="f270c-131">Pour le numéro de version actuel, voir MAPISPI. Fichier d’en-tête H.</span><span class="sxs-lookup"><span data-stu-id="f270c-131">For the current version number, see the MAPISPI.H header file.</span></span> 
    
 <span data-ttu-id="f270c-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="f270c-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="f270c-133">[out] Pointeur vers le numéro de version du spi utilisé par ce fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="f270c-133">[out] Pointer to the version number of the SPI that this address book provider uses.</span></span> 
    
 <span data-ttu-id="f270c-134">_lppABProvider_</span><span class="sxs-lookup"><span data-stu-id="f270c-134">_lppABProvider_</span></span>
  
> <span data-ttu-id="f270c-135">[out] Pointeur vers un pointeur vers l’objet fournisseur de carnet d’adresses initialisé.</span><span class="sxs-lookup"><span data-stu-id="f270c-135">[out] Pointer to a pointer to the initialized address book provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f270c-136">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f270c-136">Return value</span></span>

<span data-ttu-id="f270c-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="f270c-137">S_OK</span></span> 
  
> <span data-ttu-id="f270c-138">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="f270c-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="f270c-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="f270c-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="f270c-140">La version SPI utilisée par MAPI n’est pas compatible avec la spi utilisée par ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f270c-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f270c-141">Remarques</span><span class="sxs-lookup"><span data-stu-id="f270c-141">Remarks</span></span>

<span data-ttu-id="f270c-142">MAPI appelle la fonction de point d’entrée **ABProviderInit** pour initialiser un fournisseur de carnet d’adresses à la suite d’une inscription client.</span><span class="sxs-lookup"><span data-stu-id="f270c-142">MAPI calls the entry point function **ABProviderInit** to initialize an address book provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f270c-143">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="f270c-143">Notes to implementers</span></span>

<span data-ttu-id="f270c-144">Un fournisseur de carnet d’adresses doit implémenter **ABProviderInit** en tant que fonction de point d’entrée dans la DLL du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f270c-144">An address book provider must implement **ABProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="f270c-145">L’implémentation doit être basée sur le prototype de fonction **ABPROVIDERINIT,** également spécifié dans MAPISPI.H.</span><span class="sxs-lookup"><span data-stu-id="f270c-145">The implementation must be based on the **ABPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="f270c-146">MAPI définit **ABPROVIDERINIT** pour utiliser le type d’appel d’initialisation MAPI standard, STDMAPIINITCALLTYPE, ce qui entraîne **ABProviderInit** à respecter la convention d’appel CDECL.</span><span class="sxs-lookup"><span data-stu-id="f270c-146">MAPI defines **ABPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **ABProviderInit** to follow the CDECL calling convention.</span></span> 
  
<span data-ttu-id="f270c-147">Un fournisseur peut être initialisé plusieurs fois, suite à l’apparition de plusieurs profils dans une utilisation simultanée ou de l’apparition de plusieurs fois dans le même profil.</span><span class="sxs-lookup"><span data-stu-id="f270c-147">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="f270c-148">Étant donné que l’objet fournisseur contient du contexte, **ABProviderInit** doit retourner un autre objet fournisseur dans  _lppABProvider_ pour chaque initialisation, même pour plusieurs initialisations dans le même processus.</span><span class="sxs-lookup"><span data-stu-id="f270c-148">Because the provider object contains context, **ABProviderInit** must return a different provider object in  _lppABProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="f270c-149">Le fournisseur de carnet d’adresses doit utiliser les fonctions pointées par  _lpAllocateBuffer,_  _lpAllocateMore_ et  _lpFreeBuffer_ pour la plupart des allocations de mémoire et de la déallocation.</span><span class="sxs-lookup"><span data-stu-id="f270c-149">The address book provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="f270c-150">En particulier, le fournisseur doit utiliser ces fonctions pour allouer de la mémoire pour une utilisation par les applications clientes lors de l’appel d’interfaces d’objet telles que [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="f270c-150">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="f270c-151">Si le fournisseur s’attend également à utiliser l’allocation de mémoire OLE, il doit appeler la méthode **IUnknown::AddRef** de l’objet d’allocation pointé par le paramètre _lpMalloc._</span><span class="sxs-lookup"><span data-stu-id="f270c-151">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="f270c-152">Pour plus d’informations sur l’écriture **d’ABProviderInit,** voir [Implementing an Address Book Provider Entry Point Function](implementing-an-address-book-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="f270c-152">For more information on writing **ABProviderInit**, see [Implementing an Address Book Provider Entry Point Function](implementing-an-address-book-provider-entry-point-function.md).</span></span> <span data-ttu-id="f270c-153">Pour plus d’informations sur les fonctions de point d’entrée, voir [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="f270c-153">For more information on entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f270c-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f270c-154">See also</span></span>

- [<span data-ttu-id="f270c-155">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f270c-155">IABProvider : IUnknown</span></span>](iabprovideriunknown.md) 
- [<span data-ttu-id="f270c-156">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="f270c-156">MSProviderInit</span></span>](msproviderinit.md)
- [<span data-ttu-id="f270c-157">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="f270c-157">XPProviderInit</span></span>](xpproviderinit.md)

