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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 6624c4abf05dc7df9fc79df43f1d0fe76251d052
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784062"
---
# <a name="imapisupportstorelogofftransports"></a><span data-ttu-id="6d126-103">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="6d126-103">IMAPISupport::StoreLogoffTransports</span></span>

  
  
<span data-ttu-id="6d126-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6d126-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6d126-105">Demande la version ordonnée d’une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="6d126-105">Requests the orderly release of a message store.</span></span>
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="6d126-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d126-106">Parameters</span></span>

 <span data-ttu-id="6d126-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="6d126-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="6d126-108">[entrée, sortie] Masque de bits d’indicateurs qui contrôle la déconnexion de la banque message se produit.</span><span class="sxs-lookup"><span data-stu-id="6d126-108">[in, out] A bitmask of flags that controls how message store logoff occurs.</span></span> <span data-ttu-id="6d126-109">À l’entrée, tous les indicateurs pour ce paramètre sont mutuellement ; seul un des indicateurs suivants peut être défini par l’appel :</span><span class="sxs-lookup"><span data-stu-id="6d126-109">On input, all flags for this parameter are mutually exclusive; only one of the following flags can be set per call:</span></span>
    
<span data-ttu-id="6d126-110">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="6d126-110">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="6d126-111">Toute activité du fournisseur de transport pour ce magasin doit être arrêtée avant la fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="6d126-111">Any transport provider activity for this store should be stopped before logoff.</span></span> <span data-ttu-id="6d126-112">Contrôle est retourné au client une fois que l’activité est arrêtée et le spouleur MAPI est déconnecté de la banque.</span><span class="sxs-lookup"><span data-stu-id="6d126-112">Control is returned to the client after the activity is stopped and the MAPI spooler has logged off the store.</span></span> <span data-ttu-id="6d126-113">Si aucune activité de transport a lieu, la fermeture de session ne se produit pas et aucune modification dans le comportement du fournisseur MAPI spouleur ou de transport a lieu.</span><span class="sxs-lookup"><span data-stu-id="6d126-113">If any transport activity is taking place, the logoff does not occur and no change in the MAPI spooler or transport provider behavior occurs.</span></span> <span data-ttu-id="6d126-114">S’il n’existe actuellement aucune activité, le spouleur MAPI libère le magasin.</span><span class="sxs-lookup"><span data-stu-id="6d126-114">If there is currently no activity, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="6d126-115">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="6d126-115">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="6d126-116">Le spouleur MAPI doit libérer le magasin et retourner le contrôle au client immédiatement les messages sortants après tout qui est prêt à être envoyé.</span><span class="sxs-lookup"><span data-stu-id="6d126-116">The MAPI spooler should release the store and return control to the client immediately after all outbound mail that is ready to be sent is sent.</span></span> <span data-ttu-id="6d126-117">Si la banque de messages est la boîte de réception par défaut, tout message en cours est reçu, puis réception supplémentaire est désactivée.</span><span class="sxs-lookup"><span data-stu-id="6d126-117">If the message store has the default Inbox, any in-process message is received, and then further reception is disabled.</span></span> 
    
<span data-ttu-id="6d126-118">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="6d126-118">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="6d126-119">Le spouleur MAPI doit libérer le magasin et retourner le contrôle au client dès l’appel en attente de messages sont terminées de traitement.</span><span class="sxs-lookup"><span data-stu-id="6d126-119">The MAPI spooler should release the store and return control to the client immediately after any pending messages are finished processing.</span></span> <span data-ttu-id="6d126-120">Aucuns nouveaux messages ne doivent être traités.</span><span class="sxs-lookup"><span data-stu-id="6d126-120">No new messages should be processed.</span></span> 
    
