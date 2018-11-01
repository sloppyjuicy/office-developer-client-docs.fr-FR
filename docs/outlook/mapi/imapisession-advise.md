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
ms.openlocfilehash: 704a556b97f5fd90989641a17afe5a11d127e51b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577169"
---
# <a name="imapisessionadvise"></a><span data-ttu-id="38678-103">IMAPISession::Advise</span><span class="sxs-lookup"><span data-stu-id="38678-103">IMAPISession::Advise</span></span>

  
  
<span data-ttu-id="38678-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38678-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38678-105">Inscrit pour recevoir des notifications d’événements spécifiques qui affectent la session.</span><span class="sxs-lookup"><span data-stu-id="38678-105">Registers to receive notification of specified events that affect the session.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="38678-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38678-106">Parameters</span></span>

 <span data-ttu-id="38678-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="38678-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="38678-108">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="38678-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="38678-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="38678-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="38678-110">[in] Pointeur vers l’identificateur d’entrée du carnet d’adresses objet de banque de messages sur les notifications doivent être générées ou valeur NULL, ce qui indique que le client s’inscrit pour recevoir des notifications concernant les événements qui affectent uniquement la session.</span><span class="sxs-lookup"><span data-stu-id="38678-110">[in] A pointer to the entry identifier of the address book or message store object about which notifications should be generated, or NULL, which indicates that the client is registering to receive notifications about events that affect only the session.</span></span> 
    
 <span data-ttu-id="38678-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="38678-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="38678-112">[in] Un masque des valeurs qui indiquent les types d’événements de notification que le client s’intéresse et doit être inclus dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="38678-112">[in] A mask of values that indicate the types of notification events that the client is interested in and should be included in the registration.</span></span> <span data-ttu-id="38678-113">Si _lpEntryID_ est NULL, MAPI enregistre automatiquement le client pour les événements d’erreur critique qui affectent uniquement la session.</span><span class="sxs-lookup"><span data-stu-id="38678-113">If  _lpEntryID_ is NULL, MAPI automatically registers the client for critical error events that affect only the session.</span></span> <span data-ttu-id="38678-114">Lorsque _lpEntryID_ pointe vers un identificateur d’entrée, les valeurs suivantes sont valides pour le paramètre _ulEventMask_ :</span><span class="sxs-lookup"><span data-stu-id="38678-114">When  _lpEntryID_ points to an entry identifier, the following values are valid for the  _ulEventMask_ parameter:</span></span> 
    
<span data-ttu-id="38678-115">fnevCriticalError</span><span class="sxs-lookup"><span data-stu-id="38678-115">fnevCriticalError</span></span> 
  
> <span data-ttu-id="38678-116">Enregistre les notifications sur les erreurs graves, telles que la mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="38678-116">Registers for notifications about severe errors, such as insufficient memory.</span></span>
    
<span data-ttu-id="38678-117">fnevExtended</span><span class="sxs-lookup"><span data-stu-id="38678-117">fnevExtended</span></span> 
  
> <span data-ttu-id="38678-118">Registres notifications concernant les événements spécifiques à un carnet d’adresses ou un message de fournisseur de magasins et sur la session arrêté.</span><span class="sxs-lookup"><span data-stu-id="38678-118">Registers for notifications about events specific to a particular address book or message store provider and about session shut down.</span></span>
    
<span data-ttu-id="38678-119">fnevNewMail</span><span class="sxs-lookup"><span data-stu-id="38678-119">fnevNewMail</span></span> 
  
> <span data-ttu-id="38678-120">Enregistre les notifications relatives à l’arrivée de nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="38678-120">Registers for notifications about the arrival of new messages.</span></span> 
    
<span data-ttu-id="38678-121">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="38678-121">fnevObjectCreated</span></span> 
  
> <span data-ttu-id="38678-122">Enregistre les notifications concernant la création d’un nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="38678-122">Registers for notifications about the creation of a new object.</span></span>
    
<span data-ttu-id="38678-123">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="38678-123">fnevObjectCopied</span></span>
  
> <span data-ttu-id="38678-124">Enregistre les notifications relatives à un objet en cours de copie.</span><span class="sxs-lookup"><span data-stu-id="38678-124">Registers for notifications about an object being copied.</span></span>
    
<span data-ttu-id="38678-125">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="38678-125">fnevObjectDeleted</span></span>
  
> <span data-ttu-id="38678-126">Enregistre les notifications relatives à un objet en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="38678-126">Registers for notifications about an object being deleted.</span></span>
    
<span data-ttu-id="38678-127">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="38678-127">fnevObjectModified</span></span>
  
> <span data-ttu-id="38678-128">Enregistre les notifications relatives à un objet en cours de modification.</span><span class="sxs-lookup"><span data-stu-id="38678-128">Registers for notifications about an object being modified.</span></span>
    
<span data-ttu-id="38678-129">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="38678-129">fnevObjectMoved</span></span>
  
