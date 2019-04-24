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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 680fd16771b62d705808a04d768115a076e54750
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316558"
---
# <a name="imapisupportgetmemallocroutines"></a><span data-ttu-id="58021-103">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="58021-103">IMAPISupport::GetMemAllocRoutines</span></span>

  
  
<span data-ttu-id="58021-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58021-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58021-105">Récupère les adresses des fonctions d'allocation et de désallocation de mémoire MAPI ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)et [MAPIFreeBuffer](mapifreebuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="58021-105">Retrieves the addresses of the MAPI memory allocation and deallocation functions ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md)).</span></span>
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="58021-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58021-106">Parameters</span></span>

 <span data-ttu-id="58021-107">_lppAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="58021-107">_lppAllocateBuffer_</span></span>
  
> <span data-ttu-id="58021-108">remarquer Pointeur vers un pointeur vers la fonction **MAPIAllocateBuffer** .</span><span class="sxs-lookup"><span data-stu-id="58021-108">[out] A pointer to a pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="58021-109">**MAPIAllocateBuffer** alloue de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="58021-109">**MAPIAllocateBuffer** allocates memory.</span></span> 
    
 <span data-ttu-id="58021-110">_lppAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="58021-110">_lppAllocateMore_</span></span>
  
> <span data-ttu-id="58021-111">remarquer Pointeur vers un pointeur vers la fonction **MAPIAllocateMore** .</span><span class="sxs-lookup"><span data-stu-id="58021-111">[out] A pointer to a pointer to the **MAPIAllocateMore** function.</span></span> <span data-ttu-id="58021-112">**MAPIAllocateMore** alloue de la mémoire supplémentaire pour la mémoire qui a été initialement allouée à l'aide de **MAPIAllocateBuffer**.</span><span class="sxs-lookup"><span data-stu-id="58021-112">**MAPIAllocateMore** allocates additional memory for memory that was originally allocated by using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="58021-113">_lppFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="58021-113">_lppFreeBuffer_</span></span>
  
> <span data-ttu-id="58021-114">remarquer Pointeur vers un pointeur vers la fonction **MAPIFreeBuffer** .</span><span class="sxs-lookup"><span data-stu-id="58021-114">[out] A pointer to a pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="58021-115">**MAPIFreeBuffer** libère de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="58021-115">**MAPIFreeBuffer** frees memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="58021-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="58021-116">Return value</span></span>

<span data-ttu-id="58021-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="58021-117">S_OK</span></span> 
  
> <span data-ttu-id="58021-118">Les adresses de la fonction ont été renvoyées avec succès.</span><span class="sxs-lookup"><span data-stu-id="58021-118">The function addresses were successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="58021-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="58021-119">Remarks</span></span>

<span data-ttu-id="58021-120">La méthode **IMAPISupport:: GetMemAllocRoutines** est implémentée pour tous les objets de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="58021-120">The **IMAPISupport::GetMemAllocRoutines** method is implemented for all support objects.</span></span> <span data-ttu-id="58021-121">Les fournisseurs de services appellent **GetMemAllocRoutines** pour obtenir les adresses des trois fonctions d'allocation de mémoire qui sont transmises à leur fonction d'initialisation ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md)ou [XPProviderInit](xpproviderinit.md)).</span><span class="sxs-lookup"><span data-stu-id="58021-121">Service providers call **GetMemAllocRoutines** to get the addresses of the three memory allocation functions that are passed to their initialization function ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md), or [XPProviderInit](xpproviderinit.md)).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="58021-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58021-122">See also</span></span>



[<span data-ttu-id="58021-123">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="58021-123">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="58021-124">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="58021-124">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="58021-125">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="58021-125">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="58021-126">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="58021-126">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

