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
ms.openlocfilehash: 6c5480a8f5e008c01c7ab8141317f5f19547ab10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414766"
---
# <a name="mapioffline_notify"></a><span data-ttu-id="f467d-103">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="f467d-103">MAPIOFFLINE_NOTIFY</span></span>

<span data-ttu-id="f467d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f467d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f467d-105">Il s’agit de la notification d’une modification de l’état de connexion.</span><span class="sxs-lookup"><span data-stu-id="f467d-105">This is the notification for a change in the connection state.</span></span> <span data-ttu-id="f467d-106">Il indique la partie de l’état de connexion qui a changé, l’ancien état de connexion et le nouvel état de connexion.</span><span class="sxs-lookup"><span data-stu-id="f467d-106">It indicates the part of the connection state that has changed, the old connection state, and the new connection state.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f467d-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="f467d-107">Quick info</span></span>

<span data-ttu-id="f467d-108">Voir **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="f467d-108">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
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

## <a name="members"></a><span data-ttu-id="f467d-109">Members</span><span class="sxs-lookup"><span data-stu-id="f467d-109">Members</span></span>

 <span data-ttu-id="f467d-110">_ulSize_</span><span class="sxs-lookup"><span data-stu-id="f467d-110">_ulSize_</span></span>
  
> <span data-ttu-id="f467d-111">Taille de la **MAPIOFFLINE_NOTIFY** structure.</span><span class="sxs-lookup"><span data-stu-id="f467d-111">Size of the **MAPIOFFLINE_NOTIFY** structure.</span></span> 
    
 <span data-ttu-id="f467d-112">_NotifyType_</span><span class="sxs-lookup"><span data-stu-id="f467d-112">_NotifyType_</span></span>
  
> <span data-ttu-id="f467d-113">Type de notification.</span><span class="sxs-lookup"><span data-stu-id="f467d-113">Type of notification.</span></span> <span data-ttu-id="f467d-114">Notez que seule la notification de modification de l’état de connexion est prise en charge ; Les seules valeurs prise en charge sont les :</span><span class="sxs-lookup"><span data-stu-id="f467d-114">Note that only notification on change of the connection state is supported; the only supported values are:</span></span>
    
   - <span data-ttu-id="f467d-115">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START</span><span class="sxs-lookup"><span data-stu-id="f467d-115">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START</span></span>
    
   - <span data-ttu-id="f467d-116">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE</span><span class="sxs-lookup"><span data-stu-id="f467d-116">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE</span></span>
    
   - <span data-ttu-id="f467d-117">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE</span><span class="sxs-lookup"><span data-stu-id="f467d-117">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE</span></span>
    
 <span data-ttu-id="f467d-118">_ulClientToken_</span><span class="sxs-lookup"><span data-stu-id="f467d-118">_ulClientToken_</span></span>
  
> <span data-ttu-id="f467d-119">Jeton défini par le client dans la structure **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** dans **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="f467d-119">A token defined by the client in the **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** structure in **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> 
    
 <span data-ttu-id="f467d-120">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="f467d-120">_ulMask_</span></span>
  
> <span data-ttu-id="f467d-121">Partie de l’état de connexion qui a changé.</span><span class="sxs-lookup"><span data-stu-id="f467d-121">The part of the connection state that has changed.</span></span> <span data-ttu-id="f467d-122">La seule valeur prise en charge est MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="f467d-122">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="f467d-123">_ulStateOld_</span><span class="sxs-lookup"><span data-stu-id="f467d-123">_ulStateOld_</span></span>
  
> <span data-ttu-id="f467d-124">Ancien état de connexion.</span><span class="sxs-lookup"><span data-stu-id="f467d-124">The old connection state.</span></span> <span data-ttu-id="f467d-125">Les seules valeurs prise en charge sont :</span><span class="sxs-lookup"><span data-stu-id="f467d-125">The only supported values are:</span></span>
    
   - <span data-ttu-id="f467d-126">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="f467d-126">MAPIOFFLINE_STATE_OFFLINE</span></span>
    
   - <span data-ttu-id="f467d-127">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="f467d-127">MAPIOFFLINE_STATE_ONLINE</span></span>
    
 <span data-ttu-id="f467d-128">_ulStateNew_</span><span class="sxs-lookup"><span data-stu-id="f467d-128">_ulStateNew_</span></span>
  
