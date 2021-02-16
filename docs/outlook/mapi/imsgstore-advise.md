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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3b4abef731541e308b2c2ebc6f4aaddf4458e257
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317324"
---
# <a name="imsgstoreadvise"></a><span data-ttu-id="8a245-103">IMsgStore::Advise</span><span class="sxs-lookup"><span data-stu-id="8a245-103">IMsgStore::Advise</span></span>

  
  
<span data-ttu-id="8a245-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a245-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a245-105">S’inscrit pour recevoir une notification des événements spécifiés qui affectent la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="8a245-105">Registers to receive notification of specified events that affect the message store.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="8a245-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a245-106">Parameters</span></span>

 <span data-ttu-id="8a245-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="8a245-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="8a245-108">[in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="8a245-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="8a245-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="8a245-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="8a245-110">[in] Pointeur vers l’identificateur d’entrée du dossier ou du message concernant les notifications à générer, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="8a245-110">[in] A pointer to the entry identifier of the folder or message about which notifications should be generated, or **null**.</span></span> <span data-ttu-id="8a245-111">Si  _lpEntryID_ est définie sur NULL, **Advise** s’inscrit pour les notifications sur l’ensemble de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="8a245-111">If  _lpEntryID_ is set to NULL, **Advise** registers for notifications on the entire message store.</span></span> 
    
 <span data-ttu-id="8a245-112">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="8a245-112">_ulEventMask_</span></span>
  
> <span data-ttu-id="8a245-113">[in] Masque de valeurs qui indiquent les types d’événements de notification qui intéressent l’appelant et qui doivent être inclus dans l’inscription.</span><span class="sxs-lookup"><span data-stu-id="8a245-113">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="8a245-114">Il existe une structure [de NOTIFICATION](notification.md) correspondante associée à chaque type d’événement qui contient des informations sur l’événement.</span><span class="sxs-lookup"><span data-stu-id="8a245-114">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="8a245-115">Les valeurs suivantes sont valides pour  _le paramètre ulEventMask_ :</span><span class="sxs-lookup"><span data-stu-id="8a245-115">The following are valid values for the  _ulEventMask_ parameter:</span></span> 
    
 <span data-ttu-id="8a245-116">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="8a245-116">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="8a245-117">S’inscrit aux notifications concernant les erreurs graves, telles que la mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="8a245-117">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="8a245-118">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="8a245-118">_fnevExtended_</span></span>
  
> <span data-ttu-id="8a245-119">S’inscrit pour les notifications sur les événements spécifiques au fournisseur de magasin de messages particulier.</span><span class="sxs-lookup"><span data-stu-id="8a245-119">Registers for notifications about events specific to the particular message store provider.</span></span>
    
 <span data-ttu-id="8a245-120">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="8a245-120">_fnevNewMail_</span></span>
  
> <span data-ttu-id="8a245-121">S’inscrit aux notifications concernant l’arrivée de nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="8a245-121">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="8a245-122">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="8a245-122">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="8a245-123">S’inscrit aux notifications concernant la création d’un dossier ou d’un message.</span><span class="sxs-lookup"><span data-stu-id="8a245-123">Registers for notifications about the creation of a new folder or message.</span></span>
    
 <span data-ttu-id="8a245-124">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="8a245-124">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="8a245-125">S’inscrit aux notifications concernant un dossier ou un message en cours de copie.</span><span class="sxs-lookup"><span data-stu-id="8a245-125">Registers for notifications about a folder or message being copied.</span></span>
    
 <span data-ttu-id="8a245-126">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="8a245-126">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="8a245-127">S’inscrit aux notifications concernant la suppression d’un dossier ou d’un message.</span><span class="sxs-lookup"><span data-stu-id="8a245-127">Registers for notifications about a folder or message being deleted.</span></span>
    
 <span data-ttu-id="8a245-128">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="8a245-128">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="8a245-129">S’inscrit aux notifications concernant la modification d’un dossier ou d’un message.</span><span class="sxs-lookup"><span data-stu-id="8a245-129">Registers for notifications about a folder or message being modified.</span></span>
    
 <span data-ttu-id="8a245-130">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="8a245-130">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="8a245-131">S’inscrit aux notifications concernant un dossier ou un message déplacé.</span><span class="sxs-lookup"><span data-stu-id="8a245-131">Registers for notifications about a folder or message being moved.</span></span>
    
 <span data-ttu-id="8a245-132">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="8a245-132">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="8a245-133">S’inscrit aux notifications concernant la fin d’une opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="8a245-133">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="8a245-134">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="8a245-134">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="8a245-135">[in] Pointeur vers un objet de réception de notification pour recevoir les notifications suivantes.</span><span class="sxs-lookup"><span data-stu-id="8a245-135">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="8a245-136">Cet objet de sink de conseil doit avoir déjà été alloué.</span><span class="sxs-lookup"><span data-stu-id="8a245-136">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="8a245-137">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="8a245-137">_lpulConnection_</span></span>
  
> <span data-ttu-id="8a245-138">[out] Pointeur vers un numéro autre que zéro qui représente la connexion entre l’objet de l’objet de conseiller de l’appelant et la session.</span><span class="sxs-lookup"><span data-stu-id="8a245-138">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span> 
    
 <span data-ttu-id="8a245-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="8a245-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="8a245-140">[in] Pointeur vers un objet de réception de notification pour recevoir les notifications suivantes.</span><span class="sxs-lookup"><span data-stu-id="8a245-140">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="8a245-141">Cet objet de sink de conseil doit avoir déjà été alloué.</span><span class="sxs-lookup"><span data-stu-id="8a245-141">This advise sink object must have already been allocated.</span></span> 
    
 <span data-ttu-id="8a245-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="8a245-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="8a245-143">[out] Pointeur vers un numéro de connexion autre que zéro qui représente la connexion entre l’objet de l’objet de conseiller de l’appelant et la magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="8a245-143">[out] A pointer to a nonzero connection number that represents the connection between the caller's advise sink object and the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8a245-144">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8a245-144">Return value</span></span>

<span data-ttu-id="8a245-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="8a245-145">S_OK</span></span> 
  
> <span data-ttu-id="8a245-146">L’inscription a réussi.</span><span class="sxs-lookup"><span data-stu-id="8a245-146">The registration was successful.</span></span>
    
<span data-ttu-id="8a245-147">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="8a245-147">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="8a245-148">Le fournisseur de la boutique de messages ne prend pas en charge l’inscription pour la notification via la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="8a245-148">The message store provider does not support registration for notification through the message store.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8a245-149">Remarques</span><span class="sxs-lookup"><span data-stu-id="8a245-149">Remarks</span></span>

<span data-ttu-id="8a245-150">La **méthode IMsgStore::Advise** établit une connexion entre l’objet de l’objet de l’appelant qui le conseille et la magasin de messages ou un objet dans la magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="8a245-150">The **IMsgStore::Advise** method establishes a connection between the caller's advise sink object and either the message store or an object in the message store.</span></span> <span data-ttu-id="8a245-151">Cette connexion est utilisée pour envoyer des notifications au réception de notification lorsqu’un ou plusieurs événements, comme spécifié dans le paramètre  _ulEventMask,_ se produisent à l’objet source de notification.</span><span class="sxs-lookup"><span data-stu-id="8a245-151">This connection is used to send notifications to the advise sink when one or more events, as specified in the  _ulEventMask_ parameter, occur to the advise source object.</span></span> <span data-ttu-id="8a245-152">Lorsque le  _paramètre lpEntryID_ pointe vers un identificateur d’entrée valide, la source de conseil est l’objet identifié par cet identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="8a245-152">When the  _lpEntryID_ parameter points to a valid entry identifier, the advise source is the object identified by this entry identifier.</span></span> <span data-ttu-id="8a245-153">Lorsque  _lpEntryID_ est NULL, la source de conseil est la magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="8a245-153">When  _lpEntryID_ is NULL, the advise source is the message store.</span></span> 
  
<span data-ttu-id="8a245-154">Pour envoyer une notification, le fournisseur de magasin de messages ou MAPI appelle la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) du sink de notification inscrit.</span><span class="sxs-lookup"><span data-stu-id="8a245-154">To send a notification, either the message store provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="8a245-155">L’un des paramètres **de OnNotify**, une structure de notification, contient des informations qui décrivent l’événement spécifique.</span><span class="sxs-lookup"><span data-stu-id="8a245-155">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8a245-156">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="8a245-156">Notes to implementers</span></span>

