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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: acec07df0b72685cf9ec6b21499c730b72f58c59
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328111"
---
# <a name="abproviderinit"></a><span data-ttu-id="842d6-103">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="842d6-103">ABProviderInit</span></span>
 
<span data-ttu-id="842d6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="842d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="842d6-105">Initialise un fournisseur de carnets d'adresses pour l'opération.</span><span class="sxs-lookup"><span data-stu-id="842d6-105">Initializes an address book provider for operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="842d6-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="842d6-106">Header file:</span></span>  <br/> |<span data-ttu-id="842d6-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="842d6-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="842d6-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="842d6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="842d6-109">Fournisseurs de carnets d'adresses</span><span class="sxs-lookup"><span data-stu-id="842d6-109">Address book providers</span></span>  <br/> |
|<span data-ttu-id="842d6-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="842d6-110">Called by:</span></span>  <br/> |<span data-ttu-id="842d6-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="842d6-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="842d6-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="842d6-112">Parameters</span></span>

 <span data-ttu-id="842d6-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="842d6-113">_hInstance_</span></span>
  
> <span data-ttu-id="842d6-114">dans Instance de la bibliothèque de liens dynamiques (DLL) du fournisseur de carnet d'adresses utilisée par MAPI lors de sa liaison.</span><span class="sxs-lookup"><span data-stu-id="842d6-114">[in] The instance of the address book provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="842d6-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="842d6-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="842d6-116">dans Pointeur vers un objet de l'allocation de mémoire qui expose \*\*\*\* l'interface OLE imalloc.</span><span class="sxs-lookup"><span data-stu-id="842d6-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="842d6-117">Il se peut que le fournisseur de carnets d'adresses doive utiliser cette méthode d'allocation lorsque vous travaillez avec certaines interfaces telles que **IStream**.</span><span class="sxs-lookup"><span data-stu-id="842d6-117">The address book provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="842d6-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="842d6-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="842d6-119">dans Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) à utiliser, le cas échéant par MAPI pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="842d6-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used where required by MAPI to allocate memory.</span></span> 
    
 <span data-ttu-id="842d6-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="842d6-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="842d6-121">dans Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) à utiliser, le cas échéant par MAPI pour allouer de la mémoire supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="842d6-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used where required by MAPI to allocate additional memory.</span></span> 
    
 <span data-ttu-id="842d6-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="842d6-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="842d6-123">dans Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) à utiliser, le cas échéant par MAPI pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="842d6-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used where required by MAPI to free memory.</span></span> 
    
 <span data-ttu-id="842d6-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="842d6-124">_ulFlags_</span></span>
  
> <span data-ttu-id="842d6-125">dans Masque de réindicateur des indicateurs.</span><span class="sxs-lookup"><span data-stu-id="842d6-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="842d6-126">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="842d6-126">The following flag can be set:</span></span>
    
<span data-ttu-id="842d6-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="842d6-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="842d6-128">Le fournisseur est en cours de chargement dans le contexte d'un service Windows, un type spécial de processus sans accès à une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="842d6-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="842d6-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="842d6-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="842d6-130">dans Numéro de version de l'interface du fournisseur de services (SPI) MAPI. DLL utilise.</span><span class="sxs-lookup"><span data-stu-id="842d6-130">[in] Version number of the service provider interface (SPI) that MAPI.DLL uses.</span></span> <span data-ttu-id="842d6-131">Pour le numéro de version actuel, consultez le MAPISPI. Fichier d'en-tête H.</span><span class="sxs-lookup"><span data-stu-id="842d6-131">For the current version number, see the MAPISPI.H header file.</span></span> 
    
 <span data-ttu-id="842d6-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="842d6-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="842d6-133">remarquer Pointeur vers le numéro de version du SPI que ce fournisseur de carnet d'adresses utilise.</span><span class="sxs-lookup"><span data-stu-id="842d6-133">[out] Pointer to the version number of the SPI that this address book provider uses.</span></span> 
    
 <span data-ttu-id="842d6-134">_lppABProvider_</span><span class="sxs-lookup"><span data-stu-id="842d6-134">_lppABProvider_</span></span>
  
> <span data-ttu-id="842d6-135">remarquer Pointeur vers un pointeur vers l'objet fournisseur de carnet d'adresses initialisé.</span><span class="sxs-lookup"><span data-stu-id="842d6-135">[out] Pointer to a pointer to the initialized address book provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="842d6-136">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="842d6-136">Return value</span></span>

