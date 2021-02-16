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
# <a name="imapisupportspoolernotify"></a><span data-ttu-id="9adbf-103">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="9adbf-103">IMAPISupport::SpoolerNotify</span></span>

  
  
<span data-ttu-id="9adbf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9adbf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9adbf-105">Avertit lepooler MAPI d’un changement d’état ou d’une demande de service.</span><span class="sxs-lookup"><span data-stu-id="9adbf-105">Notifies the MAPI spooler of a change in status or a request for service.</span></span> 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a><span data-ttu-id="9adbf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9adbf-106">Parameters</span></span>

 <span data-ttu-id="9adbf-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9adbf-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9adbf-108">[in] Masque de bits d’indicateurs qui indique le type de notification.</span><span class="sxs-lookup"><span data-stu-id="9adbf-108">[in] A bitmask of flags that indicates the type of notification.</span></span> <span data-ttu-id="9adbf-109">Les fournisseurs de transport peuvent définir tous les indicateurs à l’exception de NOTIFY_NEWMAIL_RECEIVED ; seuls NOTIFY_NEWMAIL_RECEIVED et NOTIFY_READTOSEND sont valides pour les fournisseurs de magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="9adbf-109">Transport providers can set all of the flags except for NOTIFY_NEWMAIL_RECEIVED; only NOTIFY_NEWMAIL_RECEIVED and NOTIFY_READTOSEND are valid for message store providers.</span></span> <span data-ttu-id="9adbf-110">Les indicateurs suivants sont valides pour  _le paramètre ulFlags_ :</span><span class="sxs-lookup"><span data-stu-id="9adbf-110">The following flags are valid for the  _ulFlags_ parameter:</span></span> 
    
<span data-ttu-id="9adbf-111">NOTIFY_CONFIG_CHANGE</span><span class="sxs-lookup"><span data-stu-id="9adbf-111">NOTIFY_CONFIG_CHANGE</span></span> 
  
> <span data-ttu-id="9adbf-112">Enregistre une demande de modification de la configuration du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="9adbf-112">Registers a request to change the transport provider's configuration.</span></span> 
    
<span data-ttu-id="9adbf-113">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="9adbf-113">NOTIFY_CRITICAL_ERROR</span></span> 
  
> <span data-ttu-id="9adbf-114">Une erreur irrécable s’est produite au fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="9adbf-114">An unrecoverable error has occurred to the transport provider.</span></span> <span data-ttu-id="9adbf-115">Étant donné que NOTIFY_SENTDEFERRED et NOTIFY_CRITICAL_ERROR le paramètre  _lpvData_ pour les appels de fournisseur de transport, ces indicateurs s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="9adbf-115">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter for transport provider calls, these flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="9adbf-116">NOTIFY_CRITSEC</span><span class="sxs-lookup"><span data-stu-id="9adbf-116">NOTIFY_CRITSEC</span></span> 
  
> <span data-ttu-id="9adbf-117">Demande une section critique pour le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="9adbf-117">Requests a critical section for the transport provider.</span></span> <span data-ttu-id="9adbf-118">Le  _paramètre lpvData_ n’est pas définie et doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="9adbf-118">The  _lpvData_ parameter is undefined and should be NULL.</span></span> 
    
<span data-ttu-id="9adbf-119">NOTIFY_NEWMAIL</span><span class="sxs-lookup"><span data-stu-id="9adbf-119">NOTIFY_NEWMAIL</span></span> 
  
> <span data-ttu-id="9adbf-120">Lepooler MAPI doit télécharger les messages nouvellement reçus à la prochaine heure disponible.</span><span class="sxs-lookup"><span data-stu-id="9adbf-120">The MAPI spooler should download any newly received messages at the next available time.</span></span> <span data-ttu-id="9adbf-121">Le  _paramètre lpvData_ n’est pas définie et doit être définie sur NULL.</span><span class="sxs-lookup"><span data-stu-id="9adbf-121">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="9adbf-122">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="9adbf-122">NOTIFY_NEWMAIL_RECEIVED</span></span> 
  
