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
ms.openlocfilehash: 99377d63b4b5cf8731809446b70770f0c24231ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423768"
---
# <a name="imapisupportspoolernotify"></a><span data-ttu-id="28639-103">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="28639-103">IMAPISupport::SpoolerNotify</span></span>

  
  
<span data-ttu-id="28639-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="28639-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="28639-105">Avertit le spouleur MAPI de la modification de l'État ou d'une demande de service.</span><span class="sxs-lookup"><span data-stu-id="28639-105">Notifies the MAPI spooler of a change in status or a request for service.</span></span> 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a><span data-ttu-id="28639-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28639-106">Parameters</span></span>

 <span data-ttu-id="28639-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="28639-107">_ulFlags_</span></span>
  
> <span data-ttu-id="28639-108">dans Masque de des indicateurs qui indique le type de notification.</span><span class="sxs-lookup"><span data-stu-id="28639-108">[in] A bitmask of flags that indicates the type of notification.</span></span> <span data-ttu-id="28639-109">Les fournisseurs de transport peuvent définir tous les indicateurs à l'exception de NOTIFY_NEWMAIL_RECEIVED; Seuls NOTIFY_NEWMAIL_RECEIVED et NOTIFY_READTOSEND sont valides pour les fournisseurs de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="28639-109">Transport providers can set all of the flags except for NOTIFY_NEWMAIL_RECEIVED; only NOTIFY_NEWMAIL_RECEIVED and NOTIFY_READTOSEND are valid for message store providers.</span></span> <span data-ttu-id="28639-110">Les indicateurs suivants sont valides pour le paramètre _ulFlags_ :</span><span class="sxs-lookup"><span data-stu-id="28639-110">The following flags are valid for the  _ulFlags_ parameter:</span></span> 
    
<span data-ttu-id="28639-111">NOTIFY_CONFIG_CHANGE</span><span class="sxs-lookup"><span data-stu-id="28639-111">NOTIFY_CONFIG_CHANGE</span></span> 
  
> <span data-ttu-id="28639-112">Enregistre une demande de modification de la configuration du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="28639-112">Registers a request to change the transport provider's configuration.</span></span> 
    
<span data-ttu-id="28639-113">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="28639-113">NOTIFY_CRITICAL_ERROR</span></span> 
  
> <span data-ttu-id="28639-114">Une erreur irrécupérable s'est produite au fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="28639-114">An unrecoverable error has occurred to the transport provider.</span></span> <span data-ttu-id="28639-115">Étant donné que NOTIFY_SENTDEFERRED et NOTIFY_CRITICAL_ERROR utilisent le paramètre _lpvData_ pour les appels de fournisseur de transport, ces indicateurs s'excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="28639-115">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter for transport provider calls, these flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="28639-116">NOTIFY_CRITSEC</span><span class="sxs-lookup"><span data-stu-id="28639-116">NOTIFY_CRITSEC</span></span> 
  
> <span data-ttu-id="28639-117">Demande une section critique pour le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="28639-117">Requests a critical section for the transport provider.</span></span> <span data-ttu-id="28639-118">Le paramètre _lpvData_ n'est pas défini et doit être null.</span><span class="sxs-lookup"><span data-stu-id="28639-118">The  _lpvData_ parameter is undefined and should be NULL.</span></span> 
    
<span data-ttu-id="28639-119">NOTIFY_NEWMAIL</span><span class="sxs-lookup"><span data-stu-id="28639-119">NOTIFY_NEWMAIL</span></span> 
  
> <span data-ttu-id="28639-120">Le spouleur MAPI doit télécharger les messages nouvellement reçus à la prochaine heure disponible.</span><span class="sxs-lookup"><span data-stu-id="28639-120">The MAPI spooler should download any newly received messages at the next available time.</span></span> <span data-ttu-id="28639-121">Le paramètre _lpvData_ n'est pas défini et doit être défini sur null.</span><span class="sxs-lookup"><span data-stu-id="28639-121">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="28639-122">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="28639-122">NOTIFY_NEWMAIL_RECEIVED</span></span> 
  
