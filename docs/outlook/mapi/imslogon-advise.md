---
title: IMSLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Advise
api_type:
- COM
ms.assetid: a3c5d937-642b-463b-b5a0-5d099e651895
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: abe4867b965f05e781f931d2e72920474d007d78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317310"
---
# <a name="imslogonadvise"></a><span data-ttu-id="4d5ad-103">IMSLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="4d5ad-103">IMSLogon::Advise</span></span>

  
  
<span data-ttu-id="4d5ad-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d5ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d5ad-105">Inscrit un objet auprès d'un fournisseur de banque de messages pour les notifications concernant les modifications apportées à la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="4d5ad-105">Registers an object with a message store provider for notifications about changes in the message store.</span></span> <span data-ttu-id="4d5ad-106">La Banque de messages enverra ensuite des notifications sur les modifications apportées à l'objet inscrit.</span><span class="sxs-lookup"><span data-stu-id="4d5ad-106">The message store will then send notifications about changes to the registered object.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="4d5ad-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4d5ad-107">Parameters</span></span>

 <span data-ttu-id="4d5ad-108">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="4d5ad-108">_cbEntryID_</span></span>
  
> <span data-ttu-id="4d5ad-109">dans Taille, en octets, de l'identificateur d'entrée pointé par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="4d5ad-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="4d5ad-110">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="4d5ad-110">_lpEntryID_</span></span>
  
> <span data-ttu-id="4d5ad-111">dans Pointeur vers l'identificateur d'entrée de l'objet sur lequel les notifications doivent être générées.</span><span class="sxs-lookup"><span data-stu-id="4d5ad-111">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span> <span data-ttu-id="4d5ad-112">Cet objet peut être un dossier, un message ou tout autre objet dans la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="4d5ad-112">This object can be a folder, a message, or any other object in the message store.</span></span> <span data-ttu-id="4d5ad-113">Par ailleurs, si MAPI définit le paramètre _cbEntryID_ sur 0 et passe la **valeur null** pour _lpEntryID_, le récepteur de notifications fournit des notifications sur les modifications apportées à la Banque de messages entière.</span><span class="sxs-lookup"><span data-stu-id="4d5ad-113">Alternatively, if MAPI sets the  _cbEntryID_ parameter to 0 and passes **null** for  _lpEntryID_, the advise sink provides notifications about changes to the entire message store.</span></span>
    
 <span data-ttu-id="4d5ad-114">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="4d5ad-114">_ulEventMask_</span></span>
  
> <span data-ttu-id="4d5ad-115">dans Un masque d'événement des types d'événements de notification survenus pour l'objet sur lequel MAPI générera des notifications.</span><span class="sxs-lookup"><span data-stu-id="4d5ad-115">[in] An event mask of the types of notification events occurring for the object about which MAPI will generate notifications.</span></span> <span data-ttu-id="4d5ad-116">Le masque filtre des cas spécifiques.</span><span class="sxs-lookup"><span data-stu-id="4d5ad-116">The mask filters specific cases.</span></span> <span data-ttu-id="4d5ad-117">Chaque type d'événement est associé à une structure qui contient des informations supplémentaires sur l'événement.</span><span class="sxs-lookup"><span data-stu-id="4d5ad-117">Each event type has a structure associated with it that contains additional information about the event.</span></span> <span data-ttu-id="4d5ad-118">Le tableau suivant répertorie les types d'événement possibles ainsi que les structures correspondantes.</span><span class="sxs-lookup"><span data-stu-id="4d5ad-118">The following table lists the possible event types along with their corresponding structures.</span></span>
    