<span data-ttu-id="6d126-121">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="6d126-121">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="6d126-122">Fonctionnement de la même que l’indicateur LOGOFF_NO_WAIT.</span><span class="sxs-lookup"><span data-stu-id="6d126-122">Works the same as the LOGOFF_NO_WAIT flag.</span></span> <span data-ttu-id="6d126-123">L’indicateur LOGOFF_PURGE retourne le contrôle à l’appelant après la fin.</span><span class="sxs-lookup"><span data-stu-id="6d126-123">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="6d126-124">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="6d126-124">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="6d126-125">La fermeture de session ne doit pas se produire si une activité de fournisseur de transport a lieu.</span><span class="sxs-lookup"><span data-stu-id="6d126-125">The logoff should not occur if any transport provider activity is taking place.</span></span> <span data-ttu-id="6d126-126">Le type d’activité en cours est renvoyé comme un indicateur de sortie.</span><span class="sxs-lookup"><span data-stu-id="6d126-126">The type of activity taking place is returned as a flag on output.</span></span>
    
    On output, MAPI spooler can return one or more of the following flags:
    
<span data-ttu-id="6d126-127">LOGOFF_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="6d126-127">LOGOFF_COMPLETE</span></span> 
  
> <span data-ttu-id="6d126-128">Procéder à la fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="6d126-128">The logoff can complete.</span></span> <span data-ttu-id="6d126-129">Toutes les ressources associées au magasin ont été publiées, et l’objet a été désactivé.</span><span class="sxs-lookup"><span data-stu-id="6d126-129">All resources associated with the store have been released, and the object has been invalidated.</span></span> <span data-ttu-id="6d126-130">Le spouleur MAPI a effectué ou effectuera toutes les demandes.</span><span class="sxs-lookup"><span data-stu-id="6d126-130">The MAPI spooler has performed or will perform all requests.</span></span> <span data-ttu-id="6d126-131">Uniquement les méthode **IUnknown::Release** de la banque de messages doivent être appelée à ce stade.</span><span class="sxs-lookup"><span data-stu-id="6d126-131">Only the message store's **IUnknown::Release** method should be called at this point.</span></span> 
    
<span data-ttu-id="6d126-132">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="6d126-132">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="6d126-133">Un message est actuellement provenant dans le magasin d’un ou plusieurs fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="6d126-133">A message is currently coming into the store from one or more transport providers.</span></span> 
    
<span data-ttu-id="6d126-134">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="6d126-134">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="6d126-135">Un message est actuellement en cours envoyé à partir de la banque par un ou plusieurs fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="6d126-135">A message is currently being sent from the store by one or more transport providers.</span></span> 
    
<span data-ttu-id="6d126-136">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="6d126-136">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="6d126-137">Il existe actuellement des messages dans la file d’attente sortante pour le magasin.</span><span class="sxs-lookup"><span data-stu-id="6d126-137">There are currently messages in the outbound queue for the store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6d126-138">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="6d126-138">Return value</span></span>

<span data-ttu-id="6d126-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="6d126-139">S_OK</span></span> 
  
> <span data-ttu-id="6d126-140">La procédure de fermeture de session a réussi.</span><span class="sxs-lookup"><span data-stu-id="6d126-140">The logoff procedure was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6d126-141">Remarques</span><span class="sxs-lookup"><span data-stu-id="6d126-141">Remarks</span></span>

<span data-ttu-id="6d126-142">La méthode **IMAPISupport::StoreLogoffTransports** est implémentée pour les objets de prise en charge de fournisseur de magasin de message.</span><span class="sxs-lookup"><span data-stu-id="6d126-142">The **IMAPISupport::StoreLogoffTransports** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="6d126-143">Fournisseurs de magasins message appellent **StoreLogoffTransports** pour fournir des applications clientes contrôler la fermeture d’activité de fournisseur de transport de handles MAPI comme une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="6d126-143">Message store providers call **StoreLogoffTransports** to give client applications some control over how MAPI handles transport provider activity as a message store is closing.</span></span> 
  
