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
ms.openlocfilehash: beeca6ba958c38e12fba7dbc2884c81e58bdf3c4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590119"
---
# <a name="imapisupportsubscribe"></a><span data-ttu-id="062fa-103">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="062fa-103">IMAPISupport::Subscribe</span></span>

  
  
<span data-ttu-id="062fa-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="062fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="062fa-105">Enregistre un récepteur de notifications pour recevoir des notifications par le biais de MAPI.</span><span class="sxs-lookup"><span data-stu-id="062fa-105">Registers an advise sink to receive notifications through MAPI.</span></span>
  
```cpp
HRESULT Subscribe(
LPNOTIFKEY lpKey,
ULONG ulEventMask,
ULONG ulFlags,
LPMAPIADVISESINK lpAdviseSink,
ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="062fa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="062fa-106">Parameters</span></span>

 <span data-ttu-id="062fa-107">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="062fa-107">_lpKey_</span></span>
  
> <span data-ttu-id="062fa-108">[in] Pointeur vers une clé de notification qui représente l’objet source de notification.</span><span class="sxs-lookup"><span data-stu-id="062fa-108">[in] A pointer to a notification key that represents the advise source object.</span></span> <span data-ttu-id="062fa-109">Le paramètre _lpKey_ ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="062fa-109">The  _lpKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="062fa-110">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="062fa-110">_ulEventMask_</span></span>
  
> <span data-ttu-id="062fa-111">[in] Un masque des valeurs qui indiquent les types d’événements de notification que l’appelant est intéressée par et doit être inclus dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="062fa-111">[in] A mask of values that indicate the types of notification events that the caller is interested in and should be included in the registration.</span></span> <span data-ttu-id="062fa-112">Les valeurs suivantes sont valides :</span><span class="sxs-lookup"><span data-stu-id="062fa-112">The following values are valid:</span></span>
    
 <span data-ttu-id="062fa-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="062fa-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="062fa-114">Enregistre les notifications sur les erreurs graves, telles que la mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="062fa-114">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
 <span data-ttu-id="062fa-115">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="062fa-115">_fnevExtended_</span></span>
  
> <span data-ttu-id="062fa-116">Fournisseur de magasins registres pour les notifications concernant les événements spécifiques pour le carnet d’adresses ou le message.</span><span class="sxs-lookup"><span data-stu-id="062fa-116">Registers for notifications about events specific to the particular address book or message store provider.</span></span>
    
 <span data-ttu-id="062fa-117">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="062fa-117">_fnevNewMail_</span></span>
  
> <span data-ttu-id="062fa-118">Enregistre les notifications relatives à l’arrivée de nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="062fa-118">Registers for notifications about the arrival of new messages.</span></span> 
    
 <span data-ttu-id="062fa-119">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="062fa-119">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="062fa-120">Enregistre les notifications concernant la création d’un nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="062fa-120">Registers for notifications about the creation of a new object.</span></span>
    
 <span data-ttu-id="062fa-121">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="062fa-121">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="062fa-122">Enregistre les notifications relatives à un objet en cours de copie.</span><span class="sxs-lookup"><span data-stu-id="062fa-122">Registers for notifications about an object being copied.</span></span>
    
 <span data-ttu-id="062fa-123">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="062fa-123">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="062fa-124">Enregistre les notifications relatives à un objet en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="062fa-124">Registers for notifications about an object being deleted.</span></span>
    
 <span data-ttu-id="062fa-125">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="062fa-125">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="062fa-126">Enregistre les notifications relatives à un objet en cours de modification.</span><span class="sxs-lookup"><span data-stu-id="062fa-126">Registers for notifications about an object being modified.</span></span>
    
 <span data-ttu-id="062fa-127">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="062fa-127">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="062fa-128">Enregistre les notifications relatives à un objet en cours de déplacement.</span><span class="sxs-lookup"><span data-stu-id="062fa-128">Registers for notifications about an object being moved.</span></span>
    
 <span data-ttu-id="062fa-129">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="062fa-129">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="062fa-130">Enregistre les notifications relatives à la fin d’une opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="062fa-130">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="062fa-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="062fa-131">_ulFlags_</span></span>
  
> <span data-ttu-id="062fa-132">[in] Masque de bits d’indicateurs qui contrôle la notification se produit.</span><span class="sxs-lookup"><span data-stu-id="062fa-132">[in] A bitmask of flags that controls how notification occurs.</span></span> <span data-ttu-id="062fa-133">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="062fa-133">The following flag can be set:</span></span>
    
<span data-ttu-id="062fa-134">NOTIFY_SYNC</span><span class="sxs-lookup"><span data-stu-id="062fa-134">NOTIFY_SYNC</span></span> 
  
> <span data-ttu-id="062fa-135">Lorsque l’appelant appelle la méthode [IMAPISupport::Notify](imapisupport-notify.md) pour générer des notifications pour ce récepteur de notifications, **notifier** doivent effectuer tous les appels nécessaires pour informer les récepteurs avant de retourner.</span><span class="sxs-lookup"><span data-stu-id="062fa-135">When the caller calls the [IMAPISupport::Notify](imapisupport-notify.md) method to generate notifications for this advise sink, **Notify** should make all necessary calls to advise sinks before returning.</span></span> <span data-ttu-id="062fa-136">Si cet indicateur n’est pas défini, la notification est asynchrone et rappels sont en attente pour les processus qui ont souscrit et démarré lorsque ces processus prendre le contrôle de l’UC.</span><span class="sxs-lookup"><span data-stu-id="062fa-136">If this flag is not set, notification is asynchronous and callbacks are queued to the processes that have subscribed and started when those processes gain control of the CPU.</span></span> 
    
 <span data-ttu-id="062fa-137">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="062fa-137">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="062fa-138">[in] Pointeur vers un objet de réception de notifications.</span><span class="sxs-lookup"><span data-stu-id="062fa-138">[in] A pointer to an advise sink object.</span></span> 
    
 <span data-ttu-id="062fa-139">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="062fa-139">_lpulConnection_</span></span>
  
> <span data-ttu-id="062fa-140">[out] Pointeur vers un numéro de connexion différente de zéro qui représente l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="062fa-140">[out] A pointer to a nonzero connection number that represents the registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="062fa-141">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="062fa-141">Return value</span></span>

<span data-ttu-id="062fa-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="062fa-142">S_OK</span></span> 
  
> <span data-ttu-id="062fa-143">L’inscription de notification a réussi.</span><span class="sxs-lookup"><span data-stu-id="062fa-143">The notification registration was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="062fa-144">Remarques</span><span class="sxs-lookup"><span data-stu-id="062fa-144">Remarks</span></span>

<span data-ttu-id="062fa-145">La méthode **IMAPISupport::Subscribe** est implémentée pour tous les objets de prise en charge de fournisseur de service.</span><span class="sxs-lookup"><span data-stu-id="062fa-145">The **IMAPISupport::Subscribe** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="062fa-146">Fournisseurs de services à partir d’une des méthodes de leur **Advise** permettant de MAPI gérer les notifications d’appel **s’abonner** .</span><span class="sxs-lookup"><span data-stu-id="062fa-146">Service providers call **Subscribe** from one of their **Advise** methods to allow MAPI to manage the notifications.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="062fa-147">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="062fa-147">Notes to callers</span></span>

<span data-ttu-id="062fa-148">Pour utiliser les méthodes de prise en charge MAPI pour les notifications, créez une clé pour la source advise de l’objet sur les notifications doit être généré.</span><span class="sxs-lookup"><span data-stu-id="062fa-148">To use the MAPI support methods for notification, create a key for the advise source the object about which notifications should be generated.</span></span> <span data-ttu-id="062fa-149">La valeur de la clé doit être unique et doit être facilement régénérée chaque modification de l’objet.</span><span class="sxs-lookup"><span data-stu-id="062fa-149">The value of the key must be unique and should be easily regenerated each time the object changes.</span></span> 
  
<span data-ttu-id="062fa-150">MAPI utilise la clé de notification pour rechercher des fonctions de rappel enregistrées par le biais de la fonction [HrAllocAdviseSink](hrallocadvisesink.md) pour la source advise correspondant.</span><span class="sxs-lookup"><span data-stu-id="062fa-150">MAPI uses the notification key to search for any callback functions registered through the [HrAllocAdviseSink](hrallocadvisesink.md) function for the corresponding advise source.</span></span> <span data-ttu-id="062fa-151">Passez cette clé à **IMAPISupport::Notify** chaque fois que vous devez générer une notification pour la source advise correspondante.</span><span class="sxs-lookup"><span data-stu-id="062fa-151">Pass this key to **IMAPISupport::Notify** whenever you need to generate a notification for the corresponding advise source.</span></span> 
  
<span data-ttu-id="062fa-152">L’indicateur NOTIFY_SYNC affecte le fonctionnement des appels ultérieurs à **notifier**.</span><span class="sxs-lookup"><span data-stu-id="062fa-152">The NOTIFY_SYNC flag affects the operation of subsequent calls to **Notify**.</span></span> <span data-ttu-id="062fa-153">Lorsque vous définissez NOTIFY_SYNC, **notifier** ne retourne pas jusqu'à ce qu’il a terminé l’envoi de toutes les notifications nécessaires.</span><span class="sxs-lookup"><span data-stu-id="062fa-153">When you set NOTIFY_SYNC, **Notify** does not return until it has finished sending all of the necessary notifications.</span></span> <span data-ttu-id="062fa-154">Lorsque vous ne définissez pas NOTIFY_SYNC, **notifier** fonctionne de manière asynchrone, renvoyer avant toutes les notifications ont été envoyés.</span><span class="sxs-lookup"><span data-stu-id="062fa-154">When you do not set NOTIFY_SYNC, **Notify** operates asynchronously, possibly returning before all of the notifications have been sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="062fa-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="062fa-155">See also</span></span>



[<span data-ttu-id="062fa-156">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="062fa-156">HrAllocAdviseSink</span></span>](hrallocadvisesink.md)
  
[<span data-ttu-id="062fa-157">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="062fa-157">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="062fa-158">IMAPISupport::Notify</span><span class="sxs-lookup"><span data-stu-id="062fa-158">IMAPISupport::Notify</span></span>](imapisupport-notify.md)
  
[<span data-ttu-id="062fa-159">Notification</span><span class="sxs-lookup"><span data-stu-id="062fa-159">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="062fa-160">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="062fa-160">NOTIFKEY</span></span>](notifkey.md)
  
[<span data-ttu-id="062fa-161">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="062fa-161">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

