---
title: IABLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Advise
api_type:
- COM
ms.assetid: 375d65b1-607d-4e2a-8052-9bcbf08fc2ac
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4ab0e4b023e6af19f650abf421aed122dcc21879
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338576"
---
# <a name="iablogonadvise"></a><span data-ttu-id="15beb-103">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="15beb-103">IABLogon::Advise</span></span>

  
  
<span data-ttu-id="15beb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15beb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15beb-105">Inscrit l'appelant pour recevoir une notification des événements spécifiés qui affectent un conteneur, un utilisateur de messagerie ou une liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="15beb-105">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="15beb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="15beb-106">Parameters</span></span>

 <span data-ttu-id="15beb-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="15beb-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="15beb-108">dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="15beb-108">[in] The count of bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="15beb-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="15beb-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="15beb-110">dans Pointeur vers l'identificateur d'entrée de l'objet sur lequel les notifications doivent être générées.</span><span class="sxs-lookup"><span data-stu-id="15beb-110">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span>
    
 <span data-ttu-id="15beb-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="15beb-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="15beb-112">dans Masque de valeurs qui indique les types d'événements de notification qui intéressent l'appelant et qui doit être inclus dans l'inscription.</span><span class="sxs-lookup"><span data-stu-id="15beb-112">[in] A bitmask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="15beb-113">Il existe une structure de [notification](notification.md) correspondante associée à chaque type d'événement qui contient des informations sur l'événement.</span><span class="sxs-lookup"><span data-stu-id="15beb-113">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="15beb-114">Le tableau suivant répertorie les valeurs valides pour le paramètre _ulEventMask_ et les structures associées à chaque valeur.</span><span class="sxs-lookup"><span data-stu-id="15beb-114">The following table lists the valid values for the  _ulEventMask_ parameter and the structures associated with each value.</span></span> 
    
|<span data-ttu-id="15beb-115">**Type d'événement de notification**</span><span class="sxs-lookup"><span data-stu-id="15beb-115">**Notification event type**</span></span>|<span data-ttu-id="15beb-116">**Structure de **notification** correspondante**</span><span class="sxs-lookup"><span data-stu-id="15beb-116">**Corresponding **NOTIFICATION** structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="15beb-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="15beb-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="15beb-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="15beb-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="15beb-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="15beb-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="15beb-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="15beb-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="15beb-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="15beb-121">**fnevObjectDeleted**</span></span> <br/> |<span data-ttu-id="15beb-122">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="15beb-122">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="15beb-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="15beb-123">**fnevObjectModified**</span></span> <br/> |<span data-ttu-id="15beb-124">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="15beb-124">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="15beb-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="15beb-125">**fnevObjectCopied**</span></span> <br/> |<span data-ttu-id="15beb-126">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="15beb-126">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="15beb-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="15beb-127">**fnevObjectMoved**</span></span> <br/> |<span data-ttu-id="15beb-128">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="15beb-128">**OBJECT_NOTIFICATION**</span></span> <br/> |
   
 <span data-ttu-id="15beb-129">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="15beb-129">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="15beb-130">dans Pointeur vers un objet de récepteur de notification pour recevoir les notifications suivantes.</span><span class="sxs-lookup"><span data-stu-id="15beb-130">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span>
    
 <span data-ttu-id="15beb-131">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="15beb-131">_lpulConnection_</span></span>
  
> <span data-ttu-id="15beb-132">remarquer Pointeur vers une valeur différente de zéro qui représente l'enregistrement de la notification.</span><span class="sxs-lookup"><span data-stu-id="15beb-132">[out] A pointer to a nonzero value that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="15beb-133">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="15beb-133">Return value</span></span>

<span data-ttu-id="15beb-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="15beb-134">S_OK</span></span> 
  
> <span data-ttu-id="15beb-135">L'enregistrement de la notification a réussi.</span><span class="sxs-lookup"><span data-stu-id="15beb-135">The notification registration was successful.</span></span>
    
<span data-ttu-id="15beb-136">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="15beb-136">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="15beb-137">L'identificateur d'entrée passé dans le paramètre _lpEntryID_ n'est pas au format approprié.</span><span class="sxs-lookup"><span data-stu-id="15beb-137">The entry identifier passed in the  _lpEntryID_ parameter is not in the appropriate format.</span></span> 
    
