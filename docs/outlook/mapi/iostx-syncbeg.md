---
title: IOSTXSyncBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncBeg
api_type:
- COM
ms.assetid: 4a935df3-98c4-2742-206e-4e16eda7b9bc
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ae4497295328155780fc5208d1699169698e02d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411938"
---
# <a name="iostxsyncbeg"></a><span data-ttu-id="af8e1-103">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="af8e1-103">IOSTX::SyncBeg</span></span>

  
  
<span data-ttu-id="af8e1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af8e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af8e1-105">Prépare le magasin local pour la synchronisation dans un état particulier et récupère les informations nécessaires à répliquer.</span><span class="sxs-lookup"><span data-stu-id="af8e1-105">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a><span data-ttu-id="af8e1-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="af8e1-106">Parameters</span></span>

 <span data-ttu-id="af8e1-107">_uiSync_</span><span class="sxs-lookup"><span data-stu-id="af8e1-107">_uiSync_</span></span>
  
>  <span data-ttu-id="af8e1-108">[in] État entré par le magasin local.</span><span class="sxs-lookup"><span data-stu-id="af8e1-108">[in] The state that the local store will enter.</span></span> <span data-ttu-id="af8e1-109">Voici une liste des identifateurs d’état :</span><span class="sxs-lookup"><span data-stu-id="af8e1-109">The following is a list of state identifers:</span></span> 
    
<span data-ttu-id="af8e1-110">LR_SYNC_IDLE</span><span class="sxs-lookup"><span data-stu-id="af8e1-110">LR_SYNC_IDLE</span></span>
  
> 
    
<span data-ttu-id="af8e1-111">LR_SYNC</span><span class="sxs-lookup"><span data-stu-id="af8e1-111">LR_SYNC</span></span>
  
> 
    
<span data-ttu-id="af8e1-112">LR_SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="af8e1-112">LR_SYNC_UPLOAD_HIERARCHY</span></span>
  
> 
    
<span data-ttu-id="af8e1-113">LR_SYNC_UPLOAD_FOLDER</span><span class="sxs-lookup"><span data-stu-id="af8e1-113">LR_SYNC_UPLOAD_FOLDER</span></span>
  
> 
    
<span data-ttu-id="af8e1-114">LR_SYNC_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="af8e1-114">LR_SYNC_CONTENTS</span></span>
  
> 
    
<span data-ttu-id="af8e1-115">LR_SYNC_UPLOAD_TABLE</span><span class="sxs-lookup"><span data-stu-id="af8e1-115">LR_SYNC_UPLOAD_TABLE</span></span>
  
> 
    
<span data-ttu-id="af8e1-116">LR_SYNC_UPLOAD_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="af8e1-116">LR_SYNC_UPLOAD_MESSAGE</span></span>
  
> 
    
<span data-ttu-id="af8e1-117">LR_SYNC_UPLOAD_MESSAGE_READ</span><span class="sxs-lookup"><span data-stu-id="af8e1-117">LR_SYNC_UPLOAD_MESSAGE_READ</span></span>
  
> 
    
<span data-ttu-id="af8e1-118">LR_SYNC_UPLOAD_MESSAGE_DEL</span><span class="sxs-lookup"><span data-stu-id="af8e1-118">LR_SYNC_UPLOAD_MESSAGE_DEL</span></span>
  
> 
    
<span data-ttu-id="af8e1-119">LR_SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="af8e1-119">LR_SYNC_DOWNLOAD_HIERARCHY</span></span>
  
> 
    
<span data-ttu-id="af8e1-120">LR_SYNC_DOWNLOAD_TABLE</span><span class="sxs-lookup"><span data-stu-id="af8e1-120">LR_SYNC_DOWNLOAD_TABLE</span></span>
  
> 
    
 <span data-ttu-id="af8e1-121">_ppv_</span><span class="sxs-lookup"><span data-stu-id="af8e1-121">_ppv_</span></span>
  
>  <span data-ttu-id="af8e1-122">[in]/[out] Pointeur vers la structure de données correspondant à l’état à entrer.</span><span class="sxs-lookup"><span data-stu-id="af8e1-122">[in]/[out] Pointer to the data structure corresponding to the state to enter.</span></span> 
    
[<span data-ttu-id="af8e1-123">DNHIER</span><span class="sxs-lookup"><span data-stu-id="af8e1-123">DNHIER</span></span>](dnhier.md)
  
> 
    
[<span data-ttu-id="af8e1-124">DNTBL</span><span class="sxs-lookup"><span data-stu-id="af8e1-124">DNTBL</span></span>](dntbl.md)
  
> 
    
