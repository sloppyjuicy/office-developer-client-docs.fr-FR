---
title: MAPIAllocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAllocateBuffer
api_type:
- HeaderDef
ms.assetid: f1fc7fc5-c71f-44f7-930a-571773eb6809
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 589ad42199e6f2ec1039499dfd9beda044ccc3dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425693"
---
# <a name="mapiallocatebuffer"></a><span data-ttu-id="371a0-103">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="371a0-103">MAPIAllocateBuffer</span></span>

  
  
<span data-ttu-id="371a0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="371a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="371a0-105">Alloue une mémoire tampon de mémoire.</span><span class="sxs-lookup"><span data-stu-id="371a0-105">Allocates a memory buffer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="371a0-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="371a0-106">Header file:</span></span>  <br/> |<span data-ttu-id="371a0-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="371a0-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="371a0-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="371a0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="371a0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="371a0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="371a0-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="371a0-110">Called by:</span></span>  <br/> |<span data-ttu-id="371a0-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="371a0-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="371a0-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="371a0-112">Parameters</span></span>

 <span data-ttu-id="371a0-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="371a0-113">_cbSize_</span></span>
  
> <span data-ttu-id="371a0-114">dans Taille, en octets, de la mémoire tampon à allouer.</span><span class="sxs-lookup"><span data-stu-id="371a0-114">[in] Size, in bytes, of the buffer to be allocated.</span></span> 
    
 <span data-ttu-id="371a0-115">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="371a0-115">_lppBuffer_</span></span>
  
> <span data-ttu-id="371a0-116">remarquer Pointeur vers la mémoire tampon allouée renvoyée.</span><span class="sxs-lookup"><span data-stu-id="371a0-116">[out] Pointer to the returned allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="371a0-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="371a0-117">Return value</span></span>

<span data-ttu-id="371a0-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="371a0-118">S_OK</span></span> 
  
> <span data-ttu-id="371a0-119">L'appel a réussi et a renvoyé la mémoire tampon demandée.</span><span class="sxs-lookup"><span data-stu-id="371a0-119">The call succeeded and has returned the requested memory buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="371a0-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="371a0-120">Remarks</span></span>

<span data-ttu-id="371a0-121">Pendant le traitement des appels **MAPIAllocateBuffer** , l'implémentation de l'appel acquiert un bloc de mémoire à partir du système d'exploitation.</span><span class="sxs-lookup"><span data-stu-id="371a0-121">During **MAPIAllocateBuffer** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="371a0-122">La mémoire tampon est allouée sur une adresse d'octet portant un numéro pair.</span><span class="sxs-lookup"><span data-stu-id="371a0-122">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="371a0-123">Sur les plateformes où l'accès entier long est plus efficace, le système d'exploitation alloue la mémoire tampon sur une adresse dont la taille en octets est un multiple de quatre.</span><span class="sxs-lookup"><span data-stu-id="371a0-123">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="371a0-124">L'appel de la fonction [MAPIFreeBuffer](mapifreebuffer.md) libère la mémoire tampon allouée par **MAPIAllocateBuffer**, en appelant la fonction [MAPIAllocateMore](mapiallocatemore.md) et les mémoires tampon qui y sont liées, lorsque la mémoire n'est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="371a0-124">Calling the [MAPIFreeBuffer](mapifreebuffer.md) function releases the memory buffer allocated by **MAPIAllocateBuffer**, by calling the [MAPIAllocateMore](mapiallocatemore.md) function and any buffers linked to it, when the memory is no longer needed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="371a0-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="371a0-125">See also</span></span>



[<span data-ttu-id="371a0-126">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="371a0-126">MAPIReallocateBuffer</span></span>](mapireallocatebuffer.md)

