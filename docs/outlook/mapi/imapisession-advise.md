---
title: IMAPISessionAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Advise
api_type:
- COM
ms.assetid: a6a6b6b1-31e2-4899-a5fe-74d5d1c2ccfc
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d5d87d7be9cb3524445107e975a298d4afd5bf98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419834"
---
# <a name="imapisessionadvise"></a><span data-ttu-id="e6868-103">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="e6868-103">IMAPISession::Advise</span></span>

  
  
<span data-ttu-id="e6868-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6868-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6868-105">S'inscrit pour recevoir des notifications d'événements spécifiques affectant la session.</span><span class="sxs-lookup"><span data-stu-id="e6868-105">Registers to receive notification of specified events that affect the session.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="e6868-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6868-106">Parameters</span></span>

 <span data-ttu-id="e6868-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="e6868-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="e6868-108">dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="e6868-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="e6868-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="e6868-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="e6868-110">dans Pointeur vers l'identificateur d'entrée du carnet d'adresses ou de l'objet de banque de messages sur les notifications à générer, ou valeur NULL, qui indique que le client s'inscrit pour recevoir des notifications sur les événements qui affectent uniquement la session.</span><span class="sxs-lookup"><span data-stu-id="e6868-110">[in] A pointer to the entry identifier of the address book or message store object about which notifications should be generated, or NULL, which indicates that the client is registering to receive notifications about events that affect only the session.</span></span> 
    
 <span data-ttu-id="e6868-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="e6868-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="e6868-112">dans Masque de valeurs qui indiquent les types d'événements de notification qui intéressent le client et qui doivent être inclus dans l'inscription.</span><span class="sxs-lookup"><span data-stu-id="e6868-112">[in] A mask of values that indicate the types of notification events that the client is interested in and should be included in the registration.</span></span> <span data-ttu-id="e6868-113">Si _lpEntryID_ est null, MAPI inscrit automatiquement le client pour les événements d'erreur critique qui affectent uniquement la session.</span><span class="sxs-lookup"><span data-stu-id="e6868-113">If  _lpEntryID_ is NULL, MAPI automatically registers the client for critical error events that affect only the session.</span></span> <span data-ttu-id="e6868-114">Lorsque _lpEntryID_ pointe vers un identificateur d'entrée, les valeurs suivantes sont valides pour le paramètre _ulEventMask_ :</span><span class="sxs-lookup"><span data-stu-id="e6868-114">When  _lpEntryID_ points to an entry identifier, the following values are valid for the  _ulEventMask_ parameter:</span></span> 
    
<span data-ttu-id="e6868-115">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="e6868-115">fnevCriticalError</span></span> 
  
> <span data-ttu-id="e6868-116">Enregistre les notifications concernant les erreurs graves, telles que la mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="e6868-116">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
<span data-ttu-id="e6868-117">fnevExtended</span><span class="sxs-lookup"><span data-stu-id="e6868-117">fnevExtended</span></span> 
  
> <span data-ttu-id="e6868-118">S'inscrit pour les notifications concernant des événements spécifiques à un carnet d'adresses ou un fournisseur de banque de messages particulier et sur la fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="e6868-118">Registers for notifications about events specific to a particular address book or message store provider and about session shut down.</span></span>
    
<span data-ttu-id="e6868-119">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="e6868-119">fnevNewMail</span></span> 
  
> <span data-ttu-id="e6868-120">Enregistre les notifications relatives à l'arrivée de nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="e6868-120">Registers for notifications about the arrival of new messages.</span></span> 
    
<span data-ttu-id="e6868-121">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="e6868-121">fnevObjectCreated</span></span> 
  
> <span data-ttu-id="e6868-122">Enregistre les notifications relatives à la création d'un nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="e6868-122">Registers for notifications about the creation of a new object.</span></span>
    
<span data-ttu-id="e6868-123">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="e6868-123">fnevObjectCopied</span></span>
  
> <span data-ttu-id="e6868-124">Enregistre les notifications relatives à un objet en cours de copie.</span><span class="sxs-lookup"><span data-stu-id="e6868-124">Registers for notifications about an object being copied.</span></span>
    
<span data-ttu-id="e6868-125">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="e6868-125">fnevObjectDeleted</span></span>
  
> <span data-ttu-id="e6868-126">Enregistre les notifications relatives à la suppression d'un objet.</span><span class="sxs-lookup"><span data-stu-id="e6868-126">Registers for notifications about an object being deleted.</span></span>
    
<span data-ttu-id="e6868-127">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="e6868-127">fnevObjectModified</span></span>
  
