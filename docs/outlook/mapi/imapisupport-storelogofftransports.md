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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 30c91ec7a5a28b0c270da5223a2a245fb504d8c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421381"
---
# <a name="imapisupportstorelogofftransports"></a><span data-ttu-id="e7f78-103">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="e7f78-103">IMAPISupport::StoreLogoffTransports</span></span>

  
  
<span data-ttu-id="e7f78-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7f78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7f78-105">Demande la publication ordonnée d’une magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="e7f78-105">Requests the orderly release of a message store.</span></span>
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e7f78-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7f78-106">Parameters</span></span>

 <span data-ttu-id="e7f78-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="e7f78-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="e7f78-108">[in, out] Masque de bits d’indicateurs qui contrôle la façon dont la ouverture de logo de la boutique de messages se produit.</span><span class="sxs-lookup"><span data-stu-id="e7f78-108">[in, out] A bitmask of flags that controls how message store logoff occurs.</span></span> <span data-ttu-id="e7f78-109">Lors de l’entrée, tous les indicateurs pour ce paramètre s’excluent mutuellement ; Un seul des indicateurs suivants peut être définie par appel :</span><span class="sxs-lookup"><span data-stu-id="e7f78-109">On input, all flags for this parameter are mutually exclusive; only one of the following flags can be set per call:</span></span>
    
<span data-ttu-id="e7f78-110">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="e7f78-110">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="e7f78-111">Toute activité de fournisseur de transport pour ce magasin doit être arrêtée avant la ff.</span><span class="sxs-lookup"><span data-stu-id="e7f78-111">Any transport provider activity for this store should be stopped before logoff.</span></span> <span data-ttu-id="e7f78-112">Le contrôle est renvoyé au client une fois l’activité arrêtée et lepooler MAPI a ouvert une session hors du magasin.</span><span class="sxs-lookup"><span data-stu-id="e7f78-112">Control is returned to the client after the activity is stopped and the MAPI spooler has logged off the store.</span></span> <span data-ttu-id="e7f78-113">Si une activité de transport est en cours, la logoff ne se produit pas et aucun changement n’a lieu dans le comportement du fournisseur de transport ou dupooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="e7f78-113">If any transport activity is taking place, the logoff does not occur and no change in the MAPI spooler or transport provider behavior occurs.</span></span> <span data-ttu-id="e7f78-114">S’il n’y a actuellement aucune activité, lepooler MAPI libère le magasin.</span><span class="sxs-lookup"><span data-stu-id="e7f78-114">If there is currently no activity, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="e7f78-115">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="e7f78-115">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="e7f78-116">Lepooler MAPI doit libérer le magasin et retourner le contrôle au client immédiatement après l’envoi de tous les messages sortants prêts à être envoyés.</span><span class="sxs-lookup"><span data-stu-id="e7f78-116">The MAPI spooler should release the store and return control to the client immediately after all outbound mail that is ready to be sent is sent.</span></span> <span data-ttu-id="e7f78-117">Si la boîte de réception par défaut est stockée dans la boutique de messages, tout message in-process est reçu, puis la réception est désactivée.</span><span class="sxs-lookup"><span data-stu-id="e7f78-117">If the message store has the default Inbox, any in-process message is received, and then further reception is disabled.</span></span> 
    
<span data-ttu-id="e7f78-118">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="e7f78-118">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="e7f78-119">Lepooler MAPI doit libérer la boutique et retourner le contrôle au client immédiatement après la fin du traitement des messages en attente.</span><span class="sxs-lookup"><span data-stu-id="e7f78-119">The MAPI spooler should release the store and return control to the client immediately after any pending messages are finished processing.</span></span> <span data-ttu-id="e7f78-120">Aucun nouveau message ne doit être traitée.</span><span class="sxs-lookup"><span data-stu-id="e7f78-120">No new messages should be processed.</span></span> 
    
