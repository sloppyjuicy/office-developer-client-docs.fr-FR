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
# <a name="msproviderinit"></a><span data-ttu-id="08346-103">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="08346-103">MSProviderInit</span></span>

  
  
<span data-ttu-id="08346-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08346-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08346-105">Initialise un fournisseur de banque de messages pour l'opération.</span><span class="sxs-lookup"><span data-stu-id="08346-105">Initializes a message store provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="08346-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="08346-106">Header file:</span></span>  <br/> |<span data-ttu-id="08346-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="08346-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="08346-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="08346-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="08346-109">Fournisseurs de banques de messages</span><span class="sxs-lookup"><span data-stu-id="08346-109">Message store providers</span></span>  <br/> |
|<span data-ttu-id="08346-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="08346-110">Called by:</span></span>  <br/> |<span data-ttu-id="08346-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="08346-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="08346-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08346-112">Parameters</span></span>

 <span data-ttu-id="08346-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="08346-113">_hInstance_</span></span>
  
> <span data-ttu-id="08346-114">dans Instance de la bibliothèque de liens dynamiques (DLL) du fournisseur de banque de messages utilisée par MAPI lors de sa liaison.</span><span class="sxs-lookup"><span data-stu-id="08346-114">[in] The instance of the message store provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="08346-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="08346-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="08346-116">dans Pointeur vers un objet de l'allocation de mémoire qui expose \*\*\*\* l'interface OLE imalloc.</span><span class="sxs-lookup"><span data-stu-id="08346-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="08346-117">Il se peut que le fournisseur de banque de messages doive utiliser cette méthode d'allocation lorsque vous travaillez avec certaines interfaces telles que **IStream**.</span><span class="sxs-lookup"><span data-stu-id="08346-117">The message store provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="08346-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="08346-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="08346-119">dans Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="08346-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="08346-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="08346-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="08346-121">dans Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) à utiliser pour allouer de la mémoire supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="08346-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="08346-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="08346-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="08346-123">dans Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) à utiliser pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="08346-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="08346-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="08346-124">_ulFlags_</span></span>
  
> <span data-ttu-id="08346-125">dans Masque de réindicateur des indicateurs.</span><span class="sxs-lookup"><span data-stu-id="08346-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="08346-126">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="08346-126">The following flag can be set:</span></span>
    
<span data-ttu-id="08346-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="08346-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="08346-128">Le fournisseur est en cours de chargement dans le contexte d'un service Windows, un type spécial de processus sans accès à une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="08346-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="08346-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="08346-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="08346-130">dans Numéro de version de l'interface du fournisseur de services (SPI) utilisée par MAPI.</span><span class="sxs-lookup"><span data-stu-id="08346-130">[in] Version number of the service provider interface (SPI) that MAPI uses.</span></span> <span data-ttu-id="08346-131">Pour le numéro de version actuel, consultez le fichier d'en-tête Mapispi. h.</span><span class="sxs-lookup"><span data-stu-id="08346-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="08346-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="08346-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="08346-133">remarquer Pointeur vers le numéro de version du SPI que ce fournisseur de banque de messages utilise.</span><span class="sxs-lookup"><span data-stu-id="08346-133">[out] Pointer to the version number of the SPI that this message store provider uses.</span></span> 
    
 <span data-ttu-id="08346-134">_lppMSProvider_</span><span class="sxs-lookup"><span data-stu-id="08346-134">_lppMSProvider_</span></span>
  
> <span data-ttu-id="08346-135">remarquer Pointeur vers un pointeur vers l'objet fournisseur de banque de messages initialisée.</span><span class="sxs-lookup"><span data-stu-id="08346-135">[out] Pointer to a pointer to the initialized message store provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="08346-136">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="08346-136">Return value</span></span>

<span data-ttu-id="08346-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="08346-137">S_OK</span></span> 
  
> <span data-ttu-id="08346-138">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="08346-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="08346-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="08346-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="08346-140">La version SPI utilisée par MAPI n'est pas compatible avec le SPI utilisé par ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="08346-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="08346-141">Remarques</span><span class="sxs-lookup"><span data-stu-id="08346-141">Remarks</span></span>

