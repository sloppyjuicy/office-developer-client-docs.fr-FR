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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: ddc61aa42b1087ed5f0ecb7986125ceef27cddce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784331"
---
# <a name="iostxsyncbeg"></a><span data-ttu-id="baf7e-103">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="baf7e-103">IOSTX::SyncBeg</span></span>

  
  
<span data-ttu-id="baf7e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="baf7e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="baf7e-105">Prépare le magasin local de la synchronisation dans un état particulier et récupère les informations nécessaires pour répliquer.</span><span class="sxs-lookup"><span data-stu-id="baf7e-105">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a><span data-ttu-id="baf7e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="baf7e-106">Parameters</span></span>

 <span data-ttu-id="baf7e-107">_uiSync_</span><span class="sxs-lookup"><span data-stu-id="baf7e-107">_uiSync_</span></span>
  
>  <span data-ttu-id="baf7e-108">[in] Entrez le magasin local de l’état.</span><span class="sxs-lookup"><span data-stu-id="baf7e-108">[in] The state that the local store will enter.</span></span> <span data-ttu-id="baf7e-109">Voici une liste d’identificateurs d’état :</span><span class="sxs-lookup"><span data-stu-id="baf7e-109">The following is a list of state identifers:</span></span> 
    
<span data-ttu-id="baf7e-110">LR_SYNC_IDLE</span><span class="sxs-lookup"><span data-stu-id="baf7e-110">LR_SYNC_IDLE</span></span>
  
> 
    
<span data-ttu-id="baf7e-111">LR_SYNC</span><span class="sxs-lookup"><span data-stu-id="baf7e-111">LR_SYNC</span></span>
  
> 
    
<span data-ttu-id="baf7e-112">LR_SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="baf7e-112">LR_SYNC_UPLOAD_HIERARCHY</span></span>
  
> 
    
<span data-ttu-id="baf7e-113">LR_SYNC_UPLOAD_FOLDER</span><span class="sxs-lookup"><span data-stu-id="baf7e-113">LR_SYNC_UPLOAD_FOLDER</span></span>
  
> 
    
<span data-ttu-id="baf7e-114">LR_SYNC_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="baf7e-114">LR_SYNC_CONTENTS</span></span>
  
> 
    
<span data-ttu-id="baf7e-115">LR_SYNC_UPLOAD_TABLE</span><span class="sxs-lookup"><span data-stu-id="baf7e-115">LR_SYNC_UPLOAD_TABLE</span></span>
  
> 
    
<span data-ttu-id="baf7e-116">LR_SYNC_UPLOAD_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="baf7e-116">LR_SYNC_UPLOAD_MESSAGE</span></span>
  
> 
    
<span data-ttu-id="baf7e-117">LR_SYNC_UPLOAD_MESSAGE_READ</span><span class="sxs-lookup"><span data-stu-id="baf7e-117">LR_SYNC_UPLOAD_MESSAGE_READ</span></span>
  
> 
    
<span data-ttu-id="baf7e-118">LR_SYNC_UPLOAD_MESSAGE_DEL</span><span class="sxs-lookup"><span data-stu-id="baf7e-118">LR_SYNC_UPLOAD_MESSAGE_DEL</span></span>
  
> 
    
<span data-ttu-id="baf7e-119">LR_SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="baf7e-119">LR_SYNC_DOWNLOAD_HIERARCHY</span></span>
  
> 
    
<span data-ttu-id="baf7e-120">LR_SYNC_DOWNLOAD_TABLE</span><span class="sxs-lookup"><span data-stu-id="baf7e-120">LR_SYNC_DOWNLOAD_TABLE</span></span>
  
> 
    
 <span data-ttu-id="baf7e-121">_PPV_</span><span class="sxs-lookup"><span data-stu-id="baf7e-121">_ppv_</span></span>
  
>  <span data-ttu-id="baf7e-122">[in] / [out] pointeur vers la structure de données correspondant à l’état d’entrer.</span><span class="sxs-lookup"><span data-stu-id="baf7e-122">[in]/[out] Pointer to the data structure corresponding to the state to enter.</span></span> 
    
[<span data-ttu-id="baf7e-123">DNHIER</span><span class="sxs-lookup"><span data-stu-id="baf7e-123">DNHIER</span></span>](dnhier.md)
  
> 
    
[<span data-ttu-id="baf7e-124">DNTBL</span><span class="sxs-lookup"><span data-stu-id="baf7e-124">DNTBL</span></span>](dntbl.md)
  
> 
    
