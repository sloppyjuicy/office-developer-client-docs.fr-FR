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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a3235c2305d61318f482943167e5f307e5da0d70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432876"
---
# <a name="notification"></a><span data-ttu-id="c5fa3-103">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c5fa3-103">NOTIFICATION</span></span>
 
<span data-ttu-id="c5fa3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5fa3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5fa3-105">Contient des informations sur un événement qui s'est produit et sur les données qui ont été affectées par l'événement.</span><span class="sxs-lookup"><span data-stu-id="c5fa3-105">Contains information about an event that has occurred and the data that has been affected by the event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c5fa3-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c5fa3-106">Header file:</span></span>  <br/> |<span data-ttu-id="c5fa3-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c5fa3-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="c5fa3-108">Members</span><span class="sxs-lookup"><span data-stu-id="c5fa3-108">Members</span></span>

<span data-ttu-id="c5fa3-109">**ulEventType**</span><span class="sxs-lookup"><span data-stu-id="c5fa3-109">**ulEventType**</span></span>
  
> <span data-ttu-id="c5fa3-110">Type d'événement de notification qui s'est produit.</span><span class="sxs-lookup"><span data-stu-id="c5fa3-110">Type of notification event that occurred.</span></span> <span data-ttu-id="c5fa3-111">La valeur du membre **ulEventType** correspond à la structure incluse dans l'Union d' **informations** .</span><span class="sxs-lookup"><span data-stu-id="c5fa3-111">The value of the **ulEventType** member corresponds to the structure that is included in the **info** union.</span></span> <span data-ttu-id="c5fa3-112">Le membre **ulEventType** peut prendre la valeur de l'une des valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="c5fa3-112">The **ulEventType** member can be set to one of the following values:</span></span> 
    
 <span data-ttu-id="c5fa3-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="c5fa3-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="c5fa3-114">Une erreur globale s'est produite, telle qu'une session a été arrêtée en cours.</span><span class="sxs-lookup"><span data-stu-id="c5fa3-114">A global error has occurred, such as a session shut down in progress.</span></span> <span data-ttu-id="c5fa3-115">Le membre **info** contient une structure [ERROR_NOTIFICATION](error_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="c5fa3-115">The **info** member contains an [ERROR_NOTIFICATION](error_notification.md) structure.</span></span> 
    
 <span data-ttu-id="c5fa3-116">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="c5fa3-116">_fnevExtended_</span></span>
  
> <span data-ttu-id="c5fa3-117">Un événement interne défini par un fournisseur de services particulier s'est produit.</span><span class="sxs-lookup"><span data-stu-id="c5fa3-117">An internal event defined by a particular service provider has occurred.</span></span> <span data-ttu-id="c5fa3-118">Le membre **info** contient une structure [EXTENDED_NOTIFICATION](extended_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="c5fa3-118">The **info** member contains an [EXTENDED_NOTIFICATION](extended_notification.md) structure.</span></span> 
    
 <span data-ttu-id="c5fa3-119">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="c5fa3-119">_fnevNewMail_</span></span>
  
> <span data-ttu-id="c5fa3-120">Un message a été remis dans le dossier de réception approprié pour la classe de message et est en attente de traitement.</span><span class="sxs-lookup"><span data-stu-id="c5fa3-120">A message has been delivered to the appropriate receive folder for the message class and is waiting to be processed.</span></span> <span data-ttu-id="c5fa3-121">Le membre **info** contient une structure [NEWMAIL_NOTIFICATION](newmail_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="c5fa3-121">The **info** member contains an [NEWMAIL_NOTIFICATION](newmail_notification.md) structure.</span></span> 
    
 <span data-ttu-id="c5fa3-122">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="c5fa3-122">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="c5fa3-123">Un objet MAPI a été copié.</span><span class="sxs-lookup"><span data-stu-id="c5fa3-123">A MAPI object has been copied.</span></span> <span data-ttu-id="c5fa3-124">Le membre **info** contient une structure [OBJECT_NOTIFICATION](object_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="c5fa3-124">The **info** member contains an [OBJECT_NOTIFICATION](object_notification.md) structure.</span></span> 
    
 <span data-ttu-id="c5fa3-125">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="c5fa3-125">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="c5fa3-126">Un objet MAPI a été créé.</span><span class="sxs-lookup"><span data-stu-id="c5fa3-126">A MAPI object has been created.</span></span> <span data-ttu-id="c5fa3-127">Le membre **info** contient une structure **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="c5fa3-127">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="c5fa3-128">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="c5fa3-128">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="c5fa3-129">Un objet MAPI a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="c5fa3-129">A MAPI object has been deleted.</span></span> <span data-ttu-id="c5fa3-130">Le membre **info** contient une structure **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="c5fa3-130">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="c5fa3-131">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="c5fa3-131">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="c5fa3-132">Un objet MAPI a été modifié.</span><span class="sxs-lookup"><span data-stu-id="c5fa3-132">A MAPI object has changed.</span></span> <span data-ttu-id="c5fa3-133">Le membre **info** contient une structure **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="c5fa3-133">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="c5fa3-134">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="c5fa3-134">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="c5fa3-135">Un objet de banque de messages ou de carnet d'adresses a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="c5fa3-135">A message store or address book object has been moved.</span></span> <span data-ttu-id="c5fa3-136">Le membre **info** contient une structure **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="c5fa3-136">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="c5fa3-137">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="c5fa3-137">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="c5fa3-138">Une opération de recherche est terminée et les résultats sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="c5fa3-138">A search operation has finished and the results are available.</span></span> <span data-ttu-id="c5fa3-139">Le membre **info** contient une structure **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="c5fa3-139">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="c5fa3-140">_fnevTableModified_</span><span class="sxs-lookup"><span data-stu-id="c5fa3-140">_fnevTableModified_</span></span>
  
> <span data-ttu-id="c5fa3-141">Les informations d'une table ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="c5fa3-141">Information in a table has changed.</span></span> <span data-ttu-id="c5fa3-142">Le membre **info** contient une structure [TABLE_NOTIFICATION](table_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="c5fa3-142">The **info** member contains an [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    
<span data-ttu-id="c5fa3-143">**info**</span><span class="sxs-lookup"><span data-stu-id="c5fa3-143">**info**</span></span>
  
> <span data-ttu-id="c5fa3-144">Union des structures de notification décrivant les données affectées pour un type d'événement particulier.</span><span class="sxs-lookup"><span data-stu-id="c5fa3-144">Union of notification structures describing the affected data for a particular type of event.</span></span> <span data-ttu-id="c5fa3-145">La structure incluse dans le membre **info** dépend de la valeur du membre **ulEventType** .</span><span class="sxs-lookup"><span data-stu-id="c5fa3-145">The structure included in the **info** member depends on the value of the **ulEventType** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c5fa3-146">Remarques</span><span class="sxs-lookup"><span data-stu-id="c5fa3-146">Remarks</span></span>

<span data-ttu-id="c5fa3-147">Une ou plusieurs structures de notification sont transmises en tant que paramètres d'entrée avec chaque appel à la méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) du récepteur de **notification** enregistré.</span><span class="sxs-lookup"><span data-stu-id="c5fa3-147">One or more **NOTIFICATION** structures are passed as input parameters with every call to a registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="c5fa3-148">Les structures de **notification** contiennent des informations sur les événements spécifiques qui se sont produits et décrivent les objets affectés.</span><span class="sxs-lookup"><span data-stu-id="c5fa3-148">The **NOTIFICATION** structures contain information about the particular events that have occurred and describe the affected objects.</span></span> 
  
<span data-ttu-id="c5fa3-149">Avant que les clients ou fournisseurs de services recevant une notification puissent utiliser la structure pour traiter l'événement, ils doivent vérifier le type d'événement comme indiqué dans le membre **ulEventType** .</span><span class="sxs-lookup"><span data-stu-id="c5fa3-149">Before clients or service providers receiving a notification can use the structure to process the event, they must check the event type as indicated in the **ulEventType** member.</span></span> <span data-ttu-id="c5fa3-150">Par exemple, l'exemple de code illustré ci-dessous vérifie l'arrivée d'un nouveau message et, lorsqu'il détecte un événement de ce type, imprime la classe de message du message.</span><span class="sxs-lookup"><span data-stu-id="c5fa3-150">For example, the code sample that is shown here checks for the arrival of a new message and upon detecting an event of this kind, prints out the message class of the message.</span></span> 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

<span data-ttu-id="c5fa3-151">Pour plus d'informations sur la notification, reportez-vous aux rubriques décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c5fa3-151">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="c5fa3-152">**Rubrique**</span><span class="sxs-lookup"><span data-stu-id="c5fa3-152">**Topic**</span></span>|<span data-ttu-id="c5fa3-153">**Description**</span><span class="sxs-lookup"><span data-stu-id="c5fa3-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c5fa3-154">Notification d'événement dans MAPI</span><span class="sxs-lookup"><span data-stu-id="c5fa3-154">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="c5fa3-155">Vue d'ensemble générale des événements de notification et de notification.</span><span class="sxs-lookup"><span data-stu-id="c5fa3-155">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="c5fa3-156">Gestion des notifications</span><span class="sxs-lookup"><span data-stu-id="c5fa3-156">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="c5fa3-157">Présentation de la façon dont les clients doivent gérer les notifications.</span><span class="sxs-lookup"><span data-stu-id="c5fa3-157">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="c5fa3-158">Notification d'événement de prise en charge</span><span class="sxs-lookup"><span data-stu-id="c5fa3-158">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="c5fa3-159">Présentation de la façon dont les fournisseurs de services peuvent utiliser la méthode [IMAPISupport](imapisupportiunknown.md) pour générer des notifications.</span><span class="sxs-lookup"><span data-stu-id="c5fa3-159">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c5fa3-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5fa3-160">See also</span></span>


- [<span data-ttu-id="c5fa3-161">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c5fa3-161">ERROR_NOTIFICATION</span></span>](error_notification.md)  
- [<span data-ttu-id="c5fa3-162">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c5fa3-162">EXTENDED_NOTIFICATION</span></span>](extended_notification.md)  
- [<span data-ttu-id="c5fa3-163">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c5fa3-163">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md)  
- [<span data-ttu-id="c5fa3-164">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c5fa3-164">OBJECT_NOTIFICATION</span></span>](object_notification.md)  
- [<span data-ttu-id="c5fa3-165">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c5fa3-165">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md)  
- [<span data-ttu-id="c5fa3-166">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c5fa3-166">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="c5fa3-167">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="c5fa3-167">MAPI Structures</span></span>](mapi-structures.md)