> <span data-ttu-id="9adbf-123">Un nouveau message a été reçu dans la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="9adbf-123">A new message has been received in the message store.</span></span> <span data-ttu-id="9adbf-124">Le  _paramètre lpvData_ pointe vers une structure [NEWMAIL_NOTIFICATION](newmail_notification.md) qui décrit le message.</span><span class="sxs-lookup"><span data-stu-id="9adbf-124">The  _lpvData_ parameter points to a [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that describes the message.</span></span> <span data-ttu-id="9adbf-125">Cet indicateur est utilisé pour les fournisseurs de magasins de messages qui sont étroitement associés à des fournisseurs de transport et est ignoré si le fournisseur de magasins est connecté avec l’indicateur MAPI_NO_MAIL définie.</span><span class="sxs-lookup"><span data-stu-id="9adbf-125">This flag is used for message store providers that are tightly coupled with transport providers and is ignored if the store provider is logged on with the MAPI_NO_MAIL flag set.</span></span> 
    
<span data-ttu-id="9adbf-126">NOTIFY_NONCRIT</span><span class="sxs-lookup"><span data-stu-id="9adbf-126">NOTIFY_NONCRIT</span></span> 
  
> <span data-ttu-id="9adbf-127">Libère une section critique obtenue avec un appel précédent à **SpoolerNotify** avec  _ulFlags_ définie sur NOTIFY_CRITSEC.</span><span class="sxs-lookup"><span data-stu-id="9adbf-127">Releases a critical section that was obtained with a previous call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="9adbf-128">Le  _paramètre lpvData_ n’est pas définie et doit être définie sur NULL.</span><span class="sxs-lookup"><span data-stu-id="9adbf-128">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="9adbf-129">NOTIFY_READYTOSEND</span><span class="sxs-lookup"><span data-stu-id="9adbf-129">NOTIFY_READYTOSEND</span></span> 
  
> <span data-ttu-id="9adbf-130">Le fournisseur de transport ou de magasin de messages est prêt à envoyer des messages.</span><span class="sxs-lookup"><span data-stu-id="9adbf-130">The transport or message store provider is ready to send messages.</span></span> <span data-ttu-id="9adbf-131">Le  _paramètre lpvData_ n’est pas définie et doit être définie sur NULL.</span><span class="sxs-lookup"><span data-stu-id="9adbf-131">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="9adbf-132">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="9adbf-132">NOTIFY_SENTDEFERRED</span></span> 
  
> <span data-ttu-id="9adbf-133">Un message différé précédemment doit maintenant être envoyé et le fournisseur de transport doit être averti lorsque le message est prêt à être remis à l’aide d’un appel à la méthode [IXPLogon::SubmitMessage.](ixplogon-submitmessage.md)</span><span class="sxs-lookup"><span data-stu-id="9adbf-133">A previously deferred message should now be sent, and the transport provider should be notified when the message is ready to be delivered by using a call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> <span data-ttu-id="9adbf-134">L’identificateur d’entrée du message différé est contenu dans une structure [SBinary](sbinary.md) pointée par  _lpvData_.</span><span class="sxs-lookup"><span data-stu-id="9adbf-134">The entry identifier of the deferred message is contained in an [SBinary](sbinary.md) structure pointed to by  _lpvData_.</span></span> <span data-ttu-id="9adbf-135">Étant donné que NOTIFY_SENTDEFERRED et NOTIFY_CRITICAL_ERROR utiliser le paramètre  _lpvData,_ ces indicateurs s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="9adbf-135">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter, these flags are mutually exclusive.</span></span> 
    
 <span data-ttu-id="9adbf-136">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="9adbf-136">_lpvData_</span></span>
  
> <span data-ttu-id="9adbf-137">[in] Pointeur vers les données associées applicables à une notification.</span><span class="sxs-lookup"><span data-stu-id="9adbf-137">[in] A pointer to associated data applicable to a notification.</span></span> <span data-ttu-id="9adbf-138">Le  _paramètre lpvData_ pointe vers des données valides uniquement lorsque les indicateurs suivants sont définies (_lpvData_ est NULL lorsque  _ulFlags_ est définie sur les autres types de notifications) :</span><span class="sxs-lookup"><span data-stu-id="9adbf-138">The  _lpvData_ parameter points to valid data only when the following flags are set (_lpvData_ is NULL when  _ulFlags_ is set to the other notification types):</span></span> 
    
|<span data-ttu-id="9adbf-139">**_Paramètre ulFlags_**</span><span class="sxs-lookup"><span data-stu-id="9adbf-139">**_ulFlags_ setting**</span></span>|<span data-ttu-id="9adbf-140">**_Valeur lpvData_**</span><span class="sxs-lookup"><span data-stu-id="9adbf-140">**_lpvData_ value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9adbf-141">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="9adbf-141">NOTIFY_CRITICAL_ERROR</span></span>  <br/> |<span data-ttu-id="9adbf-142">Informations sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="9adbf-142">Information about the error.</span></span>  <br/> |
|<span data-ttu-id="9adbf-143">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="9adbf-143">NOTIFY_NEWMAIL_RECEIVED</span></span>  <br/> |<span data-ttu-id="9adbf-144">Structure **NEWMAIL_NOTIFICATION** qui contient des informations sur le message nouvellement remis.</span><span class="sxs-lookup"><span data-stu-id="9adbf-144">A **NEWMAIL_NOTIFICATION** structure that contains information about the newly delivered message.</span></span>  <br/> |
|<span data-ttu-id="9adbf-145">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="9adbf-145">NOTIFY_SENTDEFERRED</span></span>  <br/> |<span data-ttu-id="9adbf-146">Structure **SBinary** qui contient l’identificateur d’entrée du message différé.</span><span class="sxs-lookup"><span data-stu-id="9adbf-146">An **SBinary** structure that contains the entry identifier of deferred message.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="9adbf-147">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9adbf-147">Return value</span></span>

<span data-ttu-id="9adbf-148">S_OK</span><span class="sxs-lookup"><span data-stu-id="9adbf-148">S_OK</span></span> 
  
> <span data-ttu-id="9adbf-149">La notification a réussi.</span><span class="sxs-lookup"><span data-stu-id="9adbf-149">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9adbf-150">Remarques</span><span class="sxs-lookup"><span data-stu-id="9adbf-150">Remarks</span></span>

<span data-ttu-id="9adbf-151">La **méthode IMAPISupport::SpoolerNotify** est implémentée pour les objets de prise en charge de fournisseur de transport et de magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="9adbf-151">The **IMAPISupport::SpoolerNotify** method is implemented for message store and transport provider support objects.</span></span> <span data-ttu-id="9adbf-152">Ces fournisseurs appellent **SpoolerNotify** pour informer lepooler MAPI d’un changement d’état ou d’une demande de service.</span><span class="sxs-lookup"><span data-stu-id="9adbf-152">These providers call **SpoolerNotify** to notify the MAPI spooler of a change in status or a request for service.</span></span> <span data-ttu-id="9adbf-153">**SpoolerNotify est** principalement appelé par les fournisseurs de transport et peut être appelé à tout moment pendant la session.</span><span class="sxs-lookup"><span data-stu-id="9adbf-153">**SpoolerNotify** is called primarily by transport providers and may be called at any time during the session.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="9adbf-154">Remarques aux fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="9adbf-154">Notes to Transport Providers</span></span>

<span data-ttu-id="9adbf-155">Si vous avez modifié la configuration de votre fournisseur de transport, appelez **SpoolerNotify** et définissez  _ulFlags_ sur NOTIFY_CONFIG_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="9adbf-155">If you have changed your transport provider configuration, call **SpoolerNotify** and set  _ulFlags_ to NOTIFY_CONFIG_CHANGED.</span></span> <span data-ttu-id="9adbf-156">**SpoolerNotify répond** en appelant la méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) pour demander une modification des types d’adresses pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9adbf-156">**SpoolerNotify** responds by calling the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to query for a change in supported address types.</span></span> 
  