> <span data-ttu-id="e6868-128">Enregistre les notifications relatives à un objet modifié.</span><span class="sxs-lookup"><span data-stu-id="e6868-128">Registers for notifications about an object being modified.</span></span>
    
<span data-ttu-id="e6868-129">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="e6868-129">fnevObjectMoved</span></span>
  
> <span data-ttu-id="e6868-130">Enregistre les notifications relatives à un objet déplacé.</span><span class="sxs-lookup"><span data-stu-id="e6868-130">Registers for notifications about an object being moved.</span></span>
    
<span data-ttu-id="e6868-131">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="e6868-131">fnevSearchComplete</span></span>
  
> <span data-ttu-id="e6868-132">Enregistre les notifications relatives à l'exécution d'une opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="e6868-132">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="e6868-133">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="e6868-133">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="e6868-134">dans Pointeur vers un objet de récepteur de notification pour recevoir les notifications suivantes.</span><span class="sxs-lookup"><span data-stu-id="e6868-134">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="e6868-135">Cet objet de récepteur de notifications doit déjà avoir été alloué.</span><span class="sxs-lookup"><span data-stu-id="e6868-135">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="e6868-136">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="e6868-136">_lpulConnection_</span></span>
  
> <span data-ttu-id="e6868-137">remarquer Pointeur vers un nombre différent de zéro qui représente la connexion entre l'objet de récepteur d'avertissement de l'appelant et la session.</span><span class="sxs-lookup"><span data-stu-id="e6868-137">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e6868-138">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e6868-138">Return value</span></span>

<span data-ttu-id="e6868-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="e6868-139">S_OK</span></span> 
  
> <span data-ttu-id="e6868-140">L'inscription a réussi.</span><span class="sxs-lookup"><span data-stu-id="e6868-140">The registration was successful.</span></span>
    
<span data-ttu-id="e6868-141">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e6868-141">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="e6868-142">L'identificateur d'entrée pointé par _lpEntryID_ ne représente pas un identificateur d'entrée valide.</span><span class="sxs-lookup"><span data-stu-id="e6868-142">The entry identifier pointed to by  _lpEntryID_ does not represent a valid entry identifier.</span></span> 
    
<span data-ttu-id="e6868-143">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="e6868-143">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="e6868-144">Le fournisseur de services responsable de l'identificateur d'entrée désigné par _lpEntryID_ ne prend pas en charge le type d'événements spécifiés dans le paramètre _ulEventMask_ ou ne prend pas en charge la notification.</span><span class="sxs-lookup"><span data-stu-id="e6868-144">The service provider responsible for the entry identifier pointed to by  _lpEntryID_ either does not support the type of events specified in the  _ulEventMask_ parameter or does not support notification.</span></span> 
    
<span data-ttu-id="e6868-145">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e6868-145">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="e6868-146">L'identificateur d'entrée pointé par _lpEntryID_ ne peut pas être géré par les fournisseurs de services dans le profil.</span><span class="sxs-lookup"><span data-stu-id="e6868-146">The entry identifier pointed to by  _lpEntryID_ cannot be handled by any of the service providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e6868-147">Remarques</span><span class="sxs-lookup"><span data-stu-id="e6868-147">Remarks</span></span>

<span data-ttu-id="e6868-148">La méthode **IMAPISession:: Advise** établit une connexion entre l'objet récepteur de notification de l'appelant, la session et, éventuellement, un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="e6868-148">The **IMAPISession::Advise** method establishes a connection between the caller's advise sink object, the session and, optionally, a service provider.</span></span> <span data-ttu-id="e6868-149">Cette connexion est utilisée pour envoyer des notifications au récepteur de notifications lorsqu'un ou plusieurs événements spécifiés dans le paramètre _ulEventMask_ se produisent dans l'objet désigné par _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="e6868-149">This connection is used to send notifications to the advise sink when one or more events specified in the  _ulEventMask_ parameter occur to the object pointed to by  _lpEntryID_.</span></span> <span data-ttu-id="e6868-150">Lorsque _lpEntryID_ est null, l'objet cible est la session et les notifications sont envoyées uniquement pour les erreurs critiques et les événements étendus.</span><span class="sxs-lookup"><span data-stu-id="e6868-150">When  _lpEntryID_ is NULL, the target object is the session and notifications are sent only for critical errors and extended events.</span></span> 
  
