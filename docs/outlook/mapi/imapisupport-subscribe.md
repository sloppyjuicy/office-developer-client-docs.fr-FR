---
title: IMAPISupportSubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Subscribe
api_type:
- COM
ms.assetid: e6baaff1-446e-431a-a09b-9b529153382b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5a8c288e877078ece6ab2da8c6494d96e1714ad7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419925"
---
# <a name="imapisupportsubscribe"></a><span data-ttu-id="7601e-103">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="7601e-103">IMAPISupport::Subscribe</span></span>

  
  
<span data-ttu-id="7601e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7601e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7601e-105">Inscrit un recevoir de notification pour recevoir des notifications via MAPI.</span><span class="sxs-lookup"><span data-stu-id="7601e-105">Registers an advise sink to receive notifications through MAPI.</span></span>
  
```cpp
HRESULT Subscribe(
LPNOTIFKEY lpKey,
ULONG ulEventMask,
ULONG ulFlags,
LPMAPIADVISESINK lpAdviseSink,
ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="7601e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="7601e-106">Parameters</span></span>

 <span data-ttu-id="7601e-107">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="7601e-107">_lpKey_</span></span>
  
> <span data-ttu-id="7601e-108">[in] Pointeur vers une clé de notification qui représente l’objet source de notification.</span><span class="sxs-lookup"><span data-stu-id="7601e-108">[in] A pointer to a notification key that represents the advise source object.</span></span> <span data-ttu-id="7601e-109">Le  _paramètre lpKey_ ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="7601e-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="7601e-110">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="7601e-110">_ulEventMask_</span></span>
  
> <span data-ttu-id="7601e-111">[in] Masque de valeurs qui indiquent les types d’événements de notification qui intéressent l’appelant et qui doivent être inclus dans l’inscription.</span><span class="sxs-lookup"><span data-stu-id="7601e-111">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="7601e-112">Les valeurs suivantes sont valides :</span><span class="sxs-lookup"><span data-stu-id="7601e-112">The following values are valid:</span></span>
    
 <span data-ttu-id="7601e-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="7601e-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="7601e-114">S’inscrit aux notifications concernant les erreurs graves, telles que la mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="7601e-114">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="7601e-115">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="7601e-115">_fnevExtended_</span></span>
  
> <span data-ttu-id="7601e-116">S’inscrit pour les notifications sur les événements spécifiques au carnet d’adresses ou au fournisseur de magasin de messages particulier.</span><span class="sxs-lookup"><span data-stu-id="7601e-116">Registers for notifications about events specific to the particular address book or message store provider.</span></span>
    
 <span data-ttu-id="7601e-117">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="7601e-117">_fnevNewMail_</span></span>
  
> <span data-ttu-id="7601e-118">S’inscrit aux notifications concernant l’arrivée de nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="7601e-118">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="7601e-119">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="7601e-119">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="7601e-120">S’inscrit aux notifications concernant la création d’un nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="7601e-120">Registers for notifications about the creation of a new object.</span></span>
    
 <span data-ttu-id="7601e-121">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="7601e-121">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="7601e-122">S’inscrit aux notifications concernant un objet en cours de copie.</span><span class="sxs-lookup"><span data-stu-id="7601e-122">Registers for notifications about an object being copied.</span></span>
    
 <span data-ttu-id="7601e-123">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="7601e-123">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="7601e-124">S’inscrit aux notifications concernant un objet en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="7601e-124">Registers for notifications about an object being deleted.</span></span>
    
 <span data-ttu-id="7601e-125">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="7601e-125">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="7601e-126">S’inscrit aux notifications concernant un objet modifié.</span><span class="sxs-lookup"><span data-stu-id="7601e-126">Registers for notifications about an object being modified.</span></span>
    
 <span data-ttu-id="7601e-127">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="7601e-127">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="7601e-128">S’inscrit aux notifications concernant un objet déplacé.</span><span class="sxs-lookup"><span data-stu-id="7601e-128">Registers for notifications about an object being moved.</span></span>
    
 <span data-ttu-id="7601e-129">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="7601e-129">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="7601e-130">S’inscrit aux notifications concernant la fin d’une opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="7601e-130">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="7601e-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7601e-131">_ulFlags_</span></span>
  
> <span data-ttu-id="7601e-132">[in] Masque de bits d’indicateurs qui contrôle le fonctionnement de la notification.</span><span class="sxs-lookup"><span data-stu-id="7601e-132">[in] A bitmask of flags that controls how notification occurs.</span></span> <span data-ttu-id="7601e-133">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="7601e-133">The following flag can be set:</span></span>
    
<span data-ttu-id="7601e-134">NOTIFY_SYNC</span><span class="sxs-lookup"><span data-stu-id="7601e-134">NOTIFY_SYNC</span></span> 
  
> <span data-ttu-id="7601e-135">Lorsque l’appelant appelle la méthode [IMAPISupport::Notify](imapisupport-notify.md) pour générer des notifications pour ce réception de notification, **Notify** doit effectuer tous les appels nécessaires pour avertir les réceptions avant de revenir.</span><span class="sxs-lookup"><span data-stu-id="7601e-135">When the caller calls the [IMAPISupport::Notify](imapisupport-notify.md) method to generate notifications for this advise sink, **Notify** should make all necessary calls to advise sinks before returning.</span></span> <span data-ttu-id="7601e-136">Si cet indicateur n’est pas définie, la notification est asynchrone et les rappels sont mis en file d’attente aux processus abonnés et démarrés lorsque ces processus ont le contrôle de l’UC.</span><span class="sxs-lookup"><span data-stu-id="7601e-136">If this flag is not set, notification is asynchronous and callbacks are queued to the processes that have subscribed and started when those processes gain control of the CPU.</span></span> 
    
 <span data-ttu-id="7601e-137">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="7601e-137">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="7601e-138">[in] Pointeur vers un objet de sink de conseil.</span><span class="sxs-lookup"><span data-stu-id="7601e-138">[in] A pointer to an advise sink object.</span></span> 
    
 <span data-ttu-id="7601e-139">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="7601e-139">_lpulConnection_</span></span>
  
> <span data-ttu-id="7601e-140">[out] Pointeur vers un numéro de connexion autre que zéro qui représente l’inscription.</span><span class="sxs-lookup"><span data-stu-id="7601e-140">[out] A pointer to a nonzero connection number that represents the registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7601e-141">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7601e-141">Return value</span></span>

<span data-ttu-id="7601e-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="7601e-142">S_OK</span></span> 
  
> <span data-ttu-id="7601e-143">L’inscription de la notification a réussi.</span><span class="sxs-lookup"><span data-stu-id="7601e-143">The notification registration was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7601e-144">Remarques</span><span class="sxs-lookup"><span data-stu-id="7601e-144">Remarks</span></span>

<span data-ttu-id="7601e-145">La **méthode IMAPISupport::Subscribe** est implémentée pour tous les objets de support du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="7601e-145">The **IMAPISupport::Subscribe** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="7601e-146">Les fournisseurs de services **appellent Subscribe** à partir de l’une de leurs méthodes **Advise** pour permettre à MAPI de gérer les notifications.</span><span class="sxs-lookup"><span data-stu-id="7601e-146">Service providers call **Subscribe** from one of their **Advise** methods to allow MAPI to manage the notifications.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7601e-147">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="7601e-147">Notes to callers</span></span>

<span data-ttu-id="7601e-148">Pour utiliser les méthodes de prise en charge MAPI pour la notification, créez une clé pour la source de notifications sur l’objet sur lequel les notifications doivent être générées.</span><span class="sxs-lookup"><span data-stu-id="7601e-148">To use the MAPI support methods for notification, create a key for the advise source the object about which notifications should be generated.</span></span> <span data-ttu-id="7601e-149">La valeur de la clé doit être unique et être facilement régénérée chaque fois que l’objet change.</span><span class="sxs-lookup"><span data-stu-id="7601e-149">The value of the key must be unique and should be easily regenerated each time the object changes.</span></span> 
  
<span data-ttu-id="7601e-150">MAPI utilise la clé de notification pour rechercher les fonctions de rappel enregistrées via la fonction [HrAllocAdviseSink](hrallocadvisesink.md) pour la source de notification correspondante.</span><span class="sxs-lookup"><span data-stu-id="7601e-150">MAPI uses the notification key to search for any callback functions registered through the [HrAllocAdviseSink](hrallocadvisesink.md) function for the corresponding advise source.</span></span> <span data-ttu-id="7601e-151">Passez cette clé à **IMAPISupport::Notify** chaque fois que vous devez générer une notification pour la source de notification correspondante.</span><span class="sxs-lookup"><span data-stu-id="7601e-151">Pass this key to **IMAPISupport::Notify** whenever you need to generate a notification for the corresponding advise source.</span></span> 
  
<span data-ttu-id="7601e-152">L NOTIFY_SYNC’indicateur affecte le fonctionnement des appels ultérieurs à **Notify**.</span><span class="sxs-lookup"><span data-stu-id="7601e-152">The NOTIFY_SYNC flag affects the operation of subsequent calls to **Notify**.</span></span> <span data-ttu-id="7601e-153">Lorsque vous définissez NOTIFY_SYNC, **Notify** ne revient pas tant qu’il n’a pas terminé d’envoyer toutes les notifications nécessaires.</span><span class="sxs-lookup"><span data-stu-id="7601e-153">When you set NOTIFY_SYNC, **Notify** does not return until it has finished sending all of the necessary notifications.</span></span> <span data-ttu-id="7601e-154">Lorsque vous ne définissez pas NOTIFY_SYNC, **Notify** fonctionne de manière asynchrone, en renvoyant éventuellement avant que toutes les notifications n’ont été envoyées.</span><span class="sxs-lookup"><span data-stu-id="7601e-154">When you do not set NOTIFY_SYNC, **Notify** operates asynchronously, possibly returning before all of the notifications have been sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7601e-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7601e-155">See also</span></span>



[<span data-ttu-id="7601e-156">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="7601e-156">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="7601e-157">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="7601e-157">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="7601e-158">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="7601e-158">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="7601e-159">Notification</span><span class="sxs-lookup"><span data-stu-id="7601e-159">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="7601e-160">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="7601e-160">NOTIFKEY</span></span>](notifkey.md)
  
[<span data-ttu-id="7601e-161">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7601e-161">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

