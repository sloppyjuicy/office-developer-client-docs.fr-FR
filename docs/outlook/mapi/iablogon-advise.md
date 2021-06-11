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
ms.openlocfilehash: 4ab0e4b023e6af19f650abf421aed122dcc21879
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428227"
---
# <a name="iablogonadvise"></a><span data-ttu-id="6b8c2-103">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="6b8c2-103">IABLogon::Advise</span></span>

  
  
<span data-ttu-id="6b8c2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b8c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b8c2-105">Inscrit l’appelant pour recevoir une notification des événements spécifiés qui affectent un conteneur, un utilisateur de messagerie ou une liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="6b8c2-105">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="6b8c2-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6b8c2-106">Parameters</span></span>

 <span data-ttu-id="6b8c2-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="6b8c2-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="6b8c2-108">[in] Nombre d’octets dans l’identificateur d’entrée pointé par _le paramètre lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="6b8c2-108">[in] The count of bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="6b8c2-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="6b8c2-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="6b8c2-110">[in] Pointeur vers l’identificateur d’entrée de l’objet sur lequel les notifications doivent être générées.</span><span class="sxs-lookup"><span data-stu-id="6b8c2-110">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span>
    
 <span data-ttu-id="6b8c2-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="6b8c2-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="6b8c2-112">[in] Masque de bits de valeurs qui indiquent les types d’événements de notification qui intéressent l’appelant et qui doivent être inclus dans l’inscription.</span><span class="sxs-lookup"><span data-stu-id="6b8c2-112">[in] A bitmask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="6b8c2-113">Il existe une structure [de NOTIFICATION](notification.md) correspondante associée à chaque type d’événement qui contient des informations sur l’événement.</span><span class="sxs-lookup"><span data-stu-id="6b8c2-113">There is a corresponding [NOTIFICATION](notification.md) structure associated with each type of event that holds information about the event.</span></span> <span data-ttu-id="6b8c2-114">Le tableau suivant répertorie les valeurs valides pour le  _paramètre ulEventMask_ et les structures associées à chaque valeur.</span><span class="sxs-lookup"><span data-stu-id="6b8c2-114">The following table lists the valid values for the  _ulEventMask_ parameter and the structures associated with each value.</span></span> 
    
|<span data-ttu-id="6b8c2-115">**Type d’événement de notification**</span><span class="sxs-lookup"><span data-stu-id="6b8c2-115">**Notification event type**</span></span>|<span data-ttu-id="6b8c2-116">**Structure **de NOTIFICATION** correspondante**</span><span class="sxs-lookup"><span data-stu-id="6b8c2-116">**Corresponding **NOTIFICATION** structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6b8c2-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="6b8c2-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="6b8c2-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="6b8c2-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="6b8c2-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="6b8c2-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="6b8c2-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="6b8c2-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="6b8c2-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="6b8c2-121">**fnevObjectDeleted**</span></span> <br/> |<span data-ttu-id="6b8c2-122">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="6b8c2-122">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="6b8c2-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="6b8c2-123">**fnevObjectModified**</span></span> <br/> |<span data-ttu-id="6b8c2-124">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="6b8c2-124">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="6b8c2-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="6b8c2-125">**fnevObjectCopied**</span></span> <br/> |<span data-ttu-id="6b8c2-126">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="6b8c2-126">**OBJECT_NOTIFICATION**</span></span> <br/> |
|<span data-ttu-id="6b8c2-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="6b8c2-127">**fnevObjectMoved**</span></span> <br/> |<span data-ttu-id="6b8c2-128">**OBJECT_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="6b8c2-128">**OBJECT_NOTIFICATION**</span></span> <br/> |
   
 <span data-ttu-id="6b8c2-129">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="6b8c2-129">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="6b8c2-130">[in] Pointeur vers un objet de réception de notification pour recevoir les notifications suivantes.</span><span class="sxs-lookup"><span data-stu-id="6b8c2-130">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span>
    
 <span data-ttu-id="6b8c2-131">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="6b8c2-131">_lpulConnection_</span></span>
  
> <span data-ttu-id="6b8c2-132">[out] Pointeur vers une valeur autre que zéro qui représente l’inscription de la notification.</span><span class="sxs-lookup"><span data-stu-id="6b8c2-132">[out] A pointer to a nonzero value that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6b8c2-133">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6b8c2-133">Return value</span></span>

<span data-ttu-id="6b8c2-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="6b8c2-134">S_OK</span></span> 
  
> <span data-ttu-id="6b8c2-135">L’inscription de la notification a réussi.</span><span class="sxs-lookup"><span data-stu-id="6b8c2-135">The notification registration was successful.</span></span>
    