> <span data-ttu-id="28639-123">Un nouveau message a été reçu dans la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="28639-123">A new message has been received in the message store.</span></span> <span data-ttu-id="28639-124">Le paramètre _lpvData_ pointe vers une structure [NEWMAIL_NOTIFICATION](newmail_notification.md) qui décrit le message.</span><span class="sxs-lookup"><span data-stu-id="28639-124">The  _lpvData_ parameter points to a [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that describes the message.</span></span> <span data-ttu-id="28639-125">Cet indicateur est utilisé pour les fournisseurs de banques de messages étroitement couplés avec les fournisseurs de transport et est ignoré si le fournisseur de banque est connecté avec l'indicateur MAPI_NO_MAIL défini.</span><span class="sxs-lookup"><span data-stu-id="28639-125">This flag is used for message store providers that are tightly coupled with transport providers and is ignored if the store provider is logged on with the MAPI_NO_MAIL flag set.</span></span> 
    
<span data-ttu-id="28639-126">NOTIFY_NONCRIT</span><span class="sxs-lookup"><span data-stu-id="28639-126">NOTIFY_NONCRIT</span></span> 
  
> <span data-ttu-id="28639-127">Libère une section critique obtenue avec un appel précédent à **SpoolerNotify** avec _ULFLAGS_ défini sur NOTIFY_CRITSEC.</span><span class="sxs-lookup"><span data-stu-id="28639-127">Releases a critical section that was obtained with a previous call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="28639-128">Le paramètre _lpvData_ n'est pas défini et doit être défini sur null.</span><span class="sxs-lookup"><span data-stu-id="28639-128">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="28639-129">NOTIFY_READYTOSEND</span><span class="sxs-lookup"><span data-stu-id="28639-129">NOTIFY_READYTOSEND</span></span> 
  
> <span data-ttu-id="28639-130">Le fournisseur de banque de messages ou de transport est prêt à envoyer des messages.</span><span class="sxs-lookup"><span data-stu-id="28639-130">The transport or message store provider is ready to send messages.</span></span> <span data-ttu-id="28639-131">Le paramètre _lpvData_ n'est pas défini et doit être défini sur null.</span><span class="sxs-lookup"><span data-stu-id="28639-131">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="28639-132">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="28639-132">NOTIFY_SENTDEFERRED</span></span> 
  
> <span data-ttu-id="28639-133">Un message précédemment différé doit maintenant être envoyé et le fournisseur de transport doit être averti lorsque le message est prêt à être remis à l'aide d'un appel à la méthode [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="28639-133">A previously deferred message should now be sent, and the transport provider should be notified when the message is ready to be delivered by using a call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> <span data-ttu-id="28639-134">L'identificateur d'entrée du message différé est contenu dans une structure [SBinary](sbinary.md) désignée par _lpvData_.</span><span class="sxs-lookup"><span data-stu-id="28639-134">The entry identifier of the deferred message is contained in an [SBinary](sbinary.md) structure pointed to by  _lpvData_.</span></span> <span data-ttu-id="28639-135">Étant donné que NOTIFY_SENTDEFERRED et NOTIFY_CRITICAL_ERROR utilisent le paramètre _lpvData_ , ces indicateurs s'excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="28639-135">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter, these flags are mutually exclusive.</span></span> 
    
 <span data-ttu-id="28639-136">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="28639-136">_lpvData_</span></span>
  
> <span data-ttu-id="28639-137">dans Pointeur vers les données associées applicables à une notification.</span><span class="sxs-lookup"><span data-stu-id="28639-137">[in] A pointer to associated data applicable to a notification.</span></span> <span data-ttu-id="28639-138">Le paramètre _lpvData_ pointe vers des données valides uniquement lorsque les indicateurs suivants sont définis (_lpvData_ est NULL lorsque _ulFlags_ est défini sur les autres types de notification):</span><span class="sxs-lookup"><span data-stu-id="28639-138">The  _lpvData_ parameter points to valid data only when the following flags are set (_lpvData_ is NULL when  _ulFlags_ is set to the other notification types):</span></span> 
    
|<span data-ttu-id="28639-139">**paramètre _ulFlags_**</span><span class="sxs-lookup"><span data-stu-id="28639-139">**_ulFlags_ setting**</span></span>|<span data-ttu-id="28639-140">**valeur _lpvData_**</span><span class="sxs-lookup"><span data-stu-id="28639-140">**_lpvData_ value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="28639-141">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="28639-141">NOTIFY_CRITICAL_ERROR</span></span>  <br/> |<span data-ttu-id="28639-142">Informations sur l'erreur.</span><span class="sxs-lookup"><span data-stu-id="28639-142">Information about the error.</span></span>  <br/> |
|<span data-ttu-id="28639-143">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="28639-143">NOTIFY_NEWMAIL_RECEIVED</span></span>  <br/> |<span data-ttu-id="28639-144">Une structure **NEWMAIL_NOTIFICATION** qui contient des informations sur le message nouvellement remis.</span><span class="sxs-lookup"><span data-stu-id="28639-144">A **NEWMAIL_NOTIFICATION** structure that contains information about the newly delivered message.</span></span>  <br/> |
|<span data-ttu-id="28639-145">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="28639-145">NOTIFY_SENTDEFERRED</span></span>  <br/> |<span data-ttu-id="28639-146">Une structure **SBinary** qui contient l'identificateur d'entrée du message différé.</span><span class="sxs-lookup"><span data-stu-id="28639-146">An **SBinary** structure that contains the entry identifier of deferred message.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="28639-147">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="28639-147">Return value</span></span>

<span data-ttu-id="28639-148">S_OK</span><span class="sxs-lookup"><span data-stu-id="28639-148">S_OK</span></span> 
  
> <span data-ttu-id="28639-149">La notification a réussi.</span><span class="sxs-lookup"><span data-stu-id="28639-149">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="28639-150">Remarques</span><span class="sxs-lookup"><span data-stu-id="28639-150">Remarks</span></span>

<span data-ttu-id="28639-151">La méthode **IMAPISupport:: SpoolerNotify** est implémentée pour les objets de prise en charge du magasin de messages et du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="28639-151">The **IMAPISupport::SpoolerNotify** method is implemented for message store and transport provider support objects.</span></span> <span data-ttu-id="28639-152">Ces fournisseurs appellent **SpoolerNotify** pour informer le spouleur MAPI de la modification de l'État ou d'une demande de service.</span><span class="sxs-lookup"><span data-stu-id="28639-152">These providers call **SpoolerNotify** to notify the MAPI spooler of a change in status or a request for service.</span></span> <span data-ttu-id="28639-153">**SpoolerNotify** est appelé principalement par les fournisseurs de transport et peut être appelé à tout moment pendant la session.</span><span class="sxs-lookup"><span data-stu-id="28639-153">**SpoolerNotify** is called primarily by transport providers and may be called at any time during the session.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="28639-154">Remarques relatives aux fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="28639-154">Notes to Transport Providers</span></span>

<span data-ttu-id="28639-155">Si vous avez modifié votre configuration de fournisseur de transport, appelez **SpoolerNotify** et définissez _ulFlags_ sur NOTIFY_CONFIG_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="28639-155">If you have changed your transport provider configuration, call **SpoolerNotify** and set  _ulFlags_ to NOTIFY_CONFIG_CHANGED.</span></span> <span data-ttu-id="28639-156">**SpoolerNotify** répond en appelant la méthode [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) pour demander une modification dans les types d'adresses pris en charge.</span><span class="sxs-lookup"><span data-stu-id="28639-156">**SpoolerNotify** responds by calling the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to query for a change in supported address types.</span></span> 
  
<span data-ttu-id="28639-157">Si vous avez besoin d'une section critique pour garantir un traitement ininterrompu, appelez **SpoolerNotify** avec _ULFLAGS_ défini sur NOTIFY_CRITSEC.</span><span class="sxs-lookup"><span data-stu-id="28639-157">If you need a critical section to ensure uninterrupted processing, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="28639-158">La définition de cet indicateur informe le spouleur MAPI qu'il ne doit pas appeler les méthodes [IXPLogon:: Idle](ixplogon-idle.md) et [IXPLogon::P oll](ixplogon-poll.md) .</span><span class="sxs-lookup"><span data-stu-id="28639-158">Setting this flag informs the MAPI spooler that it should not call the [IXPLogon::Idle](ixplogon-idle.md) and [IXPLogon::Poll](ixplogon-poll.md) methods.</span></span> <span data-ttu-id="28639-159">Une fois que vous avez une section critique ouverte, renvoyez MAPI_E_BUSY à chaque appel de la méthode [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) .</span><span class="sxs-lookup"><span data-stu-id="28639-159">While you have a critical section open, return MAPI_E_BUSY whenever the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is called.</span></span> <span data-ttu-id="28639-160">Une fois que vous avez terminé la section critique, effectuez un autre appel à **SpoolerNotify** avec _ULFLAGS_ défini sur NOTIFY_NONCRIT.</span><span class="sxs-lookup"><span data-stu-id="28639-160">When you are finished with the critical section, make another call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NONCRIT.</span></span> 
  
<span data-ttu-id="28639-161">Par exemple, si votre fournisseur de transport distant est en train de télécharger des messages, vous devrez peut-être autoriser un utilisateur à entrer un numéro de téléphone pour établir la connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="28639-161">For example, if your remote transport provider is in the process of uploading messages, you might need to allow a user to enter a telephone number to establish the remote connection.</span></span> <span data-ttu-id="28639-162">Avant d'effectuer une boucle dans la procédure de la boîte de dialogue, vous devez déclarer une section critique.</span><span class="sxs-lookup"><span data-stu-id="28639-162">Before you loop through the dialog box procedure, you should declare a critical section.</span></span> <span data-ttu-id="28639-163">Lorsque l'utilisateur ferme la boîte de dialogue en terminant la procédure de la boîte de dialogue, vous devez libérer la section critique.</span><span class="sxs-lookup"><span data-stu-id="28639-163">When the user closes the dialog box, terminating the dialog box procedure, you should release the critical section.</span></span>
  
<span data-ttu-id="28639-164">Lorsque vous définissez _ulFlags_ sur NOTIFY_CRITICAL_ERROR, le spouleur MAPI ne procède à aucun autre appel du fournisseur à l'exception de sa publication.</span><span class="sxs-lookup"><span data-stu-id="28639-164">When you set  _ulFlags_ to NOTIFY_CRITICAL_ERROR, the MAPI spooler makes no further calls to the provider except to release it.</span></span> <span data-ttu-id="28639-165">Si vous appelez **SpoolerNotify** avec NOTIFY_CRITICAL_ERROR défini à partir des méthodes [IXPLogon:: StartMessage](ixplogon-startmessage.md) ou [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) , revenez avec une valeur d'erreur appropriée à partir de l'appel **StartMessage** ou \* \* SubmitMessage \* \* immédiatement après l'appel de **SpoolerNotify** .</span><span class="sxs-lookup"><span data-stu-id="28639-165">If you call **SpoolerNotify** with NOTIFY_CRITICAL_ERROR set from the [IXPLogon::StartMessage](ixplogon-startmessage.md) or [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) methods, return with an appropriate error value from the **StartMessage** or \*\* SubmitMessage \*\* call immediately after the **SpoolerNotify** call.</span></span> 
  
<span data-ttu-id="28639-166">Si votre fournisseur de transport récupère à partir d'une condition qui l'a déjà causée, appelez **SpoolerNotify** avec _ULFLAGS_ défini sur NOTIFY_READYTOSEND.</span><span class="sxs-lookup"><span data-stu-id="28639-166">If your transport provider recovered from a condition that previously caused it to fail, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_READYTOSEND.</span></span> <span data-ttu-id="28639-167">Cet indicateur indique que le fournisseur est à nouveau prêt à gérer les messages.</span><span class="sxs-lookup"><span data-stu-id="28639-167">This flag indicates that the provider is again ready to handle messages.</span></span> 
  
## <a name="notes-to-message-store-providers"></a><span data-ttu-id="28639-168">Remarques aux fournisseurs de banques de messages</span><span class="sxs-lookup"><span data-stu-id="28639-168">Notes to Message Store Providers</span></span>

<span data-ttu-id="28639-169">Appelez **SpoolerNotify**, en passant l'indicateur NOTIFY_READYTOSEND dans _ulFlags_, avant d'effectuer votre premier appel à [IMAPISupport::P Reparesubmit](imapisupport-preparesubmit.md) dans **IMessage:: SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="28639-169">Call **SpoolerNotify**, passing the NOTIFY_READYTOSEND flag in  _ulFlags_, before you make your first call to [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) in **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="28639-170">Cet appel à **SpoolerNotify** ne doit être effectué qu'une seule fois par session.</span><span class="sxs-lookup"><span data-stu-id="28639-170">This call to **SpoolerNotify** needs to be made only once per session.</span></span> 
  
<span data-ttu-id="28639-171">Si votre fournisseur de banque de messages est étroitement couplé à un fournisseur de transport et que vous appelez **SpoolerNotify** avec _ULFLAGS_ défini sur NOTIFY_NEWMAIL_RECEIVED, le spouleur MAPI ouvre le nouveau message et commence à traiter la nouvelle fonction de raccordement de message.</span><span class="sxs-lookup"><span data-stu-id="28639-171">If your message store provider is tightly coupled with a transport provider and you call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NEWMAIL_RECEIVED, the MAPI spooler opens the new message and begins processing the new message hook function.</span></span> <span data-ttu-id="28639-172">Une fois le traitement terminé, le spouleur MAPI appelle la méthode [IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md) pour vous informer de votre propre nouveau message.</span><span class="sxs-lookup"><span data-stu-id="28639-172">When processing is complete, the MAPI spooler calls the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method to inform you of your own new message.</span></span> 
  
<span data-ttu-id="28639-173">Pour plus d'informations sur l'appel de **SpoolerNotify**, reportez-vous à l'une des rubriques suivantes:</span><span class="sxs-lookup"><span data-stu-id="28639-173">For more information about calling **SpoolerNotify**, see any of the following topics:</span></span>
  
- [<span data-ttu-id="28639-174">Implémentation de la méthode FlushQueues</span><span class="sxs-lookup"><span data-stu-id="28639-174">Implementing the FlushQueues Method</span></span>](implementing-the-flushqueues-method.md)
    
- [<span data-ttu-id="28639-175">Interaction avec le spouleur MAPI</span><span class="sxs-lookup"><span data-stu-id="28639-175">Interacting with the MAPI Spooler</span></span>](interacting-with-the-mapi-spooler.md)
    
- [<span data-ttu-id="28639-176">Modèle de réception des messages</span><span class="sxs-lookup"><span data-stu-id="28639-176">Message Reception Model</span></span>](message-reception-model.md)
    
## <a name="see-also"></a><span data-ttu-id="28639-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28639-177">See also</span></span>



[<span data-ttu-id="28639-178">IMsgStore::GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="28639-178">IMsgStore::NotifyNewMail</span></span>](imsgstore-notifynewmail.md)
  
[<span data-ttu-id="28639-179">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="28639-179">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="28639-180">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="28639-180">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="28639-181">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="28639-181">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

