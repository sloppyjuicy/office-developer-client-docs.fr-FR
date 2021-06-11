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
# <a name="imsprovider--iunknown"></a><span data-ttu-id="2d1e6-103">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2d1e6-103">IMSProvider : IUnknown</span></span>

  
  
<span data-ttu-id="2d1e6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d1e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d1e6-105">Permet d’accéder à un fournisseur de magasins de messages via un objet fournisseur de magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="2d1e6-105">Provides access to a message store provider through a message store provider object.</span></span> <span data-ttu-id="2d1e6-106">Cet objet fournisseur de magasin de messages est renvoyé lors de l’ouverture de connecté du fournisseur par la fonction de point d’entrée [MSProviderInit](msproviderinit.md) du fournisseur de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="2d1e6-106">This message store provider object is returned at provider logon by the message store provider's [MSProviderInit](msproviderinit.md) entry point function.</span></span> <span data-ttu-id="2d1e6-107">L’objet fournisseur de magasin de messages est principalement utilisé par les applications clientes et lepooler MAPI pour ouvrir les magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="2d1e6-107">The message store provider object is primarily used by client applications and the MAPI spooler to open message stores.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2d1e6-108">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="2d1e6-108">Header file:</span></span>  <br/> |<span data-ttu-id="2d1e6-109">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="2d1e6-109">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="2d1e6-110">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="2d1e6-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="2d1e6-111">Objets du fournisseur de banques de messages</span><span class="sxs-lookup"><span data-stu-id="2d1e6-111">Message store provider objects</span></span>  <br/> |
|<span data-ttu-id="2d1e6-112">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="2d1e6-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="2d1e6-113">Fournisseurs de magasins de messages</span><span class="sxs-lookup"><span data-stu-id="2d1e6-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="2d1e6-114">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="2d1e6-114">Called by:</span></span>  <br/> |<span data-ttu-id="2d1e6-115">MAPI et lepooler MAPI</span><span class="sxs-lookup"><span data-stu-id="2d1e6-115">MAPI and the MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="2d1e6-116">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="2d1e6-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2d1e6-117">IID_IMSProvider</span><span class="sxs-lookup"><span data-stu-id="2d1e6-117">IID_IMSProvider</span></span>  <br/> |
|<span data-ttu-id="2d1e6-118">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="2d1e6-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="2d1e6-119">LPMSPROVIDER</span><span class="sxs-lookup"><span data-stu-id="2d1e6-119">LPMSPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2d1e6-120">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="2d1e6-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2d1e6-121">Arrêt</span><span class="sxs-lookup"><span data-stu-id="2d1e6-121">Shutdown</span></span>](imsprovider-shutdown.md) <br/> |<span data-ttu-id="2d1e6-122">Ferme un fournisseur de magasins de messages de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="2d1e6-122">Closes a message store provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="2d1e6-123">Logon</span><span class="sxs-lookup"><span data-stu-id="2d1e6-123">Logon</span></span>](imsprovider-logon.md) <br/> |<span data-ttu-id="2d1e6-124">Connecte MAPI à une instance d’un fournisseur de magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="2d1e6-124">Logs MAPI on to one instance of a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="2d1e6-125">SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="2d1e6-125">SpoolerLogon</span></span>](imsprovider-spoolerlogon.md) <br/> |<span data-ttu-id="2d1e6-126">Connecte lepooler MAPI à une boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="2d1e6-126">Logs the MAPI spooler on to a message store.</span></span>  <br/> |
|[<span data-ttu-id="2d1e6-127">CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="2d1e6-127">CompareStoreIDs</span></span>](imsprovider-comparestoreids.md) <br/> |<span data-ttu-id="2d1e6-128">Compare deux identificateurs d’entrée de magasin de messages pour déterminer s’ils font référence au même objet store.</span><span class="sxs-lookup"><span data-stu-id="2d1e6-128">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2d1e6-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="2d1e6-129">Remarks</span></span>

<span data-ttu-id="2d1e6-130">MAPI utilise un objet fournisseur de magasin de messages par session, quel que soit le nombre de magasins de messages ouverts par le fournisseur de la boutique.</span><span class="sxs-lookup"><span data-stu-id="2d1e6-130">MAPI uses one message store provider object per session, no matter how many message stores are opened by the store provider.</span></span> <span data-ttu-id="2d1e6-131">Si une deuxième session MAPI se connecte à des magasins ouverts, MAPI appelle **MSProviderInit** une deuxième fois pour créer un objet fournisseur de magasin de messages à utiliser pour cette session.</span><span class="sxs-lookup"><span data-stu-id="2d1e6-131">If a second MAPI session logs on to any open stores, MAPI calls **MSProviderInit** a second time to create a new message store provider object for that session to use.</span></span> 
  
<span data-ttu-id="2d1e6-132">Un objet fournisseur de magasin de messages doit contenir les éléments suivants pour fonctionner correctement :</span><span class="sxs-lookup"><span data-stu-id="2d1e6-132">A message store provider object must contain the following to operate correctly:</span></span>
  
- <span data-ttu-id="2d1e6-133">Pointeur de routine d’allocation de mémoire  _lpMalloc_ à utiliser par tous les magasins ouverts à l’aide de cet objet fournisseur.</span><span class="sxs-lookup"><span data-stu-id="2d1e6-133">An  _lpMalloc_ memory-allocation routine pointer for use by all stores opened by using this provider object.</span></span> 
    
- <span data-ttu-id="2d1e6-134">Les pointeurs de routine _lpfAllocateBuffer_, _ lpfAllocateMore _, et _lpfFreeBuffer_ pointent vers les fonctions d’allocation de mémoire [MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)et [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="2d1e6-134">The  _lpfAllocateBuffer_,  _ lpfAllocateMore _, and  _lpfFreeBuffer_ routine pointers to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) memory allocation functions.</span></span> 
    
- <span data-ttu-id="2d1e6-135">Liste liée de toutes les magasins ouvertes à l’aide de cet objet fournisseur et pas encore fermées.</span><span class="sxs-lookup"><span data-stu-id="2d1e6-135">A linked list of all the stores opened by using this provider object and not yet closed.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2d1e6-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d1e6-136">See also</span></span>



[<span data-ttu-id="2d1e6-137">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="2d1e6-137">MAPI Interfaces</span></span>](mapi-interfaces.md)

