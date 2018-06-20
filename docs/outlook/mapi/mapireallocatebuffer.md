---
title: MAPIReallocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 182ab0c6-c9d3-4cc8-892f-f6b09312ceb9
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 26dcc31f2ebdd1892f966bfb95fda1a65c5140cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784768"
---
# <a name="mapireallocatebuffer"></a><span data-ttu-id="80831-103">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="80831-103">MAPIReallocateBuffer</span></span>

  
  
<span data-ttu-id="80831-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="80831-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="80831-105">Réaffecte une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="80831-105">Reallocates a memory buffer.</span></span> <span data-ttu-id="80831-106">Il est utilisé avec la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="80831-106">It is used with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="80831-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="80831-107">Header file:</span></span>  <br/> |<span data-ttu-id="80831-108">omapix.h</span><span class="sxs-lookup"><span data-stu-id="80831-108">omapix.h</span></span>  <br/> |
|<span data-ttu-id="80831-109">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="80831-109">Called by:</span></span>  <br/> |<span data-ttu-id="80831-110">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="80831-110">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDMETHODIMP_(SCODE) MAPIReallocateBuffer
(
LPVOID lpv, 
ULONG ulSize, 
LPVOID * lppv
);
```

## <a name="parameters"></a><span data-ttu-id="80831-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80831-111">Parameters</span></span>

 <span data-ttu-id="80831-112">_LPV_</span><span class="sxs-lookup"><span data-stu-id="80831-112">_lpv_</span></span>
  
> <span data-ttu-id="80831-113">Pointeur vers la mémoire à être réaffecté.</span><span class="sxs-lookup"><span data-stu-id="80831-113">A pointer to the memory to be reallocated.</span></span>
    
 <span data-ttu-id="80831-114">_ulSize_</span><span class="sxs-lookup"><span data-stu-id="80831-114">_ulSize_</span></span>
  
> <span data-ttu-id="80831-115">La taille, en octets, de la mémoire tampon à allouer.</span><span class="sxs-lookup"><span data-stu-id="80831-115">The size, in bytes, of the buffer to be allocated.</span></span>
    
 <span data-ttu-id="80831-116">_lppv_</span><span class="sxs-lookup"><span data-stu-id="80831-116">_lppv_</span></span>
  
> <span data-ttu-id="80831-117">Pointeur vers la mémoire tampon allouée retournée.</span><span class="sxs-lookup"><span data-stu-id="80831-117">A pointer to the returned allocated buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="80831-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="80831-118">Remarks</span></span>

 <span data-ttu-id="80831-119">**MAPIReallocateBuffer** attribue un nouveau bloc de mémoire de la taille requise et copie le contenu de la mémoire tampon qui est passé dans ce nouveau bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="80831-119">**MAPIReallocateBuffer** allocates a new block of memory of the requested size and copies the contents of the buffer that is passed into this new block of memory.</span></span> <span data-ttu-id="80831-120">Si le bloc de mémoire est passée contient des pointeurs internes, les pointeurs ne modifiez pas pour correspondre au nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="80831-120">If the block of memory that is passed contains internal pointers, the pointers do not change to match the new location.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="80831-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80831-121">See also</span></span>



[<span data-ttu-id="80831-122">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="80831-122">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)