> <span data-ttu-id="38678-130">Enregistre les notifications relatives à un objet en cours de déplacement.</span><span class="sxs-lookup"><span data-stu-id="38678-130">Registers for notifications about an object being moved.</span></span>
    
<span data-ttu-id="38678-131">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="38678-131">fnevSearchComplete</span></span>
  
> <span data-ttu-id="38678-132">Enregistre les notifications relatives à la fin d’une opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="38678-132">Registers for notifications about the completion of a search operation.</span></span>
    
 <span data-ttu-id="38678-133">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="38678-133">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="38678-134">[in] Pointeur vers un objet de récepteur advise pour recevoir les notifications ultérieures.</span><span class="sxs-lookup"><span data-stu-id="38678-134">[in] A pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="38678-135">Cet objet de récepteur advise doit déjà affectée.</span><span class="sxs-lookup"><span data-stu-id="38678-135">This advise sink object must have already been allocated.</span></span>
    
 <span data-ttu-id="38678-136">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="38678-136">_lpulConnection_</span></span>
  
> <span data-ttu-id="38678-137">[out] Un pointeur vers un nombre différent de zéro qui représente la connexion entre l’appelant de notification objet récepteur et la session.</span><span class="sxs-lookup"><span data-stu-id="38678-137">[out] A pointer to a nonzero number that represents the connection between the caller's advise sink object and the session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="38678-138">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="38678-138">Return value</span></span>

<span data-ttu-id="38678-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="38678-139">S_OK</span></span> 
  
> <span data-ttu-id="38678-140">L’inscription a réussi.</span><span class="sxs-lookup"><span data-stu-id="38678-140">The registration was successful.</span></span>
    
<span data-ttu-id="38678-141">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="38678-141">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="38678-142">L’identificateur d’entrée désigné par _lpEntryID_ ne représente pas un identificateur d’entrée valide.</span><span class="sxs-lookup"><span data-stu-id="38678-142">The entry identifier pointed to by  _lpEntryID_ does not represent a valid entry identifier.</span></span> 
    
<span data-ttu-id="38678-143">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="38678-143">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="38678-144">Le fournisseur de services responsable de l’identificateur d’entrée désigné par _lpEntryID_ ne prend pas en charge le type d’événements spécifié dans le paramètre _ulEventMask_ ou ne prend pas en charge la notification.</span><span class="sxs-lookup"><span data-stu-id="38678-144">The service provider responsible for the entry identifier pointed to by  _lpEntryID_ either does not support the type of events specified in the  _ulEventMask_ parameter or does not support notification.</span></span> 
    
<span data-ttu-id="38678-145">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="38678-145">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="38678-146">L’identificateur d’entrée désigné par _lpEntryID_ ne peut pas être géré par les fournisseurs de services dans le profil.</span><span class="sxs-lookup"><span data-stu-id="38678-146">The entry identifier pointed to by  _lpEntryID_ cannot be handled by any of the service providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="38678-147">Remarques</span><span class="sxs-lookup"><span data-stu-id="38678-147">Remarks</span></span>

<span data-ttu-id="38678-148">La méthode **IMAPISession::Advise** établit une connexion entre l’appelant d’informer l’objet récepteur, la session et, éventuellement, un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="38678-148">The **IMAPISession::Advise** method establishes a connection between the caller's advise sink object, the session and, optionally, a service provider.</span></span> <span data-ttu-id="38678-149">Cette connexion est utilisée pour envoyer des notifications pour le récepteur de notifications lorsqu’un ou plusieurs événements spécifiés dans le paramètre _ulEventMask_ se produisent sur l’objet vers lequel pointé _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="38678-149">This connection is used to send notifications to the advise sink when one or more events specified in the  _ulEventMask_ parameter occur to the object pointed to by  _lpEntryID_.</span></span> <span data-ttu-id="38678-150">Lorsque _lpEntryID_ est NULL, l’objet cible est la session et les notifications sont envoyées uniquement pour les erreurs critiques et les événements étendus.</span><span class="sxs-lookup"><span data-stu-id="38678-150">When  _lpEntryID_ is NULL, the target object is the session and notifications are sent only for critical errors and extended events.</span></span> 
  
