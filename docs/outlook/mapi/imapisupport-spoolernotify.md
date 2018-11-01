---
title: IMAPISupportSpoolerNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SpoolerNotify
api_type:
- COM
ms.assetid: d4f153b2-939f-4153-85fb-dc510193848c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a2837e5470729ae3cdd0b83e17d0342620c986e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592114"
---
# <a name="imapisupportspoolernotify"></a><span data-ttu-id="cf8f1-103">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="cf8f1-103">IMAPISupport::SpoolerNotify</span></span>

  
  
<span data-ttu-id="cf8f1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf8f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf8f1-105">Notifie le spouleur MAPI d’un changement de statut ou une demande de service.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-105">Notifies the MAPI spooler of a change in status or a request for service.</span></span> 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a><span data-ttu-id="cf8f1-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="cf8f1-106">Parameters</span></span>

 <span data-ttu-id="cf8f1-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cf8f1-107">_ulFlags_</span></span>
  
> <span data-ttu-id="cf8f1-108">[in] Masque de bits d’indicateurs qui indique le type de notification.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-108">[in] A bitmask of flags that indicates the type of notification.</span></span> <span data-ttu-id="cf8f1-109">Fournisseurs de transport peuvent définir tous les indicateurs à l’exception de NOTIFY_NEWMAIL_RECEIVED ; uniquement NOTIFY_NEWMAIL_RECEIVED et NOTIFY_READTOSEND sont valides pour les fournisseurs de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-109">Transport providers can set all of the flags except for NOTIFY_NEWMAIL_RECEIVED; only NOTIFY_NEWMAIL_RECEIVED and NOTIFY_READTOSEND are valid for message store providers.</span></span> <span data-ttu-id="cf8f1-110">Les indicateurs suivants sont valides pour le paramètre _ulFlags_ :</span><span class="sxs-lookup"><span data-stu-id="cf8f1-110">The following flags are valid for the  _ulFlags_ parameter:</span></span> 
    
<span data-ttu-id="cf8f1-111">NOTIFY_CONFIG_CHANGE</span><span class="sxs-lookup"><span data-stu-id="cf8f1-111">NOTIFY_CONFIG_CHANGE</span></span> 
  
> <span data-ttu-id="cf8f1-112">Enregistre une demande de modification de configuration du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-112">Registers a request to change the transport provider's configuration.</span></span> 
    
<span data-ttu-id="cf8f1-113">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="cf8f1-113">NOTIFY_CRITICAL_ERROR</span></span> 
  
> <span data-ttu-id="cf8f1-114">Une erreur irrécupérable s’est produite au fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-114">An unrecoverable error has occurred to the transport provider.</span></span> <span data-ttu-id="cf8f1-115">Étant donné que les deux NOTIFY_SENTDEFERRED et NOTIFY_CRITICAL_ERROR utilisent le paramètre _lpvData_ pour les appels de fournisseur de transport, ces indicateurs s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-115">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter for transport provider calls, these flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="cf8f1-116">NOTIFY_CRITSEC</span><span class="sxs-lookup"><span data-stu-id="cf8f1-116">NOTIFY_CRITSEC</span></span> 
  
> <span data-ttu-id="cf8f1-117">Demande une section critique pour le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-117">Requests a critical section for the transport provider.</span></span> <span data-ttu-id="cf8f1-118">Le paramètre _lpvData_ n’est pas défini et doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-118">The  _lpvData_ parameter is undefined and should be NULL.</span></span> 
    
<span data-ttu-id="cf8f1-119">NOTIFY_NEWMAIL</span><span class="sxs-lookup"><span data-stu-id="cf8f1-119">NOTIFY_NEWMAIL</span></span> 
  
> <span data-ttu-id="cf8f1-120">Le spouleur MAPI doit télécharger tous les messages reçus récemment à la prochaine heure disponible.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-120">The MAPI spooler should download any newly received messages at the next available time.</span></span> <span data-ttu-id="cf8f1-121">Le paramètre _lpvData_ n’est pas défini et doit être défini avec la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-121">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="cf8f1-122">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="cf8f1-122">NOTIFY_NEWMAIL_RECEIVED</span></span> 
  
