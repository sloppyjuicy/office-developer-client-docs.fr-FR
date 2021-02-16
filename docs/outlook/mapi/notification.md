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
# <a name="notification"></a><span data-ttu-id="65058-103">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="65058-103">NOTIFICATION</span></span>
 
<span data-ttu-id="65058-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65058-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65058-105">Contient des informations sur un événement qui s’est produit et les données qui ont été affectées par l’événement.</span><span class="sxs-lookup"><span data-stu-id="65058-105">Contains information about an event that has occurred and the data that has been affected by the event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="65058-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="65058-106">Header file:</span></span>  <br/> |<span data-ttu-id="65058-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="65058-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="65058-108">Members</span><span class="sxs-lookup"><span data-stu-id="65058-108">Members</span></span>

<span data-ttu-id="65058-109">**ulEventType**</span><span class="sxs-lookup"><span data-stu-id="65058-109">**ulEventType**</span></span>
  
> <span data-ttu-id="65058-110">Type d’événement de notification qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="65058-110">Type of notification event that occurred.</span></span> <span data-ttu-id="65058-111">La valeur du **membre ulEventType** correspond à la structure incluse dans l’union **d’informations.**</span><span class="sxs-lookup"><span data-stu-id="65058-111">The value of the **ulEventType** member corresponds to the structure that is included in the **info** union.</span></span> <span data-ttu-id="65058-112">Le **membre ulEventType** peut être définie sur l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="65058-112">The **ulEventType** member can be set to one of the following values:</span></span> 
    
 <span data-ttu-id="65058-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="65058-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="65058-114">Une erreur globale s’est produite, telle qu’une session en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="65058-114">A global error has occurred, such as a session shut down in progress.</span></span> <span data-ttu-id="65058-115">Le **membre d’informations** contient [ERROR_NOTIFICATION](error_notification.md) structure.</span><span class="sxs-lookup"><span data-stu-id="65058-115">The **info** member contains an [ERROR_NOTIFICATION](error_notification.md) structure.</span></span> 
    
 <span data-ttu-id="65058-116">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="65058-116">_fnevExtended_</span></span>
  
> <span data-ttu-id="65058-117">Un événement interne défini par un fournisseur de services particulier s’est produit.</span><span class="sxs-lookup"><span data-stu-id="65058-117">An internal event defined by a particular service provider has occurred.</span></span> <span data-ttu-id="65058-118">Le **membre d’informations** contient [une structure EXTENDED_NOTIFICATION](extended_notification.md) de données.</span><span class="sxs-lookup"><span data-stu-id="65058-118">The **info** member contains an [EXTENDED_NOTIFICATION](extended_notification.md) structure.</span></span> 
    
 <span data-ttu-id="65058-119">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="65058-119">_fnevNewMail_</span></span>
  
> <span data-ttu-id="65058-120">Un message a été remis au dossier de réception approprié pour la classe de message et attend d’être traitée.</span><span class="sxs-lookup"><span data-stu-id="65058-120">A message has been delivered to the appropriate receive folder for the message class and is waiting to be processed.</span></span> <span data-ttu-id="65058-121">Le **membre d’informations** contient [une structure NEWMAIL_NOTIFICATION](newmail_notification.md) de données.</span><span class="sxs-lookup"><span data-stu-id="65058-121">The **info** member contains an [NEWMAIL_NOTIFICATION](newmail_notification.md) structure.</span></span> 
    
 <span data-ttu-id="65058-122">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="65058-122">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="65058-123">Un objet MAPI a été copié.</span><span class="sxs-lookup"><span data-stu-id="65058-123">A MAPI object has been copied.</span></span> <span data-ttu-id="65058-124">Le **membre d’informations** contient [une structure OBJECT_NOTIFICATION](object_notification.md) de données.</span><span class="sxs-lookup"><span data-stu-id="65058-124">The **info** member contains an [OBJECT_NOTIFICATION](object_notification.md) structure.</span></span> 
    
 <span data-ttu-id="65058-125">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="65058-125">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="65058-126">Un objet MAPI a été créé.</span><span class="sxs-lookup"><span data-stu-id="65058-126">A MAPI object has been created.</span></span> <span data-ttu-id="65058-127">Le **membre d’informations** contient **une structure OBJECT_NOTIFICATION** de données.</span><span class="sxs-lookup"><span data-stu-id="65058-127">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="65058-128">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="65058-128">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="65058-129">Un objet MAPI a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="65058-129">A MAPI object has been deleted.</span></span> <span data-ttu-id="65058-130">Le **membre d’informations** contient **une structure OBJECT_NOTIFICATION** de données.</span><span class="sxs-lookup"><span data-stu-id="65058-130">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="65058-131">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="65058-131">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="65058-132">Un objet MAPI a changé.</span><span class="sxs-lookup"><span data-stu-id="65058-132">A MAPI object has changed.</span></span> <span data-ttu-id="65058-133">Le **membre d’informations** contient **une structure OBJECT_NOTIFICATION** de données.</span><span class="sxs-lookup"><span data-stu-id="65058-133">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="65058-134">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="65058-134">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="65058-135">Un objet de magasin de messages ou de carnet d’adresses a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="65058-135">A message store or address book object has been moved.</span></span> <span data-ttu-id="65058-136">Le **membre d’informations** contient **une structure OBJECT_NOTIFICATION** de données.</span><span class="sxs-lookup"><span data-stu-id="65058-136">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="65058-137">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="65058-137">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="65058-138">Une opération de recherche est terminée et les résultats sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="65058-138">A search operation has finished and the results are available.</span></span> <span data-ttu-id="65058-139">Le **membre d’informations** contient **une structure OBJECT_NOTIFICATION** de données.</span><span class="sxs-lookup"><span data-stu-id="65058-139">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="65058-140">_fnevTableModified_</span><span class="sxs-lookup"><span data-stu-id="65058-140">_fnevTableModified_</span></span>
  