|<span data-ttu-id="4d5ad-119">**Type d'événement de notification**</span><span class="sxs-lookup"><span data-stu-id="4d5ad-119">**Notification event type**</span></span>|<span data-ttu-id="4d5ad-120">**Structure correspondante**</span><span class="sxs-lookup"><span data-stu-id="4d5ad-120">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4d5ad-121">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="4d5ad-121">fnevCriticalError</span></span>  <br/> |[<span data-ttu-id="4d5ad-122">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4d5ad-122">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="4d5ad-123">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="4d5ad-123">fnevNewMail</span></span>  <br/> |[<span data-ttu-id="4d5ad-124">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4d5ad-124">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="4d5ad-125">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="4d5ad-125">fnevObjectCreated</span></span>  <br/> |[<span data-ttu-id="4d5ad-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4d5ad-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4d5ad-127">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="4d5ad-127">fnevObjectDeleted</span></span>  <br/> |[<span data-ttu-id="4d5ad-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4d5ad-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4d5ad-129">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="4d5ad-129">fnevObjectModified</span></span>  <br/> |[<span data-ttu-id="4d5ad-130">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4d5ad-130">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4d5ad-131">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="4d5ad-131">fnevObjectCopied</span></span>  <br/> |[<span data-ttu-id="4d5ad-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4d5ad-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4d5ad-133">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="4d5ad-133">fnevObjectMoved</span></span>  <br/> |[<span data-ttu-id="4d5ad-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4d5ad-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4d5ad-135">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="4d5ad-135">fnevSearchComplete</span></span>  <br/> |[<span data-ttu-id="4d5ad-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4d5ad-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="4d5ad-137">fnevStatusObjectModified</span><span class="sxs-lookup"><span data-stu-id="4d5ad-137">fnevStatusObjectModified</span></span>  <br/> |[<span data-ttu-id="4d5ad-138">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4d5ad-138">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
   
 <span data-ttu-id="4d5ad-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="4d5ad-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="4d5ad-140">dans Pointeur vers un objet de récepteur de notification à appeler lorsqu'un événement de l'objet session a été demandé.</span><span class="sxs-lookup"><span data-stu-id="4d5ad-140">[in] A pointer to an advise sink object to be called when an event occurs for the session object about which notification has been requested.</span></span> <span data-ttu-id="4d5ad-141">Cet objet de récepteur de notifications doit déjà exister.</span><span class="sxs-lookup"><span data-stu-id="4d5ad-141">This advise sink object must already exist.</span></span>
    
 <span data-ttu-id="4d5ad-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="4d5ad-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="4d5ad-143">remarquer Un pointeur vers une variable qui, lorsqu'un retour réussi, conserve le numéro de connexion pour l'enregistrement de la notification.</span><span class="sxs-lookup"><span data-stu-id="4d5ad-143">[out] A pointer to a variable that upon a successful return holds the connection number for the notification registration.</span></span> <span data-ttu-id="4d5ad-144">Le numéro de connexion doit être différent de zéro.</span><span class="sxs-lookup"><span data-stu-id="4d5ad-144">The connection number must be nonzero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4d5ad-145">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4d5ad-145">Return value</span></span>

<span data-ttu-id="4d5ad-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="4d5ad-146">S_OK</span></span> 
  
> <span data-ttu-id="4d5ad-147">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="4d5ad-147">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="4d5ad-148">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="4d5ad-148">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="4d5ad-149">L'opération n'est pas prise en charge par MAPI ou par un ou plusieurs fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="4d5ad-149">The operation is not supported by MAPI or by one or more service providers.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4d5ad-150">Remarques</span><span class="sxs-lookup"><span data-stu-id="4d5ad-150">Remarks</span></span>