[<span data-ttu-id="baf7e-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="baf7e-125">DNTBL</span></span>](dntbl.md)
  
> 
    
[<span data-ttu-id="baf7e-126">SYNCHRONISATION</span><span class="sxs-lookup"><span data-stu-id="baf7e-126">SYNC</span></span>](sync.md)
  
> 
    
[<span data-ttu-id="baf7e-127">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="baf7e-127">SYNCCONT</span></span>](synccont.md)
  
> 
    
[<span data-ttu-id="baf7e-128">UPDEL</span><span class="sxs-lookup"><span data-stu-id="baf7e-128">UPDEL</span></span>](updel.md)
  
> 
    
[<span data-ttu-id="baf7e-129">UPDELE</span><span class="sxs-lookup"><span data-stu-id="baf7e-129">UPDELE</span></span>](updele.md)
  
> 
    
[<span data-ttu-id="baf7e-130">UPFLD</span><span class="sxs-lookup"><span data-stu-id="baf7e-130">UPFLD</span></span>](upfld.md)
  
> 
    
[<span data-ttu-id="baf7e-131">UPHIER</span><span class="sxs-lookup"><span data-stu-id="baf7e-131">UPHIER</span></span>](uphier.md)
  
> 
    
[<span data-ttu-id="baf7e-132">UPMOV</span><span class="sxs-lookup"><span data-stu-id="baf7e-132">UPMOV</span></span>](upmov.md)
  
> 
    
[<span data-ttu-id="baf7e-133">UPMSG</span><span class="sxs-lookup"><span data-stu-id="baf7e-133">UPMSG</span></span>](upmsg.md)
  
> 
    
[<span data-ttu-id="baf7e-134">UPREAD</span><span class="sxs-lookup"><span data-stu-id="baf7e-134">UPREAD</span></span>](upread.md)
  
> 
    
[<span data-ttu-id="baf7e-135">UPREADE</span><span class="sxs-lookup"><span data-stu-id="baf7e-135">UPREADE</span></span>](upreade.md)
  
> 
    
[<span data-ttu-id="baf7e-136">UPTBL</span><span class="sxs-lookup"><span data-stu-id="baf7e-136">UPTBL</span></span>](uptbl.md)
  
> 
    
[<span data-ttu-id="baf7e-137">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="baf7e-137">UPTBLE</span></span>](uptble.md)
  
> 
    
## <a name="remarks"></a><span data-ttu-id="baf7e-138">Remarques</span><span class="sxs-lookup"><span data-stu-id="baf7e-138">Remarks</span></span>

<span data-ttu-id="baf7e-139">Le client appelle **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** pour définir le résultat de la synchronisation et appelle ensuite **[IOSTX::SyncEnd](iostx-syncend.md)** pour mettre fin à cet état.</span><span class="sxs-lookup"><span data-stu-id="baf7e-139">The client calls **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** to set the result of the synchronization, and then calls **[IOSTX::SyncEnd](iostx-syncend.md)** to end that state.</span></span> <span data-ttu-id="baf7e-140">Le client doit appeler **[IOSTX::SyncEnd](iostx-syncend.md)** pour chaque appel à **IOSTX::SyncBeg** afin de déterminer si l’état a été répliqué avec succès.</span><span class="sxs-lookup"><span data-stu-id="baf7e-140">The client must call **[IOSTX::SyncEnd](iostx-syncend.md)** for each call to **IOSTX::SyncBeg** in order to determine whether the state has been successfully replicated.</span></span> <span data-ttu-id="baf7e-141">Une fois que cela a été déterminée, Outlook peut commencer à nettoyer son état interne.</span><span class="sxs-lookup"><span data-stu-id="baf7e-141">Once this has been determined, Outlook can begin to clean up its internal state.</span></span> 
  
<span data-ttu-id="baf7e-142">La plupart de ces structures contiennent [out] / [in] informations Outlook transmettre des informations sur le client et le client pour transmettre les informations à Outlook.</span><span class="sxs-lookup"><span data-stu-id="baf7e-142">Most of these structures contain [out]/[in] information, allowing Outlook to pass information to the client, and the client to pass information to Outlook.</span></span> <span data-ttu-id="baf7e-143">Lorsque le client appelle **IOSTX::SyncBeg**, Outlook alloue de la structure de données pour un état donné et initialise avec les informations pour cet état.</span><span class="sxs-lookup"><span data-stu-id="baf7e-143">When the client calls **IOSTX::SyncBeg**, Outlook allocates the data structure for a given state and initializes it with information for that state.</span></span> <span data-ttu-id="baf7e-144">Ce sont les informations [out].</span><span class="sxs-lookup"><span data-stu-id="baf7e-144">This is the [out] information.</span></span> <span data-ttu-id="baf7e-145">Dans un état, le client met à jour la structure de données correspondant pour cet état.</span><span class="sxs-lookup"><span data-stu-id="baf7e-145">While in a state, the client updates the corresponding data structure for that state.</span></span> <span data-ttu-id="baf7e-146">Il s’agit du [in] informations.</span><span class="sxs-lookup"><span data-stu-id="baf7e-146">This is the [in] information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="baf7e-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="baf7e-147">See also</span></span>



[<span data-ttu-id="baf7e-148">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="baf7e-148">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="baf7e-149">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="baf7e-149">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="baf7e-150">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="baf7e-150">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="baf7e-151">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="baf7e-151">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="baf7e-152">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="baf7e-152">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="baf7e-153">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="baf7e-153">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="baf7e-154">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="baf7e-154">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="baf7e-155">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="baf7e-155">MAPI Constants</span></span>](mapi-constants.md)

