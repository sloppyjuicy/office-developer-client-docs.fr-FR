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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ea72a6fd2a22fe87ad63bb9c8fa6c1416d876b66
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564247"
---
# <a name="iablogonadvise"></a><span data-ttu-id="0ce6a-103">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="0ce6a-103">IABLogon::Advise</span></span>

  
  
<span data-ttu-id="0ce6a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ce6a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ce6a-105">Enregistre l’appelant pour recevoir des notifications d’événements spécifiques qui affectent un conteneur, utilisateur ou liste de distribution de messagerie.</span><span class="sxs-lookup"><span data-stu-id="0ce6a-105">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="0ce6a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ce6a-106">Parameters</span></span>

 <span data-ttu-id="0ce6a-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="0ce6a-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="0ce6a-108">[in] Le nombre d’octets de l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="0ce6a-108">[in] The count of bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="0ce6a-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="0ce6a-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="0ce6a-110">[in] Pointeur vers l’identificateur d’entrée de l’objet sur lequel les notifications doivent être générées.</span><span class="sxs-lookup"><span data-stu-id="0ce6a-110">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span>
    
 <span data-ttu-id="0ce6a-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="0ce6a-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="0ce6a-112">[in] Un masque binaire composé des valeurs qui indiquent les types d’événements de notification que l’appelant est intéressée par et doit être inclus dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="0ce6a-112">[in] A bitmask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="0ce6a-113">Il existe une structure [NOTIFICATION](notification.md) correspondante associée à chaque type d’événement qui conserve des informations sur l’événement.</span><span class="sxs-lookup"><span data-stu-id="0ce6a-113">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="0ce6a-114">Le tableau suivant répertorie les valeurs valides pour le paramètre _ulEventMask_ et les structures associés à chaque valeur.</span><span class="sxs-lookup"><span data-stu-id="0ce6a-114">The following table lists the valid values for the  _ulEventMask_ parameter and the structures associated with each value.</span></span> 
    
|<span data-ttu-id="0ce6a-115">**Type d’événement notification**</span><span class="sxs-lookup"><span data-stu-id="0ce6a-115">**Notification event type**</span></span>|<span data-ttu-id="0ce6a-116">**Structure **NOTIFICATION** correspondante**</span><span class="sxs-lookup"><span data-stu-id="0ce6a-116">**Corresponding **NOTIFICATION** structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0ce6a-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="0ce6a-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="0ce6a-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="0ce6a-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="0ce6a-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="0ce6a-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="0ce6a-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="0ce6a-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="0ce6a-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="0ce6a-121">**fnevObjectDeleted**</span></span> <br/> |<span data-ttu-id="0ce6a-122">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="0ce6a-122">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="0ce6a-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="0ce6a-123">**fnevObjectModified**</span></span> <br/> |<span data-ttu-id="0ce6a-124">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="0ce6a-124">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="0ce6a-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="0ce6a-125">**fnevObjectCopied**</span></span> <br/> |<span data-ttu-id="0ce6a-126">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="0ce6a-126">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="0ce6a-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="0ce6a-127">**fnevObjectMoved**</span></span> <br/> |<span data-ttu-id="0ce6a-128">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="0ce6a-128">**OBJECT_NOTIFICATION**</span></span> <br/> |
   
 <span data-ttu-id="0ce6a-129">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="0ce6a-129">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="0ce6a-130">[in] Pointeur vers un objet de récepteur advise pour recevoir les notifications ultérieures.</span><span class="sxs-lookup"><span data-stu-id="0ce6a-130">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span>
    
 <span data-ttu-id="0ce6a-131">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="0ce6a-131">_lpulConnection_</span></span>
  
> <span data-ttu-id="0ce6a-132">[out] Pointeur vers une valeur différente de zéro qui représente l’enregistrement de notification.</span><span class="sxs-lookup"><span data-stu-id="0ce6a-132">[out] A pointer to a nonzero value that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0ce6a-133">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0ce6a-133">Return value</span></span>

<span data-ttu-id="0ce6a-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="0ce6a-134">S_OK</span></span> 
  
> <span data-ttu-id="0ce6a-135">L’inscription de notification a réussi.</span><span class="sxs-lookup"><span data-stu-id="0ce6a-135">The notification registration was successful.</span></span>
    