<span data-ttu-id="9adbf-157">Si vous avez besoin d’une section critique pour garantir un traitement ininterrompu, appelez **SpoolerNotify** avec  _ulFlags_ définie sur NOTIFY_CRITSEC.</span><span class="sxs-lookup"><span data-stu-id="9adbf-157">If you need a critical section to ensure uninterrupted processing, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="9adbf-158">La définition de cet indicateur informe lepooler MAPI qu’il ne doit pas appeler les méthodes [IXPLogon::Idle](ixplogon-idle.md) et [IXPLogon::P élément.](ixplogon-poll.md)</span><span class="sxs-lookup"><span data-stu-id="9adbf-158">Setting this flag informs the MAPI spooler that it should not call the [IXPLogon::Idle](ixplogon-idle.md) and [IXPLogon::Poll](ixplogon-poll.md) methods.</span></span> <span data-ttu-id="9adbf-159">Bien qu’une section critique soit ouverte, MAPI_E_BUSY chaque fois que la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="9adbf-159">While you have a critical section open, return MAPI_E_BUSY whenever the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is called.</span></span> <span data-ttu-id="9adbf-160">Lorsque vous avez terminé avec la section critique, faites un autre appel à **SpoolerNotify** avec  _ulFlags_ définie sur NOTIFY_NONCRIT.</span><span class="sxs-lookup"><span data-stu-id="9adbf-160">When you are finished with the critical section, make another call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NONCRIT.</span></span> 
  
