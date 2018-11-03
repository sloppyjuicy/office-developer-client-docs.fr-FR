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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: abe4867b965f05e781f931d2e72920474d007d78
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382756"
---
# <a name="imslogonadvise"></a><span data-ttu-id="b1683-103">IMSLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="b1683-103">IMSLogon::Advise</span></span>

  
  
<span data-ttu-id="b1683-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1683-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1683-105">Inscrit un objet avec un fournisseur de magasin de message pour les notifications sur les modifications dans la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="b1683-105">Registers an object with a message store provider for notifications about changes in the message store.</span></span> <span data-ttu-id="b1683-106">La banque de messages envoie ensuite les notifications sur les modifications apportées à l’objet inscrit.</span><span class="sxs-lookup"><span data-stu-id="b1683-106">The message store will then send notifications about changes to the registered object.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="b1683-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1683-107">Parameters</span></span>

 <span data-ttu-id="b1683-108">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b1683-108">_cbEntryID_</span></span>
  
> <span data-ttu-id="b1683-109">[in] La taille, en octets, de l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="b1683-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b1683-110">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="b1683-110">_lpEntryID_</span></span>
  
> <span data-ttu-id="b1683-111">[in] Pointeur vers l’identificateur d’entrée de l’objet sur lequel les notifications doivent être générées.</span><span class="sxs-lookup"><span data-stu-id="b1683-111">[in] A pointer to the entry identifier of the object about which notifications should be generated.</span></span> <span data-ttu-id="b1683-112">Cet objet peut être un dossier, un message ou tout autre objet dans la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="b1683-112">This object can be a folder, a message, or any other object in the message store.</span></span> <span data-ttu-id="b1683-113">Vous pouvez également si MAPI définit le paramètre _cbEntryID_ à 0 et passe **null** pour _lpEntryID_, le récepteur de notifications des notifications sur les modifications dans le magasin de l’intégralité du message.</span><span class="sxs-lookup"><span data-stu-id="b1683-113">Alternatively, if MAPI sets the  _cbEntryID_ parameter to 0 and passes **null** for  _lpEntryID_, the advise sink provides notifications about changes to the entire message store.</span></span>
    
 <span data-ttu-id="b1683-114">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="b1683-114">_ulEventMask_</span></span>
  
> <span data-ttu-id="b1683-115">[in] Un masque des types d’événements de notification de l’objet sur lequel MAPI génère des notifications d’événement.</span><span class="sxs-lookup"><span data-stu-id="b1683-115">[in] An event mask of the types of notification events occurring for the object about which MAPI will generate notifications.</span></span> <span data-ttu-id="b1683-116">Le masque de filtre cas spécifiques.</span><span class="sxs-lookup"><span data-stu-id="b1683-116">The mask filters specific cases.</span></span> <span data-ttu-id="b1683-117">Chaque type d’événement a une structure associée qui contient des informations supplémentaires sur l’événement.</span><span class="sxs-lookup"><span data-stu-id="b1683-117">Each event type has a structure associated with it that contains additional information about the event.</span></span> <span data-ttu-id="b1683-118">Le tableau suivant répertorie les types d’événements possibles ainsi que leurs structures correspondantes.</span><span class="sxs-lookup"><span data-stu-id="b1683-118">The following table lists the possible event types along with their corresponding structures.</span></span>
    
