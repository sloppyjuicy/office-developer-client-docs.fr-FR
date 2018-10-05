---
title: Gestion de la mémoire dans MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9eee6925-ab91-413e-8907-c747ab4a4bb5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 66489c09be641d8fe9ae5f3ffff46a6d5004f473
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388069"
---
# <a name="managing-memory-in-mapi"></a><span data-ttu-id="b692c-103">Gestion de la mémoire dans MAPI</span><span class="sxs-lookup"><span data-stu-id="b692c-103">Managing Memory in MAPI</span></span>

  
  
<span data-ttu-id="b692c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b692c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b692c-105">Savoir quand et comment allouer et libérer de la mémoire constitue une part importante de la programmation MAPI.</span><span class="sxs-lookup"><span data-stu-id="b692c-105">Knowing how and when to allocate and free memory is an important part of programming with MAPI.</span></span> <span data-ttu-id="b692c-106">MAPI fournit les fonctions et les macros que votre client ou fournisseur de services permettre utiliser pour gérer la mémoire de façon cohérente.</span><span class="sxs-lookup"><span data-stu-id="b692c-106">MAPI provides both functions and macros that your client or service provider can use to manage memory in a consistent way.</span></span> <span data-ttu-id="b692c-107">Les trois fonctions sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b692c-107">The three functions are as follows:</span></span>
  
[<span data-ttu-id="b692c-108">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="b692c-108">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="b692c-109">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="b692c-109">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="b692c-110">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b692c-110">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
<span data-ttu-id="b692c-111">Lorsque les clients et les fournisseurs de services utilisent ces fonctions, le problème de « propriétaire », c'est-à-dire, sait comment libérer — un bloc de mémoire particulier est éliminé.</span><span class="sxs-lookup"><span data-stu-id="b692c-111">When clients and service providers use these functions, the issue of who "owns" — that is, knows how to release — a particular block of memory is eliminated.</span></span> <span data-ttu-id="b692c-112">Un client appelant une méthode de fournisseur de service ne devez pas transmettre un tampon suffisant pour contenir une valeur de retour de toute taille.</span><span class="sxs-lookup"><span data-stu-id="b692c-112">A client calling a service provider method need not pass a buffer large enough to hold a return value of any size.</span></span> <span data-ttu-id="b692c-113">Le fournisseur de services peut allouer simplement la quantité de mémoire à l’aide de **MAPIAllocateBuffer** appropriée et, si nécessaire, **MAPIAllocateMore**et le client peuvent ultérieurement libérer à l’aide de **MAPIFreeBuffer**, indépendamment du service fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="b692c-113">The service provider can simply allocate the appropriate amount of memory using **MAPIAllocateBuffer** and, if necessary, **MAPIAllocateMore**, and the client can later release it at will using **MAPIFreeBuffer**, independent of the service provider.</span></span> 
  
<span data-ttu-id="b692c-114">Les macros de mémoire sont utilisés pour affecter des structures ou des tableaux de structures d’une taille spécifique.</span><span class="sxs-lookup"><span data-stu-id="b692c-114">The memory macros are used to allocate structures or arrays of structures of a specific size.</span></span> <span data-ttu-id="b692c-115">Clients et fournisseurs de services doivent utiliser ces macros au lieu d’allouer de la mémoire manuellement.</span><span class="sxs-lookup"><span data-stu-id="b692c-115">Clients and service providers should use these macros rather than allocate the memory manually.</span></span> <span data-ttu-id="b692c-116">Par exemple, si un client doit effectuer une résolution de traitement sur une liste de destinataires avec trois entrées, la macro **SizedADRLIST** peut être utilisée pour créer une structure **ADRLIST** à transmettre à **IAddrBook::ResolveName** avec le nombre approprié de Membres **ADRENTRY** .</span><span class="sxs-lookup"><span data-stu-id="b692c-116">For example, if a client needs to perform name resolution processing on a recipient list with three entries, the **SizedADRLIST** macro can be used to create an **ADRLIST** structure to pass to **IAddrBook::ResolveName** with the correct number of **ADRENTRY** members.</span></span> <span data-ttu-id="b692c-117">Toutes les macros de mémoire sont définies dans le MAPIDEFS. Fichier d’en-tête H.</span><span class="sxs-lookup"><span data-stu-id="b692c-117">All of the memory macros are defined in the MAPIDEFS.H header file.</span></span> <span data-ttu-id="b692c-118">Ces macros sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="b692c-118">These macros are:</span></span> 
  
|||
|:-----|:-----|
|[<span data-ttu-id="b692c-119">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="b692c-119">SizedADRLIST</span></span>](sizedadrlist.md) <br/> |[<span data-ttu-id="b692c-120">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="b692c-120">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
|[<span data-ttu-id="b692c-121">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="b692c-121">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |[<span data-ttu-id="b692c-122">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="b692c-122">SizedENTRYID</span></span>](sizedentryid.md) <br/> |
|[<span data-ttu-id="b692c-123">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="b692c-123">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |[<span data-ttu-id="b692c-124">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="b692c-124">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
|[<span data-ttu-id="b692c-125">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="b692c-125">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |[<span data-ttu-id="b692c-126">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="b692c-126">SizedSPropTagArray</span></span>](sizedsproptagarray.md) <br/> |
|[<span data-ttu-id="b692c-127">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="b692c-127">SizedDtblEdit</span></span>](sizeddtbledit.md) <br/> |[<span data-ttu-id="b692c-128">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="b692c-128">SizedSRowSet</span></span>](sizedsrowset.md) <br/> |
|[<span data-ttu-id="b692c-129">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="b692c-129">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |[<span data-ttu-id="b692c-130">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="b692c-130">SizedSSortOrderSet</span></span>](sizedssortorderset.md) <br/> |
|[<span data-ttu-id="b692c-131">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="b692c-131">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> | <br/> |
   
<span data-ttu-id="b692c-132">MAPI prend également en charge l’utilisation de l’interface COM [IMalloc](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) pour la gestion de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="b692c-132">MAPI also supports the use of the COM interface [IMalloc](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) for memory management.</span></span> <span data-ttu-id="b692c-133">Fournisseurs de services figurent un pointeur d’interface **IMalloc** par MAPI lors de l’initialisation et peuvent également récupérer par le biais de la fonction [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) .</span><span class="sxs-lookup"><span data-stu-id="b692c-133">Service providers are given an **IMalloc** interface pointer by MAPI at initialization time and can also retrieve one through the [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) function.</span></span> <span data-ttu-id="b692c-134">Le principal avantage de l’utilisation des méthodes **IMalloc** pour la gestion de la mémoire sur les fonctions MAPI est qu’avec les méthodes COM, il est possible réattribuer un tampon existant.</span><span class="sxs-lookup"><span data-stu-id="b692c-134">The main advantage to using the **IMalloc** methods for managing memory over the MAPI functions is that with the COM methods it is possible to reallocate an existing buffer.</span></span> <span data-ttu-id="b692c-135">Les fonctions de mémoire MAPI ne prennent pas en charge réaffectation.</span><span class="sxs-lookup"><span data-stu-id="b692c-135">The MAPI memory functions do not support reallocation.</span></span> 
  