<span data-ttu-id="8a245-157">Vous pouvez prendre en charge les notifications avec ou sans l’aide de MAPI.</span><span class="sxs-lookup"><span data-stu-id="8a245-157">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="8a245-158">MAPI dispose de trois méthodes objet de support pour aider les fournisseurs de services à implémenter la notification : [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)et [IMAPISupport::Notify](imapisupport-notify.md).</span><span class="sxs-lookup"><span data-stu-id="8a245-158">MAPI has three support object methods for helping service providers implement notification: [IMAPISupport::Subscribe](imapisupport-subscribe.md), [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md), and [IMAPISupport::Notify](imapisupport-notify.md).</span></span> <span data-ttu-id="8a245-159">Si vous utilisez les méthodes de support MAPI, appelez **Subscribe** lorsque votre méthode **Advise** est appelée et relâchez le pointeur _lpAdviseSink._</span><span class="sxs-lookup"><span data-stu-id="8a245-159">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="8a245-160">Si vous avez choisi de prendre en charge la notification vous-même, appelez la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) du sink de notification représenté par le paramètre  _lpAdviseSink_ pour conserver une copie de ce pointeur.</span><span class="sxs-lookup"><span data-stu-id="8a245-160">If you elect to support notification yourself, call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="8a245-161">Conservez cette copie jusqu’à ce que [votre méthode IMsgStore::Unadvise](imsgstore-unadvise.md) soit appelée pour annuler l’inscription.</span><span class="sxs-lookup"><span data-stu-id="8a245-161">Maintain this copy until your [IMsgStore::Unadvise](imsgstore-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="8a245-162">Quelle que soit la prise en charge de la notification, affectez un numéro de connexion non zéro à l’inscription de la notification et renvoyez-le dans _le paramètre lpulConnection._</span><span class="sxs-lookup"><span data-stu-id="8a245-162">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="8a245-163">Ne relâchez pas ce numéro de connexion tant **qu’Unadvise n’a** pas été appelé et n’est pas terminé.</span><span class="sxs-lookup"><span data-stu-id="8a245-163">Do not release this connection number until **Unadvise** has been called and has completed.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8a245-164">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="8a245-164">Notes to callers</span></span>

<span data-ttu-id="8a245-165">Sur les systèmes qui prendre en charge plusieurs threads d’exécution, l’appel à **OnNotify** peut également se produire sur n’importe quel thread à tout moment.</span><span class="sxs-lookup"><span data-stu-id="8a245-165">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="8a245-166">Si vous devez être certain que les notifications se produisent uniquement à un moment particulier sur un thread particulier, appelez la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) pour générer l’objet de réception de notification que vous passez à **Advise**.</span><span class="sxs-lookup"><span data-stu-id="8a245-166">If you must be assured that notifications occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to **Advise**.</span></span> 
  
