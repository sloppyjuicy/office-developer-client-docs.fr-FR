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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e76ad936cb8dc99897bc1c74d3a47b0d2aa4be46
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590049"
---
# <a name="abproviderinit"></a><span data-ttu-id="6f93b-103">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="6f93b-103">ABProviderInit</span></span>
 
<span data-ttu-id="6f93b-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f93b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f93b-105">Initialise un fournisseur de carnet d’adresses pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="6f93b-105">Initializes an address book provider for operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6f93b-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="6f93b-106">Header file:</span></span>  <br/> |<span data-ttu-id="6f93b-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="6f93b-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="6f93b-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="6f93b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6f93b-109">Fournisseurs de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="6f93b-109">Address book providers</span></span>  <br/> |
|<span data-ttu-id="6f93b-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="6f93b-110">Called by:</span></span>  <br/> |<span data-ttu-id="6f93b-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="6f93b-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="6f93b-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f93b-112">Parameters</span></span>

 <span data-ttu-id="6f93b-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="6f93b-113">_hInstance_</span></span>
  
> <span data-ttu-id="6f93b-114">[in] Instance de la bibliothèque de liens dynamiques du fournisseur de carnet d’adresses (DLL) qui MAPI utilisé lorsqu’elle est liée.</span><span class="sxs-lookup"><span data-stu-id="6f93b-114">[in] The instance of the address book provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="6f93b-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="6f93b-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="6f93b-116">[in] Pointeur vers un objet d’allocation mémoire exposant l’interface OLE **IMalloc** .</span><span class="sxs-lookup"><span data-stu-id="6f93b-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="6f93b-117">Vous devrez utiliser cette méthode de répartition lorsque vous travaillez avec certaines interfaces comme **IStream**le fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="6f93b-117">The address book provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="6f93b-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="6f93b-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="6f93b-119">[in] Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) , à utiliser lorsque MAPI pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="6f93b-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used where required by MAPI to allocate memory.</span></span> 
    
 <span data-ttu-id="6f93b-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="6f93b-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="6f93b-121">[in] Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) , à utiliser lorsque MAPI pour allouer plus de mémoire.</span><span class="sxs-lookup"><span data-stu-id="6f93b-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used where required by MAPI to allocate additional memory.</span></span> 
    
 <span data-ttu-id="6f93b-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="6f93b-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="6f93b-123">[in] Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) , à utiliser lorsque MAPI pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="6f93b-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used where required by MAPI to free memory.</span></span> 
    
 <span data-ttu-id="6f93b-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6f93b-124">_ulFlags_</span></span>
  
> <span data-ttu-id="6f93b-125">[in] Masque de bits d’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="6f93b-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="6f93b-126">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="6f93b-126">The following flag can be set:</span></span>
    
<span data-ttu-id="6f93b-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="6f93b-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="6f93b-128">Le fournisseur est chargé dans le contexte d’un service Windows, un type particulier de processus sans accès à une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6f93b-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="6f93b-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="6f93b-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="6f93b-130">[in] Numéro de version de l’interface de fournisseur de service (SPI) que MAPI. DLL utilise.</span><span class="sxs-lookup"><span data-stu-id="6f93b-130">[in] Version number of the service provider interface (SPI) that MAPI.DLL uses.</span></span> <span data-ttu-id="6f93b-131">Pour le numéro de version actuelle, consultez le MAPISPI. Fichier d’en-tête H.</span><span class="sxs-lookup"><span data-stu-id="6f93b-131">For the current version number, see the MAPISPI.H header file.</span></span> 
    
 <span data-ttu-id="6f93b-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="6f93b-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="6f93b-133">[out] Pointeur vers le numéro de version de l’index SPI qui utilise ce fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="6f93b-133">[out] Pointer to the version number of the SPI that this address book provider uses.</span></span> 
    
 <span data-ttu-id="6f93b-134">_lppABProvider_</span><span class="sxs-lookup"><span data-stu-id="6f93b-134">_lppABProvider_</span></span>
  
> <span data-ttu-id="6f93b-135">[out] Pointeur vers un pointeur vers l’objet de fournisseur de carnet d’adresses initialisé.</span><span class="sxs-lookup"><span data-stu-id="6f93b-135">[out] Pointer to a pointer to the initialized address book provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6f93b-136">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="6f93b-136">Return value</span></span>

