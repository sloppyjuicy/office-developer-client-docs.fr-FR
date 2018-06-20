---
title: IMsgStoreAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.Advise
api_type:
- COM
ms.assetid: 8c57e743-a798-4e39-a61a-46dff8b1ac7c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6a315cef8263f7e241a815a0f054dc3174d88fa7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784235"
---
# <a name="imsgstoreadvise"></a><span data-ttu-id="f4664-103">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="f4664-103">IMsgStore::Advise</span></span>

  
  
<span data-ttu-id="f4664-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f4664-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f4664-105">Inscrit pour recevoir des notifications d’événements spécifiques qui affectent la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="f4664-105">Registers to receive notification of specified events that affect the message store.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="f4664-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4664-106">Parameters</span></span>

 <span data-ttu-id="f4664-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f4664-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="f4664-108">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="f4664-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f4664-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="f4664-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="f4664-110">[in] Pointeur vers l’identificateur d’entrée du dossier ou du message sur les notifications doivent être générées, ou **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="f4664-110">[in] A pointer to the entry identifier of the folder or message about which notifications should be generated, or **null**.</span></span> <span data-ttu-id="f4664-111">Si _lpEntryID_ est défini sur NULL, **Advise** enregistre des notifications sur le magasin de l’intégralité du message.</span><span class="sxs-lookup"><span data-stu-id="f4664-111">If  _lpEntryID_ is set to NULL, **Advise** registers for notifications on the entire message store.</span></span> 
    
 <span data-ttu-id="f4664-112">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="f4664-112">_ulEventMask_</span></span>
  
> <span data-ttu-id="f4664-113">[in] Un masque des valeurs qui indiquent les types d’événements de notification que l’appelant est intéressée par et doit être inclus dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f4664-113">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="f4664-114">Il existe une structure [NOTIFICATION](notification.md) correspondante associée à chaque type d’événement qui conserve des informations sur l’événement.</span><span class="sxs-lookup"><span data-stu-id="f4664-114">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="f4664-115">Les valeurs valides pour le paramètre _ulEventMask_ sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="f4664-115">The following are valid values for the  _ulEventMask_ parameter:</span></span> 
    
 <span data-ttu-id="f4664-116">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="f4664-116">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="f4664-117">Enregistre les notifications sur les erreurs graves, telles que la mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="f4664-117">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="f4664-118">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="f4664-118">_fnevExtended_</span></span>
  
> <span data-ttu-id="f4664-119">Fournisseur de magasins registres pour les notifications concernant les événements spécifiques au message particulier.</span><span class="sxs-lookup"><span data-stu-id="f4664-119">Registers for notifications about events specific to the particular message store provider.</span></span>
    
 <span data-ttu-id="f4664-120">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="f4664-120">_fnevNewMail_</span></span>
  
> <span data-ttu-id="f4664-121">Enregistre les notifications relatives à l’arrivée de nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="f4664-121">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="f4664-122">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="f4664-122">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="f4664-123">Enregistre les notifications concernant la création d’un nouveau dossier ou un message.</span><span class="sxs-lookup"><span data-stu-id="f4664-123">Registers for notifications about the creation of a new folder or message.</span></span>
    
 <span data-ttu-id="f4664-124">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="f4664-124">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="f4664-125">Enregistre les notifications relatives à un dossier ou un message en cours de copie.</span><span class="sxs-lookup"><span data-stu-id="f4664-125">Registers for notifications about a folder or message being copied.</span></span>
    
 <span data-ttu-id="f4664-126">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="f4664-126">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="f4664-127">Enregistre les notifications relatives à un dossier ou un message en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="f4664-127">Registers for notifications about a folder or message being deleted.</span></span>
    
 <span data-ttu-id="f4664-128">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="f4664-128">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="f4664-129">Enregistre les notifications relatives à un dossier ou un message en cours de modification.</span><span class="sxs-lookup"><span data-stu-id="f4664-129">Registers for notifications about a folder or message being modified.</span></span>
    
 <span data-ttu-id="f4664-130">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="f4664-130">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="f4664-131">Enregistre les notifications relatives à un dossier ou un message en cours de déplacement.</span><span class="sxs-lookup"><span data-stu-id="f4664-131">Registers for notifications about a folder or message being moved.</span></span>
    
 <span data-ttu-id="f4664-132">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="f4664-132">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="f4664-133">Enregistre les notifications relatives à la fin d’une opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="f4664-133">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="f4664-134">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="f4664-134">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="f4664-135">[in] Pointeur vers un objet de récepteur advise pour recevoir les notifications ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f4664-135">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="f4664-136">Cet objet de récepteur advise doit déjà affectée.</span><span class="sxs-lookup"><span data-stu-id="f4664-136">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="f4664-137">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="f4664-137">_lpulConnection_</span></span>
  
