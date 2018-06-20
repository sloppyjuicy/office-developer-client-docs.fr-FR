---
title: MAPIOFFLINE_NOTIFY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e03c5a87-4513-2133-ae0a-11d242f80e4b
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 9d8eb3f2c52f20ffe57d84823a0ed736337b4d9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784762"
---
# <a name="mapiofflinenotify"></a><span data-ttu-id="3494e-103">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="3494e-103">MAPIOFFLINE_NOTIFY</span></span>

<span data-ttu-id="3494e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3494e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3494e-105">Il s’agit de la notification d’une modification dans l’état de connexion.</span><span class="sxs-lookup"><span data-stu-id="3494e-105">This is the notification for a change in the connection state.</span></span> <span data-ttu-id="3494e-106">Elle indique la partie de l’état de connexion qui a été modifié, l’état de connexion ancien et le nouvel état de connexion.</span><span class="sxs-lookup"><span data-stu-id="3494e-106">It indicates the part of the connection state that has changed, the old connection state, and the new connection state.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3494e-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="3494e-107">Quick info</span></span>

<span data-ttu-id="3494e-108">Voir **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="3494e-108">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
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

## <a name="members"></a><span data-ttu-id="3494e-109">Membres</span><span class="sxs-lookup"><span data-stu-id="3494e-109">Members</span></span>

 <span data-ttu-id="3494e-110">_ulSize_</span><span class="sxs-lookup"><span data-stu-id="3494e-110">_ulSize_</span></span>
  
> <span data-ttu-id="3494e-111">Taille de la structure **MAPIOFFLINE_NOTIFY** .</span><span class="sxs-lookup"><span data-stu-id="3494e-111">Size of the **MAPIOFFLINE_NOTIFY** structure.</span></span> 
    
 <span data-ttu-id="3494e-112">_NotifyType_</span><span class="sxs-lookup"><span data-stu-id="3494e-112">_NotifyType_</span></span>
  
> <span data-ttu-id="3494e-113">Type de notification.</span><span class="sxs-lookup"><span data-stu-id="3494e-113">Type of notification.</span></span> <span data-ttu-id="3494e-114">Notez que seule notification des modifications de l’état de connexion est pris en charge ; les seules valeurs prises en charge sont :</span><span class="sxs-lookup"><span data-stu-id="3494e-114">Note that only notification on change of the connection state is supported; the only supported values are:</span></span>
    
   - <span data-ttu-id="3494e-115">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START</span><span class="sxs-lookup"><span data-stu-id="3494e-115">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START</span></span>
    
   - <span data-ttu-id="3494e-116">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE</span><span class="sxs-lookup"><span data-stu-id="3494e-116">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE</span></span>
    
   - <span data-ttu-id="3494e-117">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE</span><span class="sxs-lookup"><span data-stu-id="3494e-117">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE</span></span>
    
 <span data-ttu-id="3494e-118">_ulClientToken_</span><span class="sxs-lookup"><span data-stu-id="3494e-118">_ulClientToken_</span></span>
  
> <span data-ttu-id="3494e-119">Jeton défini par le client dans la structure **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** dans **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="3494e-119">A token defined by the client in the **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** structure in **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> 
    
 <span data-ttu-id="3494e-120">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="3494e-120">_ulMask_</span></span>
  
> <span data-ttu-id="3494e-121">La partie de l’état de connexion qui a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="3494e-121">The part of the connection state that has changed.</span></span> <span data-ttu-id="3494e-122">La seule valeur pris en charge est MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="3494e-122">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="3494e-123">_ulStateOld_</span><span class="sxs-lookup"><span data-stu-id="3494e-123">_ulStateOld_</span></span>
  
> <span data-ttu-id="3494e-124">L’état de connexion ancien.</span><span class="sxs-lookup"><span data-stu-id="3494e-124">The old connection state.</span></span> <span data-ttu-id="3494e-125">Les seules valeurs prises en charge sont :</span><span class="sxs-lookup"><span data-stu-id="3494e-125">The only supported values are:</span></span>
    
   - <span data-ttu-id="3494e-126">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="3494e-126">MAPIOFFLINE_STATE_OFFLINE</span></span>
    
   - <span data-ttu-id="3494e-127">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="3494e-127">MAPIOFFLINE_STATE_ONLINE</span></span>
    
 <span data-ttu-id="3494e-128">_ulStateNew_</span><span class="sxs-lookup"><span data-stu-id="3494e-128">_ulStateNew_</span></span>
  
