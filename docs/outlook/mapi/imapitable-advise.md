---
title: IMAPITableAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Advise
api_type:
- COM
ms.assetid: e8b5d21e-dc14-4b61-96b3-a51bcfa0d232
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c9401c163c74ab303ec39c147e0432d1979426b8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418812"
---
# <a name="imapitableadvise"></a><span data-ttu-id="e239a-103">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="e239a-103">IMAPITable::Advise</span></span>

  
  
<span data-ttu-id="e239a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e239a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e239a-105">Inscrit un objet de récepteur de notifications pour recevoir des notifications d'événements spécifiés affectant la table.</span><span class="sxs-lookup"><span data-stu-id="e239a-105">Registers an advise sink object to receive notification of specified events affecting the table.</span></span>
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="e239a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e239a-106">Parameters</span></span>

 <span data-ttu-id="e239a-107">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="e239a-107">_ulEventMask_</span></span>
  
> <span data-ttu-id="e239a-108">dans Valeur indiquant le type d'événement qui générera la notification.</span><span class="sxs-lookup"><span data-stu-id="e239a-108">[in] Value indicating the type of event that will generate the notification.</span></span> <span data-ttu-id="e239a-109">Seule la valeur suivante est valide:</span><span class="sxs-lookup"><span data-stu-id="e239a-109">Only the following value is valid:</span></span>
    
 `fnevTableModified`
  
 <span data-ttu-id="e239a-110">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="e239a-110">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="e239a-111">dans Pointeur vers un objet de récepteur de notification pour recevoir les notifications suivantes.</span><span class="sxs-lookup"><span data-stu-id="e239a-111">[in] Pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="e239a-112">Cet objet de récepteur de notifications doit déjà avoir été alloué.</span><span class="sxs-lookup"><span data-stu-id="e239a-112">This advise sink object must have been already allocated.</span></span>
    
 <span data-ttu-id="e239a-113">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="e239a-113">_lpulConnection_</span></span>
  
> <span data-ttu-id="e239a-114">remarquer Pointeur vers une valeur différente de zéro qui représente l'enregistrement de notification réussi.</span><span class="sxs-lookup"><span data-stu-id="e239a-114">[out] Pointer to a nonzero value that represents the successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e239a-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e239a-115">Return value</span></span>

<span data-ttu-id="e239a-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="e239a-116">S_OK</span></span> 
  
> <span data-ttu-id="e239a-117">L'enregistrement des notifications est terminé.</span><span class="sxs-lookup"><span data-stu-id="e239a-117">The notification registration successfully completed.</span></span>
    
<span data-ttu-id="e239a-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="e239a-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="e239a-119">L'implémentation du tableau ne prend pas en charge les modifications apportées à ses lignes et colonnes, ou ne prend pas en charge la notification.</span><span class="sxs-lookup"><span data-stu-id="e239a-119">The table implementation either does not support changes to its rows and columns or does not support notification.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e239a-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="e239a-120">Remarks</span></span>

<span data-ttu-id="e239a-121">Utilisez la méthode **IMAPITable:: Advise** pour inscrire un objet table implémenté dans le fournisseur pour les rappels de notification.</span><span class="sxs-lookup"><span data-stu-id="e239a-121">Use the **IMAPITable::Advise** method to register a table object implemented in the provider for notification callbacks.</span></span> <span data-ttu-id="e239a-122">Chaque fois qu'une modification est apportée à l'objet table, le fournisseur vérifie le bit de masque d'événement qui a été défini dans le paramètre _ulEventMask_ et, par conséquent, le type de modification qui a eu lieu.</span><span class="sxs-lookup"><span data-stu-id="e239a-122">Whenever a change occurs to the table object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and thus what type of change occurred.</span></span> <span data-ttu-id="e239a-123">Si un bit est défini, le fournisseur appelle la méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) pour l'objet de récepteur de notifications indiqué par le paramètre _lpAdviseSink_ pour signaler l'événement.</span><span class="sxs-lookup"><span data-stu-id="e239a-123">If a bit is set, then the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="e239a-124">Les données transmises dans la structure de notification à la routine **OnNotify** décrivent l'événement.</span><span class="sxs-lookup"><span data-stu-id="e239a-124">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="e239a-125">L'appel à **OnNotify** peut se produire pendant l'appel qui modifie l'objet ou à tout moment suivant.</span><span class="sxs-lookup"><span data-stu-id="e239a-125">The call to **OnNotify** can occur during the call that changes the object, or at any following time.</span></span> <span data-ttu-id="e239a-126">Sur les systèmes qui prennent en charge plusieurs threads d'exécution, l'appel à **OnNotify** peut se produire sur n'importe quel thread.</span><span class="sxs-lookup"><span data-stu-id="e239a-126">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="e239a-127">Pour un moyen d'activer un appel vers **OnNotify** qui peut se produire à un moment inopportun en un seul à gérer, un fournisseur doit utiliser la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="e239a-127">For a way to turn a call to **OnNotify** that might happen at an inopportune time into one that is safer to handle, a provider should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="e239a-128">Pour fournir des notifications, le fournisseur qui met en œuvre l' **avis** doit conserver une copie du pointeur vers l'objet récepteur _lpAdviseSink_ . pour ce faire, il appelle la méthode **IUnknown:: AddRef** pour le récepteur de notifications afin de maintenir son pointeur d'objet jusqu'à ce que l'enregistrement de notification soit annulé avec un appel à la méthode [IMAPITable::](imapitable-unadvise.md) Unadvise.</span><span class="sxs-lookup"><span data-stu-id="e239a-128">To provide notifications, the provider implementing **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, it calls the **IUnknown::AddRef** method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMAPITable::Unadvise](imapitable-unadvise.md) method.</span></span> <span data-ttu-id="e239a-129">L'implémentation de l' **avis** doit affecter un numéro de connexion à l'enregistrement des notifications et appeler **AddRef** sur ce numéro de connexion avant de le renvoyer dans le paramètre _lpulConnection_ .</span><span class="sxs-lookup"><span data-stu-id="e239a-129">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="e239a-130">Les fournisseurs de services peuvent libérer l'objet récepteur de notification avant l'annulation de l'inscription, mais ils ne doivent pas libérer le numéro de connexion tant que l'appel à \* \* Unadvise \* \* n'a pas été appelé.</span><span class="sxs-lookup"><span data-stu-id="e239a-130">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until \*\* Unadvise \*\* has been called.</span></span> 
  
