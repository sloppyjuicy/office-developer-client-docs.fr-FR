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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: be11c536804682d1baec8188b6d7487c71d411e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348740"
---
# <a name="imsgstorestorelogoff"></a><span data-ttu-id="1aa46-103">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="1aa46-103">IMsgStore::StoreLogoff</span></span>

  
  
<span data-ttu-id="1aa46-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1aa46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1aa46-105">Active la déconnexion de la Banque de messages de façon ordonnée.</span><span class="sxs-lookup"><span data-stu-id="1aa46-105">Enables the orderly logoff of the message store.</span></span>
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1aa46-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1aa46-106">Parameters</span></span>

 <span data-ttu-id="1aa46-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="1aa46-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="1aa46-108">[in, out] Masque de des indicateurs qui contrôle la fermeture de session à partir de la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="1aa46-108">[in, out] A bitmask of flags that controls logoff from the message store.</span></span> <span data-ttu-id="1aa46-109">Lors de l'entrée, tous les indicateurs définis pour ce paramètre s'excluent mutuellement; un appelant ne doit spécifier qu'un seul indicateur par appel.</span><span class="sxs-lookup"><span data-stu-id="1aa46-109">On input, all flags set for this parameter are mutually exclusive; a caller must specify only one flag per call.</span></span> <span data-ttu-id="1aa46-110">Les indicateurs suivants sont valides à l'entrée:</span><span class="sxs-lookup"><span data-stu-id="1aa46-110">The following flags are valid on input:</span></span>
    
<span data-ttu-id="1aa46-111">LOGOFF_ABORT</span><span class="sxs-lookup"><span data-stu-id="1aa46-111">LOGOFF_ABORT</span></span> 
  
> <span data-ttu-id="1aa46-112">Toute activité de fournisseur de transport pour cette banque de messages doit être arrêtée avant la fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="1aa46-112">Any transport provider activity for this message store should be stopped before logoff.</span></span> <span data-ttu-id="1aa46-113">Le contrôle est renvoyé à l'appelant une fois l'activité arrêtée.</span><span class="sxs-lookup"><span data-stu-id="1aa46-113">Control is returned to the caller after activity is stopped.</span></span> <span data-ttu-id="1aa46-114">Si une activité de fournisseur de transport est en cours d'exécution, la déconnexion ne se produit pas et aucune modification n'est apportée au comportement du spouleur MAPI ou des fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="1aa46-114">If any transport provider activity is taking place, the logoff does not occur and no change in the behavior of the MAPI spooler or transport providers occurs.</span></span> <span data-ttu-id="1aa46-115">Si l'activité du fournisseur de transport est inactive, le spouleur MAPI libère le magasin.</span><span class="sxs-lookup"><span data-stu-id="1aa46-115">If transport provider activity is idle, the MAPI spooler releases the store.</span></span> 
    
<span data-ttu-id="1aa46-116">LOGOFF_NO_WAIT</span><span class="sxs-lookup"><span data-stu-id="1aa46-116">LOGOFF_NO_WAIT</span></span> 
  
> <span data-ttu-id="1aa46-117">La Banque de messages ne doit pas attendre les messages provenant de fournisseurs de transport avant de se fermer.</span><span class="sxs-lookup"><span data-stu-id="1aa46-117">The message store should not wait for messages from transport providers before closing.</span></span> <span data-ttu-id="1aa46-118">Les messages sortants prêts à être envoyés sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="1aa46-118">Outbound messages that are ready to be sent are sent.</span></span> <span data-ttu-id="1aa46-119">Si ce magasin contient la boîte de réception par défaut, tous les messages en cours de traitement sont reçus, puis la réception supplémentaire est désactivée.</span><span class="sxs-lookup"><span data-stu-id="1aa46-119">If this store contains the default Inbox, any in-process messages are received, and then further reception is disabled.</span></span> <span data-ttu-id="1aa46-120">Une fois toutes les activités terminées, le spouleur MAPI libère le magasin et le contrôle est immédiatement renvoyé à l'appelant.</span><span class="sxs-lookup"><span data-stu-id="1aa46-120">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the caller.</span></span> 
    
