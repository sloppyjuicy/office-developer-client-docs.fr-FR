---
title: MAPIFreeBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIFreeBuffer
api_type:
- HeaderDef
ms.assetid: 9412594f-8acc-4c7e-a668-4ec1da0ad9cf
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ad3d9d12e1073610747b0ab078c6d65c09f8c7c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569140"
---
# <a name="mapifreebuffer"></a><span data-ttu-id="5e2ec-103">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="5e2ec-103">MAPIFreeBuffer</span></span>

  
  
<span data-ttu-id="5e2ec-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e2ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e2ec-105">Libère une mémoire tampon alloué avec un appel à la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) ou [MAPIAllocateMore](mapiallocatemore.md) .</span><span class="sxs-lookup"><span data-stu-id="5e2ec-105">Frees a memory buffer allocated with a call to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function or the [MAPIAllocateMore](mapiallocatemore.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5e2ec-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="5e2ec-106">Header file:</span></span>  <br/> |<span data-ttu-id="5e2ec-107">MAPIX.h</span><span class="sxs-lookup"><span data-stu-id="5e2ec-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="5e2ec-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="5e2ec-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5e2ec-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5e2ec-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5e2ec-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="5e2ec-110">Called by:</span></span>  <br/> |<span data-ttu-id="5e2ec-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="5e2ec-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="5e2ec-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e2ec-112">Parameters</span></span>

 <span data-ttu-id="5e2ec-113">_lpBuffer_</span><span class="sxs-lookup"><span data-stu-id="5e2ec-113">_lpBuffer_</span></span>
  
> <span data-ttu-id="5e2ec-114">[in] Pointeur vers un tampon de mémoire allouée précédemment.</span><span class="sxs-lookup"><span data-stu-id="5e2ec-114">[in] Pointer to a previously allocated memory buffer.</span></span> <span data-ttu-id="5e2ec-115">Si NULL est indiqué dans le paramètre _lpBuffer_ , **MAPIFreeBuffer** est sans effet.</span><span class="sxs-lookup"><span data-stu-id="5e2ec-115">If NULL is passed in the  _lpBuffer_ parameter, **MAPIFreeBuffer** does nothing.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5e2ec-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5e2ec-116">Return value</span></span>

<span data-ttu-id="5e2ec-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="5e2ec-117">S_OK</span></span> 
  
> <span data-ttu-id="5e2ec-118">L’appel a réussi et libérer de la mémoire requise.</span><span class="sxs-lookup"><span data-stu-id="5e2ec-118">The call succeeded and freed the memory requested.</span></span> <span data-ttu-id="5e2ec-119">**MAPIFreeBuffer** peut aussi renvoyer S_OK dans des emplacements déjà libérés ou le bloc de mémoire non allouée avec **MAPIAllocateBuffer** et **MAPIAllocateMore**.</span><span class="sxs-lookup"><span data-stu-id="5e2ec-119">**MAPIFreeBuffer** can also return S_OK on already freed locations or if memory block is not allocated with **MAPIAllocateBuffer** and **MAPIAllocateMore**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5e2ec-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="5e2ec-120">Remarks</span></span>

<span data-ttu-id="5e2ec-121">En règle générale, lorsqu’une application cliente ou un fournisseur de services appelle [MAPIAllocateBuffer](mapiallocatebuffer.md) ou [MAPIAllocateMore](mapiallocatemore.md), les constructions de système d’exploitation dans une mémoire contiguë tampon un ou plusieurs des structures complexes avec plusieurs niveaux de pointeurs.</span><span class="sxs-lookup"><span data-stu-id="5e2ec-121">Usually, when a client application or service provider calls [MAPIAllocateBuffer](mapiallocatebuffer.md) or [MAPIAllocateMore](mapiallocatemore.md), the operating system constructs in one contiguous memory buffer one or more complex structures with multiple levels of pointers.</span></span> <span data-ttu-id="5e2ec-122">Lorsqu’une fonction MAPI ou méthode crée un tampon avec ce type de contenu, un client peut libérer ultérieurement toutes les structures contenues dans la mémoire tampon, en passant à **MAPIFreeBuffer** le pointeur vers la mémoire tampon retournée par la fonction MAPI qui a créé la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="5e2ec-122">When a MAPI function or method creates a buffer with such contents, a client can later free all the structures contained in the buffer by passing to **MAPIFreeBuffer** the pointer to the buffer returned by the MAPI function that created the buffer.</span></span> <span data-ttu-id="5e2ec-123">Pour un fournisseur de service libérer de l’une à l’aide de **MAPIFreeBuffer**de mémoire tampon, il doit passer le pointeur à cette mémoire tampon renvoyée avec l’objet de prise en charge du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5e2ec-123">For a service provider to free a memory buffer using **MAPIFreeBuffer**, it must pass the pointer to that buffer returned with the provider's support object.</span></span> 
  
<span data-ttu-id="5e2ec-124">L’appel à **MAPIFreeBuffer** pour libérer un tampon particulier doit être effectuée dès qu’un client ou fournisseur est terminé, à l’aide de cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="5e2ec-124">The call to **MAPIFreeBuffer** to free a particular buffer must be made as soon as a client or provider is finished using this buffer.</span></span> <span data-ttu-id="5e2ec-125">Simplement en appelant la méthode [IMAPISession::Logoff](imapisession-logoff.md) à la fin d’une session MAPI n’annule pas automatiquement les mémoires tampon.</span><span class="sxs-lookup"><span data-stu-id="5e2ec-125">Simply calling the [IMAPISession::Logoff](imapisession-logoff.md) method at the end of a MAPI session does not automatically release memory buffers.</span></span> 
  
<span data-ttu-id="5e2ec-126">Un client ou fournisseur de services doit fonctionner sur l’hypothèse que le pointeur passé _lpBuffer_ est non valide après le retour à partir de **MAPIFreeBuffer**réussi.</span><span class="sxs-lookup"><span data-stu-id="5e2ec-126">A client or service provider should operate on the assumption that the pointer passed in  _lpBuffer_ is invalid after a successful return from **MAPIFreeBuffer**.</span></span> <span data-ttu-id="5e2ec-127">Si le pointeur indique un bloc de mémoire non alloué par le système de messagerie via **MAPIAllocateBuffer** ou **MAPIAllocateMore** ou un bloc de mémoire disponible, le comportement de **MAPIFreeBuffer** est indéfini.</span><span class="sxs-lookup"><span data-stu-id="5e2ec-127">If the pointer indicates either a memory block not allocated by the messaging system through **MAPIAllocateBuffer** or **MAPIAllocateMore** or a free memory block, the behavior of **MAPIFreeBuffer** is undefined.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5e2ec-128">Passer un pointeur null à **MAPIFreeBuffer** rend application nettoyage code plus simple et plus petits car **MAPIFreeBuffer** peut initialiser des pointeurs NULL et les libérer dans le code de nettoyage sans avoir à les tester tout d’abord.</span><span class="sxs-lookup"><span data-stu-id="5e2ec-128">Passing a null pointer to **MAPIFreeBuffer** makes application cleanup code simpler and smaller because **MAPIFreeBuffer** can initialize pointers to NULL and then free them in the cleanup code without having to test them first.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5e2ec-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e2ec-129">See also</span></span>



[<span data-ttu-id="5e2ec-130">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="5e2ec-130">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)

