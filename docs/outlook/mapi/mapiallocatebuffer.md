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
ms.openlocfilehash: 0520b219c87207a54555ba74050761f6ecc4854a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579598"
---
# <a name="mapiallocatebuffer"></a><span data-ttu-id="c8057-103">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="c8057-103">MAPIAllocateBuffer</span></span>

  
  
<span data-ttu-id="c8057-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8057-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8057-105">Affecte une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c8057-105">Allocates a memory buffer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c8057-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c8057-106">Header file:</span></span>  <br/> |<span data-ttu-id="c8057-107">MAPIX.h</span><span class="sxs-lookup"><span data-stu-id="c8057-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="c8057-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="c8057-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c8057-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c8057-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c8057-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="c8057-110">Called by:</span></span>  <br/> |<span data-ttu-id="c8057-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="c8057-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="c8057-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c8057-112">Parameters</span></span>

 <span data-ttu-id="c8057-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="c8057-113">_cbSize_</span></span>
  
> <span data-ttu-id="c8057-114">[in] Taille, en octets, de la mémoire tampon à allouer.</span><span class="sxs-lookup"><span data-stu-id="c8057-114">[in] Size, in bytes, of the buffer to be allocated.</span></span> 
    
 <span data-ttu-id="c8057-115">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="c8057-115">_lppBuffer_</span></span>
  
> <span data-ttu-id="c8057-116">[out] Pointeur vers la mémoire tampon allouée retournée.</span><span class="sxs-lookup"><span data-stu-id="c8057-116">[out] Pointer to the returned allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c8057-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c8057-117">Return value</span></span>

<span data-ttu-id="c8057-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="c8057-118">S_OK</span></span> 
  
> <span data-ttu-id="c8057-119">L’appel a réussi et a renvoyé la mémoire tampon de mémoire requise.</span><span class="sxs-lookup"><span data-stu-id="c8057-119">The call succeeded and has returned the requested memory buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c8057-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="c8057-120">Remarks</span></span>

<span data-ttu-id="c8057-121">Traitement des appels pendant **MAPIAllocateBuffer** , l’implémentation appelante acquiert un bloc de mémoire du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="c8057-121">During **MAPIAllocateBuffer** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="c8057-122">La mémoire tampon est alloué sur une adresse de paires sur deux octets.</span><span class="sxs-lookup"><span data-stu-id="c8057-122">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="c8057-123">Sur les plateformes où access entier long est plus efficace, le système d’exploitation alloue de la mémoire tampon sur une adresse dont la taille en octets est un multiple de quatre.</span><span class="sxs-lookup"><span data-stu-id="c8057-123">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="c8057-124">Appel de la fonction de presse [MAPIFreeBuffer](mapifreebuffer.md) la mémoire tampon allouée par **MAPIAllocateBuffer**, en appelant la fonction [MAPIAllocateMore](mapiallocatemore.md) et les mémoires tampons liés, lorsque la mémoire n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c8057-124">Calling the [MAPIFreeBuffer](mapifreebuffer.md) function releases the memory buffer allocated by **MAPIAllocateBuffer**, by calling the [MAPIAllocateMore](mapiallocatemore.md) function and any buffers linked to it, when the memory is no longer needed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c8057-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8057-125">See also</span></span>



[<span data-ttu-id="c8057-126">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="c8057-126">MAPIReallocateBuffer</span></span>](mapireallocatebuffer.md)

