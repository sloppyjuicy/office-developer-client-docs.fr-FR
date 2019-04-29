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
ms.openlocfilehash: 8794bb233eb69d0f246fb1019954ab718db6f464
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410552"
---
# <a name="mapifreebuffer"></a><span data-ttu-id="b140e-103">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b140e-103">MAPIFreeBuffer</span></span>

  
  
<span data-ttu-id="b140e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b140e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b140e-105">Libère une mémoire tampon allouée à l'aide d'un appel à la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) ou à la fonction [MAPIAllocateMore](mapiallocatemore.md) .</span><span class="sxs-lookup"><span data-stu-id="b140e-105">Frees a memory buffer allocated with a call to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function or the [MAPIAllocateMore](mapiallocatemore.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b140e-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b140e-106">Header file:</span></span>  <br/> |<span data-ttu-id="b140e-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="b140e-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="b140e-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="b140e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b140e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b140e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b140e-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="b140e-110">Called by:</span></span>  <br/> |<span data-ttu-id="b140e-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="b140e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="b140e-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b140e-112">Parameters</span></span>

 <span data-ttu-id="b140e-113">_lpBuffer_</span><span class="sxs-lookup"><span data-stu-id="b140e-113">_lpBuffer_</span></span>
  
> <span data-ttu-id="b140e-114">dans Pointeur vers une mémoire tampon de mémoire allouée précédemment.</span><span class="sxs-lookup"><span data-stu-id="b140e-114">[in] Pointer to a previously allocated memory buffer.</span></span> <span data-ttu-id="b140e-115">Si NULL est passé dans le paramètre _lpBuffer_ , **MAPIFreeBuffer** n'a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="b140e-115">If NULL is passed in the  _lpBuffer_ parameter, **MAPIFreeBuffer** does nothing.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b140e-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b140e-116">Return value</span></span>

<span data-ttu-id="b140e-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="b140e-117">S_OK</span></span> 
  
> <span data-ttu-id="b140e-118">L'appel a réussi et a libéré la mémoire demandée.</span><span class="sxs-lookup"><span data-stu-id="b140e-118">The call succeeded and freed the memory requested.</span></span> <span data-ttu-id="b140e-119">**MAPIFreeBuffer** peut également renvoyer S_OK sur des emplacements déjà libérés ou si le bloc de mémoire n'est pas alloué avec **MAPIAllocateBuffer** et **MAPIAllocateMore**.</span><span class="sxs-lookup"><span data-stu-id="b140e-119">**MAPIFreeBuffer** can also return S_OK on already freed locations or if memory block is not allocated with **MAPIAllocateBuffer** and **MAPIAllocateMore**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b140e-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="b140e-120">Remarks</span></span>

<span data-ttu-id="b140e-121">En règle générale, lorsqu'une application cliente ou un fournisseur de services appelle [MAPIAllocateBuffer](mapiallocatebuffer.md) ou [MAPIAllocateMore](mapiallocatemore.md), le système d'exploitation construit dans un tampon de mémoire contigu une ou plusieurs structures complexes avec plusieurs niveaux de pointeurs.</span><span class="sxs-lookup"><span data-stu-id="b140e-121">Usually, when a client application or service provider calls [MAPIAllocateBuffer](mapiallocatebuffer.md) or [MAPIAllocateMore](mapiallocatemore.md), the operating system constructs in one contiguous memory buffer one or more complex structures with multiple levels of pointers.</span></span> <span data-ttu-id="b140e-122">Lorsqu'une fonction ou méthode MAPI crée une mémoire tampon avec un tel contenu, un client peut libérer ultérieurement toutes les structures contenues dans la mémoire tampon en transmettant à **MAPIFreeBuffer** le pointeur vers la mémoire tampon renvoyée par la fonction MAPI qui a créé la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b140e-122">When a MAPI function or method creates a buffer with such contents, a client can later free all the structures contained in the buffer by passing to **MAPIFreeBuffer** the pointer to the buffer returned by the MAPI function that created the buffer.</span></span> <span data-ttu-id="b140e-123">Pour qu'un fournisseur de services libère une mémoire tampon à l'aide de **MAPIFreeBuffer**, il doit transmettre le pointeur à ce tampon renvoyé avec l'objet de support du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b140e-123">For a service provider to free a memory buffer using **MAPIFreeBuffer**, it must pass the pointer to that buffer returned with the provider's support object.</span></span> 
  
<span data-ttu-id="b140e-124">L'appel à **MAPIFreeBuffer** pour libérer une mémoire tampon particulière doit être effectué dès qu'un client ou un fournisseur a terminé d'utiliser cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b140e-124">The call to **MAPIFreeBuffer** to free a particular buffer must be made as soon as a client or provider is finished using this buffer.</span></span> <span data-ttu-id="b140e-125">Le simple fait d'appeler la méthode [IMAPISession:: Logoff](imapisession-logoff.md) à la fin d'une session MAPI ne libère pas automatiquement les mémoires tampons de mémoire.</span><span class="sxs-lookup"><span data-stu-id="b140e-125">Simply calling the [IMAPISession::Logoff](imapisession-logoff.md) method at the end of a MAPI session does not automatically release memory buffers.</span></span> 
  
<span data-ttu-id="b140e-126">Un client ou un fournisseur de services doit agir en supposant que le pointeur transmis dans _lpBuffer_ n'est pas valide après un retour de **MAPIFreeBuffer**.</span><span class="sxs-lookup"><span data-stu-id="b140e-126">A client or service provider should operate on the assumption that the pointer passed in  _lpBuffer_ is invalid after a successful return from **MAPIFreeBuffer**.</span></span> <span data-ttu-id="b140e-127">Si le pointeur indique un bloc de mémoire qui n'est pas alloué par le système de messagerie via **MAPIAllocateBuffer** ou **MAPIAllocateMore** ou un bloc de mémoire libre, le comportement de **MAPIFreeBuffer** n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="b140e-127">If the pointer indicates either a memory block not allocated by the messaging system through **MAPIAllocateBuffer** or **MAPIAllocateMore** or a free memory block, the behavior of **MAPIFreeBuffer** is undefined.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b140e-128">Le passage d'un pointeur null à **MAPIFreeBuffer** rend le code de nettoyage d'application plus simple et plus petit car **MAPIFreeBuffer** peut initialiser des pointeurs vers des valeurs NULL, puis les libérer dans le code de nettoyage sans avoir à les tester d'abord.</span><span class="sxs-lookup"><span data-stu-id="b140e-128">Passing a null pointer to **MAPIFreeBuffer** makes application cleanup code simpler and smaller because **MAPIFreeBuffer** can initialize pointers to NULL and then free them in the cleanup code without having to test them first.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b140e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b140e-129">See also</span></span>



[<span data-ttu-id="b140e-130">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="b140e-130">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)

