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
ms.openlocfilehash: 5983ed3229f6b0053f15a614116cf5680e942587
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351442"
---
# <a name="imapiadvisesinkonnotify"></a><span data-ttu-id="6a886-103">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="6a886-103">IMAPIAdviseSink::OnNotify</span></span>

  
  
<span data-ttu-id="6a886-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a886-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a886-105">Répond à une notification en effectuant une ou plusieurs tâches.</span><span class="sxs-lookup"><span data-stu-id="6a886-105">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="6a886-106">Les tâches effectuées dépendent du type d'événement et de l'objet qui génère la notification.</span><span class="sxs-lookup"><span data-stu-id="6a886-106">The tasks performed depend on the type of event and the object that generates the notification.</span></span> 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="6a886-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a886-107">Parameters</span></span>

 <span data-ttu-id="6a886-108">_cNotif_</span><span class="sxs-lookup"><span data-stu-id="6a886-108">_cNotif_</span></span>
  
> <span data-ttu-id="6a886-109">dans Nombre de structures de [notification](notification.md) pointées par le paramètre _lpNotifications_ .</span><span class="sxs-lookup"><span data-stu-id="6a886-109">[in] The count of [NOTIFICATION](notification.md) structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="6a886-110">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="6a886-110">_lpNotifications_</span></span>
  
> <span data-ttu-id="6a886-111">dans Pointeur vers une ou plusieurs structures de **notification** qui fournissent des informations sur les événements qui se sont produits.</span><span class="sxs-lookup"><span data-stu-id="6a886-111">[in] A pointer to one or more **NOTIFICATION** structures that provide information about the events that have occurred.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6a886-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6a886-112">Return value</span></span>

<span data-ttu-id="6a886-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="6a886-113">S_OK</span></span> 
  
> <span data-ttu-id="6a886-114">La notification a été correctement traitée.</span><span class="sxs-lookup"><span data-stu-id="6a886-114">The notification was processed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6a886-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="6a886-115">Remarks</span></span>

<span data-ttu-id="6a886-116">Le processus de notification démarre lorsqu'un client ou MAPI effectue un appel à la méthode **Advise** d'un fournisseur de services pour s'inscrire afin de recevoir une notification d'un type particulier pour un objet particulier.</span><span class="sxs-lookup"><span data-stu-id="6a886-116">The notification process starts when a client or MAPI makes a call to a service provider's **Advise** method to register to receive a notification of a particular type for a particular object.</span></span> <span data-ttu-id="6a886-117">L'un des paramètres de la \*\*\*\* méthode Advise est un pointeur vers un objet de récepteur de notification qui implémente l'interface [IMAPIAdviseSink](imapiadvisesinkiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="6a886-117">One of the parameters to the **Advise** method is a pointer to an advise sink object that implements the [IMAPIAdviseSink](imapiadvisesinkiunknown.md) interface.</span></span> <span data-ttu-id="6a886-118">Lorsqu'un événement se produit dans l'objet cible qui correspond à la notification enregistrée, le fournisseur de services, directement ou indirectement via MAPI, appelle la méthode **OnNotify** du récepteur de notification.</span><span class="sxs-lookup"><span data-stu-id="6a886-118">When an event occurs to the target object that corresponds to the registered notification, the service provider, either directly or indirectly through MAPI, calls the advise sink's **OnNotify** method.</span></span> 
  
<span data-ttu-id="6a886-119">L'appel à **OnNotify** peut se produire soit lors de l'appel MAPI qui provoque l'événement, soit ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="6a886-119">The call to **OnNotify** can occur either during the MAPI call that is causing the event or at some later time.</span></span> <span data-ttu-id="6a886-120">Sur les systèmes qui prennent en charge plusieurs threads d'exécution, **OnNotify** peut être appelé sur le même thread qui a été utilisé pour l'inscription ou sur un autre thread.</span><span class="sxs-lookup"><span data-stu-id="6a886-120">On systems that support multiple threads of execution, **OnNotify** can be called either on the same thread that was used for registration or on a different thread.</span></span> <span data-ttu-id="6a886-121">Les clients peuvent s'assurer que l'appel **OnNotify** est effectué sur le même thread que celui utilisé pour appeler Advise en créant le récepteur de \*\*\*\* notifications qu'ils passent à la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="6a886-121">Clients can make sure that the **OnNotify** call is made on the same thread used to call **Advise** by creating the advise sink that they pass to **Advise** with the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="6a886-122">Le paramètre _lpNotifications_ pointe vers une ou plusieurs structures de **notification** qui décrivent les modifications apportées au cours de l'événement.</span><span class="sxs-lookup"><span data-stu-id="6a886-122">The  _lpNotifications_ parameter points to one or more **NOTIFICATION** structures that describe what has changed during the event.</span></span> <span data-ttu-id="6a886-123">Il existe un autre type de structure de **notification** pour chaque type d'événement.</span><span class="sxs-lookup"><span data-stu-id="6a886-123">There is a different type of **NOTIFICATION** structure for each type of event.</span></span> 
  
