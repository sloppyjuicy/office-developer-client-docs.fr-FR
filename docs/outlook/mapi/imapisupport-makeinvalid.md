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
ms.openlocfilehash: 75771670f58f4cd65e15a02d08e6f78ab9d71755
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570736"
---
# <a name="imapisupportmakeinvalid"></a><span data-ttu-id="54145-103">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="54145-103">IMAPISupport::MakeInvalid</span></span>

  
  
<span data-ttu-id="54145-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54145-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54145-105">Marque un objet comme étant inutilisable.</span><span class="sxs-lookup"><span data-stu-id="54145-105">Marks an object as unusable.</span></span>
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a><span data-ttu-id="54145-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="54145-106">Parameters</span></span>

 <span data-ttu-id="54145-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="54145-107">_ulFlags_</span></span>
  
> <span data-ttu-id="54145-108">Réservé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="54145-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="54145-109">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="54145-109">_lpObject_</span></span>
  
> <span data-ttu-id="54145-110">[in] Pointeur vers l’objet est invalidé.</span><span class="sxs-lookup"><span data-stu-id="54145-110">[in] A pointer to the object to be invalidated.</span></span> <span data-ttu-id="54145-111">Interface de l’objet doit être dérivée de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="54145-111">The object's interface must be derived from **IUnknown**.</span></span>
    
 <span data-ttu-id="54145-112">_ulRefCount_</span><span class="sxs-lookup"><span data-stu-id="54145-112">_ulRefCount_</span></span>
  
> <span data-ttu-id="54145-113">[in] Décompte de références présente de l’objet.</span><span class="sxs-lookup"><span data-stu-id="54145-113">[in] The object's present reference count.</span></span>
    
 <span data-ttu-id="54145-114">_cMethods_</span><span class="sxs-lookup"><span data-stu-id="54145-114">_cMethods_</span></span>
  
> <span data-ttu-id="54145-115">[in] Le nombre des méthodes dans vtable de l’objet.</span><span class="sxs-lookup"><span data-stu-id="54145-115">[in] The count of methods in the object's vtable.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="54145-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="54145-116">Return value</span></span>

<span data-ttu-id="54145-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="54145-117">S_OK</span></span> 
  
> <span data-ttu-id="54145-118">L’objet a été marqué comme inutilisable.</span><span class="sxs-lookup"><span data-stu-id="54145-118">The object was successfully marked as unusable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="54145-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="54145-119">Remarks</span></span>

<span data-ttu-id="54145-120">La méthode **IMAPISupport::MakeInvalid** est implémentée pour tous les objets de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="54145-120">The **IMAPISupport::MakeInvalid** method is implemented for all support objects.</span></span> <span data-ttu-id="54145-121">L’objet est invalidé doit être dérivée à partir de l’interface **IUnknown** ou d’une interface dérivée de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="54145-121">The object to be invalidated must be derived from the **IUnknown** interface or from an interface derived from **IUnknown**.</span></span>
  
 <span data-ttu-id="54145-122">**MakeInvalid** marque un objet comme étant inutilisable en remplaçant vtable de l’objet par une vtable stub de taille similaire dans lequel les méthodes **IUnknown::AddRef** and **IUnknown::Release** fonctionnent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="54145-122">**MakeInvalid** marks an object as unusable by replacing the object's vtable with a stub vtable of similar size in which the **IUnknown::AddRef** and **IUnknown::Release** methods perform as expected.</span></span> <span data-ttu-id="54145-123">Toutefois, toutes les autres méthodes échouent, retourner la valeur MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="54145-123">However, any other methods fail, returning the value MAPI_E_INVALID_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="54145-124">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="54145-124">Notes to callers</span></span>

<span data-ttu-id="54145-125">Fournisseurs de services et les services de messagerie généralement appellent **MakeInvalid** au moment de l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="54145-125">Service providers and message services typically call **MakeInvalid** at shutdown time.</span></span> <span data-ttu-id="54145-126">Toutefois, **MakeInvalid** peut être appelée à tout moment.</span><span class="sxs-lookup"><span data-stu-id="54145-126">However, **MakeInvalid** can be called at any time.</span></span> <span data-ttu-id="54145-127">Par exemple, si un client libère un objet sans relâcher certains de ses sous-objets, vous pouvez appeler **MakeInvalid** immédiatement pour libérer les sous-objets.</span><span class="sxs-lookup"><span data-stu-id="54145-127">For example, if a client releases an object without releasing some of its subobjects, you can call **MakeInvalid** immediately to release those subobjects.</span></span> 
  
<span data-ttu-id="54145-128">Vous devez posséder l’objet que vous essayez d’invalider.</span><span class="sxs-lookup"><span data-stu-id="54145-128">You must own the object that you attempt to invalidate.</span></span> <span data-ttu-id="54145-129">Elle doit être d’au moins 16 octets et avoir au moins trois méthodes dans sa table vtable.</span><span class="sxs-lookup"><span data-stu-id="54145-129">It must be at least 16 bytes long and have at least three methods in its vtable.</span></span> 
  
<span data-ttu-id="54145-130">Vous pouvez appeler **MakeInvalid** et puis effectuer n’importe quel l’arrêt, par exemple en supprimant les structures de données associées, qui est généralement effectuée lors de la publication d’un objet.</span><span class="sxs-lookup"><span data-stu-id="54145-130">You can call **MakeInvalid** and then perform any shutdown work, such as discarding associated data structures, that is usually done during the release of an object.</span></span> <span data-ttu-id="54145-131">Code pour prendre en charge l’objet pas conserver en mémoire, car MAPI libère de la mémoire en appelant [MAPIFreeBuffer](mapifreebuffer.md) , puis libère l’objet.</span><span class="sxs-lookup"><span data-stu-id="54145-131">Code to support the object need not be kept in memory, because MAPI frees the memory by calling [MAPIFreeBuffer](mapifreebuffer.md) and then releases the object.</span></span> <span data-ttu-id="54145-132">Vous pourrez libérer les ressources, appelez **MakeInvalid**et puis ignorer l’objet non valide.</span><span class="sxs-lookup"><span data-stu-id="54145-132">You can release resources, call **MakeInvalid**, and then ignore the invalidated object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="54145-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54145-133">See also</span></span>



[<span data-ttu-id="54145-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="54145-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="54145-135">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="54145-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