> <span data-ttu-id="3494e-129">Le nouvel état de connexion.</span><span class="sxs-lookup"><span data-stu-id="3494e-129">The new connection state.</span></span> <span data-ttu-id="3494e-130">Les seules valeurs prises en charge sont :</span><span class="sxs-lookup"><span data-stu-id="3494e-130">The only supported values are:</span></span>
    
   - <span data-ttu-id="3494e-131">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="3494e-131">MAPIOFFLINE_STATE_OFFLINE</span></span>
    
   - <span data-ttu-id="3494e-132">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="3494e-132">MAPIOFFLINE_STATE_ONLINE</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3494e-133">Remarques</span><span class="sxs-lookup"><span data-stu-id="3494e-133">Remarks</span></span>

<span data-ttu-id="3494e-134">L’API d’état en mode hors connexion prend en charge uniquement les notifications pour les modifications en ligne/hors connexion.</span><span class="sxs-lookup"><span data-stu-id="3494e-134">The Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="3494e-135">Un client doit vérifier que Outlook renvoie les valeurs suivantes avant d’examiner la modification :</span><span class="sxs-lookup"><span data-stu-id="3494e-135">A client must check that Outlook returns the following values before examining the actual change:</span></span>
  
1.  <span data-ttu-id="3494e-136">*NotifyType* a la valeur MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE ou MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE.</span><span class="sxs-lookup"><span data-stu-id="3494e-136">*NotifyType*  has the value MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE, or MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE.</span></span> <span data-ttu-id="3494e-137">Dans ce cas, le client peut partent du principe que la modification est un changement d’état de connexion et *Info* est de la structure *StateChange* .</span><span class="sxs-lookup"><span data-stu-id="3494e-137">In this case, the client can assume that the change is a connection state change, and  *Info*  is of the structure  *StateChange*  .</span></span> 
    
2.  <span data-ttu-id="3494e-138">*ulMask* a la valeur MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="3494e-138">*ulMask*  has the value MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span> <span data-ttu-id="3494e-139">Dans ce cas, le client peut partent du principe que la modification est un changement d’état en ligne/hors connexion et peut poursuivre examen *ulStateOld* et *ulStateNew* .</span><span class="sxs-lookup"><span data-stu-id="3494e-139">In this case, the client can assume that the change is an online/offline connection state change, and can proceed with examining  *ulStateOld*  and  *ulStateNew*  .</span></span> 
    
<span data-ttu-id="3494e-140">Il est possible qu’Outlook indique d’autres modifications ne sont pas pris en charge un client.</span><span class="sxs-lookup"><span data-stu-id="3494e-140">It is possible that Outlook notifies a client of other changes that are not supported.</span></span> <span data-ttu-id="3494e-141">Dans ce cas, *NotifyType* ne serait pas l’une des trois valeurs mentionné plus haut, ou *ulMask* ne serait pas MAPIOFFLINE_STATE_OFFLINE_MASK, et le client doit ignorer le reste des données dans les *Info* .</span><span class="sxs-lookup"><span data-stu-id="3494e-141">In such cases,  *NotifyType*  would not be any one of the three values stated previously, or  *ulMask*  would not be MAPIOFFLINE_STATE_OFFLINE_MASK, and the client must ignore the rest of the data in  *Info*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3494e-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3494e-142">See also</span></span>

- [<span data-ttu-id="3494e-143">À propos de l’API d’état en mode hors connexion</span><span class="sxs-lookup"><span data-stu-id="3494e-143">About the Offline State API</span></span>](about-the-offline-state-api.md)  
- [<span data-ttu-id="3494e-144">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="3494e-144">MAPI Constants</span></span>](mapi-constants.md)  
- [<span data-ttu-id="3494e-145">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="3494e-145">MAPIOFFLINE_NOTIFY_TYPE</span></span>](mapioffline_notify_type.md)

