---
title: IMAPISupportNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Notify
api_type:
- COM
ms.assetid: c16c668e-2c8b-4759-bbca-d0c5662b62e9
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: db23d1801bf32fd947a77dfd887c56f75ded5681
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784011"
---
# <a name="imapisupportnotify"></a><span data-ttu-id="ac6f0-103">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="ac6f0-103">IMAPISupport::Notify</span></span>

<span data-ttu-id="ac6f0-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ac6f0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ac6f0-105">Envoie une notification d’un événement spécifié à une source d’advise initialement enregistré pour la notification par le biais de la méthode [IMAPISupport::Subscribe](imapisupport-subscribe.md) .</span><span class="sxs-lookup"><span data-stu-id="ac6f0-105">Sends a notification of a specified event to an advise source that originally registered for the notification through the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span></span> 
  
```cpp
HRESULT Notify(
LPNOTIFKEY lpKey,
ULONG cNotification,
LPNOTIFICATION lpNotifications,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ac6f0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac6f0-106">Parameters</span></span>

<span data-ttu-id="ac6f0-107">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="ac6f0-107">_lpKey_</span></span>
  
> <span data-ttu-id="ac6f0-108">[in] Pointeur vers la clé de notification pour l’objet source de notification.</span><span class="sxs-lookup"><span data-stu-id="ac6f0-108">[in] A pointer to the notification key for the advise source object.</span></span> <span data-ttu-id="ac6f0-109">Le paramètre _lpKey_ ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="ac6f0-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
<span data-ttu-id="ac6f0-110">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="ac6f0-110">_cNotification_</span></span>
  
> <span data-ttu-id="ac6f0-111">[in] Le nombre de structures de notification indiqué par le paramètre _lpNotifications_ .</span><span class="sxs-lookup"><span data-stu-id="ac6f0-111">[in] The count of notification structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
<span data-ttu-id="ac6f0-112">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="ac6f0-112">_lpNotifications_</span></span>
  
> <span data-ttu-id="ac6f0-113">[in] Pointeur vers un tableau de structures [NOTIFICATION](notification.md) qui décrivent les notifications en attente.</span><span class="sxs-lookup"><span data-stu-id="ac6f0-113">[in] A pointer to an array of [NOTIFICATION](notification.md) structures that describe pending notifications.</span></span> 
    
<span data-ttu-id="ac6f0-114">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="ac6f0-114">_lpulFlags_</span></span>
  
> <span data-ttu-id="ac6f0-115">[entrée, sortie] Masque de bits d’indicateurs qui contrôle le processus de notification.</span><span class="sxs-lookup"><span data-stu-id="ac6f0-115">[in, out] A bitmask of flags that controls the notification process.</span></span> <span data-ttu-id="ac6f0-116">À l’entrée, l’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="ac6f0-116">On input, the following flag can be set:</span></span>
    
  - <span data-ttu-id="ac6f0-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ac6f0-117">MAPI_UNICODE</span></span> 
    
    > <span data-ttu-id="ac6f0-118">Les chaînes dans les structures de notification désignés par _lpNotifications_ sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="ac6f0-118">The strings in the notification structures pointed to by  _lpNotifications_ are in Unicode format.</span></span> <span data-ttu-id="ac6f0-119">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="ac6f0-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 

    <span data-ttu-id="ac6f0-120">Dans la sortie, MAPI permettre définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="ac6f0-120">On output, MAPI can set the following flag:</span></span>
        
  - <span data-ttu-id="ac6f0-121">NOTIFY_CANCELED</span><span class="sxs-lookup"><span data-stu-id="ac6f0-121">NOTIFY_CANCELED</span></span> 
    
    > <span data-ttu-id="ac6f0-122">Une fonction de rappel annulé une notification synchrone.</span><span class="sxs-lookup"><span data-stu-id="ac6f0-122">A callback function canceled a synchronous notification.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ac6f0-123">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="ac6f0-123">Return value</span></span>

<span data-ttu-id="ac6f0-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac6f0-124">S_OK</span></span> 
  
> <span data-ttu-id="ac6f0-125">Les notifications ont été correctement générées.</span><span class="sxs-lookup"><span data-stu-id="ac6f0-125">The notifications were successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ac6f0-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="ac6f0-126">Remarks</span></span>

<span data-ttu-id="ac6f0-127">La méthode **IMAPISupport::Notify** est implémentée pour tous les objets de prise en charge de fournisseur de service.</span><span class="sxs-lookup"><span data-stu-id="ac6f0-127">The **IMAPISupport::Notify** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="ac6f0-128">Fournisseurs de services d’appel **notifier** pour demander que MAPI générer une notification pour un récepteur de notifications qui a précédemment inscrit pour la notification par le biais de la méthode **IMAPISupport::Subscribe** .</span><span class="sxs-lookup"><span data-stu-id="ac6f0-128">Service providers call **Notify** to request that MAPI generate a notification for an advise sink that has previously registered for the notification through the **IMAPISupport::Subscribe** method.</span></span> 
  
<span data-ttu-id="ac6f0-129">Copies **notifier** les structures désignés par le paramètre _lpNotifications_ dans la mémoire et appelle la méthode de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) du récepteur advise approprié.</span><span class="sxs-lookup"><span data-stu-id="ac6f0-129">**Notify** copies the structures pointed to by the  _lpNotifications_ parameter into memory and calls the appropriate advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="ac6f0-130">Lors de la notification **OnNotify** est terminé, il libère la mémoire impliqués.</span><span class="sxs-lookup"><span data-stu-id="ac6f0-130">When **OnNotify** is finished with the notification, it releases the memory involved.</span></span> <span data-ttu-id="ac6f0-131">L’appelant n’a pas besoin d’allouer de la mémoire ; MAPI effectue toutes les l’allocation de mémoire nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ac6f0-131">The caller does not need to allocate memory; MAPI performs all necessary memory allocation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ac6f0-132">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="ac6f0-132">Notes to callers</span></span>

<span data-ttu-id="ac6f0-133">La clé de notification passée dans le paramètre _lpKey_ doit être identique à la clé _lpKey_ passée à la méthode **IMAPISupport::Subscribe** .</span><span class="sxs-lookup"><span data-stu-id="ac6f0-133">The notification key passed in the  _lpKey_ parameter should be identical to the key passed in  _lpKey_ to the **IMAPISupport::Subscribe** method.</span></span> <span data-ttu-id="ac6f0-134">De nombreux fournisseurs utilisent l’identificateur d’entrée de la source advise comme clé, mais autres données, telles que d’un chemin d’accès du fichier, peuvent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="ac6f0-134">Many providers use the entry identifier of the advise source as the key, but other data, such as a file path, can be used.</span></span> <span data-ttu-id="ac6f0-135">MAPI utilise cette clé pour rechercher tous les enregistrements pour les notifications sur la source advise identifiés.</span><span class="sxs-lookup"><span data-stu-id="ac6f0-135">MAPI uses this key to find all the registrations for notifications on the identified advise source.</span></span> 
  
<span data-ttu-id="ac6f0-136">N’oubliez pas que vous définissez le membre **lpEntryID** de la structure de notification sur un identificateur d’entrée à long terme.</span><span class="sxs-lookup"><span data-stu-id="ac6f0-136">Be sure that you set the **lpEntryID** member of the notification structure to a long-term entry identifier.</span></span> 
  
<span data-ttu-id="ac6f0-137">Si vous définissez l’indicateur NOTIFY_SYNC sur l' **abonnement** appels pour les notifications en attente, **notifier** les fonctions de rappel de méthode **IMAPIAdviseSink::OnNotify** avant de retourner.</span><span class="sxs-lookup"><span data-stu-id="ac6f0-137">If you set the NOTIFY_SYNC flag on the **Subscribe** call for any of the pending notifications, **Notify** calls the **IMAPIAdviseSink::OnNotify** method callback functions before returning.</span></span> <span data-ttu-id="ac6f0-138">Un récepteur de notifications peut être créé manuellement ou en appelant [HrAllocAdviseSink](hrallocadvisesink.md).</span><span class="sxs-lookup"><span data-stu-id="ac6f0-138">An advise sink can be created manually or by calling [HrAllocAdviseSink](hrallocadvisesink.md).</span></span> <span data-ttu-id="ac6f0-139">La fonction **HrAllocAdviseSink** permet à ses appelant spécifier une fonction de rappel qui appelle **notifier** dans le cadre de la notification.</span><span class="sxs-lookup"><span data-stu-id="ac6f0-139">The **HrAllocAdviseSink** function allows its caller to specify a callback function that **Notify** calls as part of the notification.</span></span> <span data-ttu-id="ac6f0-140">La fonction de rappel est conforme au prototype [NOTIFCALLBACK](notifcallback.md) .</span><span class="sxs-lookup"><span data-stu-id="ac6f0-140">The callback function conforms to the [NOTIFCALLBACK](notifcallback.md) prototype.</span></span> <span data-ttu-id="ac6f0-141">Fonctions de rappel implémentées par les clients toujours retournent S_OK ; fonctions de rappel implémentées par les fournisseurs de service peuvent renvoyer CALLBACK_DISCONTINUE.</span><span class="sxs-lookup"><span data-stu-id="ac6f0-141">Callback functions implemented by clients always return S_OK; callback functions implemented by service providers can return CALLBACK_DISCONTINUE.</span></span> 
  
<span data-ttu-id="ac6f0-142">Si une fonction de rappel renvoie CALLBACK_DISCONTINUE, MAPI arrête l’envoi de notifications et renvoie NOTIFY_CANCELED dans le paramètre _lpulFlags_ de la méthode **Notify** .</span><span class="sxs-lookup"><span data-stu-id="ac6f0-142">If a callback function returns CALLBACK_DISCONTINUE, MAPI stops sending notifications and returns NOTIFY_CANCELED in the **Notify** method's  _lpulFlags_ parameter.</span></span> <span data-ttu-id="ac6f0-143">Vous pouvez supposer que le processus est inactive et arrêter la génération de notifications pour ce processus.</span><span class="sxs-lookup"><span data-stu-id="ac6f0-143">You can assume that the process is inactive and stop generating notifications for that process.</span></span> <span data-ttu-id="ac6f0-144">Si **Notify** renvoie la valeur 0 dans _lpulFlags_, le processus est toujours actif et vous pouvez continuer à envoyer des notifications, comme il convient.</span><span class="sxs-lookup"><span data-stu-id="ac6f0-144">If **Notify** returns 0 in  _lpulFlags_, the process is still active and you should continue to send notifications, as appropriate.</span></span>
  
<span data-ttu-id="ac6f0-145">Lorsque vous utilisez des notifications synchrones, veillez à éviter les situations de blocage.</span><span class="sxs-lookup"><span data-stu-id="ac6f0-145">When you use synchronous notifications, be careful to avoid deadlock situations.</span></span>
  
<span data-ttu-id="ac6f0-146">Pour plus d’informations sur le processus de notification, reportez-vous à la section [Notification d’événement MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="ac6f0-146">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ac6f0-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac6f0-147">See also</span></span>

- [<span data-ttu-id="ac6f0-148">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="ac6f0-148">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)  
- [<span data-ttu-id="ac6f0-149">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="ac6f0-149">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)  
- [<span data-ttu-id="ac6f0-150">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="ac6f0-150">NOTIFCALLBACK</span></span>](notifcallback.md) 
- [<span data-ttu-id="ac6f0-151">Notification</span><span class="sxs-lookup"><span data-stu-id="ac6f0-151">NOTIFICATION</span></span>](notification.md)  
- [<span data-ttu-id="ac6f0-152">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="ac6f0-152">NOTIFKEY</span></span>](notifkey.md)  
- [<span data-ttu-id="ac6f0-153">Propriété canonique PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="ac6f0-153">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)  
- [<span data-ttu-id="ac6f0-154">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ac6f0-154">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