<span data-ttu-id="1aa46-121">LOGOFF_ORDERLY</span><span class="sxs-lookup"><span data-stu-id="1aa46-121">LOGOFF_ORDERLY</span></span> 
  
> <span data-ttu-id="1aa46-122">La Banque de messages ne doit pas attendre les informations des fournisseurs de transport avant de se fermer.</span><span class="sxs-lookup"><span data-stu-id="1aa46-122">The message store should not wait for information from transport providers before closing.</span></span> <span data-ttu-id="1aa46-123">Les messages en cours de traitement sont terminés, mais aucun nouveau message n'est traité.</span><span class="sxs-lookup"><span data-stu-id="1aa46-123">Messages that are currently being processed are completed, but no new messages are processed.</span></span> <span data-ttu-id="1aa46-124">Une fois toutes les activités terminées, le spouleur MAPI libère le magasin et le contrôle est immédiatement renvoyé au fournisseur de banque.</span><span class="sxs-lookup"><span data-stu-id="1aa46-124">When all activity is complete, the MAPI spooler releases the store, and control is immediately returned to the store provider.</span></span> 
    
<span data-ttu-id="1aa46-125">LOGOFF_PURGE</span><span class="sxs-lookup"><span data-stu-id="1aa46-125">LOGOFF_PURGE</span></span> 
  
> <span data-ttu-id="1aa46-126">La déconnexion doit fonctionner de la même manière que si l'indicateur LOGOFF_NO_WAIT est défini, mais la méthode [IXPLogon:: FlushQueues](ixplogon-flushqueues.md) ou [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) pour les fournisseurs de transport appropriés doit être appelée.</span><span class="sxs-lookup"><span data-stu-id="1aa46-126">The logoff should work the same as if the LOGOFF_NO_WAIT flag is set, but either the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) or [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method for the appropriate transport providers should be called.</span></span> <span data-ttu-id="1aa46-127">L'indicateur LOGOFF_PURGE renvoie le contrôle à l'appelant une fois l'opération terminée.</span><span class="sxs-lookup"><span data-stu-id="1aa46-127">The LOGOFF_PURGE flag returns control to the caller after completion.</span></span> 
    
<span data-ttu-id="1aa46-128">LOGOFF_QUIET</span><span class="sxs-lookup"><span data-stu-id="1aa46-128">LOGOFF_QUIET</span></span> 
  
> <span data-ttu-id="1aa46-129">Si une activité de fournisseur de transport est en cours, la déconnexion ne doit pas avoir lieu.</span><span class="sxs-lookup"><span data-stu-id="1aa46-129">If any transport provider activity is taking place, the logoff should not occur.</span></span>
    
    The following flags are valid on output:
    
<span data-ttu-id="1aa46-130">LOGOFF_INBOUND</span><span class="sxs-lookup"><span data-stu-id="1aa46-130">LOGOFF_INBOUND</span></span> 
  
> <span data-ttu-id="1aa46-131">Les messages entrants arrivent actuellement.</span><span class="sxs-lookup"><span data-stu-id="1aa46-131">Inbound messages are currently arriving.</span></span>
    
<span data-ttu-id="1aa46-132">LOGOFF_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="1aa46-132">LOGOFF_OUTBOUND</span></span> 
  
> <span data-ttu-id="1aa46-133">Les messages sortants sont en cours d'envoi.</span><span class="sxs-lookup"><span data-stu-id="1aa46-133">Outbound messages are in the process of being sent.</span></span>
    
<span data-ttu-id="1aa46-134">LOGOFF_OUTBOUND_QUEUE</span><span class="sxs-lookup"><span data-stu-id="1aa46-134">LOGOFF_OUTBOUND_QUEUE</span></span> 
  