<span data-ttu-id="e239a-131">Une fois qu'un \*\*\*\* appel à Advise a réussi et avant que \* \* Unadvise \* \* ait été appelé, les clients doivent être préparés pour que l'objet de récepteur de notifications soit publié.</span><span class="sxs-lookup"><span data-stu-id="e239a-131">After a call to **Advise** has succeeded and before \*\* Unadvise \*\* has been called, clients must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="e239a-132">Un client doit donc libérer son objet de récepteur d' \*\*\*\* AVERTISSEMENT une fois qu'il a été renvoyé, sauf s'il a une utilisation à long terme spécifique pour lui.</span><span class="sxs-lookup"><span data-stu-id="e239a-132">A client should therefore release its advise sink object after **Advise** returns unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="e239a-133">En raison du comportement asynchrone de la notification, les implémentations qui modifient les paramètres de colonne de tableau peuvent recevoir des notifications avec des informations organisées dans un ordre de colonne précédent.</span><span class="sxs-lookup"><span data-stu-id="e239a-133">Because of the asynchronous behavior of notification, implementations that change table column settings can receive notifications with information organized in a previous column order.</span></span> <span data-ttu-id="e239a-134">Par exemple, une ligne de tableau peut être renvoyée pour un message qui vient d'être supprimé du conteneur.</span><span class="sxs-lookup"><span data-stu-id="e239a-134">For instance, a table row might be returned for a message that has just been deleted from the container.</span></span> <span data-ttu-id="e239a-135">Une telle notification est envoyée lorsque le paramètre de colonne a été modifié et que les informations relatives à ce dernier sont envoyées, mais que la vue de table de notification n'a pas encore été mise à jour avec ces informations.</span><span class="sxs-lookup"><span data-stu-id="e239a-135">Such a notification is sent when the column setting change has been made and information about it sent but the notification table view has not been updated with that information yet.</span></span>
  
<span data-ttu-id="e239a-136">Pour plus d'informations sur le processus de notification, consultez la rubrique [notifications d'événements dans MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="e239a-136">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="e239a-137">Pour obtenir des informations spécifiques sur la notification de table, consultez la rubrique [à propos des notifications de table](about-table-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="e239a-137">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="e239a-138">Pour plus d'informations sur l'utilisation des méthodes **IMAPISupport** pour prendre en charge la notification, consultez la rubrique [prise en](supporting-event-notification.md)charge des notifications d'événements.</span><span class="sxs-lookup"><span data-stu-id="e239a-138">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e239a-139">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e239a-139">MFCMAPI reference</span></span>

<span data-ttu-id="e239a-140">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e239a-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e239a-141">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="e239a-141">**File**</span></span>|<span data-ttu-id="e239a-142">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="e239a-142">**Function**</span></span>|<span data-ttu-id="e239a-143">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="e239a-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e239a-144">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="e239a-144">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="e239a-145">CContestTableListCtrl:: NotificationOn</span><span class="sxs-lookup"><span data-stu-id="e239a-145">CContestTableListCtrl::NotificationOn</span></span>  <br/> |<span data-ttu-id="e239a-146">MFCMAPI utilise la méthode **IMAPITable:: Advise** pour enregistrer les notifications afin d'autoriser la vue de la table à rester en cours.</span><span class="sxs-lookup"><span data-stu-id="e239a-146">MFCMAPI uses the **IMAPITable::Advise** method to register for notifications to allow the table view to stay current.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e239a-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e239a-147">See also</span></span>



[<span data-ttu-id="e239a-148">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="e239a-148">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="e239a-149">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="e239a-149">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="e239a-150">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="e239a-150">IMAPITable::Unadvise</span></span>](imapitable-unadvise.md)
  
[<span data-ttu-id="e239a-151">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e239a-151">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="e239a-152">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e239a-152">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="e239a-153">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="e239a-153">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