[<span data-ttu-id="af8e1-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="af8e1-125">DNTBL</span></span>](dntbl.md)
  
> 
    
[<span data-ttu-id="af8e1-126">SYNC</span><span class="sxs-lookup"><span data-stu-id="af8e1-126">SYNC</span></span>](sync.md)
  
> 
    
[<span data-ttu-id="af8e1-127">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="af8e1-127">SYNCCONT</span></span>](synccont.md)
  
> 
    
[<span data-ttu-id="af8e1-128">UPDEL</span><span class="sxs-lookup"><span data-stu-id="af8e1-128">UPDEL</span></span>](updel.md)
  
> 
    
[<span data-ttu-id="af8e1-129">UPDELE</span><span class="sxs-lookup"><span data-stu-id="af8e1-129">UPDELE</span></span>](updele.md)
  
> 
    
[<span data-ttu-id="af8e1-130">UPFLD</span><span class="sxs-lookup"><span data-stu-id="af8e1-130">UPFLD</span></span>](upfld.md)
  
> 
    
[<span data-ttu-id="af8e1-131">UPHIER</span><span class="sxs-lookup"><span data-stu-id="af8e1-131">UPHIER</span></span>](uphier.md)
  
> 
    
[<span data-ttu-id="af8e1-132">UPMOV</span><span class="sxs-lookup"><span data-stu-id="af8e1-132">UPMOV</span></span>](upmov.md)
  
> 
    
[<span data-ttu-id="af8e1-133">UPMSG</span><span class="sxs-lookup"><span data-stu-id="af8e1-133">UPMSG</span></span>](upmsg.md)
  
> 
    
[<span data-ttu-id="af8e1-134">UPREAD</span><span class="sxs-lookup"><span data-stu-id="af8e1-134">UPREAD</span></span>](upread.md)
  
> 
    
[<span data-ttu-id="af8e1-135">UPREADE</span><span class="sxs-lookup"><span data-stu-id="af8e1-135">UPREADE</span></span>](upreade.md)
  
> 
    
[<span data-ttu-id="af8e1-136">UPTBL</span><span class="sxs-lookup"><span data-stu-id="af8e1-136">UPTBL</span></span>](uptbl.md)
  
> 
    
[<span data-ttu-id="af8e1-137">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="af8e1-137">UPTBLE</span></span>](uptble.md)
  
> 
    
## <a name="remarks"></a><span data-ttu-id="af8e1-138">Remarques</span><span class="sxs-lookup"><span data-stu-id="af8e1-138">Remarks</span></span>

<span data-ttu-id="af8e1-139">Le client appelle **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** pour définir le résultat de la synchronisation, puis appelle **[IOSTX::SyncEnd](iostx-syncend.md)** pour mettre fin à cet état.</span><span class="sxs-lookup"><span data-stu-id="af8e1-139">The client calls **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** to set the result of the synchronization, and then calls **[IOSTX::SyncEnd](iostx-syncend.md)** to end that state.</span></span> <span data-ttu-id="af8e1-140">Le client doit appeler **[IOSTX::SyncEnd](iostx-syncend.md)** pour chaque appel à **IOSTX::SyncBeg** afin de déterminer si l’état a été répliqué avec succès.</span><span class="sxs-lookup"><span data-stu-id="af8e1-140">The client must call **[IOSTX::SyncEnd](iostx-syncend.md)** for each call to **IOSTX::SyncBeg** in order to determine whether the state has been successfully replicated.</span></span> <span data-ttu-id="af8e1-141">Une fois cela déterminé, Outlook pouvez commencer à nettoyer son état interne.</span><span class="sxs-lookup"><span data-stu-id="af8e1-141">Once this has been determined, Outlook can begin to clean up its internal state.</span></span> 
  
<span data-ttu-id="af8e1-142">La plupart de ces structures contiennent des informations [out]/[in], ce qui permet aux Outlook de transmettre des informations au client et au client de transmettre des informations à Outlook.</span><span class="sxs-lookup"><span data-stu-id="af8e1-142">Most of these structures contain [out]/[in] information, allowing Outlook to pass information to the client, and the client to pass information to Outlook.</span></span> <span data-ttu-id="af8e1-143">Lorsque le client appelle **IOSTX::SyncBeg**, Outlook alloue la structure de données pour un état donné et l’initialise avec des informations pour cet état.</span><span class="sxs-lookup"><span data-stu-id="af8e1-143">When the client calls **IOSTX::SyncBeg**, Outlook allocates the data structure for a given state and initializes it with information for that state.</span></span> <span data-ttu-id="af8e1-144">Il s’agit des informations [sortantes].</span><span class="sxs-lookup"><span data-stu-id="af8e1-144">This is the [out] information.</span></span> <span data-ttu-id="af8e1-145">Lorsqu’il est dans un état, le client met à jour la structure de données correspondante pour cet état.</span><span class="sxs-lookup"><span data-stu-id="af8e1-145">While in a state, the client updates the corresponding data structure for that state.</span></span> <span data-ttu-id="af8e1-146">Il s’agit des informations [in].</span><span class="sxs-lookup"><span data-stu-id="af8e1-146">This is the [in] information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="af8e1-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af8e1-147">See also</span></span>



[<span data-ttu-id="af8e1-148">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="af8e1-148">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="af8e1-149">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="af8e1-149">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="af8e1-150">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="af8e1-150">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="af8e1-151">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="af8e1-151">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="af8e1-152">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="af8e1-152">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="af8e1-153">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="af8e1-153">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="af8e1-154">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="af8e1-154">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="af8e1-155">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="af8e1-155">MAPI Constants</span></span>](mapi-constants.md)

