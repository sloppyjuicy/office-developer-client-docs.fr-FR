---
title: MAPISIB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 16452798-7a95-43da-b95e-908debcea050
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f696d9739014659812de3309ec885f37a6f85cc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572136"
---
# <a name="mapisib"></a><span data-ttu-id="9aa82-103">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="9aa82-103">MAPISIB</span></span>

  
  
<span data-ttu-id="9aa82-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9aa82-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9aa82-105">Cette structure est utilisée avec [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span><span class="sxs-lookup"><span data-stu-id="9aa82-105">This structure is used with [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span>
  
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

## <a name="members"></a><span data-ttu-id="9aa82-106">Members</span><span class="sxs-lookup"><span data-stu-id="9aa82-106">Members</span></span>

 <span data-ttu-id="9aa82-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="9aa82-107">**ulSize**</span></span>
  
> <span data-ttu-id="9aa82-108">La taille de la structure.</span><span class="sxs-lookup"><span data-stu-id="9aa82-108">The size of the structure.</span></span>
    
 <span data-ttu-id="9aa82-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="9aa82-109">**ulFlags**</span></span>
  
> <span data-ttu-id="9aa82-110">Indicateur qui indique le type de synchronisation. Il doit être une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="9aa82-110">A flag that indicates the type of sync. It must be one of the following values:</span></span>
    
||||
|:-----|:-----|:-----|
|<span data-ttu-id="9aa82-111">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="9aa82-111">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="9aa82-112">0 x 00000200</span><span class="sxs-lookup"><span data-stu-id="9aa82-112">0x00000200</span></span>  <br/> |<span data-ttu-id="9aa82-113">Envoyer le message vers le serveur (pas en cours d’utilisation).</span><span class="sxs-lookup"><span data-stu-id="9aa82-113">Send the message to the server (not currently in use).</span></span>  <br/> |
|<span data-ttu-id="9aa82-114">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="9aa82-114">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="9aa82-115">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9aa82-115">0x00000001</span></span>  <br/> |<span data-ttu-id="9aa82-116">Propager les modifications de la hiérarchie sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="9aa82-116">Push hierarchy changes to the server.</span></span>  <br/> |
|<span data-ttu-id="9aa82-117">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="9aa82-117">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="9aa82-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9aa82-118">0x00000002</span></span>  <br/> |<span data-ttu-id="9aa82-119">Extraire des modifications de la hiérarchie à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="9aa82-119">Pull hierarchy changes from server.</span></span>  <br/> |
|<span data-ttu-id="9aa82-120">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="9aa82-120">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="9aa82-121">0 x 00000040</span><span class="sxs-lookup"><span data-stu-id="9aa82-121">0x00000040</span></span>  <br/> |<span data-ttu-id="9aa82-122">Propager les modifications de message au serveur.</span><span class="sxs-lookup"><span data-stu-id="9aa82-122">Push message changes to server.</span></span>  <br/> |
|<span data-ttu-id="9aa82-123">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="9aa82-123">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="9aa82-124">0x00000080</span><span class="sxs-lookup"><span data-stu-id="9aa82-124">0x00000080</span></span>  <br/> |<span data-ttu-id="9aa82-125">Extraire des modifications de message serveur.</span><span class="sxs-lookup"><span data-stu-id="9aa82-125">Pull message changes from server.</span></span>  <br/> |
|<span data-ttu-id="9aa82-126">SYNC_ON_DEMAND</span><span class="sxs-lookup"><span data-stu-id="9aa82-126">SYNC_ON_DEMAND</span></span>  <br/> |<span data-ttu-id="9aa82-127">0 x 20000000</span><span class="sxs-lookup"><span data-stu-id="9aa82-127">0x20000000</span></span>  <br/> |<span data-ttu-id="9aa82-128">La synchronisation a été lancée par l’utilisateur et doit être une priorité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="9aa82-128">The sync was initiated by the user and should be a higher priority.</span></span>  <br/> |
|<span data-ttu-id="9aa82-129">SYNC_GLOBAL_HEADERS</span><span class="sxs-lookup"><span data-stu-id="9aa82-129">SYNC_GLOBAL_HEADERS</span></span>  <br/> |<span data-ttu-id="9aa82-130">0x02000000</span><span class="sxs-lookup"><span data-stu-id="9aa82-130">0x02000000</span></span>  <br/> |<span data-ttu-id="9aa82-131">Doit synchroniser uniquement les en-têtes et corps pas complètes.</span><span class="sxs-lookup"><span data-stu-id="9aa82-131">Should only sync headers and not full bodies.</span></span>  <br/> |
   
 <span data-ttu-id="9aa82-132">**psesSync**</span><span class="sxs-lookup"><span data-stu-id="9aa82-132">**psesSync**</span></span>
  
> <span data-ttu-id="9aa82-133">[IN] Pointeur vers la session MAPI.</span><span class="sxs-lookup"><span data-stu-id="9aa82-133">[IN] A pointer to the MAPI session.</span></span>
    
 <span data-ttu-id="9aa82-134">**punkCallBack**</span><span class="sxs-lookup"><span data-stu-id="9aa82-134">**punkCallBack**</span></span>
  
> <span data-ttu-id="9aa82-135">[IN] Pointeur vers l’interface sur laquelle fournir la progression.</span><span class="sxs-lookup"><span data-stu-id="9aa82-135">[IN] A pointer to the interface on which to provide progress.</span></span> <span data-ttu-id="9aa82-136">Il peut être utilisé pour interroger l’interface pour [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="9aa82-136">It can be used to query the interface for [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md).</span></span>
    
 <span data-ttu-id="9aa82-137">**\*phSyncDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="9aa82-137">**\*phSyncDoneEvent**</span></span>
  
> <span data-ttu-id="9aa82-138">[OUT] L’événement se produit lorsque le thread qui vient d’être créé est terminé.</span><span class="sxs-lookup"><span data-stu-id="9aa82-138">[OUT] The event that will occur when the thread that was just created is complete.</span></span> <span data-ttu-id="9aa82-139">Le pointeur doit être valid car il contient l’événement.</span><span class="sxs-lookup"><span data-stu-id="9aa82-139">The pointer must be valid because it will contain the event.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9aa82-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9aa82-140">See also</span></span>



[<span data-ttu-id="9aa82-141">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9aa82-141">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)
  
[<span data-ttu-id="9aa82-142">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9aa82-142">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)

