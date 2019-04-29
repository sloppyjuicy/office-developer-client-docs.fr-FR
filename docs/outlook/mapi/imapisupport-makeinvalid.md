---
title: IMAPISupportMakeInvalid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.MakeInvalid
api_type:
- COM
ms.assetid: c630ecaf-b19c-4991-9779-e13cc492c755
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 84e87f8a8d3c419afc4b86e200aeaba57e6a85f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427492"
---
# <a name="imapisupportmakeinvalid"></a><span data-ttu-id="432e9-103">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="432e9-103">IMAPISupport::MakeInvalid</span></span>

  
  
<span data-ttu-id="432e9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="432e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="432e9-105">Marque un objet comme inutilisable.</span><span class="sxs-lookup"><span data-stu-id="432e9-105">Marks an object as unusable.</span></span>
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a><span data-ttu-id="432e9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="432e9-106">Parameters</span></span>

 <span data-ttu-id="432e9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="432e9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="432e9-108">MSR doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="432e9-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="432e9-109">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="432e9-109">_lpObject_</span></span>
  
> <span data-ttu-id="432e9-110">dans Pointeur vers l'objet à invalider.</span><span class="sxs-lookup"><span data-stu-id="432e9-110">[in] A pointer to the object to be invalidated.</span></span> <span data-ttu-id="432e9-111">L'interface de l'objet doit être dérivée de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="432e9-111">The object's interface must be derived from **IUnknown**.</span></span>
    
 <span data-ttu-id="432e9-112">_ulRefCount_</span><span class="sxs-lookup"><span data-stu-id="432e9-112">_ulRefCount_</span></span>
  
> <span data-ttu-id="432e9-113">dans Le compte de référence actuel de l'objet.</span><span class="sxs-lookup"><span data-stu-id="432e9-113">[in] The object's present reference count.</span></span>
    
 <span data-ttu-id="432e9-114">_cMethods_</span><span class="sxs-lookup"><span data-stu-id="432e9-114">_cMethods_</span></span>
  
> <span data-ttu-id="432e9-115">dans Nombre de méthodes dans la vtable de l'objet.</span><span class="sxs-lookup"><span data-stu-id="432e9-115">[in] The count of methods in the object's vtable.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="432e9-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="432e9-116">Return value</span></span>

<span data-ttu-id="432e9-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="432e9-117">S_OK</span></span> 
  
> <span data-ttu-id="432e9-118">L'objet a été marqué comme étant inutilisable.</span><span class="sxs-lookup"><span data-stu-id="432e9-118">The object was successfully marked as unusable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="432e9-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="432e9-119">Remarks</span></span>

<span data-ttu-id="432e9-120">La méthode **IMAPISupport:: MakeInvalid** est implémentée pour tous les objets de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="432e9-120">The **IMAPISupport::MakeInvalid** method is implemented for all support objects.</span></span> <span data-ttu-id="432e9-121">L'objet à invalider doit être dérivé de l'interface **IUnknown** ou d'une interface dérivée de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="432e9-121">The object to be invalidated must be derived from the **IUnknown** interface or from an interface derived from **IUnknown**.</span></span>
  
 <span data-ttu-id="432e9-122">**MakeInvalid** marque un objet comme inutilisable en remplaçant le vtable de l'objet par un vtable de taille similaire dans lequel les méthodes **IUnknown:: AddRef** et **IUnknown:: Release** fonctionnent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="432e9-122">**MakeInvalid** marks an object as unusable by replacing the object's vtable with a stub vtable of similar size in which the **IUnknown::AddRef** and **IUnknown::Release** methods perform as expected.</span></span> <span data-ttu-id="432e9-123">Toutefois, toutes les autres méthodes échouent, renvoyant la valeur MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="432e9-123">However, any other methods fail, returning the value MAPI_E_INVALID_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="432e9-124">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="432e9-124">Notes to callers</span></span>

<span data-ttu-id="432e9-125">Les fournisseurs de services et les services de messagerie appellent généralement **MakeInvalid** au moment de l'arrêt.</span><span class="sxs-lookup"><span data-stu-id="432e9-125">Service providers and message services typically call **MakeInvalid** at shutdown time.</span></span> <span data-ttu-id="432e9-126">Toutefois, **MakeInvalid** peut être appelé à tout moment.</span><span class="sxs-lookup"><span data-stu-id="432e9-126">However, **MakeInvalid** can be called at any time.</span></span> <span data-ttu-id="432e9-127">Par exemple, si un client libère un objet sans libérer certains de ses sous-objets, vous pouvez appeler **MakeInvalid** immédiatement pour libérer ces sous-objets.</span><span class="sxs-lookup"><span data-stu-id="432e9-127">For example, if a client releases an object without releasing some of its subobjects, you can call **MakeInvalid** immediately to release those subobjects.</span></span> 
  
<span data-ttu-id="432e9-128">Vous devez être propriétaire de l'objet que vous essayez d'invalider.</span><span class="sxs-lookup"><span data-stu-id="432e9-128">You must own the object that you attempt to invalidate.</span></span> <span data-ttu-id="432e9-129">Elle doit être d'au moins 16 octets et avoir au moins trois méthodes dans sa vtable.</span><span class="sxs-lookup"><span data-stu-id="432e9-129">It must be at least 16 bytes long and have at least three methods in its vtable.</span></span> 
  
<span data-ttu-id="432e9-130">Vous pouvez appeler **MakeInvalid** , puis effectuer les opérations d'arrêt, telles que le rejet des structures de données associées, qui sont généralement effectuées lors de la publication d'un objet.</span><span class="sxs-lookup"><span data-stu-id="432e9-130">You can call **MakeInvalid** and then perform any shutdown work, such as discarding associated data structures, that is usually done during the release of an object.</span></span> <span data-ttu-id="432e9-131">Le code permettant de prendre en charge l'objet ne doit pas nécessairement être conservé en mémoire, car MAPI libère la mémoire en appelant [MAPIFreeBuffer](mapifreebuffer.md) , puis libère l'objet.</span><span class="sxs-lookup"><span data-stu-id="432e9-131">Code to support the object need not be kept in memory, because MAPI frees the memory by calling [MAPIFreeBuffer](mapifreebuffer.md) and then releases the object.</span></span> <span data-ttu-id="432e9-132">Vous pouvez publier des ressources, appeler **MakeInvalid**, puis ignorer l'objet invalidé.</span><span class="sxs-lookup"><span data-stu-id="432e9-132">You can release resources, call **MakeInvalid**, and then ignore the invalidated object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="432e9-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="432e9-133">See also</span></span>



[<span data-ttu-id="432e9-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="432e9-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="432e9-135">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="432e9-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

