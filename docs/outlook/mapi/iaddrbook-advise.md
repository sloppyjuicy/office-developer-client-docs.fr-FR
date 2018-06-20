---
title: IAddrBookAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Advise
api_type:
- COM
ms.assetid: 2def89ed-e4ce-446a-8b80-132d11ae8f8b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8214390af883432d72f608452b8b944417884fd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783620"
---
# <a name="iaddrbookadvise"></a><span data-ttu-id="8f994-103">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="8f994-103">IAddrBook::Advise</span></span>

  
  
<span data-ttu-id="8f994-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8f994-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8f994-105">Enregistre un fournisseur de service ou client pour recevoir des notifications sur les modifications apportées à une ou plusieurs entrées dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="8f994-105">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="8f994-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f994-106">Parameters</span></span>

 <span data-ttu-id="8f994-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="8f994-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="8f994-108">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="8f994-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="8f994-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="8f994-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="8f994-110">[in] Pointeur vers l’identificateur d’entrée du conteneur de carnet d’adresses, messagerie utilisateur ou liste de distribution qui générera une notification en cas de modification du type ou de types décrits dans le paramètre _ulEventMask_ .</span><span class="sxs-lookup"><span data-stu-id="8f994-110">[in] A pointer to the entry identifier of the address book container, messaging user, or distribution list that will generate a notification when a change occurs of the type or types described in the  _ulEventMask_ parameter.</span></span> 
    
 <span data-ttu-id="8f994-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="8f994-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="8f994-112">[in] Un ou plusieurs événements de notification qui inscrit pour la réception de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="8f994-112">[in] One or more notification events that the caller is registering to receive.</span></span> <span data-ttu-id="8f994-113">Chaque événement est associé à une structure de notification spécifique qui contient des informations sur les modifications apportées.</span><span class="sxs-lookup"><span data-stu-id="8f994-113">Each event is associated with a particular notification structure that contains information about the change that occurred.</span></span> <span data-ttu-id="8f994-114">Le tableau suivant répertorie les valeurs valides pour _ulEventMask_ et leurs structures correspondantes.</span><span class="sxs-lookup"><span data-stu-id="8f994-114">The following table lists the valid values for  _ulEventMask_ and their corresponding structures.</span></span> 
    
