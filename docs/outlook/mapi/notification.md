---
title: NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFICATION
api_type:
- COM
ms.assetid: 01b6e695-a649-4efd-a893-7586b476467e
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 0d427adde72c24d4ca879c7bd883af09c4ecad53
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579969"
---
# <a name="notification"></a><span data-ttu-id="1df66-103">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1df66-103">NOTIFICATION</span></span>
 
<span data-ttu-id="1df66-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1df66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1df66-105">Contient des informations sur un événement qui s’est produite et les données qui a été affectées par l’événement.</span><span class="sxs-lookup"><span data-stu-id="1df66-105">Contains information about an event that has occurred and the data that has been affected by the event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1df66-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="1df66-106">Header file:</span></span>  <br/> |<span data-ttu-id="1df66-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1df66-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG ulEventType;
  union
  {
    ERROR_NOTIFICATION err;
    NEWMAIL_NOTIFICATION newmail;
    OBJECT_NOTIFICATION obj;
    TABLE_NOTIFICATION tab;
    EXTENDED_NOTIFICATION ext;
    STATUS_OBJECT_NOTIFICATION statobj;
  } info;
} NOTIFICATION, FAR *LPNOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="1df66-108">Members</span><span class="sxs-lookup"><span data-stu-id="1df66-108">Members</span></span>

<span data-ttu-id="1df66-109">**ulEventType**</span><span class="sxs-lookup"><span data-stu-id="1df66-109">**ulEventType**</span></span>
  
