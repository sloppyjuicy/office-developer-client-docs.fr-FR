---
title: IMAPIAdviseSinkOnNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIAdviseSink.OnNotify
api_type:
- COM
ms.assetid: 9eec90d3-2369-4340-86ed-0efa58918ed5
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 73eb92b0c1b88e114775231695b91157a3d26a2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783681"
---
# <a name="imapiadvisesinkonnotify"></a><span data-ttu-id="e0659-103">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="e0659-103">IMAPIAdviseSink::OnNotify</span></span>

  
  
<span data-ttu-id="e0659-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e0659-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e0659-105">Répond à une notification en effectuant une ou plusieurs tâches.</span><span class="sxs-lookup"><span data-stu-id="e0659-105">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="e0659-106">Les tâches exécutées varient selon le type d’événement et l’objet qui génère la notification.</span><span class="sxs-lookup"><span data-stu-id="e0659-106">The tasks performed depend on the type of event and the object that generates the notification.</span></span> 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="e0659-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e0659-107">Parameters</span></span>

 <span data-ttu-id="e0659-108">_cNotif_</span><span class="sxs-lookup"><span data-stu-id="e0659-108">_cNotif_</span></span>
  
> <span data-ttu-id="e0659-109">[in] Le nombre de structures [NOTIFICATION](notification.md) indiqué par le paramètre _lpNotifications_ .</span><span class="sxs-lookup"><span data-stu-id="e0659-109">[in] The count of [NOTIFICATION](notification.md) structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="e0659-110">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="e0659-110">_lpNotifications_</span></span>
  
> <span data-ttu-id="e0659-111">[in] Pointeur vers une ou plusieurs structures **NOTIFICATION** qui fournissent des informations sur les événements qui se sont produites.</span><span class="sxs-lookup"><span data-stu-id="e0659-111">[in] A pointer to one or more **NOTIFICATION** structures that provide information about the events that have occurred.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e0659-112">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="e0659-112">Return value</span></span>

<span data-ttu-id="e0659-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="e0659-113">S_OK</span></span> 
  
> <span data-ttu-id="e0659-114">La notification a été correctement traitée.</span><span class="sxs-lookup"><span data-stu-id="e0659-114">The notification was processed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e0659-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="e0659-115">Remarks</span></span>

<span data-ttu-id="e0659-116">Le processus de notification démarre lorsqu’un client ou un MAPI effectue un appel à la méthode **Advise** d’un fournisseur de services pour s’inscrire pour recevoir une notification d’un type particulier d’un objet particulier.</span><span class="sxs-lookup"><span data-stu-id="e0659-116">The notification process starts when a client or MAPI makes a call to a service provider's **Advise** method to register to receive a notification of a particular type for a particular object.</span></span> <span data-ttu-id="e0659-117">L’un des paramètres à la méthode **Advise** est un pointeur vers un objet récepteur advise qui implémente l’interface [IMAPIAdviseSink](imapiadvisesinkiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="e0659-117">One of the parameters to the **Advise** method is a pointer to an advise sink object that implements the [IMAPIAdviseSink](imapiadvisesinkiunknown.md) interface.</span></span> <span data-ttu-id="e0659-118">Lorsqu’un événement se produit à l’objet cible qui correspond à la notification inscrit, le fournisseur de services, directement ou indirectement via MAPI, appelle **OnNotify** (méthode) du récepteur advise.</span><span class="sxs-lookup"><span data-stu-id="e0659-118">When an event occurs to the target object that corresponds to the registered notification, the service provider, either directly or indirectly through MAPI, calls the advise sink's **OnNotify** method.</span></span> 
  
<span data-ttu-id="e0659-119">L’appel de **OnNotify** peut se produire lors de l’appel MAPI qui est à l’origine de l’événement ou ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="e0659-119">The call to **OnNotify** can occur either during the MAPI call that is causing the event or at some later time.</span></span> <span data-ttu-id="e0659-120">Sur les systèmes qui prennent en charge plusieurs threads d’exécution, **OnNotify** peut être appelée sur le même thread qui a été utilisé pour l’enregistrement ou sur un autre thread.</span><span class="sxs-lookup"><span data-stu-id="e0659-120">On systems that support multiple threads of execution, **OnNotify** can be called either on the same thread that was used for registration or on a different thread.</span></span> <span data-ttu-id="e0659-121">Les clients peuvent s’assurer que l’appel de **OnNotify** est effectué sur le même thread utilisé pour appeler **Advise** en créant le récepteur de notifications qu’elles passent à **Advise** avec la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="e0659-121">Clients can make sure that the **OnNotify** call is made on the same thread used to call **Advise** by creating the advise sink that they pass to **Advise** with the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="e0659-122">Le paramètre _lpNotifications_ pointe vers une ou plusieurs structures **NOTIFICATION** qui décrivent ce qui a changé pendant l’événement.</span><span class="sxs-lookup"><span data-stu-id="e0659-122">The  _lpNotifications_ parameter points to one or more **NOTIFICATION** structures that describe what has changed during the event.</span></span> <span data-ttu-id="e0659-123">Il existe un autre type de structure de **NOTIFICATION** pour chaque type d’événement.</span><span class="sxs-lookup"><span data-stu-id="e0659-123">There is a different type of **NOTIFICATION** structure for each type of event.</span></span> 
  