<span data-ttu-id="e7f78-121">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="e7f78-121">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="e7f78-122">Fonctionne de la même manière que l’LOGOFF_NO_WAIT’indicateur.</span><span class="sxs-lookup"><span data-stu-id="e7f78-122">Works the same as the LOGOFF_NO_WAIT flag.</span></span> <span data-ttu-id="e7f78-123">L LOGOFF_PURGE de commande renvoie le contrôle à l’appelant une fois l’exécution terminée.</span><span class="sxs-lookup"><span data-stu-id="e7f78-123">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="e7f78-124">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="e7f78-124">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="e7f78-125">La logoff ne doit pas se produire si une activité de fournisseur de transport a lieu.</span><span class="sxs-lookup"><span data-stu-id="e7f78-125">The logoff should not occur if any transport provider activity is taking place.</span></span> <span data-ttu-id="e7f78-126">Le type d’activité en cours est renvoyé sous forme d’indicateur sur la sortie.</span><span class="sxs-lookup"><span data-stu-id="e7f78-126">The type of activity taking place is returned as a flag on output.</span></span>
    
    On output, MAPI spooler can return one or more of the following flags:
    
<span data-ttu-id="e7f78-127">LOGOFF_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="e7f78-127">LOGOFF_COMPLETE</span></span> 
  
> <span data-ttu-id="e7f78-128">La ff de logo peut se terminer.</span><span class="sxs-lookup"><span data-stu-id="e7f78-128">The logoff can complete.</span></span> <span data-ttu-id="e7f78-129">Toutes les ressources associées au magasin ont été libérées et l’objet a été invalidé.</span><span class="sxs-lookup"><span data-stu-id="e7f78-129">All resources associated with the store have been released, and the object has been invalidated.</span></span> <span data-ttu-id="e7f78-130">Lepooler MAPI a effectué ou effectuera toutes les demandes.</span><span class="sxs-lookup"><span data-stu-id="e7f78-130">The MAPI spooler has performed or will perform all requests.</span></span> <span data-ttu-id="e7f78-131">Seule la méthode **IUnknown::Release** de la boutique de messages doit être appelée à ce stade.</span><span class="sxs-lookup"><span data-stu-id="e7f78-131">Only the message store's **IUnknown::Release** method should be called at this point.</span></span> 
    
<span data-ttu-id="e7f78-132">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="e7f78-132">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="e7f78-133">Un message provenant d’un ou de plusieurs fournisseurs de transport arrive actuellement dans la boutique.</span><span class="sxs-lookup"><span data-stu-id="e7f78-133">A message is currently coming into the store from one or more transport providers.</span></span> 
    
<span data-ttu-id="e7f78-134">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="e7f78-134">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="e7f78-135">Un message est actuellement envoyé à partir du magasin par un ou plusieurs fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="e7f78-135">A message is currently being sent from the store by one or more transport providers.</span></span> 
    
<span data-ttu-id="e7f78-136">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="e7f78-136">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="e7f78-137">Il existe actuellement des messages dans la file d’attente sortante pour la boutique.</span><span class="sxs-lookup"><span data-stu-id="e7f78-137">There are currently messages in the outbound queue for the store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e7f78-138">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e7f78-138">Return value</span></span>

<span data-ttu-id="e7f78-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="e7f78-139">S_OK</span></span> 
  
> <span data-ttu-id="e7f78-140">La procédure de création d’une logoff a réussi.</span><span class="sxs-lookup"><span data-stu-id="e7f78-140">The logoff procedure was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e7f78-141">Remarques</span><span class="sxs-lookup"><span data-stu-id="e7f78-141">Remarks</span></span>

<span data-ttu-id="e7f78-142">La **méthode IMAPISupport::StoreLogoffTransports** est implémentée pour les objets de prise en charge du fournisseur de magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="e7f78-142">The **IMAPISupport::StoreLogoffTransports** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="e7f78-143">Les fournisseurs de magasins de messages appellent **StoreLogoffTransports** pour donner aux applications clientes un certain contrôle sur la façon dont MAPI gère l’activité des fournisseurs de transport lors de la fermeture d’une magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="e7f78-143">Message store providers call **StoreLogoffTransports** to give client applications some control over how MAPI handles transport provider activity as a message store is closing.</span></span> 
  