<span data-ttu-id="e6868-151">Lorsque _lpEntryID_ pointe vers un identificateur d'entrée valide, MAPI appelle la \*\*\*\* méthode Advise de l'objet Logon qui appartient au fournisseur de services responsable.</span><span class="sxs-lookup"><span data-stu-id="e6868-151">When  _lpEntryID_ points to a valid entry identifier, MAPI calls the **Advise** method of the logon object that belongs to the responsible service provider.</span></span> <span data-ttu-id="e6868-152">Par exemple, si _lpEntryID_ pointe sur l'identificateur d'entrée d'une liste de distribution, MAPI appelle la méthode [IABLogon:: Advise](iablogon-advise.md) du fournisseur de carnet d'adresses approprié.</span><span class="sxs-lookup"><span data-stu-id="e6868-152">For example, if  _lpEntryID_ points to the entry identifier of a distribution list, MAPI calls the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="e6868-153">Pour envoyer une notification, le fournisseur de services ou MAPI appelle la méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) du récepteur de notification enregistré.</span><span class="sxs-lookup"><span data-stu-id="e6868-153">To send a notification, either the service provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="e6868-154">L'un des paramètres de **OnNotify**, une structure de notification, contient des informations qui décrivent l'événement spécifique.</span><span class="sxs-lookup"><span data-stu-id="e6868-154">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="e6868-155">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="e6868-155">Notes to callers</span></span>

<span data-ttu-id="e6868-156">Sur les systèmes qui prennent en charge plusieurs threads d'exécution, l'appel à **OnNotify** peut également se produire sur n'importe quel thread à tout moment.</span><span class="sxs-lookup"><span data-stu-id="e6868-156">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="e6868-157">Si vous avez besoin d'assurance que les notifications ne se produiront qu'à un moment donné sur un thread particulier, appelez la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) pour générer l'objet de récepteur de notifications que vous transmettez à la méthode Advise. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e6868-157">If you need assurance that notifications will occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to the **Advise** method.</span></span> 
  
<span data-ttu-id="e6868-158">Pour déterminer quand un client a fermé une session, inscrivez-vous aux notifications dans votre \*\*\*\* fournisseur de services en appelant Advise avec _LPENTRYID_ défini sur null et _cbEntryID_ défini sur 0.</span><span class="sxs-lookup"><span data-stu-id="e6868-158">To determine when a client has logged off, register for notifications in your service provider by calling **Advise** with  _lpEntryID_ set to NULL and  _cbEntryID_ set to 0.</span></span> <span data-ttu-id="e6868-159">Lorsque la déconnexion se produit, vous recevez une notification fnevExtended.</span><span class="sxs-lookup"><span data-stu-id="e6868-159">When the logoff occurs, you will receive an fnevExtended notification.</span></span> 
  
<span data-ttu-id="e6868-160">Une fois qu'un \*\*\*\* appel à Advise a réussi et avant [IMAPISession::](imapisession-unadvise.md) Unadvise a été appelé pour annuler l'inscription, libérer votre objet de récepteur de Conseil, sauf si vous disposez d'une utilisation de longue durée spécifique.</span><span class="sxs-lookup"><span data-stu-id="e6868-160">After a call to **Advise** has succeeded and before [IMAPISession::Unadvise](imapisession-unadvise.md) has been called to cancel the registration, release your advise sink object unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="e6868-161">Pour obtenir une vue d'ensemble du processus de notification, consultez la rubrique notifications d' [événements dans MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="e6868-161">For an overview of the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="e6868-162">Pour plus d'informations sur la gestion des notifications, consultez la rubrique [gestion](handling-notifications.md)des notifications.</span><span class="sxs-lookup"><span data-stu-id="e6868-162">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e6868-163">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e6868-163">MFCMAPI reference</span></span>

<span data-ttu-id="e6868-164">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e6868-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e6868-165">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="e6868-165">**File**</span></span>|<span data-ttu-id="e6868-166">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="e6868-166">**Function**</span></span>|<span data-ttu-id="e6868-167">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="e6868-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e6868-168">BaseDialog. cpp</span><span class="sxs-lookup"><span data-stu-id="e6868-168">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="e6868-169">CBaseDialog:: OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="e6868-169">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="e6868-170">MFCMAPI utilise la méthode **IMAPISession:: Advise** pour s'inscrire aux notifications par rapport à la session.</span><span class="sxs-lookup"><span data-stu-id="e6868-170">MFCMAPI uses the **IMAPISession::Advise** method to register for notifications against the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e6868-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6868-171">See also</span></span>



[<span data-ttu-id="e6868-172">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="e6868-172">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="e6868-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="e6868-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="e6868-174">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="e6868-174">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="e6868-175">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="e6868-175">IMAPISession::Unadvise</span></span>](imapisession-unadvise.md)
  
[<span data-ttu-id="e6868-176">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e6868-176">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="e6868-177">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="e6868-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="e6868-178">Notification d'événement dans MAPI</span><span class="sxs-lookup"><span data-stu-id="e6868-178">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)

