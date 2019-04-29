---
title: MAPISIB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 16452798-7a95-43da-b95e-908debcea050
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: cbda978a0d69367e95f9b4b1f53fd6d03b113ccc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418707"
---
# <a name="mapisib"></a><span data-ttu-id="1f58f-103">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="1f58f-103">MAPISIB</span></span>

  
  
<span data-ttu-id="1f58f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f58f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f58f-105">Cette structure est utilisée avec [IMAPISync:: SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span><span class="sxs-lookup"><span data-stu-id="1f58f-105">This structure is used with [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span>
  
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

## <a name="members"></a><span data-ttu-id="1f58f-106">Members</span><span class="sxs-lookup"><span data-stu-id="1f58f-106">Members</span></span>

 <span data-ttu-id="1f58f-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="1f58f-107">**ulSize**</span></span>
  
> <span data-ttu-id="1f58f-108">Taille de la structure.</span><span class="sxs-lookup"><span data-stu-id="1f58f-108">The size of the structure.</span></span>
    
 <span data-ttu-id="1f58f-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="1f58f-109">**ulFlags**</span></span>
  
> <span data-ttu-id="1f58f-110">Indicateur qui indique le type de synchronisation. Il doit prendre la valeur de l'une des valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="1f58f-110">A flag that indicates the type of sync. It must be one of the following values:</span></span>
    
||||
|:-----|:-----|:-----|
|<span data-ttu-id="1f58f-111">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="1f58f-111">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="1f58f-112">0x00000200</span><span class="sxs-lookup"><span data-stu-id="1f58f-112">0x00000200</span></span>  <br/> |<span data-ttu-id="1f58f-113">Envoyez le message au serveur (qui n'est pas en cours d'utilisation).</span><span class="sxs-lookup"><span data-stu-id="1f58f-113">Send the message to the server (not currently in use).</span></span>  <br/> |
|<span data-ttu-id="1f58f-114">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="1f58f-114">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="1f58f-115">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1f58f-115">0x00000001</span></span>  <br/> |<span data-ttu-id="1f58f-116">Modifications apportées à la hiérarchie sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="1f58f-116">Push hierarchy changes to the server.</span></span>  <br/> |
|<span data-ttu-id="1f58f-117">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="1f58f-117">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="1f58f-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="1f58f-118">0x00000002</span></span>  <br/> |<span data-ttu-id="1f58f-119">Modifications de la hiérarchie d'extraction du serveur.</span><span class="sxs-lookup"><span data-stu-id="1f58f-119">Pull hierarchy changes from server.</span></span>  <br/> |
|<span data-ttu-id="1f58f-120">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="1f58f-120">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="1f58f-121">0x00000040</span><span class="sxs-lookup"><span data-stu-id="1f58f-121">0x00000040</span></span>  <br/> |<span data-ttu-id="1f58f-122">Envoyer les modifications de message vers le serveur.</span><span class="sxs-lookup"><span data-stu-id="1f58f-122">Push message changes to server.</span></span>  <br/> |
|<span data-ttu-id="1f58f-123">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="1f58f-123">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="1f58f-124">0x00000080</span><span class="sxs-lookup"><span data-stu-id="1f58f-124">0x00000080</span></span>  <br/> |<span data-ttu-id="1f58f-125">Extraire les modifications de message du serveur.</span><span class="sxs-lookup"><span data-stu-id="1f58f-125">Pull message changes from server.</span></span>  <br/> |
|<span data-ttu-id="1f58f-126">SYNC_ON_DEMAND</span><span class="sxs-lookup"><span data-stu-id="1f58f-126">SYNC_ON_DEMAND</span></span>  <br/> |<span data-ttu-id="1f58f-127">0x20000000</span><span class="sxs-lookup"><span data-stu-id="1f58f-127">0x20000000</span></span>  <br/> |<span data-ttu-id="1f58f-128">La synchronisation a été lancée par l'utilisateur et doit avoir une priorité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="1f58f-128">The sync was initiated by the user and should be a higher priority.</span></span>  <br/> |
|<span data-ttu-id="1f58f-129">SYNC_GLOBAL_HEADERS</span><span class="sxs-lookup"><span data-stu-id="1f58f-129">SYNC_GLOBAL_HEADERS</span></span>  <br/> |<span data-ttu-id="1f58f-130">0x02000000</span><span class="sxs-lookup"><span data-stu-id="1f58f-130">0x02000000</span></span>  <br/> |<span data-ttu-id="1f58f-131">Ne doit synchroniser que les en-têtes et pas les corps complets.</span><span class="sxs-lookup"><span data-stu-id="1f58f-131">Should only sync headers and not full bodies.</span></span>  <br/> |
   
 <span data-ttu-id="1f58f-132">**psesSync**</span><span class="sxs-lookup"><span data-stu-id="1f58f-132">**psesSync**</span></span>
  
> <span data-ttu-id="1f58f-133">DANS Pointeur vers la session MAPI.</span><span class="sxs-lookup"><span data-stu-id="1f58f-133">[IN] A pointer to the MAPI session.</span></span>
    
 <span data-ttu-id="1f58f-134">**punkCallBack**</span><span class="sxs-lookup"><span data-stu-id="1f58f-134">**punkCallBack**</span></span>
  
> <span data-ttu-id="1f58f-135">DANS Pointeur vers l'interface sur laquelle fournir la progression.</span><span class="sxs-lookup"><span data-stu-id="1f58f-135">[IN] A pointer to the interface on which to provide progress.</span></span> <span data-ttu-id="1f58f-136">Elle peut être utilisée pour interroger l'interface de [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="1f58f-136">It can be used to query the interface for [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md).</span></span>
    
 <span data-ttu-id="1f58f-137">**\*phSyncDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="1f58f-137">**\*phSyncDoneEvent**</span></span>
  
> <span data-ttu-id="1f58f-138">REMARQUER Événement qui se produit lorsque le thread qui vient d'être créé est complet.</span><span class="sxs-lookup"><span data-stu-id="1f58f-138">[OUT] The event that will occur when the thread that was just created is complete.</span></span> <span data-ttu-id="1f58f-139">Le pointeur doit être valide, car il contiendra l'événement.</span><span class="sxs-lookup"><span data-stu-id="1f58f-139">The pointer must be valid because it will contain the event.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f58f-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f58f-140">See also</span></span>



[<span data-ttu-id="1f58f-141">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1f58f-141">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)
  
[<span data-ttu-id="1f58f-142">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1f58f-142">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)