<span data-ttu-id="38678-151">Lorsque _lpEntryID_ pointe vers un identificateur d’entrée valide, la méthode **Advise** de l’objet d’ouverture de session qui appartient au fournisseur de services responsable appels MAPI.</span><span class="sxs-lookup"><span data-stu-id="38678-151">When  _lpEntryID_ points to a valid entry identifier, MAPI calls the **Advise** method of the logon object that belongs to the responsible service provider.</span></span> <span data-ttu-id="38678-152">Par exemple, si _lpEntryID_ pointe vers l’identificateur d’entrée d’une liste de distribution, MAPI appelle la méthode de [IABLogon::Advise](iablogon-advise.md) du fournisseur livre adresse appropriée.</span><span class="sxs-lookup"><span data-stu-id="38678-152">For example, if  _lpEntryID_ points to the entry identifier of a distribution list, MAPI calls the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="38678-153">Pour envoyer une notification, le fournisseur de services ou MAPI appelle méthode de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) du récepteur des notifications.</span><span class="sxs-lookup"><span data-stu-id="38678-153">To send a notification, either the service provider or MAPI calls the registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="38678-154">L’un des paramètres à **OnNotify**, une structure de notification, contient des informations décrivant l’événement spécifique.</span><span class="sxs-lookup"><span data-stu-id="38678-154">One of the parameters to **OnNotify**, a notification structure, contains information that describes the specific event.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="38678-155">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="38678-155">Notes to callers</span></span>

<span data-ttu-id="38678-156">Sur les systèmes qui prennent en charge plusieurs threads d’exécution, l’appel de **OnNotify** peut également se produire sur n’importe quel thread à tout moment.</span><span class="sxs-lookup"><span data-stu-id="38678-156">On systems that support multiple threads of execution, the call to **OnNotify** can also occur on any thread at any time.</span></span> <span data-ttu-id="38678-157">Si vous avez besoin pour l’assurance que des notifications seront produit uniquement à un moment donné sur un thread particulier, appelez la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) pour générer l’objet récepteur advise que vous passez à la méthode **Advise** .</span><span class="sxs-lookup"><span data-stu-id="38678-157">If you need assurance that notifications will occur only at a particular time on a particular thread, call the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to generate the advise sink object that you pass to the **Advise** method.</span></span> 
  
<span data-ttu-id="38678-158">Pour déterminer si un client est déconnecté, inscrire pour les notifications dans votre fournisseur de services en appelant **Advise** _lpEntryID_ défini sur NULL et _cbEntryID_ définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="38678-158">To determine when a client has logged off, register for notifications in your service provider by calling **Advise** with  _lpEntryID_ set to NULL and  _cbEntryID_ set to 0.</span></span> <span data-ttu-id="38678-159">Lors de la fermeture de session se produit, vous recevez une notification fnevExtended.</span><span class="sxs-lookup"><span data-stu-id="38678-159">When the logoff occurs, you will receive an fnevExtended notification.</span></span> 
  
<span data-ttu-id="38678-160">Après qu’un appel à **Advise** a réussi et avant [IMAPISession::Unadvise](imapisession-unadvise.md) a été appelé pour annuler l’inscription, mise à jour votre objet de réception de notifications à moins d’avoir une utilisation à long terme spécifique pour qu’il.</span><span class="sxs-lookup"><span data-stu-id="38678-160">After a call to **Advise** has succeeded and before [IMAPISession::Unadvise](imapisession-unadvise.md) has been called to cancel the registration, release your advise sink object unless you have a specific long-term use for it.</span></span> 
  
<span data-ttu-id="38678-161">Pour une vue d’ensemble du processus de notification, voir la [Notification d’événement MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="38678-161">For an overview of the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="38678-162">Pour plus d’informations sur la gestion des notifications, voir [Gestion des Notifications](handling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="38678-162">For more information about handling notifications, see [Handling Notifications](handling-notifications.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="38678-163">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="38678-163">MFCMAPI reference</span></span>

<span data-ttu-id="38678-164">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="38678-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="38678-165">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="38678-165">**File**</span></span>|<span data-ttu-id="38678-166">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="38678-166">**Function**</span></span>|<span data-ttu-id="38678-167">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="38678-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="38678-168">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="38678-168">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="38678-169">CBaseDialog::OnNotificationsOn</span><span class="sxs-lookup"><span data-stu-id="38678-169">CBaseDialog::OnNotificationsOn</span></span>  <br/> |<span data-ttu-id="38678-170">MFCMAPI utilise la méthode **IMAPISession::Advise** pour enregistrer les notifications par rapport à la session.</span><span class="sxs-lookup"><span data-stu-id="38678-170">MFCMAPI uses the **IMAPISession::Advise** method to register for notifications against the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="38678-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38678-171">See also</span></span>



[<span data-ttu-id="38678-172">IABLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="38678-172">IABLogon::Advise</span></span>](iablogon-advise.md)
  
[<span data-ttu-id="38678-173">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="38678-173">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="38678-174">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="38678-174">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="38678-175">IMAPISession::Unadvise</span><span class="sxs-lookup"><span data-stu-id="38678-175">IMAPISession::Unadvise</span></span>](imapisession-unadvise.md)
  
[<span data-ttu-id="38678-176">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="38678-176">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="38678-177">MFCMAPI en tant qu’exemple de code</span><span class="sxs-lookup"><span data-stu-id="38678-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="38678-178">Notification d’événement MAPI</span><span class="sxs-lookup"><span data-stu-id="38678-178">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)

