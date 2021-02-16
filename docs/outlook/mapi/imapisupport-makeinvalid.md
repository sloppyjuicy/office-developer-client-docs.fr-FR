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
# <a name="imapisupportmakeinvalid"></a><span data-ttu-id="65cc8-103">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="65cc8-103">IMAPISupport::MakeInvalid</span></span>

  
  
<span data-ttu-id="65cc8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65cc8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65cc8-105">Marque un objet comme inutilisable.</span><span class="sxs-lookup"><span data-stu-id="65cc8-105">Marks an object as unusable.</span></span>
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a><span data-ttu-id="65cc8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65cc8-106">Parameters</span></span>

 <span data-ttu-id="65cc8-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="65cc8-107">_ulFlags_</span></span>
  
> <span data-ttu-id="65cc8-108">Réservé ; doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="65cc8-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="65cc8-109">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="65cc8-109">_lpObject_</span></span>
  
> <span data-ttu-id="65cc8-110">[in] Pointeur vers l’objet à invalider.</span><span class="sxs-lookup"><span data-stu-id="65cc8-110">[in] A pointer to the object to be invalidated.</span></span> <span data-ttu-id="65cc8-111">L’interface de l’objet doit être dérivée **d’IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="65cc8-111">The object's interface must be derived from **IUnknown**.</span></span>
    
 <span data-ttu-id="65cc8-112">_ulRefCount_</span><span class="sxs-lookup"><span data-stu-id="65cc8-112">_ulRefCount_</span></span>
  
> <span data-ttu-id="65cc8-113">[in] Nombre de références présentes de l’objet.</span><span class="sxs-lookup"><span data-stu-id="65cc8-113">[in] The object's present reference count.</span></span>
    
 <span data-ttu-id="65cc8-114">_cMethods_</span><span class="sxs-lookup"><span data-stu-id="65cc8-114">_cMethods_</span></span>
  
> <span data-ttu-id="65cc8-115">[in] Nombre de méthodes dans la table vtable de l’objet.</span><span class="sxs-lookup"><span data-stu-id="65cc8-115">[in] The count of methods in the object's vtable.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="65cc8-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="65cc8-116">Return value</span></span>

<span data-ttu-id="65cc8-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="65cc8-117">S_OK</span></span> 
  
> <span data-ttu-id="65cc8-118">L’objet a été marqué comme inutilisable.</span><span class="sxs-lookup"><span data-stu-id="65cc8-118">The object was successfully marked as unusable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="65cc8-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="65cc8-119">Remarks</span></span>

<span data-ttu-id="65cc8-120">La **méthode IMAPISupport::MakeInvalid** est implémentée pour tous les objets de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="65cc8-120">The **IMAPISupport::MakeInvalid** method is implemented for all support objects.</span></span> <span data-ttu-id="65cc8-121">L’objet à invalider doit être dérivé de l’interface **IUnknown** ou d’une interface dérivée de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="65cc8-121">The object to be invalidated must be derived from the **IUnknown** interface or from an interface derived from **IUnknown**.</span></span>
  
 <span data-ttu-id="65cc8-122">**MakeInvalid** marque un objet comme inutilisable en remplaçant le vtable de l’objet par un vtable stub de taille similaire dans lequel les méthodes **IUnknown::AddRef** **et IUnknown::Release** s’exécutent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="65cc8-122">**MakeInvalid** marks an object as unusable by replacing the object's vtable with a stub vtable of similar size in which the **IUnknown::AddRef** and **IUnknown::Release** methods perform as expected.</span></span> <span data-ttu-id="65cc8-123">Toutefois, toutes les autres méthodes échouent, renvoyant la valeur MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="65cc8-123">However, any other methods fail, returning the value MAPI_E_INVALID_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="65cc8-124">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="65cc8-124">Notes to callers</span></span>

<span data-ttu-id="65cc8-125">Les fournisseurs de services et les services de messagerie **appellent généralement MakeInvalid** au moment de l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="65cc8-125">Service providers and message services typically call **MakeInvalid** at shutdown time.</span></span> <span data-ttu-id="65cc8-126">Toutefois, **MakeInvalid** peut être appelé à tout moment.</span><span class="sxs-lookup"><span data-stu-id="65cc8-126">However, **MakeInvalid** can be called at any time.</span></span> <span data-ttu-id="65cc8-127">Par exemple, si un client libère un objet sans libérer certains de ses sous-objets, vous pouvez appeler **MakeInvalid** immédiatement pour libérer ces sous-objets.</span><span class="sxs-lookup"><span data-stu-id="65cc8-127">For example, if a client releases an object without releasing some of its subobjects, you can call **MakeInvalid** immediately to release those subobjects.</span></span> 
  
<span data-ttu-id="65cc8-128">Vous devez posséder l’objet que vous tentez d’invalider.</span><span class="sxs-lookup"><span data-stu-id="65cc8-128">You must own the object that you attempt to invalidate.</span></span> <span data-ttu-id="65cc8-129">Elle doit avoir une longueur d’au moins 16 octets et avoir au moins trois méthodes dans sa table vtable.</span><span class="sxs-lookup"><span data-stu-id="65cc8-129">It must be at least 16 bytes long and have at least three methods in its vtable.</span></span> 
  
<span data-ttu-id="65cc8-130">Vous pouvez appeler **MakeInvalid,** puis effectuer n’importe quel travail d’arrêt, par exemple ignorer les structures de données associées, généralement effectué lors de la libération d’un objet.</span><span class="sxs-lookup"><span data-stu-id="65cc8-130">You can call **MakeInvalid** and then perform any shutdown work, such as discarding associated data structures, that is usually done during the release of an object.</span></span> <span data-ttu-id="65cc8-131">Le code de prise en charge de l’objet n’a pas besoin d’être conservé en mémoire, car MAPI libère la mémoire en appelant [MAPIFreeBuffer,](mapifreebuffer.md) puis libère l’objet.</span><span class="sxs-lookup"><span data-stu-id="65cc8-131">Code to support the object need not be kept in memory, because MAPI frees the memory by calling [MAPIFreeBuffer](mapifreebuffer.md) and then releases the object.</span></span> <span data-ttu-id="65cc8-132">Vous pouvez libérer des ressources, **appeler MakeInvalid,** puis ignorer l’objet invalidé.</span><span class="sxs-lookup"><span data-stu-id="65cc8-132">You can release resources, call **MakeInvalid**, and then ignore the invalidated object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="65cc8-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65cc8-133">See also</span></span>



[<span data-ttu-id="65cc8-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="65cc8-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="65cc8-135">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="65cc8-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