> <span data-ttu-id="65058-141">Les informations d’un tableau ont changé.</span><span class="sxs-lookup"><span data-stu-id="65058-141">Information in a table has changed.</span></span> <span data-ttu-id="65058-142">Le **membre d’informations** contient une structure [TABLE_NOTIFICATION](table_notification.md) de données.</span><span class="sxs-lookup"><span data-stu-id="65058-142">The **info** member contains an [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    
<span data-ttu-id="65058-143">**info**</span><span class="sxs-lookup"><span data-stu-id="65058-143">**info**</span></span>
  
> <span data-ttu-id="65058-144">Union des structures de notification décrivant les données affectées pour un type particulier d’événement.</span><span class="sxs-lookup"><span data-stu-id="65058-144">Union of notification structures describing the affected data for a particular type of event.</span></span> <span data-ttu-id="65058-145">La structure incluse dans le membre **d’informations** dépend de la valeur du **membre ulEventType.**</span><span class="sxs-lookup"><span data-stu-id="65058-145">The structure included in the **info** member depends on the value of the **ulEventType** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="65058-146">Remarques</span><span class="sxs-lookup"><span data-stu-id="65058-146">Remarks</span></span>

<span data-ttu-id="65058-147">Une ou plusieurs structures **DE NOTIFICATION** sont transmises en tant que paramètres d’entrée à chaque appel à la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) d’un sink de notification inscrit.</span><span class="sxs-lookup"><span data-stu-id="65058-147">One or more **NOTIFICATION** structures are passed as input parameters with every call to a registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="65058-148">Les **structures NOTIFICATION** contiennent des informations sur les événements particuliers qui se sont produits et décrivent les objets affectés.</span><span class="sxs-lookup"><span data-stu-id="65058-148">The **NOTIFICATION** structures contain information about the particular events that have occurred and describe the affected objects.</span></span> 
  
<span data-ttu-id="65058-149">Avant que les clients ou fournisseurs de services recevant une notification ne peuvent utiliser la structure pour traiter l’événement, ils doivent vérifier le type d’événement comme indiqué dans le membre **ulEventType.**</span><span class="sxs-lookup"><span data-stu-id="65058-149">Before clients or service providers receiving a notification can use the structure to process the event, they must check the event type as indicated in the **ulEventType** member.</span></span> <span data-ttu-id="65058-150">Par exemple, l’exemple de code présenté ici vérifie l’arrivée d’un nouveau message et, lorsqu’il détecte un événement de ce type, imprime la classe de message du message.</span><span class="sxs-lookup"><span data-stu-id="65058-150">For example, the code sample that is shown here checks for the arrival of a new message and upon detecting an event of this kind, prints out the message class of the message.</span></span> 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

<span data-ttu-id="65058-151">Pour plus d’informations sur la notification, voir les rubriques décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="65058-151">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="65058-152">**Rubrique**</span><span class="sxs-lookup"><span data-stu-id="65058-152">**Topic**</span></span>|<span data-ttu-id="65058-153">**Description**</span><span class="sxs-lookup"><span data-stu-id="65058-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65058-154">Notification d’événement dans MAPI</span><span class="sxs-lookup"><span data-stu-id="65058-154">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="65058-155">Vue d’ensemble des événements de notification et de notification.</span><span class="sxs-lookup"><span data-stu-id="65058-155">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="65058-156">Gestion des notifications</span><span class="sxs-lookup"><span data-stu-id="65058-156">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="65058-157">Discussion sur la façon dont les clients doivent gérer les notifications.</span><span class="sxs-lookup"><span data-stu-id="65058-157">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="65058-158">Prise en charge des notifications d’événement</span><span class="sxs-lookup"><span data-stu-id="65058-158">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="65058-159">Discussion sur la façon dont les fournisseurs de services peuvent utiliser la méthode [IMAPISupport](imapisupportiunknown.md) pour générer des notifications.</span><span class="sxs-lookup"><span data-stu-id="65058-159">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="65058-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65058-160">See also</span></span>


- [<span data-ttu-id="65058-161">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="65058-161">ERROR_NOTIFICATION</span></span>](error_notification.md)  
- [<span data-ttu-id="65058-162">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="65058-162">EXTENDED_NOTIFICATION</span></span>](extended_notification.md)  
- [<span data-ttu-id="65058-163">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="65058-163">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md)  
- [<span data-ttu-id="65058-164">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="65058-164">OBJECT_NOTIFICATION</span></span>](object_notification.md)  
- [<span data-ttu-id="65058-165">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="65058-165">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md)  
- [<span data-ttu-id="65058-166">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="65058-166">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="65058-167">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="65058-167">MAPI Structures</span></span>](mapi-structures.md)