> <span data-ttu-id="1df66-110">Type d’événement de notification qui s’est produite.</span><span class="sxs-lookup"><span data-stu-id="1df66-110">Type of notification event that occurred.</span></span> <span data-ttu-id="1df66-111">La valeur du membre **ulEventType** correspond à la structure qui est incluse dans l’union **info** .</span><span class="sxs-lookup"><span data-stu-id="1df66-111">The value of the **ulEventType** member corresponds to the structure that is included in the **info** union.</span></span> <span data-ttu-id="1df66-112">Le membre **ulEventType** peut être défini sur une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="1df66-112">The **ulEventType** member can be set to one of the following values:</span></span> 
    
 <span data-ttu-id="1df66-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="1df66-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="1df66-114">Une erreur globale s’est produite, par exemple une session d’arrêt en cours.</span><span class="sxs-lookup"><span data-stu-id="1df66-114">A global error has occurred, such as a session shut down in progress.</span></span> <span data-ttu-id="1df66-115">Le membre **info** contient une structure [ERROR_NOTIFICATION](error_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="1df66-115">The **info** member contains an [ERROR_NOTIFICATION](error_notification.md) structure.</span></span> 
    
 <span data-ttu-id="1df66-116">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="1df66-116">_fnevExtended_</span></span>
  
> <span data-ttu-id="1df66-117">Un événement interne définie par un fournisseur de services particulier s’est produite.</span><span class="sxs-lookup"><span data-stu-id="1df66-117">An internal event defined by a particular service provider has occurred.</span></span> <span data-ttu-id="1df66-118">Le membre **info** contient une structure [EXTENDED_NOTIFICATION](extended_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="1df66-118">The **info** member contains an [EXTENDED_NOTIFICATION](extended_notification.md) structure.</span></span> 
    
 <span data-ttu-id="1df66-119">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="1df66-119">_fnevNewMail_</span></span>
  
> <span data-ttu-id="1df66-120">Un message a été remis vers le dossier pour la classe de message de réception et est en attente de traitement.</span><span class="sxs-lookup"><span data-stu-id="1df66-120">A message has been delivered to the appropriate receive folder for the message class and is waiting to be processed.</span></span> <span data-ttu-id="1df66-121">Le membre **info** contient une structure [NEWMAIL_NOTIFICATION](newmail_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="1df66-121">The **info** member contains an [NEWMAIL_NOTIFICATION](newmail_notification.md) structure.</span></span> 
    
 <span data-ttu-id="1df66-122">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="1df66-122">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="1df66-123">Un objet MAPI a été copié.</span><span class="sxs-lookup"><span data-stu-id="1df66-123">A MAPI object has been copied.</span></span> <span data-ttu-id="1df66-124">Le membre **info** contient une structure [OBJECT_NOTIFICATION](object_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="1df66-124">The **info** member contains an [OBJECT_NOTIFICATION](object_notification.md) structure.</span></span> 
    
 <span data-ttu-id="1df66-125">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="1df66-125">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="1df66-126">Un objet MAPI a été créé.</span><span class="sxs-lookup"><span data-stu-id="1df66-126">A MAPI object has been created.</span></span> <span data-ttu-id="1df66-127">Le membre **info** contient une structure **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="1df66-127">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="1df66-128">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="1df66-128">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="1df66-129">Un objet MAPI a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="1df66-129">A MAPI object has been deleted.</span></span> <span data-ttu-id="1df66-130">Le membre **info** contient une structure **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="1df66-130">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="1df66-131">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="1df66-131">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="1df66-132">Un objet MAPI a changé.</span><span class="sxs-lookup"><span data-stu-id="1df66-132">A MAPI object has changed.</span></span> <span data-ttu-id="1df66-133">Le membre **info** contient une structure **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="1df66-133">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="1df66-134">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="1df66-134">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="1df66-135">Une banque de messages ou l’adresse livre objet a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="1df66-135">A message store or address book object has been moved.</span></span> <span data-ttu-id="1df66-136">Le membre **info** contient une structure **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="1df66-136">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="1df66-137">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="1df66-137">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="1df66-138">Une opération de recherche est terminée et les résultats sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="1df66-138">A search operation has finished and the results are available.</span></span> <span data-ttu-id="1df66-139">Le membre **info** contient une structure **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="1df66-139">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="1df66-140">_fnevTableModified_</span><span class="sxs-lookup"><span data-stu-id="1df66-140">_fnevTableModified_</span></span>
  
> <span data-ttu-id="1df66-141">Informations contenues dans un tableau a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="1df66-141">Information in a table has changed.</span></span> <span data-ttu-id="1df66-142">Le membre **info** contient une structure [TABLE_NOTIFICATION](table_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="1df66-142">The **info** member contains an [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    
<span data-ttu-id="1df66-143">**Info**</span><span class="sxs-lookup"><span data-stu-id="1df66-143">**info**</span></span>
  
> <span data-ttu-id="1df66-144">Union de structures de notification décrivant les données d’un type particulier d’événement affectées.</span><span class="sxs-lookup"><span data-stu-id="1df66-144">Union of notification structures describing the affected data for a particular type of event.</span></span> <span data-ttu-id="1df66-145">La structure incluse dans le membre **info** dépend de la valeur du membre **ulEventType** .</span><span class="sxs-lookup"><span data-stu-id="1df66-145">The structure included in the **info** member depends on the value of the **ulEventType** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1df66-146">Remarques</span><span class="sxs-lookup"><span data-stu-id="1df66-146">Remarks</span></span>

<span data-ttu-id="1df66-147">Une ou plusieurs des structures **NOTIFICATION** sont passés comme paramètres d’entrée à chaque appel de méthode [d’IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) d’un récepteur de notifications enregistrés.</span><span class="sxs-lookup"><span data-stu-id="1df66-147">One or more **NOTIFICATION** structures are passed as input parameters with every call to a registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="1df66-148">Les structures **NOTIFICATION** contiennent des informations sur les événements qui se sont produites et décrivent les objets affectés.</span><span class="sxs-lookup"><span data-stu-id="1df66-148">The **NOTIFICATION** structures contain information about the particular events that have occurred and describe the affected objects.</span></span> 
  
<span data-ttu-id="1df66-149">Avant que les clients ou fournisseurs de services de recevoir une notification puissent utiliser la structure à traiter l’événement, ils doivent vérifier le type d’événement comme indiqué dans le membre **ulEventType** .</span><span class="sxs-lookup"><span data-stu-id="1df66-149">Before clients or service providers receiving a notification can use the structure to process the event, they must check the event type as indicated in the **ulEventType** member.</span></span> <span data-ttu-id="1df66-150">L’exemple de code qui est présenté ici vérifie l’arrivée d’un nouveau message et lors de la détection d’un événement de ce type, par exemple, imprime la classe de message du message.</span><span class="sxs-lookup"><span data-stu-id="1df66-150">For example, the code sample that is shown here checks for the arrival of a new message and upon detecting an event of this kind, prints out the message class of the message.</span></span> 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

<span data-ttu-id="1df66-151">Pour plus d’informations sur la notification, consultez les rubriques décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1df66-151">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="1df66-152">**Rubrique**</span><span class="sxs-lookup"><span data-stu-id="1df66-152">**Topic**</span></span>|<span data-ttu-id="1df66-153">**Description**</span><span class="sxs-lookup"><span data-stu-id="1df66-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1df66-154">Notification d’événement dans MAPI</span><span class="sxs-lookup"><span data-stu-id="1df66-154">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="1df66-155">Vue d’ensemble des notifications et les événements de notification.</span><span class="sxs-lookup"><span data-stu-id="1df66-155">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="1df66-156">Gestion des notifications</span><span class="sxs-lookup"><span data-stu-id="1df66-156">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="1df66-157">Étude de la façon dont les clients doivent gérer les notifications.</span><span class="sxs-lookup"><span data-stu-id="1df66-157">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="1df66-158">Prise en charge des notifications d’événements</span><span class="sxs-lookup"><span data-stu-id="1df66-158">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="1df66-159">Étude de comment les fournisseurs de services peuvent utiliser la méthode [IMAPISupport](imapisupportiunknown.md) pour générer des notifications.</span><span class="sxs-lookup"><span data-stu-id="1df66-159">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1df66-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1df66-160">See also</span></span>


- [<span data-ttu-id="1df66-161">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1df66-161">ERROR_NOTIFICATION</span></span>](error_notification.md)  
- [<span data-ttu-id="1df66-162">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1df66-162">EXTENDED_NOTIFICATION</span></span>](extended_notification.md)  
- [<span data-ttu-id="1df66-163">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1df66-163">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md)  
- [<span data-ttu-id="1df66-164">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1df66-164">OBJECT_NOTIFICATION</span></span>](object_notification.md)  
- [<span data-ttu-id="1df66-165">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1df66-165">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md)  
- [<span data-ttu-id="1df66-166">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1df66-166">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="1df66-167">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="1df66-167">MAPI Structures</span></span>](mapi-structures.md)

