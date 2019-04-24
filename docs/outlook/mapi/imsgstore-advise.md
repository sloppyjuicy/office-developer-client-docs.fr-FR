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
ms.openlocfilehash: 3b4abef731541e308b2c2ebc6f4aaddf4458e257
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317324"
---
# <a name="imsgstoreadvise"></a><span data-ttu-id="074db-103">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="074db-103">IMsgStore::Advise</span></span>

  
  
<span data-ttu-id="074db-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="074db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="074db-105">S'inscrire pour recevoir une notification des événements spécifiés qui affectent la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="074db-105">Registers to receive notification of specified events that affect the message store.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="074db-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="074db-106">Parameters</span></span>

 <span data-ttu-id="074db-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="074db-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="074db-108">dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="074db-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="074db-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="074db-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="074db-110">dans Pointeur vers l'identificateur d'entrée du dossier ou du message sur les notifications à générer, ou sur **null**.</span><span class="sxs-lookup"><span data-stu-id="074db-110">[in] A pointer to the entry identifier of the folder or message about which notifications should be generated, or **null**.</span></span> <span data-ttu-id="074db-111">Si _lpEntryID_ est défini sur null, **Advise** les registres des notifications sur l'intégralité de la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="074db-111">If  _lpEntryID_ is set to NULL, **Advise** registers for notifications on the entire message store.</span></span> 
    
 <span data-ttu-id="074db-112">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="074db-112">_ulEventMask_</span></span>
  
> <span data-ttu-id="074db-113">dans Masque de valeurs qui indiquent les types d'événements de notification qui intéressent l'appelant et qui doit être inclus dans l'inscription.</span><span class="sxs-lookup"><span data-stu-id="074db-113">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="074db-114">Il existe une structure de [notification](notification.md) correspondante associée à chaque type d'événement qui contient des informations sur l'événement.</span><span class="sxs-lookup"><span data-stu-id="074db-114">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="074db-115">Les valeurs valides pour le paramètre _ulEventMask_ sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="074db-115">The following are valid values for the  _ulEventMask_ parameter:</span></span> 
    
 <span data-ttu-id="074db-116">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="074db-116">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="074db-117">Enregistre les notifications concernant les erreurs graves, telles que la mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="074db-117">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="074db-118">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="074db-118">_fnevExtended_</span></span>
  
> <span data-ttu-id="074db-119">Enregistre les notifications relatives aux événements spécifiques au fournisseur de banque de messages particulier.</span><span class="sxs-lookup"><span data-stu-id="074db-119">Registers for notifications about events specific to the particular message store provider.</span></span>
    
 <span data-ttu-id="074db-120">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="074db-120">_fnevNewMail_</span></span>
  
> <span data-ttu-id="074db-121">Enregistre les notifications relatives à l'arrivée de nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="074db-121">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="074db-122">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="074db-122">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="074db-123">Enregistre les notifications relatives à la création d'un nouveau dossier ou d'un nouveau message.</span><span class="sxs-lookup"><span data-stu-id="074db-123">Registers for notifications about the creation of a new folder or message.</span></span>
    
 <span data-ttu-id="074db-124">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="074db-124">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="074db-125">Enregistre les notifications relatives à la copie d'un dossier ou d'un message.</span><span class="sxs-lookup"><span data-stu-id="074db-125">Registers for notifications about a folder or message being copied.</span></span>
    
 <span data-ttu-id="074db-126">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="074db-126">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="074db-127">Enregistre les notifications relatives à la suppression d'un dossier ou d'un message.</span><span class="sxs-lookup"><span data-stu-id="074db-127">Registers for notifications about a folder or message being deleted.</span></span>
    
 <span data-ttu-id="074db-128">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="074db-128">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="074db-129">Enregistre les notifications relatives à la modification d'un dossier ou d'un message.</span><span class="sxs-lookup"><span data-stu-id="074db-129">Registers for notifications about a folder or message being modified.</span></span>
    
 <span data-ttu-id="074db-130">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="074db-130">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="074db-131">Enregistre les notifications relatives à un dossier ou à un message déplacé.</span><span class="sxs-lookup"><span data-stu-id="074db-131">Registers for notifications about a folder or message being moved.</span></span>
    
 <span data-ttu-id="074db-132">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="074db-132">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="074db-133">Enregistre les notifications relatives à l'exécution d'une opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="074db-133">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="074db-134">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="074db-134">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="074db-135">dans Pointeur vers un objet de récepteur de notification pour recevoir les notifications suivantes.</span><span class="sxs-lookup"><span data-stu-id="074db-135">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="074db-136">Cet objet de récepteur de notifications doit déjà avoir été alloué.</span><span class="sxs-lookup"><span data-stu-id="074db-136">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="074db-137">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="074db-137">_lpulConnection_</span></span>
  
