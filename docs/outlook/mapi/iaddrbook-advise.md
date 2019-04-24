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
ms.openlocfilehash: 7abafafd3d4bd9618d85a7dac34e4556545167bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334754"
---
# <a name="iaddrbookadvise"></a><span data-ttu-id="7dcda-103">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="7dcda-103">IAddrBook::Advise</span></span>

  
  
<span data-ttu-id="7dcda-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7dcda-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7dcda-105">Inscrit un client ou un fournisseur de services pour recevoir des notifications sur les modifications apportées à une ou plusieurs entrées du carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="7dcda-105">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="7dcda-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7dcda-106">Parameters</span></span>

 <span data-ttu-id="7dcda-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="7dcda-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="7dcda-108">dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="7dcda-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="7dcda-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="7dcda-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="7dcda-110">dans Pointeur vers l'identificateur d'entrée du conteneur de carnet d'adresses, de l'utilisateur de messagerie ou de la liste de distribution qui générera une notification lorsqu'une modification est apportée au type ou aux types décrits dans le paramètre _ulEventMask_ .</span><span class="sxs-lookup"><span data-stu-id="7dcda-110">[in] A pointer to the entry identifier of the address book container, messaging user, or distribution list that will generate a notification when a change occurs of the type or types described in the  _ulEventMask_ parameter.</span></span> 
    
 <span data-ttu-id="7dcda-111">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="7dcda-111">_ulEventMask_</span></span>
  
> <span data-ttu-id="7dcda-112">dans Un ou plusieurs événements de notification que l'appelant s'inscrit à recevoir.</span><span class="sxs-lookup"><span data-stu-id="7dcda-112">[in] One or more notification events that the caller is registering to receive.</span></span> <span data-ttu-id="7dcda-113">Chaque événement est associé à une structure de notification spécifique qui contient des informations sur la modification qui s'est produite.</span><span class="sxs-lookup"><span data-stu-id="7dcda-113">Each event is associated with a particular notification structure that contains information about the change that occurred.</span></span> <span data-ttu-id="7dcda-114">Le tableau suivant répertorie les valeurs valides pour _ulEventMask_ et leurs structures correspondantes.</span><span class="sxs-lookup"><span data-stu-id="7dcda-114">The following table lists the valid values for  _ulEventMask_ and their corresponding structures.</span></span> 
    