<span data-ttu-id="6a886-124">Le tableau suivant répertorie les valeurs qui sont utilisées pour représenter les types possibles d'événements et les structures associées à chaque valeur:</span><span class="sxs-lookup"><span data-stu-id="6a886-124">The following table lists the values that are used to represent the possible types of events and the structures associated with each value:</span></span>
  
|<span data-ttu-id="6a886-125">**Type d'événement de notification**</span><span class="sxs-lookup"><span data-stu-id="6a886-125">**Notification event type**</span></span>|<span data-ttu-id="6a886-126">**Structure correspondante**</span><span class="sxs-lookup"><span data-stu-id="6a886-126">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6a886-127">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="6a886-127">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="6a886-128">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="6a886-128">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="6a886-129">**fnevNewMail**</span><span class="sxs-lookup"><span data-stu-id="6a886-129">**fnevNewMail**</span></span> <br/> |[<span data-ttu-id="6a886-130">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="6a886-130">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md) <br/> |
|<span data-ttu-id="6a886-131">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="6a886-131">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="6a886-132">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="6a886-132">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="6a886-133">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="6a886-133">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="6a886-134">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="6a886-134">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="6a886-135">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="6a886-135">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="6a886-136">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="6a886-136">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="6a886-137">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="6a886-137">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="6a886-138">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="6a886-138">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="6a886-139">**fnevSearchComplete**</span><span class="sxs-lookup"><span data-stu-id="6a886-139">**fnevSearchComplete**</span></span> <br/> |[<span data-ttu-id="6a886-140">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="6a886-140">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="6a886-141">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="6a886-141">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="6a886-142">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="6a886-142">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
|<span data-ttu-id="6a886-143">**fnevStatusObjectModified**</span><span class="sxs-lookup"><span data-stu-id="6a886-143">**fnevStatusObjectModified**</span></span> <br/> |[<span data-ttu-id="6a886-144">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="6a886-144">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md) <br/> |
|<span data-ttu-id="6a886-145">**fnevExtended**</span><span class="sxs-lookup"><span data-stu-id="6a886-145">**fnevExtended**</span></span> <br/> |[<span data-ttu-id="6a886-146">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="6a886-146">EXTENDED_NOTIFICATION</span></span>](extended_notification.md) <br/> |
   
<span data-ttu-id="6a886-147">Pour plus d'informations sur la configuration et l'arrêt des notifications, consultez les entrées de \*\*\*\* référence pour les méthodes Advise et Unadvise pour l'une des interfaces suivantes: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), \*\*\*\* [IMAPIForm](imapiformiunknown.md), [ IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md)et [IMSLogon](imslogoniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="6a886-147">For more information about how to set up and stop notifications, see the reference entries for the **Advise** and **Unadvise** methods for any of the following interfaces: [IABLogon](iablogoniunknown.md), [IAddrBook](iaddrbookimapiprop.md), [IMAPIForm](imapiformiunknown.md), [IMAPISession](imapisessioniunknown.md), [IMAPITable](imapitableiunknown.md), [IMsgStore](imsgstoreimapiprop.md), and [IMSLogon](imslogoniunknown.md).</span></span> 
  
<span data-ttu-id="6a886-148">Pour obtenir des informations générales sur le processus de notification, consultez la rubrique [notifications d'événements dans MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="6a886-148">For general information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6a886-149">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="6a886-149">Notes to implementers</span></span>

<span data-ttu-id="6a886-150">Votre implémentation de **OnNotify** se compose généralement d'un ou de plusieurs blocs de code pour chaque type de notification que vous prévoyez de recevoir.</span><span class="sxs-lookup"><span data-stu-id="6a886-150">Your **OnNotify** implementation will typically consist of one or more blocks of code for each type of notification you expect to receive.</span></span> <span data-ttu-id="6a886-151">À l'intérieur de ces blocs de code, effectuez toutes les tâches que vous jugez nécessaires en réponse à la notification.</span><span class="sxs-lookup"><span data-stu-id="6a886-151">Within these blocks of code, perform any tasks that you consider necessary as a response to the notification.</span></span> <span data-ttu-id="6a886-152">Par exemple, supposons que vous vous inscrivez pour recevoir des notifications **fnevObjectModified** sur un dossier qui est inclus dans un affichage de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="6a886-152">For example, suppose you register to receive **fnevObjectModified** notifications on a folder that is included in a dialog box display.</span></span> <span data-ttu-id="6a886-153">Dans le bloc de code que vous incluez dans votre méthode **OnNotify** pour gérer les notifications **fnevObjectModified** , vous pouvez envoyer un message Windows à la boîte de dialogue pour demander un affichage mis à jour.</span><span class="sxs-lookup"><span data-stu-id="6a886-153">In the block of code that you include in your **OnNotify** method to handle **fnevObjectModified** notifications, you might send a Windows message to the dialog box to request an updated display.</span></span> 
  
<span data-ttu-id="6a886-154">Ne modifiez pas ou ne libérez pas la structure de **notification** transmise à **OnNotify**.</span><span class="sxs-lookup"><span data-stu-id="6a886-154">Do not modify or free the **NOTIFICATION** structure passed to **OnNotify**.</span></span> <span data-ttu-id="6a886-155">Les données de la structure sont valides uniquement jusqu'à ce que **OnNotify** renvoie.</span><span class="sxs-lookup"><span data-stu-id="6a886-155">The data in the structure is valid only until **OnNotify** returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6a886-156">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="6a886-156">Notes to callers</span></span>

<span data-ttu-id="6a886-157">Lorsque des modifications sont apportées à plusieurs objets, vous pouvez avertir un récepteur de notifications enregistré en un seul appel à **OnNotify** ou dans plusieurs appels en fonction des contraintes de mémoire.</span><span class="sxs-lookup"><span data-stu-id="6a886-157">When changes occur to multiple objects, you can notify a registered advise sink in a single call to **OnNotify** or in multiple calls depending on memory constraints.</span></span> <span data-ttu-id="6a886-158">Cela est vrai, que les modifications soient le résultat d'un ou de plusieurs appels de méthode.</span><span class="sxs-lookup"><span data-stu-id="6a886-158">This is true regardless of whether the changes are the result of one method call or several.</span></span> <span data-ttu-id="6a886-159">Par exemple, un appel à [IMAPIFolder:: CopyMessages](imapifolder-copymessages.md) peut affecter plusieurs messages et dossiers.</span><span class="sxs-lookup"><span data-stu-id="6a886-159">For example, a call to [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) can affect multiple messages and folders.</span></span> <span data-ttu-id="6a886-160">En tant que fournisseur de banque de messages, vous pouvez passer un appel à **OnNotify** avec un type d'événement **fnevObjectModified** pour le dossier cible ou de nombreux appels, un pour chacun affecte les messages.</span><span class="sxs-lookup"><span data-stu-id="6a886-160">As a message store provider, you can make one call to **OnNotify** with an **fnevObjectModified** event type for the target folder or many calls, one for each affect messages.</span></span> <span data-ttu-id="6a886-161">De même, si un client effectue des appels répétés à [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md), ces appels peuvent être combinés en un seul événement **fnevObjectModified** pour le dossier ou être séparés en événements **fnevObjectCreated** individuels pour chaque nouveau message.</span><span class="sxs-lookup"><span data-stu-id="6a886-161">Similarly, if a client makes repeated calls to [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), these calls can be combined into one **fnevObjectModified** event for the folder or separated into individual **fnevObjectCreated** events for each new message.</span></span> 
  
<span data-ttu-id="6a886-162">Pour plus d'informations sur la génération de notifications, consultez la rubrique [notifications d'événements dans MAPI](event-notification-in-mapi.md) et [notification d'événement de prise en charge](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="6a886-162">For more information about how and when to generate notifications, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6a886-163">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6a886-163">MFCMAPI reference</span></span>

<span data-ttu-id="6a886-164">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6a886-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6a886-165">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="6a886-165">**File**</span></span>|<span data-ttu-id="6a886-166">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="6a886-166">**Function**</span></span>|<span data-ttu-id="6a886-167">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="6a886-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6a886-168">AdviseSink. h et AdviseSink. cpp</span><span class="sxs-lookup"><span data-stu-id="6a886-168">AdviseSink.h and AdviseSink.cpp</span></span>  <br/> |<span data-ttu-id="6a886-169">CAdviseSink:: OnNotifyDesc</span><span class="sxs-lookup"><span data-stu-id="6a886-169">CAdviseSink::OnNotifyDesc</span></span>  <br/> |<span data-ttu-id="6a886-170">La classe CAdviseSink est implémentée pour gérer toutes les notifications dans MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="6a886-170">The CAdviseSink class is implemented to handle all notifications in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6a886-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a886-171">See also</span></span>



[<span data-ttu-id="6a886-172">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="6a886-172">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="6a886-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="6a886-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="6a886-174">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="6a886-174">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="6a886-175">Notification</span><span class="sxs-lookup"><span data-stu-id="6a886-175">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="6a886-176">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6a886-176">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)


[<span data-ttu-id="6a886-177">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="6a886-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

