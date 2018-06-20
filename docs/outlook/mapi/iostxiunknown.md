---
title: IOSTX IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX
api_type:
- COM
ms.assetid: f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7419a0df7a2f3b76caeeb1ca564624d437eddd52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784358"
---
# <a name="iostx--iunknown"></a><span data-ttu-id="e7400-103">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e7400-103">IOSTX : IUnknown</span></span>

  
  
<span data-ttu-id="e7400-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e7400-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e7400-105">Fournit des méthodes de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="e7400-105">Provides synchronization methods.</span></span> <span data-ttu-id="e7400-106">Cette interface récupère les informations nécessaires pour répliquer les modifications locales vers le serveur et les modifications de serveur dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="e7400-106">This interface retrieves the necessary information to replicate local changes to the server and server changes to the local store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e7400-107">Fourni par :</span><span class="sxs-lookup"><span data-stu-id="e7400-107">Provided by:</span></span>  <br/> |[<span data-ttu-id="e7400-108">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="e7400-108">IPSTX::GetSyncObject</span></span>](iostx-setsyncresult.md) <br/> |
|<span data-ttu-id="e7400-109">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="e7400-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e7400-110">IID_IOSTX</span><span class="sxs-lookup"><span data-stu-id="e7400-110">IID_IOSTX</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e7400-111">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="e7400-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e7400-112">GetLastError</span><span class="sxs-lookup"><span data-stu-id="e7400-112">GetLastError</span></span>](iostx-getlasterror.md) <br/> |<span data-ttu-id="e7400-113">Obtient des informations sur la dernière erreur étendues.</span><span class="sxs-lookup"><span data-stu-id="e7400-113">Gets extended information about the last error.</span></span>  <br/> |
|[<span data-ttu-id="e7400-114">InitSync</span><span class="sxs-lookup"><span data-stu-id="e7400-114">InitSync</span></span>](iostx-initsync.md) <br/> |<span data-ttu-id="e7400-115">Indique le magasin local que la synchronisation est prêt à démarrer.</span><span class="sxs-lookup"><span data-stu-id="e7400-115">Informs the local store that synchronization is about to start.</span></span>  <br/> |
|[<span data-ttu-id="e7400-116">SyncBeg</span><span class="sxs-lookup"><span data-stu-id="e7400-116">SyncBeg</span></span>](iostx-syncbeg.md) <br/> |<span data-ttu-id="e7400-117">Prépare le magasin local de la synchronisation dans un état particulier et récupère les informations nécessaires pour répliquer.</span><span class="sxs-lookup"><span data-stu-id="e7400-117">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>  <br/> |
|[<span data-ttu-id="e7400-118">Processus</span><span class="sxs-lookup"><span data-stu-id="e7400-118">SyncEnd</span></span>](iostx-syncend.md) <br/> |<span data-ttu-id="e7400-119">Met fin à la synchronisation dans l’état actuel et quitte cet état.</span><span class="sxs-lookup"><span data-stu-id="e7400-119">Ends synchronization in the current state and exits that state.</span></span>  <br/> |
|[<span data-ttu-id="e7400-120">SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="e7400-120">SyncHdrBeg</span></span>](iostx-synchdrbeg.md) <br/> |<span data-ttu-id="e7400-121">Démarre la synchronisation pour un en-tête de message.</span><span class="sxs-lookup"><span data-stu-id="e7400-121">Starts synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="e7400-122">SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="e7400-122">SyncHdrEnd</span></span>](iostx-synchdrend.md) <br/> |<span data-ttu-id="e7400-123">Fin de la synchronisation pour un en-tête de message.</span><span class="sxs-lookup"><span data-stu-id="e7400-123">Ends synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="e7400-124">SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="e7400-124">SetSyncResult</span></span>](iostx-setsyncresult.md) <br/> |<span data-ttu-id="e7400-125">Définit le résultat de la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="e7400-125">Sets the result of the synchronization.</span></span>  <br/> |
| <span data-ttu-id="e7400-126">*Membres de l’espace réservé*</span><span class="sxs-lookup"><span data-stu-id="e7400-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e7400-127">*Non pris en charge ou documentés.*</span><span class="sxs-lookup"><span data-stu-id="e7400-127">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7400-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="e7400-128">Remarks</span></span>