<span data-ttu-id="842d6-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="842d6-137">S_OK</span></span> 
  
> <span data-ttu-id="842d6-138">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="842d6-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="842d6-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="842d6-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="842d6-140">La version SPI utilisée par MAPI n'est pas compatible avec le SPI utilisé par ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="842d6-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="842d6-141">Remarques</span><span class="sxs-lookup"><span data-stu-id="842d6-141">Remarks</span></span>

<span data-ttu-id="842d6-142">MAPI appelle la fonction de point d'entrée **ABProviderInit** pour initialiser un fournisseur de carnets d'adresses à la suite d'une ouverture de session client.</span><span class="sxs-lookup"><span data-stu-id="842d6-142">MAPI calls the entry point function **ABProviderInit** to initialize an address book provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="842d6-143">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="842d6-143">Notes to implementers</span></span>

<span data-ttu-id="842d6-144">Un fournisseur de carnets d'adresses doit implémenter **ABProviderInit** en tant que fonction de point d'entrée dans la dll du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="842d6-144">An address book provider must implement **ABProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="842d6-145">L'implémentation doit être basée sur le prototype de fonction **ABPROVIDERINIT** , également spécifié dans MAPISPI. H.</span><span class="sxs-lookup"><span data-stu-id="842d6-145">The implementation must be based on the **ABPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="842d6-146">MAPI définit **ABPROVIDERINIT** pour utiliser le type d'appel d'initialisation MAPI standard, STDMAPIINITCALLTYPE, qui force **ABPROVIDERINIT** à suivre la Convention d'appel CDECL.</span><span class="sxs-lookup"><span data-stu-id="842d6-146">MAPI defines **ABPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **ABProviderInit** to follow the CDECL calling convention.</span></span> 
  
<span data-ttu-id="842d6-147">Un fournisseur peut être initialisé plusieurs fois, en raison de son affichage simultané dans plusieurs profils, ou de plusieurs fois dans le même profil.</span><span class="sxs-lookup"><span data-stu-id="842d6-147">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="842d6-148">Étant donné que l'objet fournisseur contient le contexte, **ABProviderInit** doit renvoyer un objet fournisseur différent dans _lppABProvider_ pour chaque initialisation, même pour plusieurs initialisations dans le même processus.</span><span class="sxs-lookup"><span data-stu-id="842d6-148">Because the provider object contains context, **ABProviderInit** must return a different provider object in  _lppABProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="842d6-149">Le fournisseur de carnets d'adresses doit utiliser les fonctions pointées par _lpAllocateBuffer_, _lpAllocateMore_et _lpFreeBuffer_ pour la plupart de l'allocation et de la libération de mémoire.</span><span class="sxs-lookup"><span data-stu-id="842d6-149">The address book provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="842d6-150">En particulier, le fournisseur doit utiliser ces fonctions pour allouer de la mémoire à utiliser par les applications clientes lors de l'appel d'interfaces d'objets telles que [IMAPIProp:: GetProps](imapiprop-getprops.md) et [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="842d6-150">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="842d6-151">Si le fournisseur s'attend également à utiliser l'allocateur de mémoire OLE, il doit appeler la méthode **IUnknown:: AddRef** de l'objet allocater pointé par le paramètre _lpMalloc_ .</span><span class="sxs-lookup"><span data-stu-id="842d6-151">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="842d6-152">Pour plus d'informations sur l'écriture de **ABProviderInit**, consultez la rubrique [implémentation d'une fonction de point d'entrée de fournisseur de carnet d'adresses](implementing-an-address-book-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="842d6-152">For more information on writing **ABProviderInit**, see [Implementing an Address Book Provider Entry Point Function](implementing-an-address-book-provider-entry-point-function.md).</span></span> <span data-ttu-id="842d6-153">Pour plus d'informations sur les fonctions de point d'entrée, consultez [la rubrique implémentation d'une fonction de point d'entrée du fournisseur de services](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="842d6-153">For more information on entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="842d6-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="842d6-154">See also</span></span>

- [<span data-ttu-id="842d6-155">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="842d6-155">IABProvider : IUnknown</span></span>](iabprovideriunknown.md) 
- [<span data-ttu-id="842d6-156">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="842d6-156">MSProviderInit</span></span>](msproviderinit.md)
- [<span data-ttu-id="842d6-157">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="842d6-157">XPProviderInit</span></span>](xpproviderinit.md)