<span data-ttu-id="15beb-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="15beb-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="15beb-139">Le fournisseur de carnet d'adresses ne prend pas en charge la notification, probablement parce qu'il ne permet pas de modifier les objets.</span><span class="sxs-lookup"><span data-stu-id="15beb-139">The address book provider does not support notification, possibly because it does not allow changes to be made to its objects.</span></span>
    
<span data-ttu-id="15beb-140">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="15beb-140">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="15beb-141">Le fournisseur de carnet d'adresses ne peut pas gérer l'identificateur d'entrée transmis dans _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="15beb-141">The address book provider cannot handle the entry identifier passed in  _lpEntryID_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="15beb-142">Remarques</span><span class="sxs-lookup"><span data-stu-id="15beb-142">Remarks</span></span>

<span data-ttu-id="15beb-143">Les fournisseurs de carnets d'adresses implémentent la méthode **IABLogon:: Advise** pour enregistrer l'appelant lorsqu'une modification est apportée à un objet dans l'un de ses conteneurs.</span><span class="sxs-lookup"><span data-stu-id="15beb-143">Address book providers implement the **IABLogon::Advise** method to register the caller to be notified when a change occurs to an object in one of their containers.</span></span> <span data-ttu-id="15beb-144">Les appelants peuvent s'inscrire pour les notifications relatives aux utilisateurs de messagerie, aux listes de distribution ou aux conteneurs entiers.</span><span class="sxs-lookup"><span data-stu-id="15beb-144">Callers can register for notifications regarding messaging users, distribution lists, or entire containers.</span></span> 
  
<span data-ttu-id="15beb-145">Les clients appellent généralement la méthode [IAddrBook:: Advise](iaddrbook-advise.md) pour s'inscrire aux notifications de carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="15beb-145">Clients typically call the [IAddrBook::Advise](iaddrbook-advise.md) method to register for address book notifications.</span></span> <span data-ttu-id="15beb-146">MAPI appelle ensuite la \*\*\*\* méthode Advise du fournisseur de carnet d'adresses qui est responsable de l'objet représenté par l'identificateur d'entrée dans _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="15beb-146">MAPI then calls the **Advise** method of the address book provider that is responsible for the object represented by the entry identifier in  _lpEntryID_.</span></span>
  
<span data-ttu-id="15beb-147">Lorsqu'une modification est apportée à l'objet indiqué du type représenté dans _ulEventMask_, un appel est passé à la méthode **OnNotify** du récepteur conseillers vers lequel pointe _lpAdviseSink_.</span><span class="sxs-lookup"><span data-stu-id="15beb-147">When a change occurs to the indicated object of the type represented in  _ulEventMask_, a call is made to the **OnNotify** method of the advise sink pointed to by  _lpAdviseSink_.</span></span> <span data-ttu-id="15beb-148">Les données transmises dans la structure de **notification** à la routine **OnNotify** décrivent l'événement.</span><span class="sxs-lookup"><span data-stu-id="15beb-148">Data passed in the **NOTIFICATION** structure to the **OnNotify** routine describes the event.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="15beb-149">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="15beb-149">Notes to implementers</span></span>

<span data-ttu-id="15beb-150">Vous pouvez prendre en charge les notifications avec ou sans l'aide de MAPI.</span><span class="sxs-lookup"><span data-stu-id="15beb-150">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="15beb-151">MAPI dispose de trois méthodes d'objet de prise en charge pour aider les fournisseurs de services à mettre en œuvre la notification:</span><span class="sxs-lookup"><span data-stu-id="15beb-151">MAPI has three support object methods to help service providers implement notification:</span></span>
  