> <span data-ttu-id="074db-138">remarquer Pointeur vers un nombre différent de zéro qui représente la connexion entre l'objet de récepteur d'avertissement de l'appelant et la session.</span><span class="sxs-lookup"><span data-stu-id="074db-138">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span> 
    
 <span data-ttu-id="074db-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="074db-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="074db-140">dans Pointeur vers un objet de récepteur de notification pour recevoir les notifications suivantes.</span><span class="sxs-lookup"><span data-stu-id="074db-140">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="074db-141">Cet objet de récepteur de notifications doit déjà avoir été alloué.</span><span class="sxs-lookup"><span data-stu-id="074db-141">This advise sink object must have already been allocated.</span></span> 
    
 <span data-ttu-id="074db-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="074db-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="074db-143">remarquer Pointeur vers un numéro de connexion différent de zéro qui représente la connexion entre l'objet de récepteur de notification de l'appelant et la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="074db-143">[out] A pointer to a nonzero connection number that represents the connection between the caller's advise sink object and the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="074db-144">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="074db-144">Return value</span></span>

<span data-ttu-id="074db-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="074db-145">S_OK</span></span> 
  
> <span data-ttu-id="074db-146">L'inscription a réussi.</span><span class="sxs-lookup"><span data-stu-id="074db-146">The registration was successful.</span></span>
    
<span data-ttu-id="074db-147">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="074db-147">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="074db-148">Le fournisseur de banque de messages ne prend pas en charge l'enregistrement des notifications par le biais de la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="074db-148">The message store provider does not support registration for notification through the message store.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="074db-149">Remarques</span><span class="sxs-lookup"><span data-stu-id="074db-149">Remarks</span></span>

<span data-ttu-id="074db-150">La méthode **IMsgStore:: Advise** établit une connexion entre l'objet récepteur de notification de l'appelant et la Banque de messages ou un objet dans la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="074db-150">The **IMsgStore::Advise** method establishes a connection between the caller's advise sink object and either the message store or an object in the message store.</span></span> <span data-ttu-id="074db-151">Cette connexion est utilisée pour envoyer des notifications au récepteur de notifications lorsqu'un ou plusieurs événements, tels que spécifiés dans le paramètre _ulEventMask_ , ont lieu dans l'objet de source Advise.</span><span class="sxs-lookup"><span data-stu-id="074db-151">This connection is used to send notifications to the advise sink when one or more events, as specified in the  _ulEventMask_ parameter, occur to the advise source object.</span></span> <span data-ttu-id="074db-152">Lorsque le paramètre _lpEntryID_ pointe vers un identificateur d'entrée valide, la source de notification est l'objet identifié par cet identificateur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="074db-152">When the  _lpEntryID_ parameter points to a valid entry identifier, the advise source is the object identified by this entry identifier.</span></span> <span data-ttu-id="074db-153">Lorsque _lpEntryID_ est null, la source de notification est la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="074db-153">When  _lpEntryID_ is NULL, the advise source is the message store.</span></span> 
  
<span data-ttu-id="074db-154">Pour envoyer une notification, le fournisseur de banque de messages ou MAPI appelle la méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) du récepteur de notification enregistré.</span><span class="sxs-lookup"><span data-stu-id="074db-154">To send a notification, either the message store provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="074db-155">L'un des paramètres de **OnNotify**, une structure de notification, contient des informations qui décrivent l'événement spécifique.</span><span class="sxs-lookup"><span data-stu-id="074db-155">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="074db-156">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="074db-156">Notes to implementers</span></span>

