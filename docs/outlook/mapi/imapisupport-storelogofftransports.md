---
title: IMAPISupportStoreLogoffTransports
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.StoreLogoffTransports
api_type:
- COM
ms.assetid: f21fba96-c5ca-4d41-9b93-c7955ab7327f
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 30c91ec7a5a28b0c270da5223a2a245fb504d8c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326494"
---
# <a name="imapisupportstorelogofftransports"></a><span data-ttu-id="4f49a-103">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="4f49a-103">IMAPISupport::StoreLogoffTransports</span></span>

  
  
<span data-ttu-id="4f49a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f49a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f49a-105">Demande le lancement ordonné d'une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="4f49a-105">Requests the orderly release of a message store.</span></span>
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4f49a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f49a-106">Parameters</span></span>

 <span data-ttu-id="4f49a-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="4f49a-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="4f49a-108">[in, out] Masque de des indicateurs qui contrôle la manière dont la déconnexion du magasin de messages se produit.</span><span class="sxs-lookup"><span data-stu-id="4f49a-108">[in, out] A bitmask of flags that controls how message store logoff occurs.</span></span> <span data-ttu-id="4f49a-109">Lors de l'entrée, tous les indicateurs de ce paramètre s'excluent mutuellement; un seul des indicateurs suivants peut être défini par appel:</span><span class="sxs-lookup"><span data-stu-id="4f49a-109">On input, all flags for this parameter are mutually exclusive; only one of the following flags can be set per call:</span></span>
    
<span data-ttu-id="4f49a-110">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="4f49a-110">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="4f49a-111">Toute activité de fournisseur de transport pour cette banque doit être arrêtée avant la fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="4f49a-111">Any transport provider activity for this store should be stopped before logoff.</span></span> <span data-ttu-id="4f49a-112">Le contrôle est renvoyé au client après l'arrêt de l'activité et le spouleur MAPI s'est déconnecté de la Banque.</span><span class="sxs-lookup"><span data-stu-id="4f49a-112">Control is returned to the client after the activity is stopped and the MAPI spooler has logged off the store.</span></span> <span data-ttu-id="4f49a-113">Si une activité de transport a lieu, la déconnexion n'a pas lieu et aucune modification n'est apportée au comportement du spouleur MAPI ou du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="4f49a-113">If any transport activity is taking place, the logoff does not occur and no change in the MAPI spooler or transport provider behavior occurs.</span></span> <span data-ttu-id="4f49a-114">S'il n'y a actuellement aucune activité, le spouleur MAPI libère la Banque.</span><span class="sxs-lookup"><span data-stu-id="4f49a-114">If there is currently no activity, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="4f49a-115">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="4f49a-115">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="4f49a-116">Le spouleur MAPI doit libérer le magasin et renvoyer le contrôle au client immédiatement après l'envoi de tous les messages sortants prêts à être envoyés.</span><span class="sxs-lookup"><span data-stu-id="4f49a-116">The MAPI spooler should release the store and return control to the client immediately after all outbound mail that is ready to be sent is sent.</span></span> <span data-ttu-id="4f49a-117">Si la Banque de messages est dotée de la boîte de réception par défaut, tout message en cours de traitement est reçu, puis la réception supplémentaire est désactivée.</span><span class="sxs-lookup"><span data-stu-id="4f49a-117">If the message store has the default Inbox, any in-process message is received, and then further reception is disabled.</span></span> 
    
<span data-ttu-id="4f49a-118">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="4f49a-118">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="4f49a-119">Le spouleur MAPI doit libérer le magasin et renvoyer le contrôle au client immédiatement après la fin du traitement des messages en attente.</span><span class="sxs-lookup"><span data-stu-id="4f49a-119">The MAPI spooler should release the store and return control to the client immediately after any pending messages are finished processing.</span></span> <span data-ttu-id="4f49a-120">Aucun nouveau message ne doit être traité.</span><span class="sxs-lookup"><span data-stu-id="4f49a-120">No new messages should be processed.</span></span> 
    