<span data-ttu-id="e7f78-144">Si un autre processus a le magasin à ouvrir pour le même profil, MAPI ignore un appel à **StoreLogoffTransports** et renvoie l’indicateur LOGOFF_COMPLETE dans le paramètre _lpulFlags._</span><span class="sxs-lookup"><span data-stu-id="e7f78-144">If another process has the store to be logged off open for the same profile, MAPI ignores a call to **StoreLogoffTransports** and returns the flag LOGOFF_COMPLETE in the  _lpulFlags_ parameter.</span></span> 
  
<span data-ttu-id="e7f78-145">Le comportement du fournisseur de magasin qui suit le retour de **StoreLogoffTransports** doit être basé sur la valeur de  _lpulFlags_, qui indique l’état du système et transmet les instructions client pour le comportement de la logoff.</span><span class="sxs-lookup"><span data-stu-id="e7f78-145">The behavior of the store provider following the return from **StoreLogoffTransports** should be based on the value of  _lpulFlags_, which indicates system status and conveys client instructions for logoff behavior.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e7f78-146">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="e7f78-146">Notes to callers</span></span>

 <span data-ttu-id="e7f78-147">**StoreLogoffTransports est** généralement appelé à partir de la méthode [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) d’un fournisseur de magasins.</span><span class="sxs-lookup"><span data-stu-id="e7f78-147">**StoreLogoffTransports** is typically called from a store provider's [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) method.</span></span> <span data-ttu-id="e7f78-148">Toutefois, il peut également être appelé à partir de la **méthode IUnknown::Release** de la magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="e7f78-148">However, it can also be called from the **IUnknown::Release** method of the message store.</span></span> <span data-ttu-id="e7f78-149">**Implémentez la** méthode Release de votre magasin de messages pour vérifier si un appel **à StoreLogoffTransports** s’est produit.</span><span class="sxs-lookup"><span data-stu-id="e7f78-149">Implement the **Release** method of your message store so you can check whether or not a call to **StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="e7f78-150">Si un appel ne s’est pas produit, appelez **StoreLogoffTransports** avec l’LOGOFF_ABORT d’appel.</span><span class="sxs-lookup"><span data-stu-id="e7f78-150">If a call has not occurred, call **StoreLogoffTransports** with the LOGOFF_ABORT flag set.</span></span> 
  
<span data-ttu-id="e7f78-151">Le  _paramètre lpulFlags_ est paramétré sur un indicateur qui indique comment le client requiert l’arrêt de la magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="e7f78-151">The  _lpulFlags_ parameter is set to a flag that indicates how the client requires the message store to be shut down.</span></span> <span data-ttu-id="e7f78-152">Déterminez le paramètre approprié pour  _ulFlags_ en fonction du paramètre correspondant dans l’appel **à StoreLogoff**.</span><span class="sxs-lookup"><span data-stu-id="e7f78-152">Determine the appropriate setting for  _ulFlags_ based on the setting of the corresponding parameter in the call to **StoreLogoff**.</span></span> <span data-ttu-id="e7f78-153">Autrement dit, si un client a appelé votre méthode **StoreLogoff** avec  _ulFlags_ définie sur LOGOFF_ORDERLY, vous devez appeler **StoreLogoffTransports** avec  _ulFlags_ définie sur LOGOFF_ORDERLY.</span><span class="sxs-lookup"><span data-stu-id="e7f78-153">That is, if a client called your **StoreLogoff** method with  _ulFlags_ set to LOGOFF_ORDERLY, you should call **StoreLogoffTransports** with  _ulFlags_ set to LOGOFF_ORDERLY.</span></span> 
  
<span data-ttu-id="e7f78-154">Pour plus d’informations sur le processus de fermeture de la boutique de messages, voir [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e7f78-154">For more information about the message store logoff process, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e7f78-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7f78-155">See also</span></span>



[<span data-ttu-id="e7f78-156">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="e7f78-156">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="e7f78-157">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="e7f78-157">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="e7f78-158">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e7f78-158">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