|<span data-ttu-id="7dcda-115">**Notification, événement**</span><span class="sxs-lookup"><span data-stu-id="7dcda-115">**Notification event**</span></span>|<span data-ttu-id="7dcda-116">**Structure correspondante**</span><span class="sxs-lookup"><span data-stu-id="7dcda-116">**Corresponding structure**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7dcda-117">**fnevCriticalError**</span><span class="sxs-lookup"><span data-stu-id="7dcda-117">**fnevCriticalError**</span></span> <br/> |[<span data-ttu-id="7dcda-118">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7dcda-118">ERROR_NOTIFICATION</span></span>](error_notification.md) <br/> |
|<span data-ttu-id="7dcda-119">**fnevObjectCreated**</span><span class="sxs-lookup"><span data-stu-id="7dcda-119">**fnevObjectCreated**</span></span> <br/> |[<span data-ttu-id="7dcda-120">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7dcda-120">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="7dcda-121">**fnevObjectDeleted**</span><span class="sxs-lookup"><span data-stu-id="7dcda-121">**fnevObjectDeleted**</span></span> <br/> |[<span data-ttu-id="7dcda-122">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7dcda-122">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="7dcda-123">**fnevObjectModified**</span><span class="sxs-lookup"><span data-stu-id="7dcda-123">**fnevObjectModified**</span></span> <br/> |[<span data-ttu-id="7dcda-124">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7dcda-124">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="7dcda-125">**fnevObjectCopied**</span><span class="sxs-lookup"><span data-stu-id="7dcda-125">**fnevObjectCopied**</span></span> <br/> |[<span data-ttu-id="7dcda-126">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7dcda-126">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="7dcda-127">**fnevObjectMoved**</span><span class="sxs-lookup"><span data-stu-id="7dcda-127">**fnevObjectMoved**</span></span> <br/> |[<span data-ttu-id="7dcda-128">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7dcda-128">OBJECT_NOTIFICATION</span></span>](object_notification.md) <br/> |
|<span data-ttu-id="7dcda-129">**fnevTableModified**</span><span class="sxs-lookup"><span data-stu-id="7dcda-129">**fnevTableModified**</span></span> <br/> |[<span data-ttu-id="7dcda-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7dcda-130">TABLE_NOTIFICATION</span></span>](table_notification.md) <br/> |
   
 <span data-ttu-id="7dcda-131">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="7dcda-131">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="7dcda-132">dans Pointeur vers l'objet de récepteur de Conseil à appeler lorsque l'événement pour lequel la notification a été demandée se produit.</span><span class="sxs-lookup"><span data-stu-id="7dcda-132">[in] A pointer to the advise sink object to be called when the event for which notification has been requested occurs.</span></span>
    
 <span data-ttu-id="7dcda-133">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="7dcda-133">_lpulConnection_</span></span>
  
> <span data-ttu-id="7dcda-134">remarquer Pointeur vers un numéro de connexion différent de zéro qui représente l'enregistrement de la notification.</span><span class="sxs-lookup"><span data-stu-id="7dcda-134">[out] A pointer to a nonzero connection number that represents the notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7dcda-135">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7dcda-135">Return value</span></span>

<span data-ttu-id="7dcda-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="7dcda-136">S_OK</span></span> 
  
> <span data-ttu-id="7dcda-137">L'enregistrement de la notification a réussi.</span><span class="sxs-lookup"><span data-stu-id="7dcda-137">The notification registration was successful.</span></span>
    
<span data-ttu-id="7dcda-138">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7dcda-138">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="7dcda-139">Le fournisseur de carnet d'adresses responsable de l'identificateur d'entrée passé dans _lpEntryID_ n'a pas pu enregistrer une notification pour l'entrée correspondante.</span><span class="sxs-lookup"><span data-stu-id="7dcda-139">The address book provider responsible for the entry identifier passed in  _lpEntryID_ could not register a notification for the corresponding entry.</span></span> 
    
<span data-ttu-id="7dcda-140">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="7dcda-140">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="7dcda-141">La notification n'est pas prise en charge par le fournisseur de carnet d'adresses responsable de l'objet identifié par l'identificateur d'entrée passé dans le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="7dcda-141">Notification is not supported by the address book provider responsible for the object identified by the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="7dcda-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7dcda-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="7dcda-143">L'identificateur d'entrée passé dans _lpEntryID_ ne peut être géré par aucun des fournisseurs de carnet d'adresses dans le profil.</span><span class="sxs-lookup"><span data-stu-id="7dcda-143">The entry identifier passed in  _lpEntryID_ cannot be handled by any of the address book providers in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7dcda-144">Remarques</span><span class="sxs-lookup"><span data-stu-id="7dcda-144">Remarks</span></span>

<span data-ttu-id="7dcda-145">Les clients et les fournisseurs de \*\*\*\* services appellent la méthode Advise pour s'inscrire à un type particulier ou à des types de notifications sur une entrée de carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="7dcda-145">Clients and service providers call the **Advise** method to register for a particular type or types of notification on an address book entry.</span></span> <span data-ttu-id="7dcda-146">Les types de notifications sont indiqués par le masque d'événement transmis avec le paramètre _ulEventMask_ .</span><span class="sxs-lookup"><span data-stu-id="7dcda-146">The types of notification are indicated by the event mask passed in with the  _ulEventMask_ parameter.</span></span> 
  
<span data-ttu-id="7dcda-147">MAPI transmet cet appel \*\*\*\* au fournisseur de carnets d'adresses qui est responsable de l'entrée comme indiqué par l'identificateur d'entrée dans le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="7dcda-147">MAPI forwards this **Advise** call to the address book provider that is responsible for the entry as indicated by the entry identifier in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="7dcda-148">Le fournisseur de carnet d'adresses gère l'inscription proprement dite ou appelle la méthode de prise en charge, [IMAPISupport:: subscribe](imapisupport-subscribe.md), pour inviter MAPI à inscrire l'appelant.</span><span class="sxs-lookup"><span data-stu-id="7dcda-148">The address book provider either handles the registration itself or calls the support method, [IMAPISupport::Subscribe](imapisupport-subscribe.md), to prompt MAPI to register the caller.</span></span> <span data-ttu-id="7dcda-149">Un numéro de connexion différent de zéro est renvoyé pour représenter la réussite de l'inscription.</span><span class="sxs-lookup"><span data-stu-id="7dcda-149">A nonzero connection number is returned to represent the successful registration.</span></span>
  
<span data-ttu-id="7dcda-150">Chaque fois qu'une modification est apportée à l'entrée du type indiqué par l'enregistrement des notifications, le fournisseur de carnet d'adresses appelle la méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) pour l'objet récepteur de notification spécifié dans le paramètre _lpAdviseSink_ .</span><span class="sxs-lookup"><span data-stu-id="7dcda-150">Whenever a change occurs to the entry of the type indicated by the notification registration, the address book provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object specified in the  _lpAdviseSink_ parameter.</span></span> <span data-ttu-id="7dcda-151">La méthode **OnNotify** inclut une structure de [notification](notification.md) sous la forme d'un paramètre d'entrée qui contient les données de description de l'événement.</span><span class="sxs-lookup"><span data-stu-id="7dcda-151">The **OnNotify** method includes a [NOTIFICATION](notification.md) structure as an input parameter that contains data to describe the event.</span></span> 
  
<span data-ttu-id="7dcda-152">En fonction du fournisseur de carnet d'adresses, l'appel à **OnNotify** peut se produire immédiatement après la modification de l'objet inscrit ou ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="7dcda-152">Depending on the address book provider, the call to **OnNotify** can occur immediately following the change to the registered object or at a later time.</span></span> <span data-ttu-id="7dcda-153">Sur les systèmes qui prennent en charge plusieurs threads d'exécution, l'appel à **OnNotify** peut se produire sur n'importe quel thread.</span><span class="sxs-lookup"><span data-stu-id="7dcda-153">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="7dcda-154">Les clients peuvent demander que ces notifications se produisent sur un thread particulier en appelant la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) pour créer l'objet de récepteur de notifications qui est transmis à Advise. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="7dcda-154">Clients can request that these notifications occur on a particular thread by calling the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function to create the advise sink object that is passed to **Advise**.</span></span> 
  
<span data-ttu-id="7dcda-155">Étant donné qu'un fournisseur de carnet d'adresses peut libérer l'objet de récepteur de notifications transmis par les clients à tout \*\*\*\* moment après l'exécution réussie de l'appel de la méthode Advise et avant un appel [IAddrBook::](iaddrbook-unadvise.md) Unadvise pour annuler la notification, les clients doivent le libérer. leurs objets de récepteur de \*\*\*\* notification lorsque la fonction Advise renvoie.</span><span class="sxs-lookup"><span data-stu-id="7dcda-155">Because an address book provider can release the advise sink object passed in by clients at any time after the successful completion of the **Advise** call and before an [IAddrBook::Unadvise](iaddrbook-unadvise.md) call to cancel the notification, clients should release their advise sink objects when **Advise** returns.</span></span> 
  
<span data-ttu-id="7dcda-156">Pour plus d'informations sur le processus de notification, consultez la rubrique [notifications d'événements dans MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="7dcda-156">For more information about the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7dcda-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7dcda-157">See also</span></span>



[<span data-ttu-id="7dcda-158">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="7dcda-158">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="7dcda-159">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="7dcda-159">IAddrBook::Unadvise</span></span>](iaddrbook-unadvise.md)
  
[<span data-ttu-id="7dcda-160">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="7dcda-160">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="7dcda-161">Notification</span><span class="sxs-lookup"><span data-stu-id="7dcda-161">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="7dcda-162">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7dcda-162">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