> <span data-ttu-id="f4664-138">[out] Un pointeur vers un nombre différent de zéro qui représente la connexion entre l’appelant de notification objet récepteur et la session.</span><span class="sxs-lookup"><span data-stu-id="f4664-138">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span> 
    
 <span data-ttu-id="f4664-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="f4664-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="f4664-140">[in] Pointeur vers un objet de récepteur advise pour recevoir les notifications ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f4664-140">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="f4664-141">Cet objet de récepteur advise doit déjà affectée.</span><span class="sxs-lookup"><span data-stu-id="f4664-141">This advise sink object must have already been allocated.</span></span> 
    
 <span data-ttu-id="f4664-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="f4664-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="f4664-143">[out] Objet récepteur et la banque de messages de notification un pointeur vers un numéro de connexion différente de zéro qui représente la connexion entre l’appelant.</span><span class="sxs-lookup"><span data-stu-id="f4664-143">[out] A pointer to a nonzero connection number that represents the connection between the caller's advise sink object and the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f4664-144">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="f4664-144">Return value</span></span>

<span data-ttu-id="f4664-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="f4664-145">S_OK</span></span> 
  
> <span data-ttu-id="f4664-146">L’inscription a réussi.</span><span class="sxs-lookup"><span data-stu-id="f4664-146">The registration was successful.</span></span>
    
<span data-ttu-id="f4664-147">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f4664-147">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="f4664-148">Le fournisseur de banque de messages ne gère pas l’inscription pour la notification par le biais de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="f4664-148">The message store provider does not support registration for notification through the message store.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f4664-149">Remarques</span><span class="sxs-lookup"><span data-stu-id="f4664-149">Remarks</span></span>

<span data-ttu-id="f4664-150">La méthode **IMsgStore::Advise** établit une connexion entre l’appelant de notification de l’objet de réception et la banque de messages ou un objet dans la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="f4664-150">The **IMsgStore::Advise** method establishes a connection between the caller's advise sink object and either the message store or an object in the message store.</span></span> <span data-ttu-id="f4664-151">Cette connexion est utilisée pour envoyer des notifications pour le récepteur de notifications lorsqu’un ou plusieurs événements, tel que spécifié dans le paramètre _ulEventMask_ , se produisent sur l’objet source de notification.</span><span class="sxs-lookup"><span data-stu-id="f4664-151">This connection is used to send notifications to the advise sink when one or more events, as specified in the  _ulEventMask_ parameter, occur to the advise source object.</span></span> <span data-ttu-id="f4664-152">Lorsque le paramètre _lpEntryID_ pointe vers un identificateur d’entrée valide, la source advise est l’objet identifié par l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f4664-152">When the  _lpEntryID_ parameter points to a valid entry identifier, the advise source is the object identified by this entry identifier.</span></span> <span data-ttu-id="f4664-153">Lorsque _lpEntryID_ est NULL, la source advise est la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="f4664-153">When  _lpEntryID_ is NULL, the advise source is the message store.</span></span> 
  
<span data-ttu-id="f4664-154">Pour envoyer une notification, le fournisseur de banque de messages ou MAPI appelle méthode de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) du récepteur des notifications.</span><span class="sxs-lookup"><span data-stu-id="f4664-154">To send a notification, either the message store provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="f4664-155">L’un des paramètres à **OnNotify**, une structure de notification, contient des informations décrivant l’événement spécifique.</span><span class="sxs-lookup"><span data-stu-id="f4664-155">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f4664-156">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="f4664-156">Notes to implementers</span></span>