<span data-ttu-id="0ce6a-136">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="0ce6a-136">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="0ce6a-137">L’identificateur d’entrée passé dans le paramètre _lpEntryID_ n’est pas au format approprié.</span><span class="sxs-lookup"><span data-stu-id="0ce6a-137">The entry identifier passed in the  _lpEntryID_ parameter is not in the appropriate format.</span></span> 
    
<span data-ttu-id="0ce6a-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="0ce6a-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="0ce6a-139">Le fournisseur de carnet d’adresses ne gère pas la notification, éventuellement, car il n’autorise pas les modifications apportées à ses objets.</span><span class="sxs-lookup"><span data-stu-id="0ce6a-139">The address book provider does not support notification, possibly because it does not allow changes to be made to its objects.</span></span>
    
<span data-ttu-id="0ce6a-140">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="0ce6a-140">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="0ce6a-141">Le fournisseur de carnet d’adresses ne peut pas gérer l’identificateur d’entrée passé _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="0ce6a-141">The address book provider cannot handle the entry identifier passed in  _lpEntryID_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0ce6a-142">Remarques</span><span class="sxs-lookup"><span data-stu-id="0ce6a-142">Remarks</span></span>

<span data-ttu-id="0ce6a-143">Fournisseurs de carnet d’adresses implémentent la méthode **IABLogon::Advise** pour enregistrer l’appelant à être averti lorsque cet événement se produit une modification à un objet dans un de leurs conteneurs.</span><span class="sxs-lookup"><span data-stu-id="0ce6a-143">Address book providers implement the **IABLogon::Advise** method to register the caller to be notified when a change occurs to an object in one of their containers.</span></span> <span data-ttu-id="0ce6a-144">Les appelants peuvent s’inscrire pour les notifications concernant les utilisateurs de messagerie, des listes de distribution ou des conteneurs entières.</span><span class="sxs-lookup"><span data-stu-id="0ce6a-144">Callers can register for notifications regarding messaging users, distribution lists, or entire containers.</span></span> 
  
<span data-ttu-id="0ce6a-145">Généralement, les clients appeler la méthode [IAddrBook::Advise](iaddrbook-advise.md) pour enregistrer les notifications de carnet d’adresse.</span><span class="sxs-lookup"><span data-stu-id="0ce6a-145">Clients typically call the [IAddrBook::Advise](iaddrbook-advise.md) method to register for address book notifications.</span></span> <span data-ttu-id="0ce6a-146">MAPI appelle ensuite la méthode **Advise** du fournisseur de carnet d’adresses qui est responsable de l’objet représenté par l’identificateur d’entrée dans _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="0ce6a-146">MAPI then calls the **Advise** method of the address book provider that is responsible for the object represented by the entry identifier in  _lpEntryID_.</span></span>
  
<span data-ttu-id="0ce6a-147">Lorsqu’une modification est apportée à l’objet du type représenté dans _ulEventMask_indiqué, un appel est effectué à la méthode **OnNotify** du récepteur advise désigné par _lpAdviseSink_.</span><span class="sxs-lookup"><span data-stu-id="0ce6a-147">When a change occurs to the indicated object of the type represented in  _ulEventMask_, a call is made to the **OnNotify** method of the advise sink pointed to by  _lpAdviseSink_.</span></span> <span data-ttu-id="0ce6a-148">Données transmises dans la structure de **NOTIFICATION** à la routine **OnNotify** décrivent l’événement.</span><span class="sxs-lookup"><span data-stu-id="0ce6a-148">Data passed in the **NOTIFICATION** structure to the **OnNotify** routine describes the event.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0ce6a-149">Remarques à l’attention des responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="0ce6a-149">Notes to implementers</span></span>

<span data-ttu-id="0ce6a-150">Vous pouvez prendre en charge notification avec ou sans l’aide de MAPI.</span><span class="sxs-lookup"><span data-stu-id="0ce6a-150">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="0ce6a-151">MAPI a trois méthodes d’objet de prise en charge pour aider les fournisseurs de services à implémenter la notification :</span><span class="sxs-lookup"><span data-stu-id="0ce6a-151">MAPI has three support object methods to help service providers implement notification:</span></span>
  