|<span data-ttu-id="b1683-119">**Type d’événement notification**</span><span class="sxs-lookup"><span data-stu-id="b1683-119">**Notification event type**</span></span>|<span data-ttu-id="b1683-120">**Structure correspondante**</span><span class="sxs-lookup"><span data-stu-id="b1683-120">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b1683-121">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="b1683-121">fnevCriticalError</span></span>  <br/> |[<span data-ttu-id="b1683-122">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b1683-122">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="b1683-123">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="b1683-123">fnevNewMail</span></span>  <br/> |[<span data-ttu-id="b1683-124">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b1683-124">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="b1683-125">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="b1683-125">fnevObjectCreated</span></span>  <br/> |[<span data-ttu-id="b1683-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b1683-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="b1683-127">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="b1683-127">fnevObjectDeleted</span></span>  <br/> |[<span data-ttu-id="b1683-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b1683-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="b1683-129">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="b1683-129">fnevObjectModified</span></span>  <br/> |[<span data-ttu-id="b1683-130">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b1683-130">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="b1683-131">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="b1683-131">fnevObjectCopied</span></span>  <br/> |[<span data-ttu-id="b1683-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b1683-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="b1683-133">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="b1683-133">fnevObjectMoved</span></span>  <br/> |[<span data-ttu-id="b1683-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b1683-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="b1683-135">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="b1683-135">fnevSearchComplete</span></span>  <br/> |[<span data-ttu-id="b1683-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b1683-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="b1683-137">fnevStatusObjectModified</span><span class="sxs-lookup"><span data-stu-id="b1683-137">fnevStatusObjectModified</span></span>  <br/> |[<span data-ttu-id="b1683-138">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b1683-138">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
   
 <span data-ttu-id="b1683-139">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="b1683-139">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="b1683-140">[in] Pointeur vers un objet de récepteur advise appelée lorsqu’un événement se produit pour l’objet session sur lequel la notification a été demandée.</span><span class="sxs-lookup"><span data-stu-id="b1683-140">[in] A pointer to an advise sink object to be called when an event occurs for the session object about which notification has been requested.</span></span> <span data-ttu-id="b1683-141">Cet objet de récepteur advise doit déjà exister.</span><span class="sxs-lookup"><span data-stu-id="b1683-141">This advise sink object must already exist.</span></span>
    
 <span data-ttu-id="b1683-142">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="b1683-142">_lpulConnection_</span></span>
  
> <span data-ttu-id="b1683-143">[out] Pointeur vers une variable qui conserve le numéro de connexion pour l’enregistrement de notification à un retour réussi.</span><span class="sxs-lookup"><span data-stu-id="b1683-143">[out] A pointer to a variable that upon a successful return holds the connection number for the notification registration.</span></span> <span data-ttu-id="b1683-144">Le numéro de connexion doit être différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="b1683-144">The connection number must be nonzero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b1683-145">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b1683-145">Return value</span></span>

<span data-ttu-id="b1683-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="b1683-146">S_OK</span></span> 
  
> <span data-ttu-id="b1683-147">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="b1683-147">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="b1683-148">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="b1683-148">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="b1683-149">L’opération n’est pas pris en charge par MAPI ou par un ou plusieurs fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="b1683-149">The operation is not supported by MAPI or by one or more service providers.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b1683-150">Remarques</span><span class="sxs-lookup"><span data-stu-id="b1683-150">Remarks</span></span>

<span data-ttu-id="b1683-151">Fournisseurs de magasins de message implémentent la méthode **IMSLogon::Advise** pour enregistrer un objet pour les rappels de notification.</span><span class="sxs-lookup"><span data-stu-id="b1683-151">Message store providers implement the **IMSLogon::Advise** method to register an object for notification callbacks.</span></span> <span data-ttu-id="b1683-152">Chaque fois qu’une modification est apportée à l’objet indiqué, le fournisseur vérifie les bits de masque événement a été défini dans le paramètre _ulEventMask_ et, par conséquent, le type de modification s’est produite.</span><span class="sxs-lookup"><span data-stu-id="b1683-152">Whenever a change occurs to the indicated object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and, therefore, what type of change occurred.</span></span> <span data-ttu-id="b1683-153">Si un bit est défini, le fournisseur appelle la méthode de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pour l’objet de récepteur advise indiqué par le paramètre _lpAdviseSink_ pour signaler l’événement.</span><span class="sxs-lookup"><span data-stu-id="b1683-153">If a bit is set, the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="b1683-154">Données transmises dans la structure de notification à la routine **OnNotify** décrivent l’événement.</span><span class="sxs-lookup"><span data-stu-id="b1683-154">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="b1683-155">L’appel de **OnNotify** peut se produire lors de l’appel qui modifie l’objet, ou ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="b1683-155">The call to **OnNotify** can occur during the call that changes the object, or at any later time.</span></span> <span data-ttu-id="b1683-156">Sur les systèmes qui prennent en charge plusieurs threads d’exécution, l’appel de **OnNotify** peut se produire sur n’importe quel thread.</span><span class="sxs-lookup"><span data-stu-id="b1683-156">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="b1683-157">Pour gérer en toute sécurité un appel à **OnNotify** qui peut se produire à un moment peu opportuns, une application cliente doit utiliser la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="b1683-157">To safely handle a call to **OnNotify** that might happen at an inopportune time, a client application should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="b1683-158">Pour fournir des notifications, le fournisseur de banque de messages qui implémente **Advise** doit conserver une copie du pointeur pour la _lpAdviseSink_ conseiller objet récepteur ; Pour ce faire, le fournisseur appelle la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) pour le récepteur de notifications maintenir son pointeur de l’objet jusqu'à ce que l’inscription aux notifications est annulée par un appel à la méthode [IMSLogon::Unadvise](imslogon-unadvise.md) .</span><span class="sxs-lookup"><span data-stu-id="b1683-158">To provide notifications, the message store provider that implements **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, the provider calls the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMSLogon::Unadvise](imslogon-unadvise.md) method.</span></span> <span data-ttu-id="b1683-159">L’implémentation **Advise** doit affecter un numéro de connexion à l’enregistrement de notification et appelez **AddRef** sur ce numéro de connexion avant de la retourner dans le paramètre _lpulConnection_ .</span><span class="sxs-lookup"><span data-stu-id="b1683-159">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="b1683-160">Fournisseurs de services peuvent libérer l’objet de récepteur advise avant l’enregistrement est annulée, mais ils ne doivent libérer le numéro de connexion jusqu'à ce que **Unadvise** a été appelée.</span><span class="sxs-lookup"><span data-stu-id="b1683-160">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until **Unadvise** has been called.</span></span> 
  
<span data-ttu-id="b1683-161">Après qu’un appel à **Advise** a réussi et avant **Unadvise** a été appelée, les fournisseurs doivent être préparés pour l’objet de récepteur advise doit être publié.</span><span class="sxs-lookup"><span data-stu-id="b1683-161">After a call to **Advise** has succeeded and before **Unadvise** has been called, providers must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="b1683-162">Par conséquent, un fournisseur doit libérer son objet de récepteur advise après **Advise** renvoie, à moins qu’une utilisation à long terme spécifique pour qu’il.</span><span class="sxs-lookup"><span data-stu-id="b1683-162">Therefore, a provider should release its advise sink object after **Advise** returns, unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="b1683-163">Pour plus d’informations sur le processus de notification, reportez-vous à la section [Notification d’événement MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="b1683-163">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b1683-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1683-164">See also</span></span>



[<span data-ttu-id="b1683-165">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="b1683-165">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="b1683-166">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="b1683-166">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="b1683-167">IMSLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="b1683-167">IMSLogon::Unadvise</span></span>](imslogon-unadvise.md)
  
[<span data-ttu-id="b1683-168">Notification</span><span class="sxs-lookup"><span data-stu-id="b1683-168">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="b1683-169">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b1683-169">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