<span data-ttu-id="4d5ad-151">Les fournisseurs de banque de messages implémentent la méthode **IMSLogon:: Advise** pour enregistrer un objet pour les rappels de notification.</span><span class="sxs-lookup"><span data-stu-id="4d5ad-151">Message store providers implement the **IMSLogon::Advise** method to register an object for notification callbacks.</span></span> <span data-ttu-id="4d5ad-152">Chaque fois qu'une modification est apportée à l'objet indiqué, le fournisseur vérifie le bit de masque d'événement qui a été défini dans le paramètre _ulEventMask_ et, par conséquent, le type de modification qui a eu lieu.</span><span class="sxs-lookup"><span data-stu-id="4d5ad-152">Whenever a change occurs to the indicated object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and, therefore, what type of change occurred.</span></span> <span data-ttu-id="4d5ad-153">Si un bit est défini, le fournisseur appelle la méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) pour l'objet de récepteur de notifications indiqué par le paramètre _lpAdviseSink_ pour signaler l'événement.</span><span class="sxs-lookup"><span data-stu-id="4d5ad-153">If a bit is set, the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="4d5ad-154">Les données transmises dans la structure de notification à la routine **OnNotify** décrivent l'événement.</span><span class="sxs-lookup"><span data-stu-id="4d5ad-154">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="4d5ad-155">L'appel à **OnNotify** peut se produire pendant l'appel qui modifie l'objet ou ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="4d5ad-155">The call to **OnNotify** can occur during the call that changes the object, or at any later time.</span></span> <span data-ttu-id="4d5ad-156">Sur les systèmes qui prennent en charge plusieurs threads d'exécution, l'appel à **OnNotify** peut se produire sur n'importe quel thread.</span><span class="sxs-lookup"><span data-stu-id="4d5ad-156">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="4d5ad-157">Pour gérer en toute sécurité un appel à **OnNotify** susceptible de se produire à un moment inopportun, une application cliente doit utiliser la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="4d5ad-157">To safely handle a call to **OnNotify** that might happen at an inopportune time, a client application should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="4d5ad-158">Pour fournir des notifications, le fournisseur de banque de messages qui implémente l' **avis** doit conserver une copie du pointeur vers l'objet récepteur _lpAdviseSink_ . pour ce faire, le fournisseur appelle la méthode [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) pour le récepteur de notifications afin de maintenir son pointeur d'objet jusqu'à ce que l'enregistrement de notification soit annulé avec un appel à la méthode [IMSLogon::](imslogon-unadvise.md) Unadvise.</span><span class="sxs-lookup"><span data-stu-id="4d5ad-158">To provide notifications, the message store provider that implements **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, the provider calls the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMSLogon::Unadvise](imslogon-unadvise.md) method.</span></span> <span data-ttu-id="4d5ad-159">L'implémentation de l' **avis** doit affecter un numéro de connexion à l'enregistrement des notifications et appeler **AddRef** sur ce numéro de connexion avant de le renvoyer dans le paramètre _lpulConnection_ .</span><span class="sxs-lookup"><span data-stu-id="4d5ad-159">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="4d5ad-160">Les fournisseurs de services peuvent libérer l'objet récepteur de notification avant l'annulation de l'inscription, mais ils ne doivent pas libérer \*\*\*\* le numéro de connexion tant qu'Unadvise n'a pas été appelé.</span><span class="sxs-lookup"><span data-stu-id="4d5ad-160">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until **Unadvise** has been called.</span></span> 
  
<span data-ttu-id="4d5ad-161">Une fois qu'un \*\*\*\* appel à Advise a réussi et avant que Unadvise ait été appelé, les fournisseurs doivent être préparés pour que l'objet de récepteur de notifications soit publié. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4d5ad-161">After a call to **Advise** has succeeded and before **Unadvise** has been called, providers must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="4d5ad-162">Par conséquent, un fournisseur doit libérer son objet de récepteur \*\*\*\* de notification une fois qu'il a été renvoyé, sauf s'il a une utilisation longue durée spécifique pour lui.</span><span class="sxs-lookup"><span data-stu-id="4d5ad-162">Therefore, a provider should release its advise sink object after **Advise** returns, unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="4d5ad-163">Pour plus d'informations sur le processus de notification, consultez la rubrique [notifications d'événements dans MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="4d5ad-163">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4d5ad-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d5ad-164">See also</span></span>



[<span data-ttu-id="4d5ad-165">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="4d5ad-165">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="4d5ad-166">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="4d5ad-166">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="4d5ad-167">IMSLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="4d5ad-167">IMSLogon::Unadvise</span></span>](imslogon-unadvise.md)
  
[<span data-ttu-id="4d5ad-168">Notification</span><span class="sxs-lookup"><span data-stu-id="4d5ad-168">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="4d5ad-169">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4d5ad-169">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