<span data-ttu-id="6f93b-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="6f93b-137">S_OK</span></span> 
  
> <span data-ttu-id="6f93b-138">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="6f93b-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="6f93b-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="6f93b-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="6f93b-140">La version SPI utilisée par MAPI n’est pas compatible avec le SPI utilisé par ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="6f93b-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6f93b-141">Remarques</span><span class="sxs-lookup"><span data-stu-id="6f93b-141">Remarks</span></span>

<span data-ttu-id="6f93b-142">MAPI appelle la fonction de point d’entrée **ABProviderInit** d’initialisation d’un fournisseur de carnet d’adresses après une ouverture de session client.</span><span class="sxs-lookup"><span data-stu-id="6f93b-142">MAPI calls the entry point function **ABProviderInit** to initialize an address book provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6f93b-143">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="6f93b-143">Notes to implementers</span></span>

<span data-ttu-id="6f93b-144">Un fournisseur de carnet d’adresses doit implémenter **ABProviderInit** en tant que fonction d’un point d’entrée dans la DLL du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="6f93b-144">An address book provider must implement **ABProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="6f93b-145">L’implémentation doit être basée sur le prototype de fonction **ABPROVIDERINIT** , également spécifié dans MAPISPI. H.</span><span class="sxs-lookup"><span data-stu-id="6f93b-145">The implementation must be based on the **ABPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="6f93b-146">MAPI définit **ABPROVIDERINIT** pour utiliser le type appel de l’initialisation de MAPI standard, STDMAPIINITCALLTYPE, ce qui entraîne **ABProviderInit** à suivre la convention d’appel CDECL.</span><span class="sxs-lookup"><span data-stu-id="6f93b-146">MAPI defines **ABPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **ABProviderInit** to follow the CDECL calling convention.</span></span> 
  
<span data-ttu-id="6f93b-147">Un fournisseur peut être initialisé plusieurs fois, à la suite d’apparaître dans plusieurs profils simultanées ou d’apparaître plusieurs fois dans le même profil.</span><span class="sxs-lookup"><span data-stu-id="6f93b-147">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="6f93b-148">Étant donné que l’objet fournisseur contient contexte, **ABProviderInit** doit retourner un objet de fournisseur différent dans _lppABProvider_ pour chaque d’initialisation, même pour plusieurs initialisations dans le même processus.</span><span class="sxs-lookup"><span data-stu-id="6f93b-148">Because the provider object contains context, **ABProviderInit** must return a different provider object in  _lppABProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="6f93b-149">Le fournisseur de carnet d’adresses doit utiliser les fonctions désignées par _lpAllocateBuffer_, _lpAllocateMore_et _lpFreeBuffer_ pour la plupart des allocation de mémoire et libération.</span><span class="sxs-lookup"><span data-stu-id="6f93b-149">The address book provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="6f93b-150">En particulier, le fournisseur doit utiliser ces fonctions pour allouer de la mémoire pour une utilisation par les applications clientes lors de l’appel des interfaces de l’objet tels que [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="6f93b-150">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="6f93b-151">Si le fournisseur attend également utiliser l’allocation de mémoire OLE, il doit appeler la méthode **IUnknown::AddRef** de l’objet d’allocation désigné par le paramètre _lpMalloc_ .</span><span class="sxs-lookup"><span data-stu-id="6f93b-151">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="6f93b-152">Pour plus d’informations sur l’écriture de **ABProviderInit**, voir [implémentation de fonction un Point d’entrée adresse carnet de fournisseur](implementing-an-address-book-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="6f93b-152">For more information on writing **ABProviderInit**, see [Implementing an Address Book Provider Entry Point Function](implementing-an-address-book-provider-entry-point-function.md).</span></span> <span data-ttu-id="6f93b-153">Pour plus d’informations sur les fonctions de point d’entrée, voir [implémentation d’une fonction de Point de Service fournisseur de l’entrée](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="6f93b-153">For more information on entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6f93b-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f93b-154">See also</span></span>

- [<span data-ttu-id="6f93b-155">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6f93b-155">IABProvider : IUnknown</span></span>](iabprovideriunknown.md) 
- [<span data-ttu-id="6f93b-156">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="6f93b-156">MSProviderInit</span></span>](msproviderinit.md)
- [<span data-ttu-id="6f93b-157">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="6f93b-157">XPProviderInit</span></span>](xpproviderinit.md)