<span data-ttu-id="9adbf-161">Par exemple, si votre fournisseur de transport distant est en train de télécharger des messages, vous devrez peut-être autoriser un utilisateur à entrer un numéro de téléphone pour établir la connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="9adbf-161">For example, if your remote transport provider is in the process of uploading messages, you might need to allow a user to enter a telephone number to establish the remote connection.</span></span> <span data-ttu-id="9adbf-162">Avant de passer en boucle dans la procédure de la boîte de dialogue, vous devez déclarer une section critique.</span><span class="sxs-lookup"><span data-stu-id="9adbf-162">Before you loop through the dialog box procedure, you should declare a critical section.</span></span> <span data-ttu-id="9adbf-163">Lorsque l’utilisateur ferme la boîte de dialogue et termine la procédure de la boîte de dialogue, vous devez libérer la section critique.</span><span class="sxs-lookup"><span data-stu-id="9adbf-163">When the user closes the dialog box, terminating the dialog box procedure, you should release the critical section.</span></span>
  
<span data-ttu-id="9adbf-164">Lorsque vous définissez  _ulFlags_ sur NOTIFY_CRITICAL_ERROR, lepooler MAPI ne fait aucun autre appel au fournisseur, sauf pour le libérer.</span><span class="sxs-lookup"><span data-stu-id="9adbf-164">When you set  _ulFlags_ to NOTIFY_CRITICAL_ERROR, the MAPI spooler makes no further calls to the provider except to release it.</span></span> <span data-ttu-id="9adbf-165">Si vous appelez **SpoolerNotify** avec NOTIFY_CRITICAL_ERROR définie à partir des méthodes [IXPLogon::StartMessage](ixplogon-startmessage.md) ou [IXPLogon::SubmitMessage,](ixplogon-submitmessage.md) renvoyez avec une valeur d’erreur appropriée à partir de l’appel **StartMessage** ou \*\* SubmitMessage \*\* immédiatement après l’appel **SpoolerNotify.**</span><span class="sxs-lookup"><span data-stu-id="9adbf-165">If you call **SpoolerNotify** with NOTIFY_CRITICAL_ERROR set from the [IXPLogon::StartMessage](ixplogon-startmessage.md) or [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) methods, return with an appropriate error value from the **StartMessage** or \*\* SubmitMessage \*\* call immediately after the **SpoolerNotify** call.</span></span> 
  
