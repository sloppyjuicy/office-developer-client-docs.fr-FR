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
ms.openlocfilehash: 01980b2da735838eeffa9afa5a0d139b69e76d0c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435389"
---
# <a name="mapiallocatemore"></a><span data-ttu-id="1c1a0-103">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="1c1a0-103">MAPIAllocateMore</span></span>

  
  
<span data-ttu-id="1c1a0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c1a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c1a0-105">Alloue une mémoire tampon liée à une autre mémoire tampon précédemment allouée à l'aide de la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="1c1a0-105">Allocates a memory buffer that is linked to another buffer previously allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1c1a0-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="1c1a0-106">Header file:</span></span>  <br/> |<span data-ttu-id="1c1a0-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="1c1a0-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="1c1a0-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="1c1a0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1c1a0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1c1a0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1c1a0-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="1c1a0-110">Called by:</span></span>  <br/> |<span data-ttu-id="1c1a0-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="1c1a0-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="1c1a0-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c1a0-112">Parameters</span></span>

 <span data-ttu-id="1c1a0-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="1c1a0-113">_cbSize_</span></span>
  
> <span data-ttu-id="1c1a0-114">dans Taille, en octets, de la nouvelle mémoire tampon à allouer.</span><span class="sxs-lookup"><span data-stu-id="1c1a0-114">[in] Size, in bytes, of the new buffer to be allocated.</span></span> 
    
 <span data-ttu-id="1c1a0-115">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="1c1a0-115">_lpObject_</span></span>
  
> <span data-ttu-id="1c1a0-116">dans Pointeur vers un tampon MAPI existant alloué à l'aide de **MAPIAllocateBuffer**.</span><span class="sxs-lookup"><span data-stu-id="1c1a0-116">[in] Pointer to an existing MAPI buffer allocated using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="1c1a0-117">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="1c1a0-117">_lppBuffer_</span></span>
  
> <span data-ttu-id="1c1a0-118">remarquer Pointeur vers la mémoire tampon renvoyée qui vient d'être allouée.</span><span class="sxs-lookup"><span data-stu-id="1c1a0-118">[out] Pointer to the returned, newly allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1c1a0-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1c1a0-119">Return value</span></span>

<span data-ttu-id="1c1a0-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="1c1a0-120">S_OK</span></span> 
  
> <span data-ttu-id="1c1a0-121">L'appel a réussi et a renvoyé un pointeur vers la mémoire demandée.</span><span class="sxs-lookup"><span data-stu-id="1c1a0-121">The call succeeded and has returned a pointer to the requested memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1c1a0-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="1c1a0-122">Remarks</span></span>

<span data-ttu-id="1c1a0-123">Pendant le traitement des appels **MAPIAllocateMore** , l'implémentation de l'appel acquiert un bloc de mémoire à partir du système d'exploitation.</span><span class="sxs-lookup"><span data-stu-id="1c1a0-123">During **MAPIAllocateMore** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="1c1a0-124">La mémoire tampon est allouée sur une adresse d'octet portant un numéro pair.</span><span class="sxs-lookup"><span data-stu-id="1c1a0-124">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="1c1a0-125">Sur les plateformes où l'accès entier long est plus efficace, le système d'exploitation alloue la mémoire tampon sur une adresse dont la taille en octets est un multiple de quatre.</span><span class="sxs-lookup"><span data-stu-id="1c1a0-125">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="1c1a0-126">La seule façon de libérer un tampon alloué avec **MAPIAllocateMore** est de transmettre le pointeur de mémoire tampon spécifié dans le paramètre _lpObject_ à la fonction [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="1c1a0-126">The only way to release a buffer allocated with **MAPIAllocateMore** is to pass the buffer pointer specified in the  _lpObject_ parameter to the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="1c1a0-127">Le lien entre les mémoires tampons de mémoire allouées avec [MAPIAllocateBuffer](mapiallocatebuffer.md) et **MAPIAllocateMore** permet à **MAPIFreeBuffer** de libérer les deux tampons à l'aide d'un seul appel.</span><span class="sxs-lookup"><span data-stu-id="1c1a0-127">The link between the memory buffers allocated with [MAPIAllocateBuffer](mapiallocatebuffer.md) and **MAPIAllocateMore** enables **MAPIFreeBuffer** to release both buffers with a single call.</span></span> 
  

