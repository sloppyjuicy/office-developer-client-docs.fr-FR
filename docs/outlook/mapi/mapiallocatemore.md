---
title: MAPIAllocateMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAllocateMore
api_type:
- HeaderDef
ms.assetid: 3e48f76a-bc97-4cbc-9082-c07dd674b73e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0e6226dd0fc9c04070ed3d1dda1770f77fbc585c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583007"
---
# <a name="mapiallocatemore"></a><span data-ttu-id="6711b-103">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="6711b-103">MAPIAllocateMore</span></span>

  
  
<span data-ttu-id="6711b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6711b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6711b-105">Affecte une mémoire tampon qui est liée à une autre mémoire tampon précédemment allouée avec la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="6711b-105">Allocates a memory buffer that is linked to another buffer previously allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6711b-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="6711b-106">Header file:</span></span>  <br/> |<span data-ttu-id="6711b-107">MAPIX.h</span><span class="sxs-lookup"><span data-stu-id="6711b-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="6711b-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="6711b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6711b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6711b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6711b-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="6711b-110">Called by:</span></span>  <br/> |<span data-ttu-id="6711b-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="6711b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="6711b-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6711b-112">Parameters</span></span>

 <span data-ttu-id="6711b-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="6711b-113">_cbSize_</span></span>
  
> <span data-ttu-id="6711b-114">[in] Taille, en octets, de la nouvelle mémoire tampon à allouer.</span><span class="sxs-lookup"><span data-stu-id="6711b-114">[in] Size, in bytes, of the new buffer to be allocated.</span></span> 
    
 <span data-ttu-id="6711b-115">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="6711b-115">_lpObject_</span></span>
  
> <span data-ttu-id="6711b-116">[in] Pointeur vers un tampon MAPI existant alloué à l’aide de **MAPIAllocateBuffer**.</span><span class="sxs-lookup"><span data-stu-id="6711b-116">[in] Pointer to an existing MAPI buffer allocated using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="6711b-117">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="6711b-117">_lppBuffer_</span></span>
  
> <span data-ttu-id="6711b-118">[out] Pointeur vers retourné nouvellement allouer de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="6711b-118">[out] Pointer to the returned, newly allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6711b-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6711b-119">Return value</span></span>

<span data-ttu-id="6711b-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="6711b-120">S_OK</span></span> 
  
> <span data-ttu-id="6711b-121">L’appel a réussi et a renvoyé un pointeur vers la mémoire requise.</span><span class="sxs-lookup"><span data-stu-id="6711b-121">The call succeeded and has returned a pointer to the requested memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6711b-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="6711b-122">Remarks</span></span>

<span data-ttu-id="6711b-123">Traitement des appels pendant **MAPIAllocateMore** , l’implémentation appelante acquiert un bloc de mémoire du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="6711b-123">During **MAPIAllocateMore** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="6711b-124">La mémoire tampon est alloué sur une adresse de paires sur deux octets.</span><span class="sxs-lookup"><span data-stu-id="6711b-124">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="6711b-125">Sur les plateformes où access entier long est plus efficace, le système d’exploitation alloue de la mémoire tampon sur une adresse dont la taille en octets est un multiple de quatre.</span><span class="sxs-lookup"><span data-stu-id="6711b-125">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="6711b-126">Le seul moyen pour libérer la mémoire tampon allouée avec **MAPIAllocateMore** consiste à passer le pointeur de la mémoire tampon spécifié dans le paramètre _lpObject_ à la fonction [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="6711b-126">The only way to release a buffer allocated with **MAPIAllocateMore** is to pass the buffer pointer specified in the  _lpObject_ parameter to the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="6711b-127">La liaison entre les mémoire tampon allouée avec [MAPIAllocateBuffer](mapiallocatebuffer.md) et **MAPIAllocateMore** active **MAPIFreeBuffer** libérer les deux tampons avec un seul appel.</span><span class="sxs-lookup"><span data-stu-id="6711b-127">The link between the memory buffers allocated with [MAPIAllocateBuffer](mapiallocatebuffer.md) and **MAPIAllocateMore** enables **MAPIFreeBuffer** to release both buffers with a single call.</span></span> 
  