<span data-ttu-id="9adbf-166">Si votre fournisseur de transport a récupéré d’une condition qui a précédemment provoqué son échec, appelez **SpoolerNotify** avec  _ulFlags_ définie sur NOTIFY_READYTOSEND.</span><span class="sxs-lookup"><span data-stu-id="9adbf-166">If your transport provider recovered from a condition that previously caused it to fail, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_READYTOSEND.</span></span> <span data-ttu-id="9adbf-167">Cet indicateur indique que le fournisseur est à nouveau prêt à gérer les messages.</span><span class="sxs-lookup"><span data-stu-id="9adbf-167">This flag indicates that the provider is again ready to handle messages.</span></span> 
  
## <a name="notes-to-message-store-providers"></a><span data-ttu-id="9adbf-168">Remarques pour les fournisseurs de banque de messages</span><span class="sxs-lookup"><span data-stu-id="9adbf-168">Notes to Message Store Providers</span></span>

<span data-ttu-id="9adbf-169">Appelez **SpoolerNotify**, en passant l’indicateur NOTIFY_READYTOSEND dans  _ulFlags_, avant d’effectuer votre premier appel à [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) dans **IMessage::SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="9adbf-169">Call **SpoolerNotify**, passing the NOTIFY_READYTOSEND flag in  _ulFlags_, before you make your first call to [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) in **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="9adbf-170">Cet appel à **SpoolerNotify** doit être effectué une seule fois par session.</span><span class="sxs-lookup"><span data-stu-id="9adbf-170">This call to **SpoolerNotify** needs to be made only once per session.</span></span> 
  
<span data-ttu-id="9adbf-171">Si votre fournisseur de magasins de messages est étroitement associé à un fournisseur de transport et que vous appelez **SpoolerNotify** avec  _ulFlags_ définie sur NOTIFY_NEWMAIL_RECEIVED, lepooler MAPI ouvre le nouveau message et commence le traitement de la nouvelle fonction de hook de message.</span><span class="sxs-lookup"><span data-stu-id="9adbf-171">If your message store provider is tightly coupled with a transport provider and you call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NEWMAIL_RECEIVED, the MAPI spooler opens the new message and begins processing the new message hook function.</span></span> <span data-ttu-id="9adbf-172">Une fois le traitement terminé, lepooler MAPI appelle la méthode [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) pour vous informer de votre propre nouveau message.</span><span class="sxs-lookup"><span data-stu-id="9adbf-172">When processing is complete, the MAPI spooler calls the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method to inform you of your own new message.</span></span> 
  
<span data-ttu-id="9adbf-173">Pour plus d’informations sur **l’appel de SpoolerNotify,** consultez l’une des rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="9adbf-173">For more information about calling **SpoolerNotify**, see any of the following topics:</span></span>
  
- [<span data-ttu-id="9adbf-174">Mise en œuvre de la méthode FlushQueues</span><span class="sxs-lookup"><span data-stu-id="9adbf-174">Implementing the FlushQueues Method</span></span>](implementing-the-flushqueues-method.md)
    
- [<span data-ttu-id="9adbf-175">Interaction avec le spooler MAPI</span><span class="sxs-lookup"><span data-stu-id="9adbf-175">Interacting with the MAPI Spooler</span></span>](interacting-with-the-mapi-spooler.md)
    
- [<span data-ttu-id="9adbf-176">Modèle de réception des messages</span><span class="sxs-lookup"><span data-stu-id="9adbf-176">Message Reception Model</span></span>](message-reception-model.md)
    
## <a name="see-also"></a><span data-ttu-id="9adbf-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9adbf-177">See also</span></span>



[<span data-ttu-id="9adbf-178">IMsgStore::GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="9adbf-178">IMsgStore::NotifyNewMail</span></span>](imsgstore-notifynewmail.md)
  
[<span data-ttu-id="9adbf-179">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="9adbf-179">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="9adbf-180">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="9adbf-180">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="9adbf-181">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9adbf-181">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