> <span data-ttu-id="cf8f1-123">Un nouveau message a été reçu dans la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-123">A new message has been received in the message store.</span></span> <span data-ttu-id="cf8f1-124">Le paramètre _lpvData_ pointe vers une structure [NEWMAIL_NOTIFICATION](newmail_notification.md) qui décrit le message.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-124">The  _lpvData_ parameter points to a [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that describes the message.</span></span> <span data-ttu-id="cf8f1-125">Cet indicateur est utilisé pour les fournisseurs de banque de messages qui sont étroitement liés à des fournisseurs de transport et est ignoré si le fournisseur de banque est connecté avec l’indicateur MAPI_NO_MAIL.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-125">This flag is used for message store providers that are tightly coupled with transport providers and is ignored if the store provider is logged on with the MAPI_NO_MAIL flag set.</span></span> 
    
<span data-ttu-id="cf8f1-126">NOTIFY_NONCRIT</span><span class="sxs-lookup"><span data-stu-id="cf8f1-126">NOTIFY_NONCRIT</span></span> 
  
> <span data-ttu-id="cf8f1-127">Publie une section critique qui a été obtenue par un appel précédent à **SpoolerNotify** avec _ulFlags_ défini sur NOTIFY_CRITSEC.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-127">Releases a critical section that was obtained with a previous call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="cf8f1-128">Le paramètre _lpvData_ n’est pas défini et doit être défini avec la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-128">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="cf8f1-129">NOTIFY_READYTOSEND</span><span class="sxs-lookup"><span data-stu-id="cf8f1-129">NOTIFY_READYTOSEND</span></span> 
  
> <span data-ttu-id="cf8f1-130">Le fournisseur de magasin de transport ou d’un message est prêt à envoyer des messages.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-130">The transport or message store provider is ready to send messages.</span></span> <span data-ttu-id="cf8f1-131">Le paramètre _lpvData_ n’est pas défini et doit être défini avec la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-131">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="cf8f1-132">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="cf8f1-132">NOTIFY_SENTDEFERRED</span></span> 
  
> <span data-ttu-id="cf8f1-133">Un message précédemment différé doit maintenant être envoyé et le fournisseur de transport doit être averti lorsque le message est prêt à être remis à l’aide d’un appel à la méthode [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="cf8f1-133">A previously deferred message should now be sent, and the transport provider should be notified when the message is ready to be delivered by using a call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> <span data-ttu-id="cf8f1-134">L’identificateur d’entrée du message différé est contenue dans une structure [SBinary](sbinary.md) désignée par _lpvData_.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-134">The entry identifier of the deferred message is contained in an [SBinary](sbinary.md) structure pointed to by  _lpvData_.</span></span> <span data-ttu-id="cf8f1-135">Étant donné que les deux NOTIFY_SENTDEFERRED et NOTIFY_CRITICAL_ERROR utilisent le paramètre _lpvData_ , ces indicateurs s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-135">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter, these flags are mutually exclusive.</span></span> 
    
 <span data-ttu-id="cf8f1-136">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="cf8f1-136">_lpvData_</span></span>
  
> <span data-ttu-id="cf8f1-137">[in] Pointeur vers les données associées applicables à une notification.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-137">[in] A pointer to associated data applicable to a notification.</span></span> <span data-ttu-id="cf8f1-138">Le paramètre _lpvData_ pointe vers des données valides uniquement lorsque les indicateurs suivants sont définis (_lpvData_ est NULL lorsque _ulFlags_ est défini sur les autres types de notification) :</span><span class="sxs-lookup"><span data-stu-id="cf8f1-138">The  _lpvData_ parameter points to valid data only when the following flags are set (_lpvData_ is NULL when  _ulFlags_ is set to the other notification types):</span></span> 
    
|<span data-ttu-id="cf8f1-139">**paramètre _ulFlags_**</span><span class="sxs-lookup"><span data-stu-id="cf8f1-139">**_ulFlags_ setting**</span></span>|<span data-ttu-id="cf8f1-140">**valeur _lpvData_**</span><span class="sxs-lookup"><span data-stu-id="cf8f1-140">**_lpvData_ value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf8f1-141">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="cf8f1-141">NOTIFY_CRITICAL_ERROR</span></span>  <br/> |<span data-ttu-id="cf8f1-142">Informations sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-142">Information about the error.</span></span>  <br/> |
|<span data-ttu-id="cf8f1-143">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="cf8f1-143">NOTIFY_NEWMAIL_RECEIVED</span></span>  <br/> |<span data-ttu-id="cf8f1-144">Une structure **NEWMAIL_NOTIFICATION** qui contient des informations sur le message nouvellement remis.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-144">A **NEWMAIL_NOTIFICATION** structure that contains information about the newly delivered message.</span></span>  <br/> |
|<span data-ttu-id="cf8f1-145">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="cf8f1-145">NOTIFY_SENTDEFERRED</span></span>  <br/> |<span data-ttu-id="cf8f1-146">Une structure **SBinary** qui contient l’identificateur d’entrée du message différé.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-146">An **SBinary** structure that contains the entry identifier of deferred message.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="cf8f1-147">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cf8f1-147">Return value</span></span>

<span data-ttu-id="cf8f1-148">S_OK</span><span class="sxs-lookup"><span data-stu-id="cf8f1-148">S_OK</span></span> 
  
> <span data-ttu-id="cf8f1-149">La notification a réussi.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-149">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cf8f1-150">Remarques</span><span class="sxs-lookup"><span data-stu-id="cf8f1-150">Remarks</span></span>

<span data-ttu-id="cf8f1-151">La méthode **IMAPISupport::SpoolerNotify** est implémentée pour message stocker et transporter des objets du fournisseur de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-151">The **IMAPISupport::SpoolerNotify** method is implemented for message store and transport provider support objects.</span></span> <span data-ttu-id="cf8f1-152">Ces fournisseurs appellent **SpoolerNotify** pour notifier le spouleur MAPI d’un changement de statut ou une demande de service.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-152">These providers call **SpoolerNotify** to notify the MAPI spooler of a change in status or a request for service.</span></span> <span data-ttu-id="cf8f1-153">**SpoolerNotify** est appelé principalement par les fournisseurs de transport et peut être appelé à tout moment pendant la session.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-153">**SpoolerNotify** is called primarily by transport providers and may be called at any time during the session.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="cf8f1-154">Remarques pour les fournisseurs de Transport</span><span class="sxs-lookup"><span data-stu-id="cf8f1-154">Notes to Transport Providers</span></span>

<span data-ttu-id="cf8f1-155">Si vous avez modifié la configuration de votre fournisseur de transport, appelez **SpoolerNotify** et NOTIFY_CONFIG_CHANGED la valeur _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="cf8f1-155">If you have changed your transport provider configuration, call **SpoolerNotify** and set  _ulFlags_ to NOTIFY_CONFIG_CHANGED.</span></span> <span data-ttu-id="cf8f1-156">**SpoolerNotify** répond en appelant la méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) pour interroger une modification dans les types d’adresse pris en charge.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-156">**SpoolerNotify** responds by calling the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to query for a change in supported address types.</span></span> 
  
<span data-ttu-id="cf8f1-157">Si vous avez besoin d’une section critique pour assurer le traitement ininterrompu, appelez **SpoolerNotify** avec _ulFlags_ défini sur NOTIFY_CRITSEC.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-157">If you need a critical section to ensure uninterrupted processing, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="cf8f1-158">Définition de cet indicateur informe le spouleur MAPI qu’elle ne doit pas appeler les méthodes [IXPLogon::Idle](ixplogon-idle.md) et [IXPLogon::Poll](ixplogon-poll.md) .</span><span class="sxs-lookup"><span data-stu-id="cf8f1-158">Setting this flag informs the MAPI spooler that it should not call the [IXPLogon::Idle](ixplogon-idle.md) and [IXPLogon::Poll](ixplogon-poll.md) methods.</span></span> <span data-ttu-id="cf8f1-159">Alors que vous avez une section critique ouvert, retourne MAPI_E_BUSY chaque fois que la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-159">While you have a critical section open, return MAPI_E_BUSY whenever the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is called.</span></span> <span data-ttu-id="cf8f1-160">Lorsque vous avez terminé avec la section critique, appelez une autre **SpoolerNotify** avec _ulFlags_ défini sur NOTIFY_NONCRIT.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-160">When you are finished with the critical section, make another call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NONCRIT.</span></span> 
  
<span data-ttu-id="cf8f1-161">Par exemple, si votre fournisseur de transport à distance est en cours de téléchargement des messages, vous devrez peut-être autoriser un utilisateur à entrer un numéro de téléphone pour établir la connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-161">For example, if your remote transport provider is in the process of uploading messages, you might need to allow a user to enter a telephone number to establish the remote connection.</span></span> <span data-ttu-id="cf8f1-162">Avant de vous boucle par le biais de la procédure de boîte de dialogue, vous devez déclarer une section critique.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-162">Before you loop through the dialog box procedure, you should declare a critical section.</span></span> <span data-ttu-id="cf8f1-163">Lorsque l’utilisateur ferme la boîte de dialogue, abandon de la procédure de boîte de dialogue, vous devez libérer la section critique.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-163">When the user closes the dialog box, terminating the dialog box procedure, you should release the critical section.</span></span>
  
<span data-ttu-id="cf8f1-164">Lorsque vous définissez _ulFlags_ sur NOTIFY_CRITICAL_ERROR, le spouleur MAPI ne rend plus aucun appel au fournisseur à l’exception aux libérer.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-164">When you set  _ulFlags_ to NOTIFY_CRITICAL_ERROR, the MAPI spooler makes no further calls to the provider except to release it.</span></span> <span data-ttu-id="cf8f1-165">Si vous appelez **SpoolerNotify** avec NOTIFY_CRITICAL_ERROR défini à partir des méthodes [IXPLogon::StartMessage](ixplogon-startmessage.md) ou [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) , renvoyer avec une valeur d’erreur appropriés à partir de la **StartMessage** ou \*\* SubmitMessage \*\* d’appel immédiatement après l’appel de **SpoolerNotify** .</span><span class="sxs-lookup"><span data-stu-id="cf8f1-165">If you call **SpoolerNotify** with NOTIFY_CRITICAL_ERROR set from the [IXPLogon::StartMessage](ixplogon-startmessage.md) or [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) methods, return with an appropriate error value from the **StartMessage** or \*\* SubmitMessage \*\* call immediately after the **SpoolerNotify** call.</span></span> 
  
<span data-ttu-id="cf8f1-166">Si votre fournisseur de transport récupérés à partir d’une condition qui provoquaient antérieurement qu’il échoue, appelez **SpoolerNotify** avec _ulFlags_ défini sur NOTIFY_READYTOSEND.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-166">If your transport provider recovered from a condition that previously caused it to fail, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_READYTOSEND.</span></span> <span data-ttu-id="cf8f1-167">Cet indicateur indique que le fournisseur est à nouveau prêt à traiter les messages.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-167">This flag indicates that the provider is again ready to handle messages.</span></span> 
  
## <a name="notes-to-message-store-providers"></a><span data-ttu-id="cf8f1-168">Remarques pour les fournisseurs de banque de messages</span><span class="sxs-lookup"><span data-stu-id="cf8f1-168">Notes to Message Store Providers</span></span>

<span data-ttu-id="cf8f1-169">Appelez **SpoolerNotify**, en passant l’indicateur NOTIFY_READYTOSEND _ulFlags_, avant de rendre votre premier appel à [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) dans **IMessage::SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-169">Call **SpoolerNotify**, passing the NOTIFY_READYTOSEND flag in  _ulFlags_, before you make your first call to [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) in **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="cf8f1-170">Cet appel à **SpoolerNotify** doit être effectuée qu’une seule fois par session.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-170">This call to **SpoolerNotify** needs to be made only once per session.</span></span> 
  
<span data-ttu-id="cf8f1-171">Si votre fournisseur de banque de messages est étroitement avec un transport de fournisseur et que vous appelez **SpoolerNotify** avec la valeur _ulFlags_ NOTIFY_NEWMAIL_RECEIVED, le spouleur MAPI ouvre le nouveau message et commence à traiter la nouvelle fonction raccordement de message.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-171">If your message store provider is tightly coupled with a transport provider and you call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NEWMAIL_RECEIVED, the MAPI spooler opens the new message and begins processing the new message hook function.</span></span> <span data-ttu-id="cf8f1-172">Lorsque le traitement est terminé, le spouleur MAPI appelle la méthode de [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) pour vous informer du nouveau message.</span><span class="sxs-lookup"><span data-stu-id="cf8f1-172">When processing is complete, the MAPI spooler calls the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method to inform you of your own new message.</span></span> 
  
<span data-ttu-id="cf8f1-173">Pour plus d’informations sur l’appel de **SpoolerNotify**, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="cf8f1-173">For more information about calling **SpoolerNotify**, see any of the following topics:</span></span>
  
- [<span data-ttu-id="cf8f1-174">Implémentation de la méthode FlushQueues</span><span class="sxs-lookup"><span data-stu-id="cf8f1-174">Implementing the FlushQueues Method</span></span>](implementing-the-flushqueues-method.md)
    
- [<span data-ttu-id="cf8f1-175">Interaction avec le spouleur MAPI</span><span class="sxs-lookup"><span data-stu-id="cf8f1-175">Interacting with the MAPI Spooler</span></span>](interacting-with-the-mapi-spooler.md)
    
- [<span data-ttu-id="cf8f1-176">Modèle de réception de message</span><span class="sxs-lookup"><span data-stu-id="cf8f1-176">Message Reception Model</span></span>](message-reception-model.md)
    
## <a name="see-also"></a><span data-ttu-id="cf8f1-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf8f1-177">See also</span></span>



[<span data-ttu-id="cf8f1-178">IMsgStore::GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="cf8f1-178">IMsgStore::NotifyNewMail</span></span>](imsgstore-notifynewmail.md)
  
[<span data-ttu-id="cf8f1-179">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="cf8f1-179">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="cf8f1-180">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="cf8f1-180">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="cf8f1-181">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cf8f1-181">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