<span data-ttu-id="f4664-157">Vous pouvez prendre en charge notification avec ou sans l’aide de MAPI.</span><span class="sxs-lookup"><span data-stu-id="f4664-157">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="f4664-158">MAPI a trois méthodes d’objet de prise en charge pour aider les fournisseurs de services à implémenter la notification : [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)et [IMAPISupport::Notify](imapisupport-notify.md).</span><span class="sxs-lookup"><span data-stu-id="f4664-158">MAPI has three support object methods for helping service providers implement notification: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md), and [IMAPISupport::Notify](imapisupport-notify.md).</span></span> <span data-ttu-id="f4664-159">Si vous choisissez d’utiliser les méthodes de prise en charge MAPI, appelé la méthode **Subscribe** lorsque votre méthode **Advise** est appelée et libérer le pointeur _lpAdviseSink_ .</span><span class="sxs-lookup"><span data-stu-id="f4664-159">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="f4664-160">Si vous choisissez prendre en charge de notification vous-même, appelez la méthode de [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) du récepteur advise représenté par le paramètre _lpAdviseSink_ de conserver une copie de ce pointeur.</span><span class="sxs-lookup"><span data-stu-id="f4664-160">If you elect to support notification yourself, call the [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="f4664-161">Mettre à jour cette copie jusqu'à ce que votre méthode [IMsgStore::Unadvise](imsgstore-unadvise.md) est appelée pour annuler l’inscription.</span><span class="sxs-lookup"><span data-stu-id="f4664-161">Maintain this copy until your [IMsgStore::Unadvise](imsgstore-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="f4664-162">Quelle que soit la façon dont vous prenez en charge la notification, affecter un numéro de connexion différente de zéro pour l’inscription de notification et la faire revenir dans le paramètre _lpulConnection_ .</span><span class="sxs-lookup"><span data-stu-id="f4664-162">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="f4664-163">Ne relâchez pas ce numéro de connexion jusqu'à ce que **Unadvise** a été appelée et terminé.</span><span class="sxs-lookup"><span data-stu-id="f4664-163">Do not release this connection number until **Unadvise** has been called and has completed.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f4664-164">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="f4664-164">Notes to callers</span></span>

<span data-ttu-id="f4664-165">Sur les systèmes qui prennent en charge plusieurs threads d’exécution, l’appel de **OnNotify** peut également se produire sur n’importe quel thread à tout moment.</span><span class="sxs-lookup"><span data-stu-id="f4664-165">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="f4664-166">Si vous devez être assuré que les notifications se produisent uniquement à un moment donné sur un thread particulier, appelez la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) pour générer l’objet récepteur advise que vous passez à **Advise**.</span><span class="sxs-lookup"><span data-stu-id="f4664-166">If you must be assured that notifications occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to **Advise**.</span></span> 
  
<span data-ttu-id="f4664-167">Après un appel **Advise** a réussi et **Unadvise** a été appelé pour annuler l’enregistrement, avant d’être préparé pour l’objet de récepteur advise doit être publié.</span><span class="sxs-lookup"><span data-stu-id="f4664-167">After a call to **Advise** has succeeded and before **Unadvise** has been called to cancel the registration, be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="f4664-168">Vous devez libérer votre objet de récepteur advise après **Advise** renvoie à moins d’avoir une utilisation à long terme spécifique pour qu’il.</span><span class="sxs-lookup"><span data-stu-id="f4664-168">You should release your advise sink object after **Advise** returns unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="f4664-169">Pour plus d’informations sur le processus de notification, reportez-vous à la section [Notification d’événement MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="f4664-169">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="f4664-170">Pour plus d’informations sur la gestion des notifications, voir [Gestion des Notifications](handling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="f4664-170">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f4664-171">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f4664-171">MFCMAPI reference</span></span>

<span data-ttu-id="f4664-172">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f4664-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f4664-173">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="f4664-173">**File**</span></span>|<span data-ttu-id="f4664-174">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="f4664-174">**Function**</span></span>|<span data-ttu-id="f4664-175">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="f4664-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f4664-176">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="f4664-176">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="f4664-177">CBaseDialog::OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="f4664-177">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="f4664-178">MFCMAPI utilise la méthode **IMsgStore::Advise** pour enregistrer les notifications dans le magasin de l’intégralité du message.</span><span class="sxs-lookup"><span data-stu-id="f4664-178">MFCMAPI uses the **IMsgStore::Advise** method to register for notifications on the entire message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f4664-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4664-179">See also</span></span>



[<span data-ttu-id="f4664-180">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="f4664-180">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="f4664-181">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="f4664-181">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="f4664-182">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="f4664-182">IMsgStore::Unadvise</span></span>](imsgstore-unadvise.md)
  
[<span data-ttu-id="f4664-183">Notification</span><span class="sxs-lookup"><span data-stu-id="f4664-183">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="f4664-184">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f4664-184">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="f4664-185">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="f4664-185">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

