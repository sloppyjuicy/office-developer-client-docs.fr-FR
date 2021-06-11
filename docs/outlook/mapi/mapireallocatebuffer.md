---
title: MAPIReallocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 182ab0c6-c9d3-4cc8-892f-f6b09312ceb9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 59d0ce192605257dc0aebed46d8093a352fce05f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435284"
---
# <a name="mapireallocatebuffer"></a><span data-ttu-id="d7d41-103">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="d7d41-103">MAPIReallocateBuffer</span></span>

  
  
<span data-ttu-id="d7d41-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7d41-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7d41-105">Réaffecte une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="d7d41-105">Reallocates a memory buffer.</span></span> <span data-ttu-id="d7d41-106">Il est utilisé avec la [fonction MAPIAllocateBuffer.](mapiallocatebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="d7d41-106">It is used with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d7d41-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="d7d41-107">Header file:</span></span>  <br/> |<span data-ttu-id="d7d41-108">omapix.h</span><span class="sxs-lookup"><span data-stu-id="d7d41-108">omapix.h</span></span>  <br/> |
|<span data-ttu-id="d7d41-109">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="d7d41-109">Called by:</span></span>  <br/> |<span data-ttu-id="d7d41-110">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="d7d41-110">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDMETHODIMP_(SCODE) MAPIReallocateBuffer
(
LPVOID lpv, 
ULONG ulSize, 
LPVOID * lppv
);
```

## <a name="parameters"></a><span data-ttu-id="d7d41-111">Parameters</span><span class="sxs-lookup"><span data-stu-id="d7d41-111">Parameters</span></span>

 <span data-ttu-id="d7d41-112">_lpv_</span><span class="sxs-lookup"><span data-stu-id="d7d41-112">_lpv_</span></span>
  
> <span data-ttu-id="d7d41-113">Pointeur vers la mémoire à réaffecter.</span><span class="sxs-lookup"><span data-stu-id="d7d41-113">A pointer to the memory to be reallocated.</span></span>
    
 <span data-ttu-id="d7d41-114">_ulSize_</span><span class="sxs-lookup"><span data-stu-id="d7d41-114">_ulSize_</span></span>
  
> <span data-ttu-id="d7d41-115">Taille, en octets, de la mémoire tampon à allouer.</span><span class="sxs-lookup"><span data-stu-id="d7d41-115">The size, in bytes, of the buffer to be allocated.</span></span>
    
 <span data-ttu-id="d7d41-116">_lppv_</span><span class="sxs-lookup"><span data-stu-id="d7d41-116">_lppv_</span></span>
  
> <span data-ttu-id="d7d41-117">Pointeur vers la mémoire tampon allouée renvoyée.</span><span class="sxs-lookup"><span data-stu-id="d7d41-117">A pointer to the returned allocated buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d7d41-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="d7d41-118">Remarks</span></span>

 <span data-ttu-id="d7d41-119">**MAPIReallocateBuffer** alloue un nouveau bloc de mémoire de la taille demandée et copie le contenu de la mémoire tampon qui est passée dans ce nouveau bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="d7d41-119">**MAPIReallocateBuffer** allocates a new block of memory of the requested size and copies the contents of the buffer that is passed into this new block of memory.</span></span> <span data-ttu-id="d7d41-120">Si le bloc de mémoire transmis contient des pointeurs internes, les pointeurs ne changent pas pour correspondre au nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="d7d41-120">If the block of memory that is passed contains internal pointers, the pointers do not change to match the new location.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d7d41-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7d41-121">See also</span></span>



[<span data-ttu-id="d7d41-122">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="d7d41-122">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)