- [<span data-ttu-id="0ce6a-152">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="0ce6a-152">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
    
- [<span data-ttu-id="0ce6a-153">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="0ce6a-153">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)
    
- [<span data-ttu-id="0ce6a-154">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="0ce6a-154">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
    
<span data-ttu-id="0ce6a-155">Si vous choisissez d’utiliser les méthodes de prise en charge MAPI, appelé la méthode **Subscribe** lorsque votre méthode **Advise** est appelée et libérer le pointeur _lpAdviseSink_ .</span><span class="sxs-lookup"><span data-stu-id="0ce6a-155">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="0ce6a-156">Si vous choisissez prendre en charge de notification vous-même, appeler la méthode **AddRef** du récepteur advise représenté par le paramètre _lpAdviseSink_ de conserver une copie de ce pointeur.</span><span class="sxs-lookup"><span data-stu-id="0ce6a-156">If you elect to support notification yourself, call the **AddRef** method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="0ce6a-157">Mettre à jour cette copie jusqu'à ce que votre méthode [IABLogon::Unadvise](iablogon-unadvise.md) est appelée pour annuler l’inscription.</span><span class="sxs-lookup"><span data-stu-id="0ce6a-157">Maintain this copy until your [IABLogon::Unadvise](iablogon-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="0ce6a-158">Quelle que soit la façon dont vous prenez en charge la notification, affecter un numéro de connexion différente de zéro pour l’inscription de notification et la faire revenir dans le paramètre _lpulConnection_ .</span><span class="sxs-lookup"><span data-stu-id="0ce6a-158">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="0ce6a-159">Ne relâchez pas ce numéro de connexion jusqu'à ce que la méthode **Unadvise** a été appelée.</span><span class="sxs-lookup"><span data-stu-id="0ce6a-159">Do not release this connection number until the **Unadvise** method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0ce6a-160">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="0ce6a-160">Notes to callers</span></span>

<span data-ttu-id="0ce6a-161">Le pointeur du récepteur advise que vous passez dans le paramètre _lpAdviseSink_ à **Advise** peut pointer vers un objet que vous avez créé ou MAPI créé par le biais de la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="0ce6a-161">The advise sink pointer that you pass in the  _lpAdviseSink_ parameter to **Advise** can point to an object that you have created or that MAPI has created through the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> <span data-ttu-id="0ce6a-162">Vous pouvez souhaiter utiliser **HrThisThreadAdviseSink** si vous prennent en charge plusieurs threads d’exécution et que vous voulez utiliser pour vous assurer que les appels suivants à votre méthode **OnNotify** se produire à un moment opportun sur une thread approprié.</span><span class="sxs-lookup"><span data-stu-id="0ce6a-162">You might want to use **HrThisThreadAdviseSink** if you support multiple threads of execution and want to be sure that that subsequent calls to your **OnNotify** method occur at an appropriate time on an appropriate thread.</span></span> 
  
<span data-ttu-id="0ce6a-163">Être préparé pour être libéré à tout moment après votre appel **Advise** et avant l’appel de **Unadvise**votre objet récepteur advise.</span><span class="sxs-lookup"><span data-stu-id="0ce6a-163">Be prepared for your advise sink object to be released any time after your call to **Advise** and before your call to **Unadvise**.</span></span> <span data-ttu-id="0ce6a-164">Par conséquent, vous devez libérer votre objet de récepteur advise après **Advise** renvoie, à moins d’avoir une utilisation à long terme spécifique pour qu’il.</span><span class="sxs-lookup"><span data-stu-id="0ce6a-164">Therefore, you should release your advise sink object after **Advise** returns, unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="0ce6a-165">Pour plus d’informations sur le processus de notification, reportez-vous à la section [Notification d’événement MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="0ce6a-165">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="0ce6a-166">Pour plus d’informations sur la façon d’utiliser les méthodes **IMAPISupport** pour prendre en charge la notification, voir [Prise en charge de Notification d’événement](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="0ce6a-166">For information about how to use the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span> <span data-ttu-id="0ce6a-167">Pour plus d’informations sur le multithreading et MAPI, consultez [Threading MAPI](threading-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="0ce6a-167">For more information about multithreading and MAPI, see [Threading in MAPI](threading-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0ce6a-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ce6a-168">See also</span></span>



[<span data-ttu-id="0ce6a-169">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="0ce6a-169">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="0ce6a-170">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="0ce6a-170">IABLogon::Unadvise</span></span>](iablogon-unadvise.md)
  
[<span data-ttu-id="0ce6a-171">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="0ce6a-171">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="0ce6a-172">Notification</span><span class="sxs-lookup"><span data-stu-id="0ce6a-172">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="0ce6a-173">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0ce6a-173">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

