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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7a8d25dc7cac4226f38baab593b254108210549e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784929"
---
# <a name="notification"></a><span data-ttu-id="65183-103">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="65183-103">NOTIFICATION</span></span>
 
<span data-ttu-id="65183-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="65183-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="65183-105">Contient des informations sur un événement qui s’est produite et les données qui a été affectées par l’événement.</span><span class="sxs-lookup"><span data-stu-id="65183-105">Contains information about an event that has occurred and the data that has been affected by the event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="65183-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="65183-106">Header file:</span></span>  <br/> |<span data-ttu-id="65183-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="65183-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="65183-108">Membres</span><span class="sxs-lookup"><span data-stu-id="65183-108">Members</span></span>

<span data-ttu-id="65183-109">**ulEventType**</span><span class="sxs-lookup"><span data-stu-id="65183-109">**ulEventType**</span></span>
  
> <span data-ttu-id="65183-110">Type d’événement de notification qui s’est produite.</span><span class="sxs-lookup"><span data-stu-id="65183-110">Type of notification event that occurred.</span></span> <span data-ttu-id="65183-111">La valeur du membre **ulEventType** correspond à la structure qui est incluse dans l’union **info** .</span><span class="sxs-lookup"><span data-stu-id="65183-111">The value of the **ulEventType** member corresponds to the structure that is included in the **info** union.</span></span> <span data-ttu-id="65183-112">Le membre **ulEventType** peut être défini sur une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="65183-112">The **ulEventType** member can be set to one of the following values:</span></span> 
    
 <span data-ttu-id="65183-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="65183-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="65183-114">Une erreur globale s’est produite, par exemple une session d’arrêt en cours.</span><span class="sxs-lookup"><span data-stu-id="65183-114">A global error has occurred, such as a session shut down in progress.</span></span> <span data-ttu-id="65183-115">Le membre **info** contient une structure [ERROR_NOTIFICATION](error_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="65183-115">The **info** member contains an [ERROR_NOTIFICATION](error_notification.md) structure.</span></span> 
    
 <span data-ttu-id="65183-116">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="65183-116">_fnevExtended_</span></span>
  
> <span data-ttu-id="65183-117">Un événement interne définie par un fournisseur de services particulier s’est produite.</span><span class="sxs-lookup"><span data-stu-id="65183-117">An internal event defined by a particular service provider has occurred.</span></span> <span data-ttu-id="65183-118">Le membre **info** contient une structure [EXTENDED_NOTIFICATION](extended_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="65183-118">The **info** member contains an [EXTENDED_NOTIFICATION](extended_notification.md) structure.</span></span> 
    
 <span data-ttu-id="65183-119">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="65183-119">_fnevNewMail_</span></span>
  
> <span data-ttu-id="65183-120">Un message a été remis vers le dossier pour la classe de message de réception et est en attente de traitement.</span><span class="sxs-lookup"><span data-stu-id="65183-120">A message has been delivered to the appropriate receive folder for the message class and is waiting to be processed.</span></span> <span data-ttu-id="65183-121">Le membre **info** contient une structure [NEWMAIL_NOTIFICATION](newmail_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="65183-121">The **info** member contains an [NEWMAIL_NOTIFICATION](newmail_notification.md) structure.</span></span> 
    
 <span data-ttu-id="65183-122">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="65183-122">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="65183-123">Un objet MAPI a été copié.</span><span class="sxs-lookup"><span data-stu-id="65183-123">A MAPI object has been copied.</span></span> <span data-ttu-id="65183-124">Le membre **info** contient une structure [OBJECT_NOTIFICATION](object_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="65183-124">The **info** member contains an [OBJECT_NOTIFICATION](object_notification.md) structure.</span></span> 
    
 <span data-ttu-id="65183-125">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="65183-125">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="65183-126">Un objet MAPI a été créé.</span><span class="sxs-lookup"><span data-stu-id="65183-126">A MAPI object has been created.</span></span> <span data-ttu-id="65183-127">Le membre **info** contient une structure **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="65183-127">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="65183-128">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="65183-128">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="65183-129">Un objet MAPI a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="65183-129">A MAPI object has been deleted.</span></span> <span data-ttu-id="65183-130">Le membre **info** contient une structure **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="65183-130">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="65183-131">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="65183-131">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="65183-132">Un objet MAPI a changé.</span><span class="sxs-lookup"><span data-stu-id="65183-132">A MAPI object has changed.</span></span> <span data-ttu-id="65183-133">Le membre **info** contient une structure **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="65183-133">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="65183-134">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="65183-134">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="65183-135">Une banque de messages ou l’adresse livre objet a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="65183-135">A message store or address book object has been moved.</span></span> <span data-ttu-id="65183-136">Le membre **info** contient une structure **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="65183-136">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="65183-137">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="65183-137">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="65183-138">Une opération de recherche est terminée et les résultats sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="65183-138">A search operation has finished and the results are available.</span></span> <span data-ttu-id="65183-139">Le membre **info** contient une structure **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="65183-139">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="65183-140">_fnevTableModified_</span><span class="sxs-lookup"><span data-stu-id="65183-140">_fnevTableModified_</span></span>
  
> <span data-ttu-id="65183-141">Informations contenues dans un tableau a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="65183-141">Information in a table has changed.</span></span> <span data-ttu-id="65183-142">Le membre **info** contient une structure [TABLE_NOTIFICATION](table_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="65183-142">The **info** member contains an [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    
<span data-ttu-id="65183-143">**Info**</span><span class="sxs-lookup"><span data-stu-id="65183-143">**info**</span></span>
  
> <span data-ttu-id="65183-144">Union de structures de notification décrivant les données d’un type particulier d’événement affectées.</span><span class="sxs-lookup"><span data-stu-id="65183-144">Union of notification structures describing the affected data for a particular type of event.</span></span> <span data-ttu-id="65183-145">La structure incluse dans le membre **info** dépend de la valeur du membre **ulEventType** .</span><span class="sxs-lookup"><span data-stu-id="65183-145">The structure included in the **info** member depends on the value of the **ulEventType** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="65183-146">Remarques</span><span class="sxs-lookup"><span data-stu-id="65183-146">Remarks</span></span>

<span data-ttu-id="65183-147">Une ou plusieurs des structures **NOTIFICATION** sont passés comme paramètres d’entrée à chaque appel de méthode [d’IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) d’un récepteur de notifications enregistrés.</span><span class="sxs-lookup"><span data-stu-id="65183-147">One or more **NOTIFICATION** structures are passed as input parameters with every call to a registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="65183-148">Les structures **NOTIFICATION** contiennent des informations sur les événements qui se sont produites et décrivent les objets affectés.</span><span class="sxs-lookup"><span data-stu-id="65183-148">The **NOTIFICATION** structures contain information about the particular events that have occurred and describe the affected objects.</span></span> 
  
<span data-ttu-id="65183-149">Avant que les clients ou fournisseurs de services de recevoir une notification puissent utiliser la structure à traiter l’événement, ils doivent vérifier le type d’événement comme indiqué dans le membre **ulEventType** .</span><span class="sxs-lookup"><span data-stu-id="65183-149">Before clients or service providers receiving a notification can use the structure to process the event, they must check the event type as indicated in the **ulEventType** member.</span></span> <span data-ttu-id="65183-150">L’exemple de code qui est présenté ici vérifie l’arrivée d’un nouveau message et lors de la détection d’un événement de ce type, par exemple, imprime la classe de message du message.</span><span class="sxs-lookup"><span data-stu-id="65183-150">For example, the code sample that is shown here checks for the arrival of a new message and upon detecting an event of this kind, prints out the message class of the message.</span></span> 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

<span data-ttu-id="65183-151">Pour plus d’informations sur la notification, consultez les rubriques décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="65183-151">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="65183-152">**Rubrique**</span><span class="sxs-lookup"><span data-stu-id="65183-152">**Topic**</span></span>|<span data-ttu-id="65183-153">**Description**</span><span class="sxs-lookup"><span data-stu-id="65183-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65183-154">Notification d’événement MAPI</span><span class="sxs-lookup"><span data-stu-id="65183-154">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="65183-155">Vue d’ensemble des notifications et les événements de notification.</span><span class="sxs-lookup"><span data-stu-id="65183-155">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="65183-156">Gérer les Notifications</span><span class="sxs-lookup"><span data-stu-id="65183-156">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="65183-157">Étude de la façon dont les clients doivent gérer les notifications.</span><span class="sxs-lookup"><span data-stu-id="65183-157">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="65183-158">Prise en charge de la Notification d’événement</span><span class="sxs-lookup"><span data-stu-id="65183-158">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="65183-159">Étude de comment les fournisseurs de services peuvent utiliser la méthode [IMAPISupport](imapisupportiunknown.md) pour générer des notifications.</span><span class="sxs-lookup"><span data-stu-id="65183-159">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="65183-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65183-160">See also</span></span>


- [<span data-ttu-id="65183-161">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="65183-161">ERROR_NOTIFICATION</span></span>](error_notification.md)  
- [<span data-ttu-id="65183-162">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="65183-162">EXTENDED_NOTIFICATION</span></span>](extended_notification.md)  
- [<span data-ttu-id="65183-163">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="65183-163">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md)  
- [<span data-ttu-id="65183-164">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="65183-164">OBJECT_NOTIFICATION</span></span>](object_notification.md)  
- [<span data-ttu-id="65183-165">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="65183-165">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md)  
- [<span data-ttu-id="65183-166">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="65183-166">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="65183-167">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="65183-167">MAPI Structures</span></span>](mapi-structures.md)

