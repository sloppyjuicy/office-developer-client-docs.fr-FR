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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6160b8e75bdc9059965c2358b9fe7d296e1f66d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435935"
---
# <a name="imapisupportnotify"></a><span data-ttu-id="e060b-103">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="e060b-103">IMAPISupport::Notify</span></span>

<span data-ttu-id="e060b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e060b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e060b-105">Envoie une notification d’un événement spécifié à une source de conseil qui s’est inscrite à l’origine pour la notification via la méthode [IMAPISupport::Subscribe.](imapisupport-subscribe.md)</span><span class="sxs-lookup"><span data-stu-id="e060b-105">Sends a notification of a specified event to an advise source that originally registered for the notification through the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span></span> 
  
```cpp
HRESULT Notify(
LPNOTIFKEY lpKey,
ULONG cNotification,
LPNOTIFICATION lpNotifications,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e060b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e060b-106">Parameters</span></span>

<span data-ttu-id="e060b-107">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="e060b-107">_lpKey_</span></span>
  
> <span data-ttu-id="e060b-108">[in] Pointeur vers la clé de notification pour l’objet source de notification.</span><span class="sxs-lookup"><span data-stu-id="e060b-108">[in] A pointer to the notification key for the advise source object.</span></span> <span data-ttu-id="e060b-109">Le  _paramètre lpKey_ ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="e060b-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
<span data-ttu-id="e060b-110">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="e060b-110">_cNotification_</span></span>
  
> <span data-ttu-id="e060b-111">[in] Nombre de structures de notifications pointées par _le paramètre lpNotifications._</span><span class="sxs-lookup"><span data-stu-id="e060b-111">[in] The count of notification structures pointed to by the  _lpNotifications_ parameter.</span></span> 
    
<span data-ttu-id="e060b-112">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="e060b-112">_lpNotifications_</span></span>
  
> <span data-ttu-id="e060b-113">[in] Pointeur vers un tableau de structures [de NOTIFICATION](notification.md) qui décrivent les notifications en attente.</span><span class="sxs-lookup"><span data-stu-id="e060b-113">[in] A pointer to an array of [NOTIFICATION](notification.md) structures that describe pending notifications.</span></span> 
    
<span data-ttu-id="e060b-114">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="e060b-114">_lpulFlags_</span></span>
  
> <span data-ttu-id="e060b-115">[in, out] Masque de bits d’indicateurs qui contrôle le processus de notification.</span><span class="sxs-lookup"><span data-stu-id="e060b-115">[in, out] A bitmask of flags that controls the notification process.</span></span> <span data-ttu-id="e060b-116">Lors de l’entrée, l’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="e060b-116">On input, the following flag can be set:</span></span>
    
  - <span data-ttu-id="e060b-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e060b-117">MAPI_UNICODE</span></span> 
    
    > <span data-ttu-id="e060b-118">Les chaînes dans les structures de notification pointées par  _lpNotifications_ sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="e060b-118">The strings in the notification structures pointed to by  _lpNotifications_ are in Unicode format.</span></span> <span data-ttu-id="e060b-119">Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="e060b-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 

    <span data-ttu-id="e060b-120">Lors de la sortie, MAPI peut définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="e060b-120">On output, MAPI can set the following flag:</span></span>
        
  - <span data-ttu-id="e060b-121">NOTIFY_CANCELED</span><span class="sxs-lookup"><span data-stu-id="e060b-121">NOTIFY_CANCELED</span></span> 
    
    > <span data-ttu-id="e060b-122">Une fonction de rappel a annulé une notification synchrone.</span><span class="sxs-lookup"><span data-stu-id="e060b-122">A callback function canceled a synchronous notification.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e060b-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e060b-123">Return value</span></span>

<span data-ttu-id="e060b-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="e060b-124">S_OK</span></span> 
  
> <span data-ttu-id="e060b-125">Les notifications ont été correctement générées.</span><span class="sxs-lookup"><span data-stu-id="e060b-125">The notifications were successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e060b-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="e060b-126">Remarks</span></span>

<span data-ttu-id="e060b-127">La **méthode IMAPISupport::Notify** est implémentée pour tous les objets de support du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="e060b-127">The **IMAPISupport::Notify** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="e060b-128">Les fournisseurs de services appellent **Notify** pour demander à MAPI de générer une notification pour un recevoir de notification qui s’est précédemment inscrit pour la notification via la méthode **IMAPISupport::Subscribe.**</span><span class="sxs-lookup"><span data-stu-id="e060b-128">Service providers call **Notify** to request that MAPI generate a notification for an advise sink that has previously registered for the notification through the **IMAPISupport::Subscribe** method.</span></span> 
  
<span data-ttu-id="e060b-129">**Notify** copie les structures pointées vers le paramètre  _lpNotifications_ dans la mémoire et appelle la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) du sink de notification approprié.</span><span class="sxs-lookup"><span data-stu-id="e060b-129">**Notify** copies the structures pointed to by the  _lpNotifications_ parameter into memory and calls the appropriate advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="e060b-130">Une fois la notification terminée, **OnNotify** libère la mémoire impliquée.</span><span class="sxs-lookup"><span data-stu-id="e060b-130">When **OnNotify** is finished with the notification, it releases the memory involved.</span></span> <span data-ttu-id="e060b-131">L’appelant n’a pas besoin d’allouer de mémoire . MAPI effectue toutes les allocations de mémoire nécessaires.</span><span class="sxs-lookup"><span data-stu-id="e060b-131">The caller does not need to allocate memory; MAPI performs all necessary memory allocation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e060b-132">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="e060b-132">Notes to callers</span></span>

<span data-ttu-id="e060b-133">La clé de notification transmise dans le paramètre _lpKey_ doit être identique à la clé transmise dans _lpKey_ à la méthode **IMAPISupport::Subscribe.**</span><span class="sxs-lookup"><span data-stu-id="e060b-133">The notification key passed in the  _lpKey_ parameter should be identical to the key passed in  _lpKey_ to the **IMAPISupport::Subscribe** method.</span></span> <span data-ttu-id="e060b-134">De nombreux fournisseurs utilisent l’identificateur d’entrée de la source de conseil comme clé, mais d’autres données, telles qu’un chemin d’accès à un fichier, peuvent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="e060b-134">Many providers use the entry identifier of the advise source as the key, but other data, such as a file path, can be used.</span></span> <span data-ttu-id="e060b-135">MAPI utilise cette clé pour rechercher toutes les inscriptions pour les notifications sur la source de notification identifiée.</span><span class="sxs-lookup"><span data-stu-id="e060b-135">MAPI uses this key to find all the registrations for notifications on the identified advise source.</span></span> 
  
<span data-ttu-id="e060b-136">Assurez-vous de définir le membre **lpEntryID** de la structure de notification sur un identificateur d’entrée à long terme.</span><span class="sxs-lookup"><span data-stu-id="e060b-136">Be sure that you set the **lpEntryID** member of the notification structure to a long-term entry identifier.</span></span> 
  
<span data-ttu-id="e060b-137">Si vous définissez l’indicateur  NOTIFY_SYNC sur l’appel d’abonnement pour l’une des notifications en attente, **Notify** appelle les fonctions de rappel de la méthode **IMAPIAdviseSink::OnNotify** avant de les renvoyer.</span><span class="sxs-lookup"><span data-stu-id="e060b-137">If you set the NOTIFY_SYNC flag on the **Subscribe** call for any of the pending notifications, **Notify** calls the **IMAPIAdviseSink::OnNotify** method callback functions before returning.</span></span> <span data-ttu-id="e060b-138">Un sink de conseil peut être créé manuellement ou en appelant [HrAllocAdviseSink](hrallocadvisesink.md).</span><span class="sxs-lookup"><span data-stu-id="e060b-138">An advise sink can be created manually or by calling [HrAllocAdviseSink](hrallocadvisesink.md).</span></span> <span data-ttu-id="e060b-139">La **fonction HrAllocAdviseSink** permet à son appelant de  spécifier une fonction de rappel qui notifie les appels dans le cadre de la notification.</span><span class="sxs-lookup"><span data-stu-id="e060b-139">The **HrAllocAdviseSink** function allows its caller to specify a callback function that **Notify** calls as part of the notification.</span></span> <span data-ttu-id="e060b-140">La fonction de rappel est conforme au prototype [NOTIFCALLBACK.](notifcallback.md)</span><span class="sxs-lookup"><span data-stu-id="e060b-140">The callback function conforms to the [NOTIFCALLBACK](notifcallback.md) prototype.</span></span> <span data-ttu-id="e060b-141">Les fonctions de rappel implémentées par les clients retournent toujours S_OK ; les fonctions de rappel implémentées par les fournisseurs de services peuvent renvoyer CALLBACK_DISCONTINUE.</span><span class="sxs-lookup"><span data-stu-id="e060b-141">Callback functions implemented by clients always return S_OK; callback functions implemented by service providers can return CALLBACK_DISCONTINUE.</span></span> 
  
<span data-ttu-id="e060b-142">Si une fonction de rappel renvoie CALLBACK_DISCONTINUE, MAPI cesse d’envoyer des notifications et renvoie NOTIFY_CANCELED dans le paramètre _lpulFlags_ de la méthode **Notify.**</span><span class="sxs-lookup"><span data-stu-id="e060b-142">If a callback function returns CALLBACK_DISCONTINUE, MAPI stops sending notifications and returns NOTIFY_CANCELED in the **Notify** method's  _lpulFlags_ parameter.</span></span> <span data-ttu-id="e060b-143">Vous pouvez supposer que le processus est inactif et arrêter de générer des notifications pour ce processus.</span><span class="sxs-lookup"><span data-stu-id="e060b-143">You can assume that the process is inactive and stop generating notifications for that process.</span></span> <span data-ttu-id="e060b-144">Si **Notify** renvoie 0 dans  _lpulFlags,_ le processus est toujours actif et vous devez continuer à envoyer des notifications, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="e060b-144">If **Notify** returns 0 in  _lpulFlags_, the process is still active and you should continue to send notifications, as appropriate.</span></span>
  
<span data-ttu-id="e060b-145">Lorsque vous utilisez des notifications synchrones, évitez les blocages.</span><span class="sxs-lookup"><span data-stu-id="e060b-145">When you use synchronous notifications, be careful to avoid deadlock situations.</span></span>
  
<span data-ttu-id="e060b-146">Pour plus d’informations sur le processus de notification, voir [notification d’événement dans MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="e060b-146">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e060b-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e060b-147">See also</span></span>

- [<span data-ttu-id="e060b-148">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="e060b-148">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)  
- [<span data-ttu-id="e060b-149">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="e060b-149">IMAPISupport::Unsubscribe</span></span>](imapisupport-unsubscribe.md)  
- [<span data-ttu-id="e060b-150">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="e060b-150">NOTIFCALLBACK</span></span>](notifcallback.md) 
- [<span data-ttu-id="e060b-151">Notification</span><span class="sxs-lookup"><span data-stu-id="e060b-151">NOTIFICATION</span></span>](notification.md)  
- [<span data-ttu-id="e060b-152">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="e060b-152">NOTIFKEY</span></span>](notifkey.md)  
- [<span data-ttu-id="e060b-153">Propriété canonique PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="e060b-153">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)  
- [<span data-ttu-id="e060b-154">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e060b-154">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