<span data-ttu-id="8a245-167">Une fois qu’un appel à **Advise** a réussi et avant **qu’Unadvise** ait été appelé pour annuler l’inscription, soyez prêt à libérer l’objet du reçu de conseil.</span><span class="sxs-lookup"><span data-stu-id="8a245-167">After a call to **Advise** has succeeded and before **Unadvise** has been called to cancel the registration, be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="8a245-168">Vous devez libérer votre objet de sink de conseil après le retour **de Advise,** sauf si vous avez une utilisation spécifique à long terme pour lui.</span><span class="sxs-lookup"><span data-stu-id="8a245-168">You should release your advise sink object after **Advise** returns unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="8a245-169">Pour plus d’informations sur le processus de notification, voir [notification d’événement dans MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="8a245-169">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="8a245-170">Pour plus d’informations sur la gestion des notifications, voir [Gestion des notifications.](handling-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="8a245-170">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8a245-171">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="8a245-171">MFCMAPI reference</span></span>

<span data-ttu-id="8a245-172">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8a245-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8a245-173">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="8a245-173">**File**</span></span>|<span data-ttu-id="8a245-174">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="8a245-174">**Function**</span></span>|<span data-ttu-id="8a245-175">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="8a245-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8a245-176">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="8a245-176">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="8a245-177">CBaseDialog::OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="8a245-177">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="8a245-178">MFCMAPI utilise la **méthode IMsgStore::Advise** pour s’inscrire aux notifications sur l’ensemble de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="8a245-178">MFCMAPI uses the **IMsgStore::Advise** method to register for notifications on the entire message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8a245-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a245-179">See also</span></span>



[<span data-ttu-id="8a245-180">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="8a245-180">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="8a245-181">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="8a245-181">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="8a245-182">IMsgStore::Unadvise</span><span class="sxs-lookup"><span data-stu-id="8a245-182">IMsgStore::Unadvise</span></span>](imsgstore-unadvise.md)
  
[<span data-ttu-id="8a245-183">Notification</span><span class="sxs-lookup"><span data-stu-id="8a245-183">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="8a245-184">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8a245-184">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="8a245-185">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="8a245-185">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