<span data-ttu-id="6d126-144">Si un autre processus a le magasin de session ouvrir pour le même profil, MAPI ignore un appel à **StoreLogoffTransports** et retourne l’indicateur LOGOFF_COMPLETE dans le paramètre _lpulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="6d126-144">If another process has the store to be logged off open for the same profile, MAPI ignores a call to **StoreLogoffTransports** and returns the flag LOGOFF_COMPLETE in the  _lpulFlags_ parameter.</span></span> 
  
<span data-ttu-id="6d126-145">Le comportement du fournisseur de banque après le retour de **StoreLogoffTransports** doit être basé sur la valeur de _lpulFlags_, qui indique l’état du système et des instructions pour le comportement de fermeture de session client dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6d126-145">The behavior of the store provider following the return from **StoreLogoffTransports** should be based on the value of  _lpulFlags_, which indicates system status and conveys client instructions for logoff behavior.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6d126-146">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="6d126-146">Notes to callers</span></span>

 <span data-ttu-id="6d126-147">**StoreLogoffTransports** est généralement appelée à partir [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) méthode d’un fournisseur de magasins.</span><span class="sxs-lookup"><span data-stu-id="6d126-147">**StoreLogoffTransports** is typically called from a store provider's [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) method.</span></span> <span data-ttu-id="6d126-148">Toutefois, il peut également être appelée à partir de la méthode **IUnknown::Release** de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="6d126-148">However, it can also be called from the **IUnknown::Release** method of the message store.</span></span> <span data-ttu-id="6d126-149">Implémentez la méthode de **publication** de vos messages afin de pouvoir vérifier si un appel à **StoreLogoffTransports** s’est produite.</span><span class="sxs-lookup"><span data-stu-id="6d126-149">Implement the **Release** method of your message store so you can check whether or not a call to **StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="6d126-150">Si un appel n’a pas eu lieu, appelez **StoreLogoffTransports** avec l’indicateur LOGOFF_ABORT.</span><span class="sxs-lookup"><span data-stu-id="6d126-150">If a call has not occurred, call **StoreLogoffTransports** with the LOGOFF_ABORT flag set.</span></span> 
  
<span data-ttu-id="6d126-151">Le paramètre _lpulFlags_ est défini à un indicateur qui indique comment le client requiert la banque de messages à arrêter.</span><span class="sxs-lookup"><span data-stu-id="6d126-151">The  _lpulFlags_ parameter is set to a flag that indicates how the client requires the message store to be shut down.</span></span> <span data-ttu-id="6d126-152">Déterminez le paramètre approprié pour _ulFlags_ en fonction de la valeur du paramètre dans l’appel de **StoreLogoff**correspondant.</span><span class="sxs-lookup"><span data-stu-id="6d126-152">Determine the appropriate setting for  _ulFlags_ based on the setting of the corresponding parameter in the call to **StoreLogoff**.</span></span> <span data-ttu-id="6d126-153">Autrement dit, si un client appelé votre méthode **StoreLogoff** avec _ulFlags_ défini sur LOGOFF_ORDERLY, vous devez appeler **StoreLogoffTransports** avec _ulFlags_ défini sur LOGOFF_ORDERLY.</span><span class="sxs-lookup"><span data-stu-id="6d126-153">That is, if a client called your **StoreLogoff** method with  _ulFlags_ set to LOGOFF_ORDERLY, you should call **StoreLogoffTransports** with  _ulFlags_ set to LOGOFF_ORDERLY.</span></span> 
  
<span data-ttu-id="6d126-154">Pour plus d’informations sur le processus de fermeture de session de magasin de messages, voir [Arrêt vers le bas un Message Store Provider](shutting-down-a-message-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6d126-154">For more information about the message store logoff process, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6d126-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d126-155">See also</span></span>



[<span data-ttu-id="6d126-156">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="6d126-156">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="6d126-157">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="6d126-157">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="6d126-158">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6d126-158">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