|<span data-ttu-id="8f994-115">**Événement de notification**</span><span class="sxs-lookup"><span data-stu-id="8f994-115">**Notification event**</span></span>|<span data-ttu-id="8f994-116">**Structure correspondante**</span><span class="sxs-lookup"><span data-stu-id="8f994-116">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8f994-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="8f994-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="8f994-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8f994-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="8f994-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="8f994-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="8f994-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8f994-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="8f994-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="8f994-121">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="8f994-122">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8f994-122">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="8f994-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="8f994-123">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="8f994-124">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8f994-124">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="8f994-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="8f994-125">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="8f994-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8f994-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="8f994-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="8f994-127">**fnevObjectMoved**</span></span> <br/> |[<span data-ttu-id="8f994-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8f994-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="8f994-129">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="8f994-129">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="8f994-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8f994-130">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
   
 <span data-ttu-id="8f994-131">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="8f994-131">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="8f994-132">[in] Pointeur vers l’objet de récepteur advise à appeler lorsque l’événement pour lequel la notification a été demandée.</span><span class="sxs-lookup"><span data-stu-id="8f994-132">[in] A pointer to the advise sink object to be called when the event for which notification has been requested occurs.</span></span>
    
 <span data-ttu-id="8f994-133">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="8f994-133">_lpulConnection_</span></span>
  
> <span data-ttu-id="8f994-134">[out] Pointeur vers un numéro de connexion différente de zéro qui représente l’enregistrement de notification.</span><span class="sxs-lookup"><span data-stu-id="8f994-134">[out] A pointer to a nonzero connection number that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8f994-135">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="8f994-135">Return value</span></span>

<span data-ttu-id="8f994-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="8f994-136">S_OK</span></span> 
  
> <span data-ttu-id="8f994-137">L’inscription de notification a réussi.</span><span class="sxs-lookup"><span data-stu-id="8f994-137">The notification registration was successful.</span></span>
    
<span data-ttu-id="8f994-138">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="8f994-138">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="8f994-139">Le fournisseur de carnet d’adresses responsable de l’identificateur d’entrée passé _lpEntryID_ n’a pas pu enregistrer une notification de l’entrée correspondante.</span><span class="sxs-lookup"><span data-stu-id="8f994-139">The address book provider responsible for the entry identifier passed in  _lpEntryID_ could not register a notification for the corresponding entry.</span></span> 
    
<span data-ttu-id="8f994-140">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="8f994-140">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="8f994-141">Notification n’est pas pris en charge par le fournisseur de carnet d’adresses responsable de l’objet identifié par l’identificateur d’entrée passé dans le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="8f994-141">Notification is not supported by the address book provider responsible for the object identified by the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="8f994-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="8f994-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="8f994-143">L’identificateur d’entrée passé _lpEntryID_ ne peuvent pas être géré par des fournisseurs du carnet d’adresses dans le profil.</span><span class="sxs-lookup"><span data-stu-id="8f994-143">The entry identifier passed in  _lpEntryID_ cannot be handled by any of the address book providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8f994-144">Remarques</span><span class="sxs-lookup"><span data-stu-id="8f994-144">Remarks</span></span>

<span data-ttu-id="8f994-145">Clients et fournisseurs de services appellent la méthode **Advise** pour inscrire pour un type particulier ou les types de notification sur une entrée de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="8f994-145">Clients and service providers call the **Advise** method to register for a particular type or types of notification on an address book entry.</span></span> <span data-ttu-id="8f994-146">Les types de notification sont indiqués par le masque d’événement passé avec le paramètre _ulEventMask_ .</span><span class="sxs-lookup"><span data-stu-id="8f994-146">The types of notification are indicated by the event mask passed in with the  _ulEventMask_ parameter.</span></span> 
  
<span data-ttu-id="8f994-147">MAPI transfère cet appel **Advise** pour le fournisseur de carnet d’adresses qui est responsable de l’entrée telle qu’indiquée par l’identificateur d’entrée dans le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="8f994-147">MAPI forwards this **Advise** call to the address book provider that is responsible for the entry as indicated by the entry identifier in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="8f994-148">Le fournisseur de carnet d’adresses gère l’inscription proprement dite ou appelle la méthode de prise en charge, [IMAPISupport::Subscribe](imapisupport-subscribe.md), pour demander MAPI pour inscrire l’appelant.</span><span class="sxs-lookup"><span data-stu-id="8f994-148">The address book provider either handles the registration itself or calls the support method, [IMAPISupport::Subscribe](imapisupport-subscribe.md), to prompt MAPI to register the caller.</span></span> <span data-ttu-id="8f994-149">Un numéro de connexion différente de zéro est renvoyé pour représenter l’inscription réussie.</span><span class="sxs-lookup"><span data-stu-id="8f994-149">A nonzero connection number is returned to represent the successful registration.</span></span>
  
<span data-ttu-id="8f994-150">Chaque fois qu’une modification est apportée à l’entrée du type indiqué par l’inscription de notification, le fournisseur de carnet d’adresses appelle la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pour l’objet de récepteur advise spécifié dans le paramètre _lpAdviseSink_ .</span><span class="sxs-lookup"><span data-stu-id="8f994-150">Whenever a change occurs to the entry of the type indicated by the notification registration, the address book provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object specified in the  _lpAdviseSink_ parameter.</span></span> <span data-ttu-id="8f994-151">La méthode **OnNotify** inclut une structure [NOTIFICATION](notification.md) comme paramètre d’entrée qui contient des données pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="8f994-151">The **OnNotify** method includes a [NOTIFICATION](notification.md) structure as an input parameter that contains data to describe the event.</span></span> 
  
<span data-ttu-id="8f994-152">Selon le fournisseur de carnet d’adresses, l’appel de **OnNotify** peut se produire immédiatement après la modification de l’objet inscrit ou à une date ultérieure.</span><span class="sxs-lookup"><span data-stu-id="8f994-152">Depending on the address book provider, the call to **OnNotify** can occur immediately following the change to the registered object or at a later time.</span></span> <span data-ttu-id="8f994-153">Sur les systèmes qui prennent en charge plusieurs threads d’exécution, l’appel de **OnNotify** peut se produire sur n’importe quel thread.</span><span class="sxs-lookup"><span data-stu-id="8f994-153">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="8f994-154">Les clients peuvent demander que ces notifications se produisent sur un thread particulier en appelant la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) pour créer l’objet récepteur advise qui est transmis à **Advise**.</span><span class="sxs-lookup"><span data-stu-id="8f994-154">Clients can request that these notifications occur on a particular thread by calling the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to create the advise sink object that is passed to **Advise**.</span></span> 
  
<span data-ttu-id="8f994-155">Car un fournisseur de carnet d’adresses peut libérer l’objet de récepteur advise passé par les clients à tout moment après l’exécution réussie de **notification** d’appel et avant une [IAddrBook::Unadvise](iaddrbook-unadvise.md) pour annuler la notification d’appel, les clients doivent version leurs objets récepteur advise **Advise** retourne.</span><span class="sxs-lookup"><span data-stu-id="8f994-155">Because an address book provider can release the advise sink object passed in by clients at any time after the successful completion of the **Advise** call and before an [IAddrBook::Unadvise](iaddrbook-unadvise.md) call to cancel the notification, clients should release their advise sink objects when **Advise** returns.</span></span> 
  
<span data-ttu-id="8f994-156">Pour plus d’informations sur le processus de notification, reportez-vous à la section [Notification d’événement MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="8f994-156">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8f994-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f994-157">See also</span></span>



[<span data-ttu-id="8f994-158">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="8f994-158">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="8f994-159">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="8f994-159">IAddrBook::Unadvise</span></span>](iaddrbook-unadvise.md)
  
[<span data-ttu-id="8f994-160">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="8f994-160">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="8f994-161">Notification</span><span class="sxs-lookup"><span data-stu-id="8f994-161">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="8f994-162">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8f994-162">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

