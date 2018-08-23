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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 1c00e54d02ba494c94c9826eabe142e1bd3b9a80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579626"
---
# <a name="imsprovider--iunknown"></a><span data-ttu-id="22212-103">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="22212-103">IMSProvider : IUnknown</span></span>

  
  
<span data-ttu-id="22212-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22212-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22212-105">Permet d’accéder à un fournisseur de magasin de message via un objet de fournisseur de magasin de message.</span><span class="sxs-lookup"><span data-stu-id="22212-105">Provides access to a message store provider through a message store provider object.</span></span> <span data-ttu-id="22212-106">Cet objet de fournisseur de magasin de message est renvoyé à la connexion au fournisseur en fonction du point d’entrée [MSProviderInit](msproviderinit.md) du fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="22212-106">This message store provider object is returned at provider logon by the message store provider's [MSProviderInit](msproviderinit.md) entry point function.</span></span> <span data-ttu-id="22212-107">L’objet de fournisseur de banque de messages est principalement utilisé par les applications clientes et le spouleur MAPI pour ouvrir les banques de messages.</span><span class="sxs-lookup"><span data-stu-id="22212-107">The message store provider object is primarily used by client applications and the MAPI spooler to open message stores.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="22212-108">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="22212-108">Header file:</span></span>  <br/> |<span data-ttu-id="22212-109">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="22212-109">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="22212-110">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="22212-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="22212-111">Objets du fournisseur de banque de messages</span><span class="sxs-lookup"><span data-stu-id="22212-111">Message store provider objects</span></span>  <br/> |
|<span data-ttu-id="22212-112">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="22212-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="22212-113">Fournisseurs de banque de messages</span><span class="sxs-lookup"><span data-stu-id="22212-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="22212-114">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="22212-114">Called by:</span></span>  <br/> |<span data-ttu-id="22212-115">MAPI et le spouleur MAPI</span><span class="sxs-lookup"><span data-stu-id="22212-115">MAPI and the MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="22212-116">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="22212-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="22212-117">IID_IMSProvider</span><span class="sxs-lookup"><span data-stu-id="22212-117">IID_IMSProvider</span></span>  <br/> |
|<span data-ttu-id="22212-118">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="22212-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="22212-119">LPMSPROVIDER</span><span class="sxs-lookup"><span data-stu-id="22212-119">LPMSPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="22212-120">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="22212-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="22212-121">Arrêt</span><span class="sxs-lookup"><span data-stu-id="22212-121">Shutdown</span></span>](imsprovider-shutdown.md) <br/> |<span data-ttu-id="22212-122">Ferme un fournisseur de magasin de message de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="22212-122">Closes a message store provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="22212-123">Logon</span><span class="sxs-lookup"><span data-stu-id="22212-123">Logon</span></span>](imsprovider-logon.md) <br/> |<span data-ttu-id="22212-124">Journaux MAPI sur une instance d’un fournisseur de magasin de message.</span><span class="sxs-lookup"><span data-stu-id="22212-124">Logs MAPI on to one instance of a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="22212-125">SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="22212-125">SpoolerLogon</span></span>](imsprovider-spoolerlogon.md) <br/> |<span data-ttu-id="22212-126">Enregistre le spouleur MAPI sur une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="22212-126">Logs the MAPI spooler on to a message store.</span></span>  <br/> |
|[<span data-ttu-id="22212-127">CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="22212-127">CompareStoreIDs</span></span>](imsprovider-comparestoreids.md) <br/> |<span data-ttu-id="22212-128">Compare deux messages magasin identificateurs d’entrée pour déterminer si elles font référence au même objet store.</span><span class="sxs-lookup"><span data-stu-id="22212-128">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22212-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="22212-129">Remarks</span></span>

<span data-ttu-id="22212-130">MAPI utilise un objet de fournisseur de magasins de message par session, quel que soit le nombre de messages ouverts par le fournisseur de magasin de magasins.</span><span class="sxs-lookup"><span data-stu-id="22212-130">MAPI uses one message store provider object per session, no matter how many message stores are opened by the store provider.</span></span> <span data-ttu-id="22212-131">Si un deuxième MAPI session se connecte à tous les magasins, appels MAPI **MSProviderInit** une deuxième fois pour créer un nouvel objet de fournisseur de magasin de message pour cette session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="22212-131">If a second MAPI session logs on to any open stores, MAPI calls **MSProviderInit** a second time to create a new message store provider object for that session to use.</span></span> 
  
<span data-ttu-id="22212-132">Un objet de fournisseur de magasin de message doit contenir ce qui suit pour fonctionner correctement :</span><span class="sxs-lookup"><span data-stu-id="22212-132">A message store provider object must contain the following to operate correctly:</span></span>
  
- <span data-ttu-id="22212-133">_LpMalloc_ allocation de mémoire routine pointeur de pour une utilisation par tous les magasins ouvert à l’aide de l’objet de ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="22212-133">An  _lpMalloc_ memory-allocation routine pointer for use by all stores opened by using this provider object.</span></span> 
    
- <span data-ttu-id="22212-134">Le _lpfAllocateBuffer_, _ lpfAllocateMore _, ainsi que des pointeurs routine _lpfFreeBuffer_ pour les fonctions d’allocation de mémoire [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)et [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="22212-134">The  _lpfAllocateBuffer_,  _ lpfAllocateMore _, and  _lpfFreeBuffer_ routine pointers to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) memory allocation functions.</span></span> 
    
- <span data-ttu-id="22212-135">Une liste de toutes les banques liée ouvert à l’aide de cet objet de fournisseur et n’est pas encore fermé.</span><span class="sxs-lookup"><span data-stu-id="22212-135">A linked list of all the stores opened by using this provider object and not yet closed.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="22212-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22212-136">See also</span></span>



[<span data-ttu-id="22212-137">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="22212-137">MAPI Interfaces</span></span>](mapi-interfaces.md)

