---
title: IMsgStoreStoreLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.StoreLogoff
api_type:
- COM
ms.assetid: 3773c98e-531e-4bdc-a39a-2c3bb7378cd3
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 2ac8fb6f4e56b6f086e6061c227120cd49fc621a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784261"
---
# <a name="imsgstorestorelogoff"></a><span data-ttu-id="296e7-103">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="296e7-103">IMsgStore::StoreLogoff</span></span>

  
  
<span data-ttu-id="296e7-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="296e7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="296e7-105">Permet la déconnexion ordonnée de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="296e7-105">Enables the orderly logoff of the message store.</span></span>
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="296e7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="296e7-106">Parameters</span></span>

 <span data-ttu-id="296e7-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="296e7-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="296e7-108">[entrée, sortie] Masque de bits d’indicateurs qui contrôle la fermeture de session à partir de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="296e7-108">[in, out] A bitmask of flags that controls logoff from the message store.</span></span> <span data-ttu-id="296e7-109">À l’entrée, tous les indicateurs de ce paramètre sont mutuellement ; l’appelant doit spécifier qu’un seul indicateur par appel.</span><span class="sxs-lookup"><span data-stu-id="296e7-109">On input, all flags set for this parameter are mutually exclusive; a caller must specify only one flag per call.</span></span> <span data-ttu-id="296e7-110">Les indicateurs suivants sont valides sur ENTRÉE :</span><span class="sxs-lookup"><span data-stu-id="296e7-110">The following flags are valid on input:</span></span>
    
<span data-ttu-id="296e7-111">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="296e7-111">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="296e7-112">Toute activité du fournisseur de transport pour cette banque de messages doit être arrêtée avant la fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="296e7-112">Any transport provider activity for this message store should be stopped before logoff.</span></span> <span data-ttu-id="296e7-113">Contrôle est renvoyé à l’appelant une fois que l’activité est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="296e7-113">Control is returned to the caller after activity is stopped.</span></span> <span data-ttu-id="296e7-114">Si aucune activité de fournisseur de transport a lieu, la fermeture de session ne se produit pas et aucune modification du comportement des fournisseurs de transport ou spouleur MAPI se produit.</span><span class="sxs-lookup"><span data-stu-id="296e7-114">If any transport provider activity is taking place, the logoff does not occur and no change in the behavior of the MAPI spooler or transport providers occurs.</span></span> <span data-ttu-id="296e7-115">Si l’activité de fournisseur de transport est inactive, le spouleur MAPI libère le magasin.</span><span class="sxs-lookup"><span data-stu-id="296e7-115">If transport provider activity is idle, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="296e7-116">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="296e7-116">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="296e7-117">La banque de messages ne doit pas attendre pour les messages de fournisseurs de transport avant la fermeture.</span><span class="sxs-lookup"><span data-stu-id="296e7-117">The message store should not wait for messages from transport providers before closing.</span></span> <span data-ttu-id="296e7-118">Les messages sortants qui sont prêts à être envoyés sont envoyées.</span><span class="sxs-lookup"><span data-stu-id="296e7-118">Outbound messages that are ready to be sent are sent.</span></span> <span data-ttu-id="296e7-119">Si ce magasin contient la boîte de réception par défaut, tous les messages en cours sont reçus, puis réception supplémentaire est désactivée.</span><span class="sxs-lookup"><span data-stu-id="296e7-119">If this store contains the default Inbox, any in-process messages are received, and then further reception is disabled.</span></span> <span data-ttu-id="296e7-120">Lorsque toutes les activités sont terminée, le spouleur MAPI libère le magasin et contrôle est immédiatement renvoyé à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="296e7-120">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the caller.</span></span> 
    
<span data-ttu-id="296e7-121">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="296e7-121">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="296e7-122">La banque de messages ne doit pas attendre pour plus d’informations à partir des fournisseurs de transport avant de se fermer.</span><span class="sxs-lookup"><span data-stu-id="296e7-122">The message store should not wait for information from transport providers before closing.</span></span> <span data-ttu-id="296e7-123">Les messages qui sont actuellement en cours de traitement sont terminées, mais aucuns nouveaux messages ne sont traités.</span><span class="sxs-lookup"><span data-stu-id="296e7-123">Messages that are currently being processed are completed, but no new messages are processed.</span></span> <span data-ttu-id="296e7-124">Lorsque toutes les activités sont terminée, le spouleur MAPI libère le magasin et contrôle est immédiatement renvoyé au fournisseur de magasin.</span><span class="sxs-lookup"><span data-stu-id="296e7-124">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the store provider.</span></span> 
    
