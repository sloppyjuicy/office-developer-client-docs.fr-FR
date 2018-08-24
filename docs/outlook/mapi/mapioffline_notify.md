---
title: MAPIOFFLINE_NOTIFY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e03c5a87-4513-2133-ae0a-11d242f80e4b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b18a4ae4ee25898d1100d9763714e5be21c69fd8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580725"
---
# <a name="mapiofflinenotify"></a><span data-ttu-id="270a4-103">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="270a4-103">MAPIOFFLINE_NOTIFY</span></span>

<span data-ttu-id="270a4-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="270a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="270a4-105">Il s’agit de la notification d’une modification dans l’état de connexion.</span><span class="sxs-lookup"><span data-stu-id="270a4-105">This is the notification for a change in the connection state.</span></span> <span data-ttu-id="270a4-106">Elle indique la partie de l’état de connexion qui a été modifié, l’état de connexion ancien et le nouvel état de connexion.</span><span class="sxs-lookup"><span data-stu-id="270a4-106">It indicates the part of the connection state that has changed, the old connection state, and the new connection state.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="270a4-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="270a4-107">Quick info</span></span>

<span data-ttu-id="270a4-108">Voir **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="270a4-108">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
```cpp
typedef struct  
{ 
      ULONG ulSize; 
      MAPIOFFLINE_NOTIFY_TYPE NotifyType; 
      ULONG ulClientToken; 
      union { 
         struct 
           { 
           ULONG ulMask; 
           ULONG ulStateOld; 
           ULONG ulStateNew; 
           } StateChange; 
             } Info; 
} MAPIOFFLINE_NOTIFY;
```

## <a name="members"></a><span data-ttu-id="270a4-109">Members</span><span class="sxs-lookup"><span data-stu-id="270a4-109">Members</span></span>

 <span data-ttu-id="270a4-110">_ulSize_</span><span class="sxs-lookup"><span data-stu-id="270a4-110">_ulSize_</span></span>
  
> <span data-ttu-id="270a4-111">Taille de la structure **MAPIOFFLINE_NOTIFY** .</span><span class="sxs-lookup"><span data-stu-id="270a4-111">Size of the **MAPIOFFLINE_NOTIFY** structure.</span></span> 
    
 <span data-ttu-id="270a4-112">_NotifyType_</span><span class="sxs-lookup"><span data-stu-id="270a4-112">_NotifyType_</span></span>
  
> <span data-ttu-id="270a4-113">Type de notification.</span><span class="sxs-lookup"><span data-stu-id="270a4-113">Type of notification.</span></span> <span data-ttu-id="270a4-114">Notez que seule notification des modifications de l’état de connexion est pris en charge ; les seules valeurs prises en charge sont :</span><span class="sxs-lookup"><span data-stu-id="270a4-114">Note that only notification on change of the connection state is supported; the only supported values are:</span></span>
    
   - <span data-ttu-id="270a4-115">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START</span><span class="sxs-lookup"><span data-stu-id="270a4-115">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START</span></span>
    
   - <span data-ttu-id="270a4-116">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE</span><span class="sxs-lookup"><span data-stu-id="270a4-116">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE</span></span>
    
   - <span data-ttu-id="270a4-117">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE</span><span class="sxs-lookup"><span data-stu-id="270a4-117">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE</span></span>
    
 <span data-ttu-id="270a4-118">_ulClientToken_</span><span class="sxs-lookup"><span data-stu-id="270a4-118">_ulClientToken_</span></span>
  
> <span data-ttu-id="270a4-119">Jeton défini par le client dans la structure **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** dans **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="270a4-119">A token defined by the client in the **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** structure in **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> 
    
 <span data-ttu-id="270a4-120">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="270a4-120">_ulMask_</span></span>
  
> <span data-ttu-id="270a4-121">La partie de l’état de connexion qui a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="270a4-121">The part of the connection state that has changed.</span></span> <span data-ttu-id="270a4-122">La seule valeur pris en charge est MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="270a4-122">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="270a4-123">_ulStateOld_</span><span class="sxs-lookup"><span data-stu-id="270a4-123">_ulStateOld_</span></span>
  
