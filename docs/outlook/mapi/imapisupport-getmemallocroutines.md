---
title: IMAPISupportGetMemAllocRoutines
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetMemAllocRoutines
api_type:
- COM
ms.assetid: 52d45876-367b-42da-b99a-29cdb71fa5a9
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c3ec99e4e284ca2cdc4fba8fcf53a6c5741594cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577813"
---
# <a name="imapisupportgetmemallocroutines"></a><span data-ttu-id="03847-103">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="03847-103">IMAPISupport::GetMemAllocRoutines</span></span>

  
  
<span data-ttu-id="03847-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03847-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03847-105">Récupère les adresses des mémoire allocation et libération de fonctions MAPI ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)et [MAPIFreeBuffer](mapifreebuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="03847-105">Retrieves the addresses of the MAPI memory allocation and deallocation functions ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md)).</span></span>
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="03847-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03847-106">Parameters</span></span>

 <span data-ttu-id="03847-107">_lppAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="03847-107">_lppAllocateBuffer_</span></span>
  
> <span data-ttu-id="03847-108">[out] Pointeur vers un pointeur vers la fonction **MAPIAllocateBuffer** .</span><span class="sxs-lookup"><span data-stu-id="03847-108">[out] A pointer to a pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="03847-109">**MAPIAllocateBuffer** alloue de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="03847-109">**MAPIAllocateBuffer** allocates memory.</span></span> 
    
 <span data-ttu-id="03847-110">_lppAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="03847-110">_lppAllocateMore_</span></span>
  
> <span data-ttu-id="03847-111">[out] Pointeur vers un pointeur vers la fonction **MAPIAllocateMore** .</span><span class="sxs-lookup"><span data-stu-id="03847-111">[out] A pointer to a pointer to the **MAPIAllocateMore** function.</span></span> <span data-ttu-id="03847-112">**MAPIAllocateMore** alloue de la mémoire supplémentaire pour la mémoire qui était alloué à l’aide de **MAPIAllocateBuffer**.</span><span class="sxs-lookup"><span data-stu-id="03847-112">**MAPIAllocateMore** allocates additional memory for memory that was originally allocated by using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="03847-113">_lppFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="03847-113">_lppFreeBuffer_</span></span>
  
> <span data-ttu-id="03847-114">[out] Pointeur vers un pointeur vers la fonction **MAPIFreeBuffer** .</span><span class="sxs-lookup"><span data-stu-id="03847-114">[out] A pointer to a pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="03847-115">**MAPIFreeBuffer** libère de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="03847-115">**MAPIFreeBuffer** frees memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="03847-116">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="03847-116">Return value</span></span>

<span data-ttu-id="03847-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="03847-117">S_OK</span></span> 
  
> <span data-ttu-id="03847-118">Les fonction adresses ont été correctement renvoyées.</span><span class="sxs-lookup"><span data-stu-id="03847-118">The function addresses were successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="03847-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="03847-119">Remarks</span></span>

<span data-ttu-id="03847-120">La méthode **IMAPISupport::GetMemAllocRoutines** est implémentée pour tous les objets de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="03847-120">The **IMAPISupport::GetMemAllocRoutines** method is implemented for all support objects.</span></span> <span data-ttu-id="03847-121">Fournisseurs de services appellent **GetMemAllocRoutines** pour obtenir les adresses des fonctions d’allocation trois mémoire qui sont transmises à leur fonction d’initialisation ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md)ou [XPProviderInit](xpproviderinit.md)).</span><span class="sxs-lookup"><span data-stu-id="03847-121">Service providers call **GetMemAllocRoutines** to get the addresses of the three memory allocation functions that are passed to their initialization function ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md), or [XPProviderInit](xpproviderinit.md)).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="03847-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03847-122">See also</span></span>



[<span data-ttu-id="03847-123">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="03847-123">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="03847-124">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="03847-124">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="03847-125">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="03847-125">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="03847-126">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="03847-126">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