<span data-ttu-id="6b8c2-136">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="6b8c2-136">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="6b8c2-137">L’identificateur d’entrée transmis dans  _le paramètre lpEntryID_ n’est pas dans le format approprié.</span><span class="sxs-lookup"><span data-stu-id="6b8c2-137">The entry identifier passed in the  _lpEntryID_ parameter is not in the appropriate format.</span></span> 
    
<span data-ttu-id="6b8c2-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="6b8c2-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="6b8c2-139">Le fournisseur de carnet d’adresses ne prend pas en charge la notification, éventuellement parce qu’il n’autorise pas les modifications apportées à ses objets.</span><span class="sxs-lookup"><span data-stu-id="6b8c2-139">The address book provider does not support notification, possibly because it does not allow changes to be made to its objects.</span></span>
    
<span data-ttu-id="6b8c2-140">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="6b8c2-140">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="6b8c2-141">Le fournisseur de carnet d’adresses ne peut pas gérer l’identificateur d’entrée transmis  _dans lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="6b8c2-141">The address book provider cannot handle the entry identifier passed in  _lpEntryID_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6b8c2-142">Remarques</span><span class="sxs-lookup"><span data-stu-id="6b8c2-142">Remarks</span></span>

<span data-ttu-id="6b8c2-143">Les fournisseurs de carnets d’adresses implémentent la méthode **IABLogon::Advise** pour inscrire l’appelant afin qu’il soit averti lorsqu’une modification est appliquée à un objet dans l’un de ses conteneurs.</span><span class="sxs-lookup"><span data-stu-id="6b8c2-143">Address book providers implement the **IABLogon::Advise** method to register the caller to be notified when a change occurs to an object in one of their containers.</span></span> <span data-ttu-id="6b8c2-144">Les appelants peuvent s’inscrire aux notifications concernant les utilisateurs de messagerie, les listes de distribution ou les conteneurs entiers.</span><span class="sxs-lookup"><span data-stu-id="6b8c2-144">Callers can register for notifications regarding messaging users, distribution lists, or entire containers.</span></span> 
  
<span data-ttu-id="6b8c2-145">Les clients appellent généralement [la méthode IAddrBook::Advise](iaddrbook-advise.md) pour s’inscrire aux notifications de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="6b8c2-145">Clients typically call the [IAddrBook::Advise](iaddrbook-advise.md) method to register for address book notifications.</span></span> <span data-ttu-id="6b8c2-146">MAPI appelle ensuite la méthode **Advise** du fournisseur de carnet d’adresses responsable de l’objet représenté par l’identificateur d’entrée dans  _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="6b8c2-146">MAPI then calls the **Advise** method of the address book provider that is responsible for the object represented by the entry identifier in  _lpEntryID_.</span></span>
  
<span data-ttu-id="6b8c2-147">Lorsqu’une modification a lieu sur l’objet indiqué du type représenté dans  _ulEventMask_, un appel est effectué à la méthode **OnNotify** du sink de conseil pointé par  _lpAdviseSink_.</span><span class="sxs-lookup"><span data-stu-id="6b8c2-147">When a change occurs to the indicated object of the type represented in  _ulEventMask_, a call is made to the **OnNotify** method of the advise sink pointed to by  _lpAdviseSink_.</span></span> <span data-ttu-id="6b8c2-148">Les données transmises dans la structure **NOTIFICATION** à la routine **OnNotify** décrivent l’événement.</span><span class="sxs-lookup"><span data-stu-id="6b8c2-148">Data passed in the **NOTIFICATION** structure to the **OnNotify** routine describes the event.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6b8c2-149">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="6b8c2-149">Notes to implementers</span></span>

<span data-ttu-id="6b8c2-150">Vous pouvez prendre en charge les notifications avec ou sans l’aide de MAPI.</span><span class="sxs-lookup"><span data-stu-id="6b8c2-150">You can support notification with or without help from MAPI.</span></span> <span data-ttu-id="6b8c2-151">MAPI dispose de trois méthodes objet de support pour aider les fournisseurs de services à implémenter la notification :</span><span class="sxs-lookup"><span data-stu-id="6b8c2-151">MAPI has three support object methods to help service providers implement notification:</span></span>
  