<span data-ttu-id="4f49a-121">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="4f49a-121">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="4f49a-122">Fonctionne de la même manière que l'indicateur LOGOFF_NO_WAIT.</span><span class="sxs-lookup"><span data-stu-id="4f49a-122">Works the same as the LOGOFF_NO_WAIT flag.</span></span> <span data-ttu-id="4f49a-123">L'indicateur LOGOFF_PURGE renvoie le contrôle à l'appelant une fois l'opération terminée.</span><span class="sxs-lookup"><span data-stu-id="4f49a-123">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="4f49a-124">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="4f49a-124">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="4f49a-125">La déconnexion ne doit pas se produire si l'activité d'un fournisseur de transport a lieu.</span><span class="sxs-lookup"><span data-stu-id="4f49a-125">The logoff should not occur if any transport provider activity is taking place.</span></span> <span data-ttu-id="4f49a-126">Le type d'activité qui a lieu est renvoyé sous la forme d'un indicateur sur la sortie.</span><span class="sxs-lookup"><span data-stu-id="4f49a-126">The type of activity taking place is returned as a flag on output.</span></span>
    
    On output, MAPI spooler can return one or more of the following flags:
    
<span data-ttu-id="4f49a-127">LOGOFF_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="4f49a-127">LOGOFF_COMPLETE</span></span> 
  
> <span data-ttu-id="4f49a-128">La déconnexion peut être terminée.</span><span class="sxs-lookup"><span data-stu-id="4f49a-128">The logoff can complete.</span></span> <span data-ttu-id="4f49a-129">Toutes les ressources associées à la Banque ont été libérées, et l'objet a été invalidé.</span><span class="sxs-lookup"><span data-stu-id="4f49a-129">All resources associated with the store have been released, and the object has been invalidated.</span></span> <span data-ttu-id="4f49a-130">Le spouleur MAPI a effectué ou exécutera toutes les demandes.</span><span class="sxs-lookup"><span data-stu-id="4f49a-130">The MAPI spooler has performed or will perform all requests.</span></span> <span data-ttu-id="4f49a-131">Seule la méthode **IUnknown:: Release** de la Banque de messages doit être appelée à ce stade.</span><span class="sxs-lookup"><span data-stu-id="4f49a-131">Only the message store's **IUnknown::Release** method should be called at this point.</span></span> 
    
<span data-ttu-id="4f49a-132">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="4f49a-132">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="4f49a-133">Un message arrive actuellement dans le magasin à partir d'un ou plusieurs fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="4f49a-133">A message is currently coming into the store from one or more transport providers.</span></span> 
    
<span data-ttu-id="4f49a-134">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="4f49a-134">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="4f49a-135">Un message est actuellement envoyé à partir de la Banque par un ou plusieurs fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="4f49a-135">A message is currently being sent from the store by one or more transport providers.</span></span> 
    
<span data-ttu-id="4f49a-136">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="4f49a-136">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="4f49a-137">Il y a actuellement des messages dans la file d'attente des messages sortants pour le magasin.</span><span class="sxs-lookup"><span data-stu-id="4f49a-137">There are currently messages in the outbound queue for the store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4f49a-138">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4f49a-138">Return value</span></span>

<span data-ttu-id="4f49a-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="4f49a-139">S_OK</span></span> 
  
> <span data-ttu-id="4f49a-140">La procédure de fermeture de session a réussi.</span><span class="sxs-lookup"><span data-stu-id="4f49a-140">The logoff procedure was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4f49a-141">Remarques</span><span class="sxs-lookup"><span data-stu-id="4f49a-141">Remarks</span></span>

<span data-ttu-id="4f49a-142">La méthode **IMAPISupport:: StoreLogoffTransports** est implémentée pour les objets de prise en charge du fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="4f49a-142">The **IMAPISupport::StoreLogoffTransports** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="4f49a-143">Les fournisseurs de banques de messages appellent **StoreLogoffTransports** pour donner aux applications clientes un contrôle sur la façon dont MAPI gère l'activité du fournisseur de transport lorsqu'une banque de messages se ferme.</span><span class="sxs-lookup"><span data-stu-id="4f49a-143">Message store providers call **StoreLogoffTransports** to give client applications some control over how MAPI handles transport provider activity as a message store is closing.</span></span> 
  
