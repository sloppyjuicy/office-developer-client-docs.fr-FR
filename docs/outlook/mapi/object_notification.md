---
title: OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: de3a2297-e0cc-427b-a978-52bade4d9bce
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c637b3b03a22f208123397f7277cf8968f2509a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430167"
---
# <a name="objectnotification"></a><span data-ttu-id="c8414-103">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c8414-103">OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="c8414-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8414-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8414-105">Contient des informations sur un objet qui a subi une modification, comme une opération de copie ou de modification.</span><span class="sxs-lookup"><span data-stu-id="c8414-105">Contains information about an object that has undergone a change, such as being copied or modified.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c8414-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c8414-106">Header file:</span></span>  <br/> |<span data-ttu-id="c8414-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c8414-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _OBJECT_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG ulObjType;
  ULONG cbParentID;
  LPENTRYID lpParentID;
  ULONG cbOldID;
  LPENTRYID lpOldID;
  ULONG cbOldParentID;
  LPENTRYID lpOldParentID;
  LPSPropTagArray lpPropTagArray;
} OBJECT_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="c8414-108">Members</span><span class="sxs-lookup"><span data-stu-id="c8414-108">Members</span></span>

 <span data-ttu-id="c8414-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="c8414-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="c8414-110">Nombre d'octets dans l'identificateur d'entrée vers lequel pointe le membre **lpEntryID** .</span><span class="sxs-lookup"><span data-stu-id="c8414-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="c8414-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="c8414-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="c8414-112">Pointeur vers l'identificateur d'entrée de l'objet affecté.</span><span class="sxs-lookup"><span data-stu-id="c8414-112">Pointer to the entry identifier of the affected object.</span></span>
    
 <span data-ttu-id="c8414-113">**ulObjType**</span><span class="sxs-lookup"><span data-stu-id="c8414-113">**ulObjType**</span></span>
  
> <span data-ttu-id="c8414-114">Type d'objet affecté.</span><span class="sxs-lookup"><span data-stu-id="c8414-114">Type of object affected.</span></span> <span data-ttu-id="c8414-115">Les types possibles sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="c8414-115">Possible types are as follows:</span></span>
    
<span data-ttu-id="c8414-116">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="c8414-116">MAPI_STORE</span></span> 
  
> <span data-ttu-id="c8414-117">Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="c8414-117">Message store.</span></span> 
    
<span data-ttu-id="c8414-118">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="c8414-118">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="c8414-119">Carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="c8414-119">Address book.</span></span> 
    
<span data-ttu-id="c8414-120">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="c8414-120">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="c8414-121">Sous.</span><span class="sxs-lookup"><span data-stu-id="c8414-121">Folder.</span></span>
    
<span data-ttu-id="c8414-122">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="c8414-122">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="c8414-123">Conteneur de carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="c8414-123">Address book container.</span></span>
    
<span data-ttu-id="c8414-124">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="c8414-124">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="c8414-125">Message.</span><span class="sxs-lookup"><span data-stu-id="c8414-125">Message.</span></span>
    
<span data-ttu-id="c8414-126">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="c8414-126">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="c8414-127">Utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="c8414-127">Messaging user.</span></span>
    
<span data-ttu-id="c8414-128">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="c8414-128">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="c8414-129">Connexion.</span><span class="sxs-lookup"><span data-stu-id="c8414-129">Attachment.</span></span>
    
<span data-ttu-id="c8414-130">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="c8414-130">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="c8414-131">Liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="c8414-131">Distribution list.</span></span>
    
<span data-ttu-id="c8414-132">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="c8414-132">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="c8414-133">Section profil.</span><span class="sxs-lookup"><span data-stu-id="c8414-133">Profile section.</span></span>
    
<span data-ttu-id="c8414-134">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="c8414-134">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="c8414-135">Objet Status.</span><span class="sxs-lookup"><span data-stu-id="c8414-135">Status object.</span></span>
    
<span data-ttu-id="c8414-136">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="c8414-136">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="c8414-137">Objet session.</span><span class="sxs-lookup"><span data-stu-id="c8414-137">Session object.</span></span>
    
 <span data-ttu-id="c8414-138">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="c8414-138">**cbParentID**</span></span>
  
> <span data-ttu-id="c8414-139">Nombre d'octets dans l'identificateur d'entrée vers lequel pointe le membre **lpParentID** .</span><span class="sxs-lookup"><span data-stu-id="c8414-139">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="c8414-140">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="c8414-140">**lpParentID**</span></span>
  
> <span data-ttu-id="c8414-141">Pointeur vers l'identificateur d'entrée du parent de l'objet affecté.</span><span class="sxs-lookup"><span data-stu-id="c8414-141">Pointer to the entry identifier of the parent of the affected object.</span></span>
    
 <span data-ttu-id="c8414-142">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="c8414-142">**cbOldID**</span></span>
  
> <span data-ttu-id="c8414-143">Nombre d'octets dans l'identificateur d'entrée vers lequel pointe le membre **lpOldID** .</span><span class="sxs-lookup"><span data-stu-id="c8414-143">Count of bytes in the entry identifier pointed to by the **lpOldID** member.</span></span> 
    
 <span data-ttu-id="c8414-144">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="c8414-144">**lpOldID**</span></span>
  
> <span data-ttu-id="c8414-145">Pointeur vers l'identificateur d'entrée de l'objet d'origine.</span><span class="sxs-lookup"><span data-stu-id="c8414-145">Pointer to the entry identifier of the original object.</span></span> <span data-ttu-id="c8414-146">Ce pointeur peut être NULL si l'événement ne requiert pas d'objet d'origine.</span><span class="sxs-lookup"><span data-stu-id="c8414-146">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="c8414-147">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="c8414-147">**cbOldParentID**</span></span>
  