<span data-ttu-id="e7400-129">Lorsqu’un client télécharge ou synchronise les dossiers et le contenu du dossier sur un magasin local, il déplace le magasin local d’un état à l’autre comme illustré dans le diagramme de transition d’état de [L’ordinateur d’état de réplication](about-the-replication-state-machine.md).</span><span class="sxs-lookup"><span data-stu-id="e7400-129">When a client uploads or synchronizes folders and folder contents on a local store, it moves the local store from one state to another as depicted in the state transition diagram in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="e7400-130">Voici l’ordre des événements pour le client déplacer le magasin local d’un état à un autre :</span><span class="sxs-lookup"><span data-stu-id="e7400-130">The following is the order of events for the client to move the local store from one state to another:</span></span>
  
1. <span data-ttu-id="e7400-131">Le client appelle **IOSTX::InitSync** pour informer le magasin local que la réplication est prêt à démarrer.</span><span class="sxs-lookup"><span data-stu-id="e7400-131">The client calls **IOSTX::InitSync** to inform the local store that replication is about to start.</span></span> 
    
2. <span data-ttu-id="e7400-132">En fonction de la direction de la réplication et les objets à répliquer, le client appelle **IOSTX::SyncBeg** pour commencer la réplication dans l’état approprié.</span><span class="sxs-lookup"><span data-stu-id="e7400-132">Depending on the direction of replication and the objects to replicate, the client calls **IOSTX::SyncBeg** to begin replication in the appropriate state.</span></span> <span data-ttu-id="e7400-133">Outlook fournit au client les informations nécessaires, et le client effectue la réplication.</span><span class="sxs-lookup"><span data-stu-id="e7400-133">Outlook provides the client the necessary information, and the client performs the replication.</span></span> 
    
3. <span data-ttu-id="e7400-134">Le client appelle **IOSTX::SetSyncResult** pour renvoyer le résultat de la réplication.</span><span class="sxs-lookup"><span data-stu-id="e7400-134">The client calls **IOSTX::SetSyncResult** to return the result of the replication.</span></span> 
    
4. <span data-ttu-id="e7400-135">Le client appelle **IOSTX::SyncEnd** pour mettre fin à la réplication, fournissant Outlook les informations nécessaires pour la réplication suivante.</span><span class="sxs-lookup"><span data-stu-id="e7400-135">The client calls **IOSTX::SyncEnd** to end the replication, providing Outlook the necessary information for subsequent replication.</span></span> 
    
<span data-ttu-id="e7400-136">En particulier, lors du téléchargement des éléments de message, le client utilise **IOSTX::SyncHdrBeg** et **IOSTX::SyncHdrEnd** pour mettre à jour un élément de message complète avec l’en-tête du message dans la banque locale :</span><span class="sxs-lookup"><span data-stu-id="e7400-136">In particular, when downloading message items, the client uses **IOSTX::SyncHdrBeg** and **IOSTX::SyncHdrEnd** to update a full message item with the message header on the local store:</span></span> 
  
1. <span data-ttu-id="e7400-137">Fonction **IOSTX::SyncHdrBeg**, local stocker les transitions dans l’état d’en-tête de message téléchargement.</span><span class="sxs-lookup"><span data-stu-id="e7400-137">Upon **IOSTX::SyncHdrBeg**, the local store transitions into the download message header state.</span></span> <span data-ttu-id="e7400-138">Outlook fournit à l’origine du client avec l’en-tête du message en cours dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="e7400-138">Outlook initially provides the client with the current message header on the local store.</span></span>
    
2. <span data-ttu-id="e7400-139">Le client télécharge un élément de message complet ainsi que l’en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="e7400-139">The client downloads a full message item together with the message header.</span></span>
    
3. <span data-ttu-id="e7400-140">Outlook met à jour l’élément dans le magasin local avec l’élément de message complet.</span><span class="sxs-lookup"><span data-stu-id="e7400-140">Outlook updates the item on the local store with the full message item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e7400-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7400-141">See also</span></span>



[<span data-ttu-id="e7400-142">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="e7400-142">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="e7400-143">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="e7400-143">MAPI Constants</span></span>](mapi-constants.md)