<span data-ttu-id="074db-157">Vous pouvez prendre en charge les notifications avec ou sans l'aide de MAPI.</span><span class="sxs-lookup"><span data-stu-id="074db-157">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="074db-158">MAPI dispose de trois méthodes d'objet de prise en charge pour aider les fournisseurs de services à implémenter la notification: [IMAPISupport:: subscribe](imapisupport-subscribe.md), [IMAPISupport:: unsubscribe](imapisupport-unsubscribe.md)et [IMAPISupport:: Notify](imapisupport-notify.md).</span><span class="sxs-lookup"><span data-stu-id="074db-158">MAPI has three support object methods for helping service providers implement notification: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md), and [IMAPISupport::Notify](imapisupport-notify.md).</span></span> <span data-ttu-id="074db-159">Si vous choisissez d'utiliser les méthodes de prise en charge MAPI, appelez **subscribe** lorsque votre méthode Advise est appelée et relâchez le pointeur _lpAdviseSink_ . \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="074db-159">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="074db-160">Si vous choisissez de prendre en charge la notification vous-même, appelez la méthode [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) du récepteur de notifications représenté par le paramètre _lpAdviseSink_ pour conserver une copie de ce pointeur.</span><span class="sxs-lookup"><span data-stu-id="074db-160">If you elect to support notification yourself, call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="074db-161">Conservez cette copie jusqu'à ce que la méthode [IMsgStore::](imsgstore-unadvise.md) Unadvise soit appelée pour annuler l'inscription.</span><span class="sxs-lookup"><span data-stu-id="074db-161">Maintain this copy until your [IMsgStore::Unadvise](imsgstore-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="074db-162">Quelle que soit la façon dont vous prenez en charge la notification, attribuez un numéro de connexion différent de zéro à l'enregistrement des notifications et renvoyez-le dans le paramètre _lpulConnection_ .</span><span class="sxs-lookup"><span data-stu-id="074db-162">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="074db-163">Ne libérez pas ce numéro de \*\*\*\* connexion tant que Unadvise n'a pas été appelé et qu'il est terminé.</span><span class="sxs-lookup"><span data-stu-id="074db-163">Do not release this connection number until **Unadvise** has been called and has completed.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="074db-164">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="074db-164">Notes to callers</span></span>

<span data-ttu-id="074db-165">Sur les systèmes qui prennent en charge plusieurs threads d'exécution, l'appel à **OnNotify** peut également se produire sur n'importe quel thread à tout moment.</span><span class="sxs-lookup"><span data-stu-id="074db-165">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="074db-166">Si vous devez être sûr que les notifications ne se produisent qu'à un moment donné sur un thread particulier, appelez la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) pour générer l'objet de récepteur de notifications que vous transmettez à l' **avis**.</span><span class="sxs-lookup"><span data-stu-id="074db-166">If you must be assured that notifications occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to **Advise**.</span></span> 
  
<span data-ttu-id="074db-167">Une fois qu'un \*\*\*\* appel à Advise a réussi et avant que Unadvise ait été appelé pour annuler l'inscription, soyez prêt à libérer l'objet de récepteur de notifications. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="074db-167">After a call to **Advise** has succeeded and before **Unadvise** has been called to cancel the registration, be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="074db-168">Vous devez libérer votre objet de récepteur d' \*\*\*\* avertissement après le renvoi de la fonction Advise, sauf si vous disposez d'une utilisation de longue durée spécifique.</span><span class="sxs-lookup"><span data-stu-id="074db-168">You should release your advise sink object after **Advise** returns unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="074db-169">Pour plus d'informations sur le processus de notification, consultez la rubrique [notifications d'événements dans MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="074db-169">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="074db-170">Pour plus d'informations sur la gestion des notifications, consultez la rubrique [gestion](handling-notifications.md)des notifications.</span><span class="sxs-lookup"><span data-stu-id="074db-170">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="074db-171">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="074db-171">MFCMAPI reference</span></span>

<span data-ttu-id="074db-172">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="074db-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="074db-173">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="074db-173">**File**</span></span>|<span data-ttu-id="074db-174">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="074db-174">**Function**</span></span>|<span data-ttu-id="074db-175">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="074db-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="074db-176">BaseDialog. cpp</span><span class="sxs-lookup"><span data-stu-id="074db-176">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="074db-177">CBaseDialog:: OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="074db-177">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="074db-178">MFCMAPI utilise la méthode **IMsgStore:: Advise** pour s'inscrire aux notifications sur l'intégralité de la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="074db-178">MFCMAPI uses the **IMsgStore::Advise** method to register for notifications on the entire message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="074db-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="074db-179">See also</span></span>



[<span data-ttu-id="074db-180">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="074db-180">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="074db-181">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="074db-181">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="074db-182">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="074db-182">IMsgStore::Unadvise</span></span>](imsgstore-unadvise.md)
  
[<span data-ttu-id="074db-183">Notification</span><span class="sxs-lookup"><span data-stu-id="074db-183">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="074db-184">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="074db-184">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="074db-185">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="074db-185">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