> <span data-ttu-id="f467d-129">Nouvel état de connexion.</span><span class="sxs-lookup"><span data-stu-id="f467d-129">The new connection state.</span></span> <span data-ttu-id="f467d-130">Les seules valeurs prise en charge sont :</span><span class="sxs-lookup"><span data-stu-id="f467d-130">The only supported values are:</span></span>
    
   - <span data-ttu-id="f467d-131">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="f467d-131">MAPIOFFLINE_STATE_OFFLINE</span></span>
    
   - <span data-ttu-id="f467d-132">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="f467d-132">MAPIOFFLINE_STATE_ONLINE</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f467d-133">Remarques</span><span class="sxs-lookup"><span data-stu-id="f467d-133">Remarks</span></span>

<span data-ttu-id="f467d-134">L’API d’état hors connexion prend uniquement en charge les notifications pour les modifications en ligne/hors connexion.</span><span class="sxs-lookup"><span data-stu-id="f467d-134">The Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="f467d-135">Un client doit vérifier qu’Outlook renvoie les valeurs suivantes avant d’examiner la modification réelle :</span><span class="sxs-lookup"><span data-stu-id="f467d-135">A client must check that Outlook returns the following values before examining the actual change:</span></span>
  
1.  <span data-ttu-id="f467d-136">*NotifyType*  a la valeur MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE ou MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE.</span><span class="sxs-lookup"><span data-stu-id="f467d-136">*NotifyType*  has the value MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE, or MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE.</span></span> <span data-ttu-id="f467d-137">Dans ce cas, le client peut supposer que la modification est un changement d’état de connexion et que  *Info*  est de la structure  *StateChange*  .</span><span class="sxs-lookup"><span data-stu-id="f467d-137">In this case, the client can assume that the change is a connection state change, and  *Info*  is of the structure  *StateChange*  .</span></span> 
    
2.  <span data-ttu-id="f467d-138">*ulMask a*  la valeur MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="f467d-138">*ulMask*  has the value MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span> <span data-ttu-id="f467d-139">Dans ce cas, le client peut supposer que la modification est un changement d’état de connexion en ligne/hors connexion et peut passer à l’examen de  *ulStateOld*  et  *ulStateNew*  .</span><span class="sxs-lookup"><span data-stu-id="f467d-139">In this case, the client can assume that the change is an online/offline connection state change, and can proceed with examining  *ulStateOld*  and  *ulStateNew*  .</span></span> 
    
<span data-ttu-id="f467d-140">Il est possible que Outlook avertisse un client d’autres modifications qui ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f467d-140">It is possible that Outlook notifies a client of other changes that are not supported.</span></span> <span data-ttu-id="f467d-141">Dans ce cas,  *NotifyType*  ne serait pas l’une des trois valeurs précédemment énoncés, ou  *ulMask*  ne serait pas MAPIOFFLINE_STATE_OFFLINE_MASK, et le client doit ignorer le reste des données dans  *Info*  .</span><span class="sxs-lookup"><span data-stu-id="f467d-141">In such cases,  *NotifyType*  would not be any one of the three values stated previously, or  *ulMask*  would not be MAPIOFFLINE_STATE_OFFLINE_MASK, and the client must ignore the rest of the data in  *Info*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f467d-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f467d-142">See also</span></span>

- [<span data-ttu-id="f467d-143">À propos de l’API d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="f467d-143">About the Offline State API</span></span>](about-the-offline-state-api.md)  
- [<span data-ttu-id="f467d-144">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="f467d-144">MAPI Constants</span></span>](mapi-constants.md)  
- [<span data-ttu-id="f467d-145">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="f467d-145">MAPIOFFLINE_NOTIFY_TYPE</span></span>](mapioffline_notify_type.md)