<span data-ttu-id="e0659-124">Le tableau suivant répertorie les valeurs qui sont utilisées pour représenter les types d’événements et les structures associés à chaque valeur possibles :</span><span class="sxs-lookup"><span data-stu-id="e0659-124">The following table lists the values that are used to represent the possible types of events and the structures associated with each value:</span></span>
  
|<span data-ttu-id="e0659-125">**Type d’événement notification**</span><span class="sxs-lookup"><span data-stu-id="e0659-125">**Notification event type**</span></span>|<span data-ttu-id="e0659-126">**Structure correspondante**</span><span class="sxs-lookup"><span data-stu-id="e0659-126">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e0659-127">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="e0659-127">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="e0659-128">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e0659-128">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="e0659-129">**fnevNewMail**</span><span class="sxs-lookup"><span data-stu-id="e0659-129">**fnevNewMail**</span></span> <br/> |[<span data-ttu-id="e0659-130">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e0659-130">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="e0659-131">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="e0659-131">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="e0659-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e0659-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="e0659-133">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="e0659-133">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="e0659-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e0659-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="e0659-135">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="e0659-135">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="e0659-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e0659-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="e0659-137">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="e0659-137">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="e0659-138">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e0659-138">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="e0659-139">**fnevSearchComplete**</span><span class="sxs-lookup"><span data-stu-id="e0659-139">**fnevSearchComplete**</span></span> <br/> |[<span data-ttu-id="e0659-140">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e0659-140">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="e0659-141">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="e0659-141">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="e0659-142">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e0659-142">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
|<span data-ttu-id="e0659-143">**fnevStatusObjectModified**</span><span class="sxs-lookup"><span data-stu-id="e0659-143">**fnevStatusObjectModified**</span></span> <br/> |[<span data-ttu-id="e0659-144">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e0659-144">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
|<span data-ttu-id="e0659-145">**fnevExtended**</span><span class="sxs-lookup"><span data-stu-id="e0659-145">**fnevExtended**</span></span> <br/> |[<span data-ttu-id="e0659-146">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e0659-146">EXTENDED_NOTIFICATION</span></span>](extended_notification.md) <br/> |
   
<span data-ttu-id="e0659-147">Pour plus d’informations sur la façon de configurer et d’arrêter les notifications, consultez les entrées de référence pour les méthodes **Advise** et **Unadvise** pour une des interfaces suivantes : [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [ IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md)et [IMSLogon](imslogoniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="e0659-147">For more information about how to set up and stop notifications, see the reference entries for the **Advise** and **Unadvise** methods for any of the following interfaces: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md), and [IMSLogon](imslogoniunknown.md).</span></span> 
  
<span data-ttu-id="e0659-148">Pour obtenir des informations générales sur le processus de notification, voir [Notification d’événement MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="e0659-148">For general information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e0659-149">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="e0659-149">Notes to implementers</span></span>

<span data-ttu-id="e0659-150">Votre implémentation **OnNotify** consiste à un ou plusieurs blocs de code pour chaque type de notification que vous souhaitez recevoir.</span><span class="sxs-lookup"><span data-stu-id="e0659-150">Your **OnNotify** implementation will typically consist of one or more blocks of code for each type of notification you expect to receive.</span></span> <span data-ttu-id="e0659-151">Dans ces blocs de code, effectuez toutes les tâches que vous prenez en compte nécessaire en réponse à la notification.</span><span class="sxs-lookup"><span data-stu-id="e0659-151">Within these blocks of code, perform any tasks that you consider necessary as a response to the notification.</span></span> <span data-ttu-id="e0659-152">Par exemple, supposons que vous inscrivez pour recevoir des notifications **fnevObjectModified** dans un dossier qui est inclus dans l’affichage d’une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e0659-152">For example, suppose you register to receive **fnevObjectModified** notifications on a folder that is included in a dialog box display.</span></span> <span data-ttu-id="e0659-153">Dans le bloc de code que vous incluez dans votre méthode **OnNotify** pour gérer les notifications **fnevObjectModified** , vous pouvez envoyer un message Windows à la boîte de dialogue pour demander un affichage mis à jour.</span><span class="sxs-lookup"><span data-stu-id="e0659-153">In the block of code that you include in your **OnNotify** method to handle **fnevObjectModified** notifications, you might send a Windows message to the dialog box to request an updated display.</span></span> 
  
<span data-ttu-id="e0659-154">Ne modifiez pas ou ne libérer la structure **NOTIFICATION** transmise à **OnNotify**.</span><span class="sxs-lookup"><span data-stu-id="e0659-154">Do not modify or free the **NOTIFICATION** structure passed to **OnNotify**.</span></span> <span data-ttu-id="e0659-155">Les données de la structure sont valides uniquement jusqu'à **OnNotify** renvoie.</span><span class="sxs-lookup"><span data-stu-id="e0659-155">The data in the structure is valid only until **OnNotify** returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e0659-156">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="e0659-156">Notes to callers</span></span>

<span data-ttu-id="e0659-157">En cas de modifications apportées à plusieurs objets, vous pouvez signaler un récepteur de notifications enregistrés dans un seul appel à **OnNotify** ou dans plusieurs appels en fonction des contraintes de mémoire.</span><span class="sxs-lookup"><span data-stu-id="e0659-157">When changes occur to multiple objects, you can notify a registered advise sink in a single call to **OnNotify** or in multiple calls depending on memory constraints.</span></span> <span data-ttu-id="e0659-158">Cela est vrai, même si les modifications sont le résultat d’un appel de méthode ou plusieurs.</span><span class="sxs-lookup"><span data-stu-id="e0659-158">This is true regardless of whether the changes are the result of one method call or several.</span></span> <span data-ttu-id="e0659-159">Par exemple, un appel à [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) peut affecter plusieurs dossiers et messages.</span><span class="sxs-lookup"><span data-stu-id="e0659-159">For example, a call to [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) can affect multiple messages and folders.</span></span> <span data-ttu-id="e0659-160">Comme un fournisseur de magasins de message, vous pouvez appeler **OnNotify** avec un type d’événement **fnevObjectModified** pour le dossier cible ou un grand nombre d’appels, un pour chaque affectent les messages.</span><span class="sxs-lookup"><span data-stu-id="e0659-160">As a message store provider, you can make one call to **OnNotify** with an **fnevObjectModified** event type for the target folder or many calls, one for each affect messages.</span></span> <span data-ttu-id="e0659-161">De même, si un client effectue des appels répétés à [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), ces appels peuvent être combinées dans un événement **fnevObjectModified** pour le dossier ou séparés en événements individuels **fnevObjectCreated** pour chaque nouveau message.</span><span class="sxs-lookup"><span data-stu-id="e0659-161">Similarly, if a client makes repeated calls to [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), these calls can be combined into one **fnevObjectModified** event for the folder or separated into individual **fnevObjectCreated** events for each new message.</span></span> 
  
<span data-ttu-id="e0659-162">Pour plus d’informations sur la façon et le moment générer des notifications, voir [Notification d’événement MAPI](event-notification-in-mapi.md) et [Prenant en charge les notifications](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="e0659-162">For more information about how and when to generate notifications, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e0659-163">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e0659-163">MFCMAPI reference</span></span>

<span data-ttu-id="e0659-164">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e0659-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e0659-165">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="e0659-165">**File**</span></span>|<span data-ttu-id="e0659-166">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="e0659-166">**Function**</span></span>|<span data-ttu-id="e0659-167">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="e0659-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e0659-168">AdviseSink.h et AdviseSink.cpp</span><span class="sxs-lookup"><span data-stu-id="e0659-168">AdviseSink.h and AdviseSink.cpp</span></span>  <br/> |<span data-ttu-id="e0659-169">CAdviseSink::OnNotifyDesc</span><span class="sxs-lookup"><span data-stu-id="e0659-169">CAdviseSink::OnNotifyDesc</span></span>  <br/> |<span data-ttu-id="e0659-170">La classe CAdviseSink est implémentée pour gérer toutes les notifications de MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="e0659-170">The CAdviseSink class is implemented to handle all notifications in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e0659-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0659-171">See also</span></span>



[<span data-ttu-id="e0659-172">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="e0659-172">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="e0659-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="e0659-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="e0659-174">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="e0659-174">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="e0659-175">Notification</span><span class="sxs-lookup"><span data-stu-id="e0659-175">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="e0659-176">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e0659-176">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)


[<span data-ttu-id="e0659-177">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="e0659-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

