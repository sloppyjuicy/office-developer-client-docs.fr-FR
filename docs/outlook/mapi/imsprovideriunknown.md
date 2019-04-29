---
title: IMSProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider
api_type:
- COM
ms.assetid: 0f17aa44-abcb-4732-b013-d91652847cf6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c5305ddd20b690f5c2e5807fb7ce2410549f7124
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412862"
---
# <a name="imsprovider--iunknown"></a><span data-ttu-id="bc5d4-103">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bc5d4-103">IMSProvider : IUnknown</span></span>

  
  
<span data-ttu-id="bc5d4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc5d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc5d4-105">Permet d'accéder à un fournisseur de banque de messages par le biais d'un objet fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="bc5d4-105">Provides access to a message store provider through a message store provider object.</span></span> <span data-ttu-id="bc5d4-106">Cet objet fournisseur de banque de messages est renvoyé lors de l'ouverture de session du fournisseur par la fonction de point d'entrée [MSProviderInit](msproviderinit.md) du fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="bc5d4-106">This message store provider object is returned at provider logon by the message store provider's [MSProviderInit](msproviderinit.md) entry point function.</span></span> <span data-ttu-id="bc5d4-107">L'objet fournisseur de banque de messages est principalement utilisé par les applications clientes et le spouleur MAPI pour ouvrir les banques de messages.</span><span class="sxs-lookup"><span data-stu-id="bc5d4-107">The message store provider object is primarily used by client applications and the MAPI spooler to open message stores.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc5d4-108">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="bc5d4-108">Header file:</span></span>  <br/> |<span data-ttu-id="bc5d4-109">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="bc5d4-109">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="bc5d4-110">Exposé par:</span><span class="sxs-lookup"><span data-stu-id="bc5d4-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="bc5d4-111">Objets du fournisseur de banques de messages</span><span class="sxs-lookup"><span data-stu-id="bc5d4-111">Message store provider objects</span></span>  <br/> |
|<span data-ttu-id="bc5d4-112">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="bc5d4-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="bc5d4-113">Fournisseurs de banques de messages</span><span class="sxs-lookup"><span data-stu-id="bc5d4-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="bc5d4-114">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="bc5d4-114">Called by:</span></span>  <br/> |<span data-ttu-id="bc5d4-115">MAPI et spouleur MAPI</span><span class="sxs-lookup"><span data-stu-id="bc5d4-115">MAPI and the MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="bc5d4-116">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="bc5d4-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="bc5d4-117">IID_IMSProvider</span><span class="sxs-lookup"><span data-stu-id="bc5d4-117">IID_IMSProvider</span></span>  <br/> |
|<span data-ttu-id="bc5d4-118">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="bc5d4-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="bc5d4-119">LPMSPROVIDER</span><span class="sxs-lookup"><span data-stu-id="bc5d4-119">LPMSPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="bc5d4-120">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="bc5d4-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="bc5d4-121">Arrêt</span><span class="sxs-lookup"><span data-stu-id="bc5d4-121">Shutdown</span></span>](imsprovider-shutdown.md) <br/> |<span data-ttu-id="bc5d4-122">Ferme un fournisseur de banque de messages de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="bc5d4-122">Closes a message store provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="bc5d4-123">Logon</span><span class="sxs-lookup"><span data-stu-id="bc5d4-123">Logon</span></span>](imsprovider-logon.md) <br/> |<span data-ttu-id="bc5d4-124">Journalise MAPI sur une instance d'un fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="bc5d4-124">Logs MAPI on to one instance of a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="bc5d4-125">SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="bc5d4-125">SpoolerLogon</span></span>](imsprovider-spoolerlogon.md) <br/> |<span data-ttu-id="bc5d4-126">Enregistre le spouleur MAPI sur une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="bc5d4-126">Logs the MAPI spooler on to a message store.</span></span>  <br/> |
|[<span data-ttu-id="bc5d4-127">CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="bc5d4-127">CompareStoreIDs</span></span>](imsprovider-comparestoreids.md) <br/> |<span data-ttu-id="bc5d4-128">Compare deux identificateurs d'entrée de banque de messages pour déterminer s'ils font référence au même objet Store.</span><span class="sxs-lookup"><span data-stu-id="bc5d4-128">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc5d4-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="bc5d4-129">Remarks</span></span>

<span data-ttu-id="bc5d4-130">MAPI utilise un seul objet fournisseur de banque de messages par session, quel que soit le nombre de banques de messages ouvertes par le fournisseur de banque d'informations.</span><span class="sxs-lookup"><span data-stu-id="bc5d4-130">MAPI uses one message store provider object per session, no matter how many message stores are opened by the store provider.</span></span> <span data-ttu-id="bc5d4-131">Si une deuxième session MAPI se connecte à des magasins ouverts, MAPI appelle **MSProviderInit** une deuxième fois pour créer un nouvel objet fournisseur de banque de messages pour cette session.</span><span class="sxs-lookup"><span data-stu-id="bc5d4-131">If a second MAPI session logs on to any open stores, MAPI calls **MSProviderInit** a second time to create a new message store provider object for that session to use.</span></span> 
  
<span data-ttu-id="bc5d4-132">Pour fonctionner correctement, un objet fournisseur de banque de messages doit contenir les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="bc5d4-132">A message store provider object must contain the following to operate correctly:</span></span>
  
- <span data-ttu-id="bc5d4-133">Pointeur de routine d'allocation de mémoire _lpMalloc_ pour une utilisation par tous les magasins ouverts à l'aide de cet objet fournisseur.</span><span class="sxs-lookup"><span data-stu-id="bc5d4-133">An  _lpMalloc_ memory-allocation routine pointer for use by all stores opened by using this provider object.</span></span> 
    
- <span data-ttu-id="bc5d4-134">Les pointeurs de routine _lpfAllocateBuffer_, _ lpfAllocateMore _ et _lpfFreeBuffer_ vers les fonctions d'allocation de mémoire [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)et [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="bc5d4-134">The  _lpfAllocateBuffer_,  _ lpfAllocateMore _, and  _lpfFreeBuffer_ routine pointers to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) memory allocation functions.</span></span> 
    
- <span data-ttu-id="bc5d4-135">Liste liée de tous les magasins ouverts à l'aide de cet objet fournisseur et non encore fermés.</span><span class="sxs-lookup"><span data-stu-id="bc5d4-135">A linked list of all the stores opened by using this provider object and not yet closed.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bc5d4-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc5d4-136">See also</span></span>



[<span data-ttu-id="bc5d4-137">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="bc5d4-137">MAPI Interfaces</span></span>](mapi-interfaces.md)