> <span data-ttu-id="270a4-124">L’état de connexion ancien.</span><span class="sxs-lookup"><span data-stu-id="270a4-124">The old connection state.</span></span> <span data-ttu-id="270a4-125">Les seules valeurs prises en charge sont :</span><span class="sxs-lookup"><span data-stu-id="270a4-125">The only supported values are:</span></span>
    
   - <span data-ttu-id="270a4-126">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="270a4-126">MAPIOFFLINE_STATE_OFFLINE</span></span>
    
   - <span data-ttu-id="270a4-127">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="270a4-127">MAPIOFFLINE_STATE_ONLINE</span></span>
    
 <span data-ttu-id="270a4-128">_ulStateNew_</span><span class="sxs-lookup"><span data-stu-id="270a4-128">_ulStateNew_</span></span>
  
> <span data-ttu-id="270a4-129">Le nouvel état de connexion.</span><span class="sxs-lookup"><span data-stu-id="270a4-129">The new connection state.</span></span> <span data-ttu-id="270a4-130">Les seules valeurs prises en charge sont :</span><span class="sxs-lookup"><span data-stu-id="270a4-130">The only supported values are:</span></span>
    
   - <span data-ttu-id="270a4-131">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="270a4-131">MAPIOFFLINE_STATE_OFFLINE</span></span>
    
   - <span data-ttu-id="270a4-132">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="270a4-132">MAPIOFFLINE_STATE_ONLINE</span></span>
    
## <a name="remarks"></a><span data-ttu-id="270a4-133">Remarques</span><span class="sxs-lookup"><span data-stu-id="270a4-133">Remarks</span></span>

<span data-ttu-id="270a4-134">L’API d’état en mode hors connexion prend en charge uniquement les notifications pour les modifications en ligne/hors connexion.</span><span class="sxs-lookup"><span data-stu-id="270a4-134">The Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="270a4-135">Un client doit vérifier que Outlook renvoie les valeurs suivantes avant d’examiner la modification :</span><span class="sxs-lookup"><span data-stu-id="270a4-135">A client must check that Outlook returns the following values before examining the actual change:</span></span>
  
1.  <span data-ttu-id="270a4-136">*NotifyType* a la valeur MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE ou MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE.</span><span class="sxs-lookup"><span data-stu-id="270a4-136">*NotifyType*  has the value MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE, or MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE.</span></span> <span data-ttu-id="270a4-137">Dans ce cas, le client peut partent du principe que la modification est un changement d’état de connexion et *Info* est de la structure *StateChange* .</span><span class="sxs-lookup"><span data-stu-id="270a4-137">In this case, the client can assume that the change is a connection state change, and  *Info*  is of the structure  *StateChange*  .</span></span> 
    
2.  <span data-ttu-id="270a4-138">*ulMask* a la valeur MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="270a4-138">*ulMask*  has the value MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span> <span data-ttu-id="270a4-139">Dans ce cas, le client peut partent du principe que la modification est un changement d’état en ligne/hors connexion et peut poursuivre examen *ulStateOld* et *ulStateNew* .</span><span class="sxs-lookup"><span data-stu-id="270a4-139">In this case, the client can assume that the change is an online/offline connection state change, and can proceed with examining  *ulStateOld*  and  *ulStateNew*  .</span></span> 
    
<span data-ttu-id="270a4-140">Il est possible qu’Outlook indique d’autres modifications ne sont pas pris en charge un client.</span><span class="sxs-lookup"><span data-stu-id="270a4-140">It is possible that Outlook notifies a client of other changes that are not supported.</span></span> <span data-ttu-id="270a4-141">Dans ce cas, *NotifyType* ne serait pas l’une des trois valeurs mentionné plus haut, ou *ulMask* ne serait pas MAPIOFFLINE_STATE_OFFLINE_MASK, et le client doit ignorer le reste des données dans les *Info* .</span><span class="sxs-lookup"><span data-stu-id="270a4-141">In such cases,  *NotifyType*  would not be any one of the three values stated previously, or  *ulMask*  would not be MAPIOFFLINE_STATE_OFFLINE_MASK, and the client must ignore the rest of the data in  *Info*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="270a4-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="270a4-142">See also</span></span>

- [<span data-ttu-id="270a4-143">À propos de l’API d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="270a4-143">About the Offline State API</span></span>](about-the-offline-state-api.md)  
- [<span data-ttu-id="270a4-144">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="270a4-144">MAPI Constants</span></span>](mapi-constants.md)  
- [<span data-ttu-id="270a4-145">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="270a4-145">MAPIOFFLINE_NOTIFY_TYPE</span></span>](mapioffline_notify_type.md)

