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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7abafafd3d4bd9618d85a7dac34e4556545167bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406275"
---
# <a name="iaddrbookadvise"></a><span data-ttu-id="40177-103">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="40177-103">IAddrBook::Advise</span></span>

  
  
<span data-ttu-id="40177-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40177-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40177-105">Enregistre un client ou un fournisseur de services pour recevoir des notifications concernant les modifications apportées à une ou plusieurs entrées dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="40177-105">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="40177-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40177-106">Parameters</span></span>

 <span data-ttu-id="40177-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="40177-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="40177-108">[in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="40177-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="40177-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="40177-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="40177-110">[in] Pointeur vers l’identificateur d’entrée du conteneur de carnet d’adresses, de l’utilisateur de messagerie ou de la liste de distribution qui génère une notification lorsqu’une modification se produit du ou des types décrits dans le paramètre _ulEventMask._</span><span class="sxs-lookup"><span data-stu-id="40177-110">[in] A pointer to the entry identifier of the address book container, messaging user, or distribution list that will generate a notification when a change occurs of the type or types described in the  _ulEventMask_ parameter.</span></span> 
    
 <span data-ttu-id="40177-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="40177-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="40177-112">[in] Un ou plusieurs événements de notification que l’appelant inscrit pour recevoir.</span><span class="sxs-lookup"><span data-stu-id="40177-112">[in] One or more notification events that the caller is registering to receive.</span></span> <span data-ttu-id="40177-113">Chaque événement est associé à une structure de notification particulière qui contient des informations sur la modification qui s’est produite.</span><span class="sxs-lookup"><span data-stu-id="40177-113">Each event is associated with a particular notification structure that contains information about the change that occurred.</span></span> <span data-ttu-id="40177-114">Le tableau suivant répertorie les valeurs valides  _pour ulEventMask_ et leurs structures correspondantes.</span><span class="sxs-lookup"><span data-stu-id="40177-114">The following table lists the valid values for  _ulEventMask_ and their corresponding structures.</span></span> 
    
|<span data-ttu-id="40177-115">**Événement de notification**</span><span class="sxs-lookup"><span data-stu-id="40177-115">**Notification event**</span></span>|<span data-ttu-id="40177-116">**Structure correspondante**</span><span class="sxs-lookup"><span data-stu-id="40177-116">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="40177-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="40177-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="40177-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="40177-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="40177-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="40177-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="40177-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="40177-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="40177-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="40177-121">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="40177-122">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="40177-122">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="40177-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="40177-123">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="40177-124">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="40177-124">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="40177-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="40177-125">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="40177-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="40177-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="40177-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="40177-127">**fnevObjectMoved**</span></span> <br/> |[<span data-ttu-id="40177-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="40177-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="40177-129">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="40177-129">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="40177-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="40177-130">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
   
 <span data-ttu-id="40177-131">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="40177-131">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="40177-132">[in] Pointeur vers l’objet de réception de notification à appeler lorsque l’événement pour lequel une notification a été demandée se produit.</span><span class="sxs-lookup"><span data-stu-id="40177-132">[in] A pointer to the advise sink object to be called when the event for which notification has been requested occurs.</span></span>
    
 <span data-ttu-id="40177-133">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="40177-133">_lpulConnection_</span></span>
  
> <span data-ttu-id="40177-134">[out] Pointeur vers un numéro de connexion autre que zéro qui représente l’inscription de la notification.</span><span class="sxs-lookup"><span data-stu-id="40177-134">[out] A pointer to a nonzero connection number that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="40177-135">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="40177-135">Return value</span></span>

<span data-ttu-id="40177-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="40177-136">S_OK</span></span> 
  
> <span data-ttu-id="40177-137">L’inscription de la notification a réussi.</span><span class="sxs-lookup"><span data-stu-id="40177-137">The notification registration was successful.</span></span>
    
<span data-ttu-id="40177-138">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="40177-138">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="40177-139">Le fournisseur de carnet d’adresses responsable de l’identificateur d’entrée transmis  _dans lpEntryID_ n’a pas pu enregistrer de notification pour l’entrée correspondante.</span><span class="sxs-lookup"><span data-stu-id="40177-139">The address book provider responsible for the entry identifier passed in  _lpEntryID_ could not register a notification for the corresponding entry.</span></span> 
    
<span data-ttu-id="40177-140">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="40177-140">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="40177-141">La notification n’est pas prise en charge par le fournisseur de carnet d’adresses responsable de l’objet identifié par l’identificateur d’entrée transmis dans le paramètre _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="40177-141">Notification is not supported by the address book provider responsible for the object identified by the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="40177-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="40177-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="40177-143">L’identificateur d’entrée transmis  _dans lpEntryID_ ne peut être géré par aucun des fournisseurs de carnet d’adresses dans le profil.</span><span class="sxs-lookup"><span data-stu-id="40177-143">The entry identifier passed in  _lpEntryID_ cannot be handled by any of the address book providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="40177-144">Remarques</span><span class="sxs-lookup"><span data-stu-id="40177-144">Remarks</span></span>

<span data-ttu-id="40177-145">Les clients et les fournisseurs de services appellent la **méthode Advise** pour s’inscrire à un type particulier ou à des types de notifications sur une entrée de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="40177-145">Clients and service providers call the **Advise** method to register for a particular type or types of notification on an address book entry.</span></span> <span data-ttu-id="40177-146">Les types de notification sont indiqués par le masque d’événement transmis avec le _paramètre ulEventMask._</span><span class="sxs-lookup"><span data-stu-id="40177-146">The types of notification are indicated by the event mask passed in with the  _ulEventMask_ parameter.</span></span> 
  
<span data-ttu-id="40177-147">MAPI a transmis cet appel **Advise** au fournisseur de carnet d’adresses responsable de l’entrée, comme indiqué par l’identificateur d’entrée dans le paramètre _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="40177-147">MAPI forwards this **Advise** call to the address book provider that is responsible for the entry as indicated by the entry identifier in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="40177-148">Le fournisseur de carnet d’adresses gère l’inscription proprement dite ou appelle la méthode de support, [IMAPISupport::Subscribe,](imapisupport-subscribe.md)pour demander à MAPI d’inscrire l’appelant.</span><span class="sxs-lookup"><span data-stu-id="40177-148">The address book provider either handles the registration itself or calls the support method, [IMAPISupport::Subscribe](imapisupport-subscribe.md), to prompt MAPI to register the caller.</span></span> <span data-ttu-id="40177-149">Un numéro de connexion autre que zéro est renvoyé pour représenter l’inscription réussie.</span><span class="sxs-lookup"><span data-stu-id="40177-149">A nonzero connection number is returned to represent the successful registration.</span></span>
  
<span data-ttu-id="40177-150">Chaque fois qu’une modification a lieu sur l’entrée du type indiqué par l’inscription de notification, le fournisseur de carnet d’adresses appelle la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pour l’objet de réception de notification spécifié dans le paramètre _lpAdviseSink._</span><span class="sxs-lookup"><span data-stu-id="40177-150">Whenever a change occurs to the entry of the type indicated by the notification registration, the address book provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object specified in the  _lpAdviseSink_ parameter.</span></span> <span data-ttu-id="40177-151">La **méthode OnNotify inclut** une structure [NOTIFICATION](notification.md) en tant que paramètre d’entrée qui contient des données pour décrire l’événement.</span><span class="sxs-lookup"><span data-stu-id="40177-151">The **OnNotify** method includes a [NOTIFICATION](notification.md) structure as an input parameter that contains data to describe the event.</span></span> 
  
<span data-ttu-id="40177-152">Selon le fournisseur de carnet d’adresses, l’appel à **OnNotify** peut se produire immédiatement après la modification de l’objet inscrit ou ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="40177-152">Depending on the address book provider, the call to **OnNotify** can occur immediately following the change to the registered object or at a later time.</span></span> <span data-ttu-id="40177-153">Sur les systèmes qui prendre en charge plusieurs threads d’exécution, l’appel à **OnNotify** peut se produire sur n’importe quel thread.</span><span class="sxs-lookup"><span data-stu-id="40177-153">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="40177-154">Les clients peuvent demander que ces notifications se produisent sur un thread particulier en appelant la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) pour créer l’objet de réception de notification qui est transmis à **Advise**.</span><span class="sxs-lookup"><span data-stu-id="40177-154">Clients can request that these notifications occur on a particular thread by calling the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to create the advise sink object that is passed to **Advise**.</span></span> 
  
<span data-ttu-id="40177-155">Étant donné qu’un fournisseur de carnet d’adresses peut libérer l’objet de réception de notification transmis par les clients à tout moment après l’exécution de l’appel Advise et avant un appel [IAddrBook::Unadvise](iaddrbook-unadvise.md) pour annuler la notification, les clients doivent libérer leurs objets de réception de notification lorsque **Advise** renvoie. </span><span class="sxs-lookup"><span data-stu-id="40177-155">Because an address book provider can release the advise sink object passed in by clients at any time after the successful completion of the **Advise** call and before an [IAddrBook::Unadvise](iaddrbook-unadvise.md) call to cancel the notification, clients should release their advise sink objects when **Advise** returns.</span></span> 
  
<span data-ttu-id="40177-156">Pour plus d’informations sur le processus de notification, voir [notification d’événement dans MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="40177-156">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="40177-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40177-157">See also</span></span>



[<span data-ttu-id="40177-158">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="40177-158">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="40177-159">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="40177-159">IAddrBook::Unadvise</span></span>](iaddrbook-unadvise.md)
  
[<span data-ttu-id="40177-160">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="40177-160">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="40177-161">Notification</span><span class="sxs-lookup"><span data-stu-id="40177-161">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="40177-162">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="40177-162">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