<span data-ttu-id="296e7-125">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="296e7-125">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="296e7-126">La fermeture de session doit utiliser la même comme si l’indicateur LOGOFF_NO_WAIT est défini, mais la [IXPLogon::FlushQueues](ixplogon-flushqueues.md) [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) méthode ou pour les fournisseurs de transport approprié doit être appelée.</span><span class="sxs-lookup"><span data-stu-id="296e7-126">The logoff should work the same as if the LOGOFF_NO_WAIT flag is set, but either the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) or [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method for the appropriate transport providers should be called.</span></span> <span data-ttu-id="296e7-127">L’indicateur LOGOFF_PURGE retourne le contrôle à l’appelant après la fin.</span><span class="sxs-lookup"><span data-stu-id="296e7-127">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="296e7-128">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="296e7-128">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="296e7-129">Si aucune activité de fournisseur de transport a lieu, la fermeture de session ne doit pas se produire.</span><span class="sxs-lookup"><span data-stu-id="296e7-129">If any transport provider activity is taking place, the logoff should not occur.</span></span>
    
    The following flags are valid on output:
    
<span data-ttu-id="296e7-130">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="296e7-130">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="296e7-131">Les messages entrants arrivent actuellement.</span><span class="sxs-lookup"><span data-stu-id="296e7-131">Inbound messages are currently arriving.</span></span>
    
<span data-ttu-id="296e7-132">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="296e7-132">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="296e7-133">Les messages sortants sont en cours d’envoi.</span><span class="sxs-lookup"><span data-stu-id="296e7-133">Outbound messages are in the process of being sent.</span></span>
    
<span data-ttu-id="296e7-134">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="296e7-134">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="296e7-135">Les messages sortants sont en attente (autrement dit, ils sont dans la boîte d’envoi).</span><span class="sxs-lookup"><span data-stu-id="296e7-135">Outbound messages are pending (that is, they are in the Outbox).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="296e7-136">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="296e7-136">Return value</span></span>

<span data-ttu-id="296e7-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="296e7-137">S_OK</span></span> 
  
> <span data-ttu-id="296e7-138">La fermeture de session s’est terminée correctement.</span><span class="sxs-lookup"><span data-stu-id="296e7-138">The logoff completed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="296e7-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="296e7-139">Remarks</span></span>

<span data-ttu-id="296e7-140">La méthode **IMsgStore::StoreLogoff** exerce de contrôle sur l’interaction du message stocker et fournisseurs de transport au cours du processus de fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="296e7-140">The **IMsgStore::StoreLogoff** method exerts control over the interaction of the message store and transport providers during the logoff process.</span></span> <span data-ttu-id="296e7-141">L’appel **StoreLogoff** est valide uniquement pour les banques de messages qui sont utilisés uniquement par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="296e7-141">Calling **StoreLogoff** is valid only for message stores that are being used only by the caller.</span></span> <span data-ttu-id="296e7-142">Par exemple, lorsque deux clients utilisent le même magasin de message et un d'entre eux appelle **StoreLogoff**, la banque de messages est immédiatement publiée et le contrôle est retourné au client appelant.</span><span class="sxs-lookup"><span data-stu-id="296e7-142">For example, when two clients are using the same message store and one of them calls **StoreLogoff**, the message store is immediately released and control is returned to the calling client.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="296e7-143">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="296e7-143">Notes to implementers</span></span>

<span data-ttu-id="296e7-144">Enregistrez les indicateurs qui sont passés à **StoreLogoff** et transmettez-les lorsque vous appelez la méthode [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) .</span><span class="sxs-lookup"><span data-stu-id="296e7-144">Save the flags that are passed to **StoreLogoff** and pass them when you call the [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) method.</span></span> <span data-ttu-id="296e7-145">N’appelez pas **StoreLogoffTransports** jusqu'à ce que le décompte de références de la banque de messages tombe à zéro.</span><span class="sxs-lookup"><span data-stu-id="296e7-145">Do not call **StoreLogoffTransports** until the message store's reference count drops to zero.</span></span> <span data-ttu-id="296e7-146">Plusieurs appels à **StoreLogoffTransports** remplacent simplement les indicateurs enregistrés.</span><span class="sxs-lookup"><span data-stu-id="296e7-146">Multiple calls to **StoreLogoffTransports** simply overwrite the saved flags.</span></span> 
  
<span data-ttu-id="296e7-147">Si aucun appel n’a été apporté à **StoreLogoff** avant le message décompte de références du magasin est égal à zéro, définir l’indicateur LOGOFF_ABORT dans le paramètre _ulFlags_ que vous passez à **StoreLogoffTransports**.</span><span class="sxs-lookup"><span data-stu-id="296e7-147">If no call has been made to **StoreLogoff** before the message store's reference count reaches zero, set the LOGOFF_ABORT flag in the  _ulFlags_ parameter that you pass to **StoreLogoffTransports**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="296e7-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="296e7-148">See also</span></span>



[<span data-ttu-id="296e7-149">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="296e7-149">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="296e7-150">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="296e7-150">IMAPISupport::StoreLogoffTransports</span></span>](imapisupport-storelogofftransports.md)
  
[<span data-ttu-id="296e7-151">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="296e7-151">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="296e7-152">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="296e7-152">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

