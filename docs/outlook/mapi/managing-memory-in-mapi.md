---
title: Gestion de la mémoire dans MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9eee6925-ab91-413e-8907-c747ab4a4bb5
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 66489c09be641d8fe9ae5f3ffff46a6d5004f473
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298095"
---
# <a name="managing-memory-in-mapi"></a><span data-ttu-id="6bae5-103">Gestion de la mémoire dans MAPI</span><span class="sxs-lookup"><span data-stu-id="6bae5-103">Managing Memory in MAPI</span></span>

  
  
<span data-ttu-id="6bae5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6bae5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6bae5-105">Savoir comment et quand allouer et libérer de la mémoire est une partie importante de la programmation avec MAPI.</span><span class="sxs-lookup"><span data-stu-id="6bae5-105">Knowing how and when to allocate and free memory is an important part of programming with MAPI.</span></span> <span data-ttu-id="6bae5-106">MAPI fournit à la fois des fonctions et des macros que votre client ou fournisseur de services peut utiliser pour gérer la mémoire de manière cohérente.</span><span class="sxs-lookup"><span data-stu-id="6bae5-106">MAPI provides both functions and macros that your client or service provider can use to manage memory in a consistent way.</span></span> <span data-ttu-id="6bae5-107">Les trois fonctions sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="6bae5-107">The three functions are as follows:</span></span>
  
[<span data-ttu-id="6bae5-108">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="6bae5-108">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="6bae5-109">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="6bae5-109">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="6bae5-110">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="6bae5-110">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
<span data-ttu-id="6bae5-111">Lorsque les clients et les fournisseurs de services utilisent ces fonctions, le «propriétaire» (c'est-à-dire, dont il est question) sait comment lancer un bloc de mémoire particulier.</span><span class="sxs-lookup"><span data-stu-id="6bae5-111">When clients and service providers use these functions, the issue of who "owns" — that is, knows how to release — a particular block of memory is eliminated.</span></span> <span data-ttu-id="6bae5-112">Un client appelant une méthode de fournisseur de services n'a pas besoin de transmettre un tampon assez grand pour contenir une valeur de retour de n'importe quelle taille.</span><span class="sxs-lookup"><span data-stu-id="6bae5-112">A client calling a service provider method need not pass a buffer large enough to hold a return value of any size.</span></span> <span data-ttu-id="6bae5-113">Le fournisseur de services peut simplement allouer la quantité de mémoire appropriée à l'aide de **MAPIAllocateBuffer** et, si nécessaire, **MAPIAllocateMore**, et le client peut le libérer ultérieurement à l'aide de **MAPIFreeBuffer**, indépendamment du service moteur.</span><span class="sxs-lookup"><span data-stu-id="6bae5-113">The service provider can simply allocate the appropriate amount of memory using **MAPIAllocateBuffer** and, if necessary, **MAPIAllocateMore**, and the client can later release it at will using **MAPIFreeBuffer**, independent of the service provider.</span></span> 
  
<span data-ttu-id="6bae5-114">Les macros de mémoire sont utilisées pour allouer des structures ou des tableaux de structures d'une taille spécifique.</span><span class="sxs-lookup"><span data-stu-id="6bae5-114">The memory macros are used to allocate structures or arrays of structures of a specific size.</span></span> <span data-ttu-id="6bae5-115">Les clients et les fournisseurs de services doivent utiliser ces macros au lieu d'allouer manuellement la mémoire.</span><span class="sxs-lookup"><span data-stu-id="6bae5-115">Clients and service providers should use these macros rather than allocate the memory manually.</span></span> <span data-ttu-id="6bae5-116">Par exemple, si un client doit exécuter le traitement de la résolution de noms sur une liste de destinataires avec trois entrées, la macro **SizedADRLIST** peut être utilisée pour créer une structure **ADRLIST** à transmettre à **IAddrBook:: ResolveName** avec le nombre correct de Membres **ADRENTRY** .</span><span class="sxs-lookup"><span data-stu-id="6bae5-116">For example, if a client needs to perform name resolution processing on a recipient list with three entries, the **SizedADRLIST** macro can be used to create an **ADRLIST** structure to pass to **IAddrBook::ResolveName** with the correct number of **ADRENTRY** members.</span></span> <span data-ttu-id="6bae5-117">Toutes les macros de mémoire sont définies dans le MAPIDEFS. Fichier d'en-tête H.</span><span class="sxs-lookup"><span data-stu-id="6bae5-117">All of the memory macros are defined in the MAPIDEFS.H header file.</span></span> <span data-ttu-id="6bae5-118">Ces macros sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="6bae5-118">These macros are:</span></span> 
  
|||
|:-----|:-----|
|[<span data-ttu-id="6bae5-119">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="6bae5-119">SizedADRLIST</span></span>](sizedadrlist.md) <br/> |[<span data-ttu-id="6bae5-120">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="6bae5-120">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
|[<span data-ttu-id="6bae5-121">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="6bae5-121">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |[<span data-ttu-id="6bae5-122">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="6bae5-122">SizedENTRYID</span></span>](sizedentryid.md) <br/> |
|[<span data-ttu-id="6bae5-123">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="6bae5-123">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |[<span data-ttu-id="6bae5-124">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="6bae5-124">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
|[<span data-ttu-id="6bae5-125">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="6bae5-125">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |[<span data-ttu-id="6bae5-126">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="6bae5-126">SizedSPropTagArray</span></span>](sizedsproptagarray.md) <br/> |
|[<span data-ttu-id="6bae5-127">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="6bae5-127">SizedDtblEdit</span></span>](sizeddtbledit.md) <br/> |[<span data-ttu-id="6bae5-128">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="6bae5-128">SizedSRowSet</span></span>](sizedsrowset.md) <br/> |
|[<span data-ttu-id="6bae5-129">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="6bae5-129">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |[<span data-ttu-id="6bae5-130">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="6bae5-130">SizedSSortOrderSet</span></span>](sizedssortorderset.md) <br/> |
|[<span data-ttu-id="6bae5-131">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="6bae5-131">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> | <br/> |
   
<span data-ttu-id="6bae5-132">MAPI prend également en charge l'utilisation de l' [](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) interface com IMalloc pour la gestion de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="6bae5-132">MAPI also supports the use of the COM interface [IMalloc](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) for memory management.</span></span> <span data-ttu-id="6bae5-133">Les fournisseurs de services reçoivent \*\*\*\* un pointeur d'interface IMalloc par MAPI au moment de l'initialisation et peuvent également en récupérer un par le biais de la fonction [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) .</span><span class="sxs-lookup"><span data-stu-id="6bae5-133">Service providers are given an **IMalloc** interface pointer by MAPI at initialization time and can also retrieve one through the [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) function.</span></span> <span data-ttu-id="6bae5-134">Le principal avantage de l'utilisation \*\*\*\* des méthodes IMalloc pour la gestion de la mémoire sur les fonctions MAPI est qu'avec les méthodes com, il est possible de réaffecter une mémoire tampon existante.</span><span class="sxs-lookup"><span data-stu-id="6bae5-134">The main advantage to using the **IMalloc** methods for managing memory over the MAPI functions is that with the COM methods it is possible to reallocate an existing buffer.</span></span> <span data-ttu-id="6bae5-135">Les fonctions de mémoire MAPI ne prennent pas en charge la réallocation.</span><span class="sxs-lookup"><span data-stu-id="6bae5-135">The MAPI memory functions do not support reallocation.</span></span> 
  

