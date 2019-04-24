---
title: MAPISIB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 16452798-7a95-43da-b95e-908debcea050
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: cbda978a0d69367e95f9b4b1f53fd6d03b113ccc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270209"
---
# <a name="mapisib"></a><span data-ttu-id="4a45e-103">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="4a45e-103">MAPISIB</span></span>

  
  
<span data-ttu-id="4a45e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a45e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a45e-105">Cette structure est utilisée avec [IMAPISync:: SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span><span class="sxs-lookup"><span data-stu-id="4a45e-105">This structure is used with [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span>
  
```cpp
typedef struct _MAPISIB
{
ULONG           ulSize;                
ULONG           ulFlags;
LPMAPISESSION   psesSync;
LPUNKNOWN       punkCallBack;
HANDLE          *phSyncDoneEvent;    
} MAPISIB, *PMAPISIB
```

## <a name="members"></a><span data-ttu-id="4a45e-106">Members</span><span class="sxs-lookup"><span data-stu-id="4a45e-106">Members</span></span>

 <span data-ttu-id="4a45e-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="4a45e-107">**ulSize**</span></span>
  
> <span data-ttu-id="4a45e-108">Taille de la structure.</span><span class="sxs-lookup"><span data-stu-id="4a45e-108">The size of the structure.</span></span>
    
 <span data-ttu-id="4a45e-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="4a45e-109">**ulFlags**</span></span>
  
> <span data-ttu-id="4a45e-110">Indicateur qui indique le type de synchronisation. Il doit prendre la valeur de l'une des valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="4a45e-110">A flag that indicates the type of sync. It must be one of the following values:</span></span>
    
||||
|:-----|:-----|:-----|
|<span data-ttu-id="4a45e-111">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="4a45e-111">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="4a45e-112">0x00000200</span><span class="sxs-lookup"><span data-stu-id="4a45e-112">0x00000200</span></span>  <br/> |<span data-ttu-id="4a45e-113">Envoyez le message au serveur (qui n'est pas en cours d'utilisation).</span><span class="sxs-lookup"><span data-stu-id="4a45e-113">Send the message to the server (not currently in use).</span></span>  <br/> |
|<span data-ttu-id="4a45e-114">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="4a45e-114">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="4a45e-115">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4a45e-115">0x00000001</span></span>  <br/> |<span data-ttu-id="4a45e-116">Modifications apportées à la hiérarchie sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="4a45e-116">Push hierarchy changes to the server.</span></span>  <br/> |
|<span data-ttu-id="4a45e-117">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="4a45e-117">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="4a45e-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="4a45e-118">0x00000002</span></span>  <br/> |<span data-ttu-id="4a45e-119">Modifications de la hiérarchie d'extraction du serveur.</span><span class="sxs-lookup"><span data-stu-id="4a45e-119">Pull hierarchy changes from server.</span></span>  <br/> |
|<span data-ttu-id="4a45e-120">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="4a45e-120">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="4a45e-121">0x00000040</span><span class="sxs-lookup"><span data-stu-id="4a45e-121">0x00000040</span></span>  <br/> |<span data-ttu-id="4a45e-122">Envoyer les modifications de message vers le serveur.</span><span class="sxs-lookup"><span data-stu-id="4a45e-122">Push message changes to server.</span></span>  <br/> |
|<span data-ttu-id="4a45e-123">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="4a45e-123">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="4a45e-124">0x00000080</span><span class="sxs-lookup"><span data-stu-id="4a45e-124">0x00000080</span></span>  <br/> |<span data-ttu-id="4a45e-125">Extraire les modifications de message du serveur.</span><span class="sxs-lookup"><span data-stu-id="4a45e-125">Pull message changes from server.</span></span>  <br/> |
|<span data-ttu-id="4a45e-126">SYNC_ON_DEMAND</span><span class="sxs-lookup"><span data-stu-id="4a45e-126">SYNC_ON_DEMAND</span></span>  <br/> |<span data-ttu-id="4a45e-127">0x20000000</span><span class="sxs-lookup"><span data-stu-id="4a45e-127">0x20000000</span></span>  <br/> |<span data-ttu-id="4a45e-128">La synchronisation a été lancée par l'utilisateur et doit avoir une priorité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="4a45e-128">The sync was initiated by the user and should be a higher priority.</span></span>  <br/> |
|<span data-ttu-id="4a45e-129">SYNC_GLOBAL_HEADERS</span><span class="sxs-lookup"><span data-stu-id="4a45e-129">SYNC_GLOBAL_HEADERS</span></span>  <br/> |<span data-ttu-id="4a45e-130">0x02000000</span><span class="sxs-lookup"><span data-stu-id="4a45e-130">0x02000000</span></span>  <br/> |<span data-ttu-id="4a45e-131">Ne doit synchroniser que les en-têtes et pas les corps complets.</span><span class="sxs-lookup"><span data-stu-id="4a45e-131">Should only sync headers and not full bodies.</span></span>  <br/> |
   
 <span data-ttu-id="4a45e-132">**psesSync**</span><span class="sxs-lookup"><span data-stu-id="4a45e-132">**psesSync**</span></span>
  
> <span data-ttu-id="4a45e-133">DANS Pointeur vers la session MAPI.</span><span class="sxs-lookup"><span data-stu-id="4a45e-133">[IN] A pointer to the MAPI session.</span></span>
    
 <span data-ttu-id="4a45e-134">**punkCallBack**</span><span class="sxs-lookup"><span data-stu-id="4a45e-134">**punkCallBack**</span></span>
  
> <span data-ttu-id="4a45e-135">DANS Pointeur vers l'interface sur laquelle fournir la progression.</span><span class="sxs-lookup"><span data-stu-id="4a45e-135">[IN] A pointer to the interface on which to provide progress.</span></span> <span data-ttu-id="4a45e-136">Elle peut être utilisée pour interroger l'interface de [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="4a45e-136">It can be used to query the interface for [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md).</span></span>
    
 <span data-ttu-id="4a45e-137">**\*phSyncDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="4a45e-137">**\*phSyncDoneEvent**</span></span>
  
> <span data-ttu-id="4a45e-138">REMARQUER Événement qui se produit lorsque le thread qui vient d'être créé est complet.</span><span class="sxs-lookup"><span data-stu-id="4a45e-138">[OUT] The event that will occur when the thread that was just created is complete.</span></span> <span data-ttu-id="4a45e-139">Le pointeur doit être valide, car il contiendra l'événement.</span><span class="sxs-lookup"><span data-stu-id="4a45e-139">The pointer must be valid because it will contain the event.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a45e-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a45e-140">See also</span></span>



[<span data-ttu-id="4a45e-141">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4a45e-141">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)
  
[<span data-ttu-id="4a45e-142">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4a45e-142">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)