> <span data-ttu-id="1aa46-135">Les messages sortants sont en attente (ils se trouvent dans la boîte d'envoi).</span><span class="sxs-lookup"><span data-stu-id="1aa46-135">Outbound messages are pending (that is, they are in the Outbox).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1aa46-136">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1aa46-136">Return value</span></span>

<span data-ttu-id="1aa46-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="1aa46-137">S_OK</span></span> 
  
> <span data-ttu-id="1aa46-138">La déconnexion s'est déroulée correctement.</span><span class="sxs-lookup"><span data-stu-id="1aa46-138">The logoff completed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1aa46-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="1aa46-139">Remarks</span></span>

<span data-ttu-id="1aa46-140">La méthode **IMsgStore:: StoreLogoff** exerce un contrôle sur l'interaction de la Banque de messages et des fournisseurs de transport lors du processus de fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="1aa46-140">The **IMsgStore::StoreLogoff** method exerts control over the interaction of the message store and transport providers during the logoff process.</span></span> <span data-ttu-id="1aa46-141">L'appel de **StoreLogoff** est valide uniquement pour les banques de messages qui sont utilisées uniquement par l'appelant.</span><span class="sxs-lookup"><span data-stu-id="1aa46-141">Calling **StoreLogoff** is valid only for message stores that are being used only by the caller.</span></span> <span data-ttu-id="1aa46-142">Par exemple, lorsque deux clients utilisent le même magasin de messages et que l'un d'entre eux appelle **StoreLogoff**, la Banque de messages est immédiatement libérée et le contrôle est renvoyé au client appelant.</span><span class="sxs-lookup"><span data-stu-id="1aa46-142">For example, when two clients are using the same message store and one of them calls **StoreLogoff**, the message store is immediately released and control is returned to the calling client.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1aa46-143">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="1aa46-143">Notes to implementers</span></span>

<span data-ttu-id="1aa46-144">Enregistrez les indicateurs transmis à **StoreLogoff** et transmettez-les lorsque vous appelez la méthode [IMAPISupport:: StoreLogoffTransports](imapisupport-storelogofftransports.md) .</span><span class="sxs-lookup"><span data-stu-id="1aa46-144">Save the flags that are passed to **StoreLogoff** and pass them when you call the [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) method.</span></span> <span data-ttu-id="1aa46-145">N'appelez pas **StoreLogoffTransports** tant que le nombre de références de la Banque de messages n'est pas inférieur à zéro.</span><span class="sxs-lookup"><span data-stu-id="1aa46-145">Do not call **StoreLogoffTransports** until the message store's reference count drops to zero.</span></span> <span data-ttu-id="1aa46-146">Plusieurs appels à **StoreLogoffTransports** remplacent simplement les indicateurs enregistrés.</span><span class="sxs-lookup"><span data-stu-id="1aa46-146">Multiple calls to **StoreLogoffTransports** simply overwrite the saved flags.</span></span> 
  
<span data-ttu-id="1aa46-147">Si aucun appel n'a été passé à **StoreLogoff** avant que le nombre de références de la Banque de messages n'atteigne zéro, définissez l'indicateur LOGOFF_ABORT dans le paramètre _ulFlags_ que vous transmettez à **StoreLogoffTransports**.</span><span class="sxs-lookup"><span data-stu-id="1aa46-147">If no call has been made to **StoreLogoff** before the message store's reference count reaches zero, set the LOGOFF_ABORT flag in the  _ulFlags_ parameter that you pass to **StoreLogoffTransports**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1aa46-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1aa46-148">See also</span></span>



[<span data-ttu-id="1aa46-149">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="1aa46-149">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="1aa46-150">IMAPISupport::StoreLogoffTransports</span><span class="sxs-lookup"><span data-stu-id="1aa46-150">IMAPISupport::StoreLogoffTransports</span></span>](imapisupport-storelogofftransports.md)
  
[<span data-ttu-id="1aa46-151">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="1aa46-151">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
  
[<span data-ttu-id="1aa46-152">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1aa46-152">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