<span data-ttu-id="4f49a-144">Si le magasin doit être déconnecté pour un autre processus, MAPI ignore un appel vers **StoreLogoffTransports** et renvoie l'indicateur LOGOFF_COMPLETE dans le paramètre _lpulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="4f49a-144">If another process has the store to be logged off open for the same profile, MAPI ignores a call to **StoreLogoffTransports** and returns the flag LOGOFF_COMPLETE in the  _lpulFlags_ parameter.</span></span> 
  
<span data-ttu-id="4f49a-145">Le comportement du fournisseur de banque suivant le retour de **StoreLogoffTransports** doit être basé sur la valeur de _lpulFlags_, qui indique l'état du système et transmet les instructions du client pour le comportement de fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="4f49a-145">The behavior of the store provider following the return from **StoreLogoffTransports** should be based on the value of  _lpulFlags_, which indicates system status and conveys client instructions for logoff behavior.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4f49a-146">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="4f49a-146">Notes to callers</span></span>

 <span data-ttu-id="4f49a-147">**StoreLogoffTransports** est généralement appelé à partir de la méthode [IMsgStore:: StoreLogoff](imsgstore-storelogoff.md) d'un fournisseur de magasins.</span><span class="sxs-lookup"><span data-stu-id="4f49a-147">**StoreLogoffTransports** is typically called from a store provider's [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) method.</span></span> <span data-ttu-id="4f49a-148">Toutefois, elle peut également être appelée à partir de la méthode **IUnknown:: Release** de la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="4f49a-148">However, it can also be called from the **IUnknown::Release** method of the message store.</span></span> <span data-ttu-id="4f49a-149">Implémentez la méthode **Release** de votre banque de messages pour vérifier si un appel à **StoreLogoffTransports** s'est produit.</span><span class="sxs-lookup"><span data-stu-id="4f49a-149">Implement the **Release** method of your message store so you can check whether or not a call to **StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="4f49a-150">Si un appel n'a pas été effectué, appelez **StoreLogoffTransports** avec l'indicateur LOGOFF_ABORT défini.</span><span class="sxs-lookup"><span data-stu-id="4f49a-150">If a call has not occurred, call **StoreLogoffTransports** with the LOGOFF_ABORT flag set.</span></span> 
  
<span data-ttu-id="4f49a-151">Le paramètre _lpulFlags_ est défini sur un indicateur qui indique la façon dont le client nécessite l'arrêt de la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="4f49a-151">The  _lpulFlags_ parameter is set to a flag that indicates how the client requires the message store to be shut down.</span></span> <span data-ttu-id="4f49a-152">Déterminez le paramètre approprié pour _ulFlags_ en fonction de la valeur du paramètre correspondant dans l'appel à **StoreLogoff**.</span><span class="sxs-lookup"><span data-stu-id="4f49a-152">Determine the appropriate setting for  _ulFlags_ based on the setting of the corresponding parameter in the call to **StoreLogoff**.</span></span> <span data-ttu-id="4f49a-153">Autrement dit, si un client a appelé votre méthode **StoreLogoff** avec _ULFLAGS_ défini sur LOGOFF_ORDERLY, vous devez appeler **STORELOGOFFTRANSPORTS** avec _ulFlags_ défini sur LOGOFF_ORDERLY.</span><span class="sxs-lookup"><span data-stu-id="4f49a-153">That is, if a client called your **StoreLogoff** method with  _ulFlags_ set to LOGOFF_ORDERLY, you should call **StoreLogoffTransports** with  _ulFlags_ set to LOGOFF_ORDERLY.</span></span> 
  
<span data-ttu-id="4f49a-154">Pour plus d'informations sur le processus de fermeture de la Banque de messages, consultez la rubrique [arrêt d'un fournisseur de banque de messages](shutting-down-a-message-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4f49a-154">For more information about the message store logoff process, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4f49a-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f49a-155">See also</span></span>



[<span data-ttu-id="4f49a-156">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="4f49a-156">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="4f49a-157">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="4f49a-157">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="4f49a-158">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4f49a-158">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