- [<span data-ttu-id="6b8c2-152">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="6b8c2-152">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
    
- [<span data-ttu-id="6b8c2-153">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="6b8c2-153">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)
    
- [<span data-ttu-id="6b8c2-154">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="6b8c2-154">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
    
<span data-ttu-id="6b8c2-155">Si vous avez choisi d’utiliser les méthodes de support MAPI, appelez **Subscribe** lorsque votre méthode **Advise** est appelée et relâchez le pointeur _lpAdviseSink._</span><span class="sxs-lookup"><span data-stu-id="6b8c2-155">If you elect to use the MAPI support methods, call **Subscribe** when your **Advise** method is called and release the  _lpAdviseSink_ pointer.</span></span> 
  
<span data-ttu-id="6b8c2-156">Si vous avez choisi de prendre en charge la notification vous-même, appelez la méthode **AddRef** du sink de notification représenté par le paramètre  _lpAdviseSink_ pour conserver une copie de ce pointeur.</span><span class="sxs-lookup"><span data-stu-id="6b8c2-156">If you elect to support notification yourself, call the **AddRef** method of the advise sink represented by the  _lpAdviseSink_ parameter to keep a copy of this pointer.</span></span> <span data-ttu-id="6b8c2-157">Conservez cette copie jusqu’à ce que votre [méthode IABLogon::Unadvise](iablogon-unadvise.md) soit appelée pour annuler l’inscription.</span><span class="sxs-lookup"><span data-stu-id="6b8c2-157">Maintain this copy until your [IABLogon::Unadvise](iablogon-unadvise.md) method is called to cancel the registration.</span></span> 
  
<span data-ttu-id="6b8c2-158">Quelle que soit la façon dont vous supportez la notification, affectez un numéro de connexion autre que zéro à l’inscription de notification et renvoyez-le dans _le paramètre lpulConnection._</span><span class="sxs-lookup"><span data-stu-id="6b8c2-158">Regardless of how you support notification, assign a nonzero connection number to the notification registration and return it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="6b8c2-159">Ne relâchez pas ce numéro de connexion tant que la méthode **Unadvise** n’a pas été appelée.</span><span class="sxs-lookup"><span data-stu-id="6b8c2-159">Do not release this connection number until the **Unadvise** method has been called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6b8c2-160">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="6b8c2-160">Notes to callers</span></span>

<span data-ttu-id="6b8c2-161">Le pointeur de sink de conseil que vous passez au paramètre _lpAdviseSink_ à **Advise** peut pointer vers un objet que vous avez créé ou que MAPI a créé via la fonction [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md)</span><span class="sxs-lookup"><span data-stu-id="6b8c2-161">The advise sink pointer that you pass in the  _lpAdviseSink_ parameter to **Advise** can point to an object that you have created or that MAPI has created through the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> <span data-ttu-id="6b8c2-162">Vous pouvez utiliser **HrThisThreadAdviseSink** si vous prisez en charge plusieurs threads d’exécution et que vous souhaitez vous assurer que les appels ultérieurs à votre méthode **OnNotify** se produisent à un moment approprié sur un thread approprié.</span><span class="sxs-lookup"><span data-stu-id="6b8c2-162">You might want to use **HrThisThreadAdviseSink** if you support multiple threads of execution and want to be sure that that subsequent calls to your **OnNotify** method occur at an appropriate time on an appropriate thread.</span></span> 
  
<span data-ttu-id="6b8c2-163">Soyez prêt à ce que votre objet de sink de conseil soit libéré à tout moment après votre appel à **Advise** et avant votre appel à **Unadvise**.</span><span class="sxs-lookup"><span data-stu-id="6b8c2-163">Be prepared for your advise sink object to be released any time after your call to **Advise** and before your call to **Unadvise**.</span></span> <span data-ttu-id="6b8c2-164">Par conséquent, vous devez libérer votre objet de sink de conseil après le retour de **Advise,** sauf si vous avez une utilisation spécifique à long terme pour lui.</span><span class="sxs-lookup"><span data-stu-id="6b8c2-164">Therefore, you should release your advise sink object after **Advise** returns, unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="6b8c2-165">Pour plus d’informations sur le processus de notification, voir [notification d’événement dans MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="6b8c2-165">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="6b8c2-166">Pour plus d’informations sur l’utilisation des méthodes **IMAPISupport** pour prendre en charge la notification, voir [Notification d’événement de prise en charge.](supporting-event-notification.md)</span><span class="sxs-lookup"><span data-stu-id="6b8c2-166">For information about how to use the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span> <span data-ttu-id="6b8c2-167">Pour plus d’informations sur le multithreading et MAPI, voir [Threading dans MAPI](threading-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="6b8c2-167">For more information about multithreading and MAPI, see [Threading in MAPI](threading-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6b8c2-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b8c2-168">See also</span></span>



[<span data-ttu-id="6b8c2-169">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="6b8c2-169">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="6b8c2-170">IABLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="6b8c2-170">IABLogon::Unadvise</span></span>](iablogon-unadvise.md)
  
[<span data-ttu-id="6b8c2-171">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="6b8c2-171">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="6b8c2-172">Notification</span><span class="sxs-lookup"><span data-stu-id="6b8c2-172">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="6b8c2-173">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6b8c2-173">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