- [<span data-ttu-id="15beb-152">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="15beb-152">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
    
- [<span data-ttu-id="15beb-153">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="15beb-153">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)
    
- [<span data-ttu-id="15beb-154">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="15beb-154">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
    
<span data-ttu-id="15beb-155">Si vous choisissez d'utiliser les méthodes de prise en charge MAPI, appelez **subscribe** lorsque votre méthode Advise est appelée et relâchez le pointeur _lpAdviseSink_ . \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="15beb-155">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="15beb-156">Si vous choisissez de prendre en charge la notification vous-même, appelez la méthode **AddRef** du récepteur de notifications représenté par le paramètre _lpAdviseSink_ pour conserver une copie de ce pointeur.</span><span class="sxs-lookup"><span data-stu-id="15beb-156">If you elect to support notification yourself, call the **AddRef** method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="15beb-157">Conservez cette copie jusqu'à ce que la méthode [IABLogon::](iablogon-unadvise.md) Unadvise soit appelée pour annuler l'inscription.</span><span class="sxs-lookup"><span data-stu-id="15beb-157">Maintain this copy until your [IABLogon::Unadvise](iablogon-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="15beb-158">Quelle que soit la façon dont vous prenez en charge la notification, attribuez un numéro de connexion différent de zéro à l'enregistrement des notifications et renvoyez-le dans le paramètre _lpulConnection_ .</span><span class="sxs-lookup"><span data-stu-id="15beb-158">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="15beb-159">Ne libérez pas ce numéro de connexion \*\*\*\* tant que la méthode Unadvise n'a pas été appelée.</span><span class="sxs-lookup"><span data-stu-id="15beb-159">Do not release this connection number until the **Unadvise** method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="15beb-160">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="15beb-160">Notes to callers</span></span>

<span data-ttu-id="15beb-161">Le pointeur de récepteur de notifications transmis dans le paramètre _lpAdviseSink_ à Advise peut pointer vers un objet que vous avez créé ou que MAPI a créé par le biais de la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="15beb-161">The advise sink pointer that you pass in the  _lpAdviseSink_ parameter to **Advise** can point to an object that you have created or that MAPI has created through the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> <span data-ttu-id="15beb-162">Vous pouvez utiliser **HrThisThreadAdviseSink** si vous prenez en charge plusieurs threads d'exécution et que vous souhaitez vous assurer que les appels suivants à votre méthode **OnNotify** se produisent à un moment approprié sur un thread approprié.</span><span class="sxs-lookup"><span data-stu-id="15beb-162">You might want to use **HrThisThreadAdviseSink** if you support multiple threads of execution and want to be sure that that subsequent calls to your **OnNotify** method occur at an appropriate time on an appropriate thread.</span></span> 
  
<span data-ttu-id="15beb-163">Préparez-vous à ce que votre objet de récepteur de notifications soit libéré à tout moment après votre appel à **conseiller** et avant l'appel à Unadvise. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="15beb-163">Be prepared for your advise sink object to be released any time after your call to **Advise** and before your call to **Unadvise**.</span></span> <span data-ttu-id="15beb-164">Par conséquent, vous devez libérer votre objet de récepteur \*\*\*\* d'avertissement une fois qu'il a été renvoyé, sauf si vous disposez d'une utilisation de longue durée spécifique.</span><span class="sxs-lookup"><span data-stu-id="15beb-164">Therefore, you should release your advise sink object after **Advise** returns, unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="15beb-165">Pour plus d'informations sur le processus de notification, consultez la rubrique [notifications d'événements dans MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="15beb-165">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="15beb-166">Pour plus d'informations sur l'utilisation des méthodes **IMAPISupport** pour prendre en charge la notification, consultez la rubrique [prise en](supporting-event-notification.md)charge des notifications d'événements.</span><span class="sxs-lookup"><span data-stu-id="15beb-166">For information about how to use the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span> <span data-ttu-id="15beb-167">Pour plus d'informations sur le multithreading et MAPI, voir [Threading in MAPI](threading-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="15beb-167">For more information about multithreading and MAPI, see [Threading in MAPI](threading-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="15beb-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15beb-168">See also</span></span>



[<span data-ttu-id="15beb-169">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="15beb-169">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="15beb-170">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="15beb-170">IABLogon::Unadvise</span></span>](iablogon-unadvise.md)
  
[<span data-ttu-id="15beb-171">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="15beb-171">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="15beb-172">Notification</span><span class="sxs-lookup"><span data-stu-id="15beb-172">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="15beb-173">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="15beb-173">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