> <span data-ttu-id="c8414-148">Nombre d'octets dans l'identificateur d'entrée vers lequel pointe le membre **lpOldParentID** .</span><span class="sxs-lookup"><span data-stu-id="c8414-148">Count of bytes in the entry identifier pointed to by the **lpOldParentID** member.</span></span> 
    
 <span data-ttu-id="c8414-149">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="c8414-149">**lpOldParentID**</span></span>
  
> <span data-ttu-id="c8414-150">Pointeur vers l'identificateur d'entrée du parent de l'objet d'origine.</span><span class="sxs-lookup"><span data-stu-id="c8414-150">Pointer to the entry identifier of the parent of the original object.</span></span> <span data-ttu-id="c8414-151">Ce pointeur peut être NULL si l'événement ne requiert pas d'objet d'origine.</span><span class="sxs-lookup"><span data-stu-id="c8414-151">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="c8414-152">**lpPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="c8414-152">**lpPropTagArray**</span></span>
  
> <span data-ttu-id="c8414-153">Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient les balises de propriété qui identifient les propriétés affectées par l'événement.</span><span class="sxs-lookup"><span data-stu-id="c8414-153">Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the property tags identifying properties affected by the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c8414-154">Remarques</span><span class="sxs-lookup"><span data-stu-id="c8414-154">Remarks</span></span>

<span data-ttu-id="c8414-155">La structure **OBJECT_NOTIFICATION** est l'un des membres de l'Union des structures incluses dans le membre **info** de la structure de [notification](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="c8414-155">The **OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="c8414-156">Lorsque le membre **info** d'une structure de **notification** contient une structure **OBJECT_NOTIFICATION** , le membre **ulEventType** de la structure de **notification** est défini sur l'un des types d'événements suivants:</span><span class="sxs-lookup"><span data-stu-id="c8414-156">When the **info** member of a **NOTIFICATION** structure contains an **OBJECT_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to one of the following types of events:</span></span> 
  
- <span data-ttu-id="c8414-157">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="c8414-157">fnevObjectCreated</span></span>
    
- <span data-ttu-id="c8414-158">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="c8414-158">fnevObjectModified</span></span>
    
- <span data-ttu-id="c8414-159">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="c8414-159">fnevObjectDeleted</span></span>
    
- <span data-ttu-id="c8414-160">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="c8414-160">fnevObjectMoved</span></span>
    
- <span data-ttu-id="c8414-161">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="c8414-161">fnevObjectCopied</span></span>
    
- <span data-ttu-id="c8414-162">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="c8414-162">fnevSearchComplete</span></span>
    
<span data-ttu-id="c8414-163">L'événement de recherche terminée, représenté par le type d'événement fnevSearchComplete, indique que la recherche initiale du domaine pour un dossier de recherche est terminée.</span><span class="sxs-lookup"><span data-stu-id="c8414-163">The search complete event, represented by the fnevSearchComplete event type, indicates that the initial search of the domain for one search folder has completed.</span></span>
  
<span data-ttu-id="c8414-164">Les membres suivants qui contiennent des informations sur l'objet d'origine sont utilisés uniquement dans les événements de déplacement et de copie.</span><span class="sxs-lookup"><span data-stu-id="c8414-164">The following members that contain information about the original object are used only in move and copy events.</span></span> 
  
- <span data-ttu-id="c8414-165">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="c8414-165">**cbOldID**</span></span>
    
- <span data-ttu-id="c8414-166">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="c8414-166">**lpOldID**</span></span>
    
- <span data-ttu-id="c8414-167">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="c8414-167">**cbOldParentID**</span></span>
    
- <span data-ttu-id="c8414-168">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="c8414-168">**lpOldParentID**</span></span>
    
<span data-ttu-id="c8414-169">Ces membres ne s'appliquent pas aux autres types d'événements.</span><span class="sxs-lookup"><span data-stu-id="c8414-169">These members do not apply to the other types of events.</span></span>
  
<span data-ttu-id="c8414-170">Pour plus d'informations sur la notification, reportez-vous aux rubriques décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c8414-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="c8414-171">**Rubrique**</span><span class="sxs-lookup"><span data-stu-id="c8414-171">**Topic**</span></span>|<span data-ttu-id="c8414-172">**Description**</span><span class="sxs-lookup"><span data-stu-id="c8414-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8414-173">Notification d'événement dans MAPI</span><span class="sxs-lookup"><span data-stu-id="c8414-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="c8414-174">Vue d'ensemble générale des événements de notification et de notification.</span><span class="sxs-lookup"><span data-stu-id="c8414-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="c8414-175">Gestion des notifications</span><span class="sxs-lookup"><span data-stu-id="c8414-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="c8414-176">Présentation de la façon dont les clients doivent gérer les notifications.</span><span class="sxs-lookup"><span data-stu-id="c8414-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="c8414-177">Notification d'événement de prise en charge</span><span class="sxs-lookup"><span data-stu-id="c8414-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="c8414-178">Présentation de la façon dont les fournisseurs de services peuvent utiliser la méthode [IMAPISupport](imapisupportiunknown.md) pour générer des notifications.</span><span class="sxs-lookup"><span data-stu-id="c8414-178">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c8414-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8414-179">See also</span></span>



[<span data-ttu-id="c8414-180">Notification</span><span class="sxs-lookup"><span data-stu-id="c8414-180">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="c8414-181">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="c8414-181">SPropTagArray</span></span>](sproptagarray.md)


[<span data-ttu-id="c8414-182">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="c8414-182">MAPI Structures</span></span>](mapi-structures.md)