<span data-ttu-id="08346-142">MAPI appelle la fonction de point d'entrée **MSProviderInit** pour initialiser un fournisseur de banque de messages à la suite d'une ouverture de session client.</span><span class="sxs-lookup"><span data-stu-id="08346-142">MAPI calls the entry point function **MSProviderInit** to initialize a message store provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="08346-143">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="08346-143">Notes to implementers</span></span>

<span data-ttu-id="08346-144">Un fournisseur de banque de messages doit implémenter **MSProviderInit** comme fonction de point d'entrée dans la dll du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="08346-144">A message store provider must implement **MSProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="08346-145">L'implémentation doit être basée sur le prototype de fonction **MSPROVIDERINIT** , également spécifié dans MAPISPI. H.</span><span class="sxs-lookup"><span data-stu-id="08346-145">The implementation must be based on the **MSPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="08346-146">MAPI définit **MSPROVIDERINIT** pour utiliser le type d'appel d'initialisation MAPI standard, STDMAPIINITCALLTYPE, qui force **MSPROVIDERINIT** à suivre la Convention d'appel CDECL.</span><span class="sxs-lookup"><span data-stu-id="08346-146">MAPI defines **MSPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **MSProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="08346-147">L'un des avantages de CDECL est que les appels peuvent être tentés même si le nombre de paramètres d'appel ne correspond pas au nombre de paramètres définis.</span><span class="sxs-lookup"><span data-stu-id="08346-147">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="08346-148">Un fournisseur peut être initialisé plusieurs fois, en raison de son affichage simultané dans plusieurs profils, ou de plusieurs fois dans le même profil.</span><span class="sxs-lookup"><span data-stu-id="08346-148">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="08346-149">Étant donné que l'objet fournisseur contient le contexte, **MSProviderInit** doit renvoyer un objet fournisseur différent dans _lppMSProvider_ pour chaque initialisation, même pour plusieurs initialisations dans le même processus.</span><span class="sxs-lookup"><span data-stu-id="08346-149">Because the provider object contains context, **MSProviderInit** must return a different provider object in  _lppMSProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="08346-150">La DLL du fournisseur ne doit pas être liée à mapix. dll.</span><span class="sxs-lookup"><span data-stu-id="08346-150">The provider DLL should not be linked with Mapix.dll.</span></span> <span data-ttu-id="08346-151">Au lieu de cela, il doit utiliser ces pointeurs pour l'allocation ou la désallocation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="08346-151">Instead, it should use these pointers for memory allocation or deallocation.</span></span> 
  
<span data-ttu-id="08346-152">Le fournisseur de banque de messages doit utiliser les fonctions pointées par _lpAllocateBuffer_, _lpAllocateMore_et _lpFreeBuffer_ pour la plupart de l'allocation et de la libération de mémoire.</span><span class="sxs-lookup"><span data-stu-id="08346-152">The message store provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="08346-153">En particulier, le fournisseur doit utiliser ces fonctions pour allouer de la mémoire à utiliser par les applications clientes lors de l'appel d'interfaces d'objets telles que [IMAPIProp:: GetProps](imapiprop-getprops.md) et [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="08346-153">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="08346-154">Si le fournisseur s'attend également à utiliser l'allocateur de mémoire OLE, il doit appeler la méthode **IUnknown:: AddRef** de l'objet allocater pointé par le paramètre _lpMalloc_ .</span><span class="sxs-lookup"><span data-stu-id="08346-154">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="08346-155">Pour plus d'informations sur l'écriture de **MSProviderInit**, voir [chargement des fournisseurs de banques de messages](loading-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="08346-155">For more information about writing **MSProviderInit**, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span> <span data-ttu-id="08346-156">Pour plus d'informations sur les fonctions de point d'entrée, consultez [la rubrique implémentation d'une fonction de point d'entrée du fournisseur de services](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="08346-156">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="08346-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08346-157">See also</span></span>



[<span data-ttu-id="08346-158">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="08346-158">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="08346-159">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="08346-159">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)
  
[<span data-ttu-id="08346-160">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="08346-160">XPProviderInit</span></span>](xpproviderinit.md)

