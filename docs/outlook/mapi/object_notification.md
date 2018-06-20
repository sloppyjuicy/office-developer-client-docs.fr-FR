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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1593152786a3345827089e5f6702454896944b1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784922"
---
# <a name="objectnotification"></a><span data-ttu-id="6dc0e-103">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="6dc0e-103">OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="6dc0e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6dc0e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6dc0e-105">Contient des informations sur un objet qui a subi une modification, tel qu’en cours copié ou modifié.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-105">Contains information about an object that has undergone a change, such as being copied or modified.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6dc0e-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="6dc0e-106">Header file:</span></span>  <br/> |<span data-ttu-id="6dc0e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6dc0e-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="6dc0e-108">Membres</span><span class="sxs-lookup"><span data-stu-id="6dc0e-108">Members</span></span>

 <span data-ttu-id="6dc0e-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="6dc0e-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="6dc0e-110">Nombre d’octets de l’identificateur d’entrée vers laquelle pointe le membre **lpEntryID** .</span><span class="sxs-lookup"><span data-stu-id="6dc0e-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="6dc0e-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="6dc0e-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="6dc0e-112">Pointeur vers l’identificateur d’entrée de l’objet concerné.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-112">Pointer to the entry identifier of the affected object.</span></span>
    
 <span data-ttu-id="6dc0e-113">**ulObjType**</span><span class="sxs-lookup"><span data-stu-id="6dc0e-113">**ulObjType**</span></span>
  
> <span data-ttu-id="6dc0e-114">Type d’objet affecté.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-114">Type of object affected.</span></span> <span data-ttu-id="6dc0e-115">Les types possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="6dc0e-115">Possible types are as follows:</span></span>
    
<span data-ttu-id="6dc0e-116">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="6dc0e-116">MAPI_STORE</span></span> 
  
> <span data-ttu-id="6dc0e-117">Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-117">Message store.</span></span> 
    
<span data-ttu-id="6dc0e-118">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="6dc0e-118">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="6dc0e-119">Carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-119">Address book.</span></span> 
    
<span data-ttu-id="6dc0e-120">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="6dc0e-120">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="6dc0e-121">Dossier.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-121">Folder.</span></span>
    
<span data-ttu-id="6dc0e-122">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="6dc0e-122">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="6dc0e-123">Conteneur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-123">Address book container.</span></span>
    
<span data-ttu-id="6dc0e-124">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="6dc0e-124">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="6dc0e-125">Message.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-125">Message.</span></span>
    
<span data-ttu-id="6dc0e-126">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="6dc0e-126">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="6dc0e-127">Utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-127">Messaging user.</span></span>
    
<span data-ttu-id="6dc0e-128">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="6dc0e-128">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="6dc0e-129">Objet Attachment.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-129">Attachment.</span></span>
    
<span data-ttu-id="6dc0e-130">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="6dc0e-130">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="6dc0e-131">Liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-131">Distribution list.</span></span>
    
<span data-ttu-id="6dc0e-132">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="6dc0e-132">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="6dc0e-133">Section de profil.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-133">Profile section.</span></span>
    
<span data-ttu-id="6dc0e-134">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="6dc0e-134">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="6dc0e-135">Objet d’état.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-135">Status object.</span></span>
    
<span data-ttu-id="6dc0e-136">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="6dc0e-136">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="6dc0e-137">Objet de la session.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-137">Session object.</span></span>
    
 <span data-ttu-id="6dc0e-138">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="6dc0e-138">**cbParentID**</span></span>
  
> <span data-ttu-id="6dc0e-139">Nombre d’octets de l’identificateur d’entrée vers laquelle pointe le membre **lpParentID** .</span><span class="sxs-lookup"><span data-stu-id="6dc0e-139">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="6dc0e-140">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="6dc0e-140">**lpParentID**</span></span>
  
> <span data-ttu-id="6dc0e-141">Pointeur vers l’identificateur d’entrée du parent de l’objet concerné.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-141">Pointer to the entry identifier of the parent of the affected object.</span></span>
    
 <span data-ttu-id="6dc0e-142">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="6dc0e-142">**cbOldID**</span></span>
  
> <span data-ttu-id="6dc0e-143">Nombre d’octets de l’identificateur d’entrée vers laquelle pointe le membre **lpOldID** .</span><span class="sxs-lookup"><span data-stu-id="6dc0e-143">Count of bytes in the entry identifier pointed to by the **lpOldID** member.</span></span> 
    
 <span data-ttu-id="6dc0e-144">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="6dc0e-144">**lpOldID**</span></span>
  
> <span data-ttu-id="6dc0e-145">Pointeur vers l’identificateur d’entrée de l’objet d’origine.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-145">Pointer to the entry identifier of the original object.</span></span> <span data-ttu-id="6dc0e-146">Ce pointeur peut être NULL si l’événement ne nécessite pas d’un objet d’origine.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-146">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="6dc0e-147">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="6dc0e-147">**cbOldParentID**</span></span>
  
> <span data-ttu-id="6dc0e-148">Nombre d’octets de l’identificateur d’entrée vers laquelle pointe le membre **lpOldParentID** .</span><span class="sxs-lookup"><span data-stu-id="6dc0e-148">Count of bytes in the entry identifier pointed to by the **lpOldParentID** member.</span></span> 
    
 <span data-ttu-id="6dc0e-149">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="6dc0e-149">**lpOldParentID**</span></span>
  
> <span data-ttu-id="6dc0e-150">Pointeur vers l’identificateur d’entrée du parent de l’objet d’origine.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-150">Pointer to the entry identifier of the parent of the original object.</span></span> <span data-ttu-id="6dc0e-151">Ce pointeur peut être NULL si l’événement ne nécessite pas d’un objet d’origine.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-151">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="6dc0e-152">**lpPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="6dc0e-152">**lpPropTagArray**</span></span>
  
> <span data-ttu-id="6dc0e-153">Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient les étiquettes de propriété identifiant les propriétés affectées par l’événement.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-153">Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the property tags identifying properties affected by the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6dc0e-154">Remarques</span><span class="sxs-lookup"><span data-stu-id="6dc0e-154">Remarks</span></span>

<span data-ttu-id="6dc0e-155">La structure **OBJECT_NOTIFICATION** est un des membres de l’union de structures inclus dans le membre **info** de la structure de [NOTIFICATION](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="6dc0e-155">The **OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="6dc0e-156">Lorsque le membre **d’informations** d’une structure **NOTIFICATION** contient une structure **OBJECT_NOTIFICATION** , le membre **ulEventType** de la structure de **NOTIFICATION** est défini sur un des types suivants d’événements :</span><span class="sxs-lookup"><span data-stu-id="6dc0e-156">When the **info** member of a **NOTIFICATION** structure contains an **OBJECT_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to one of the following types of events:</span></span> 
  
- <span data-ttu-id="6dc0e-157">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="6dc0e-157">fnevObjectCreated</span></span>
    
- <span data-ttu-id="6dc0e-158">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="6dc0e-158">fnevObjectModified</span></span>
    
- <span data-ttu-id="6dc0e-159">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="6dc0e-159">fnevObjectDeleted</span></span>
    
- <span data-ttu-id="6dc0e-160">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="6dc0e-160">fnevObjectMoved</span></span>
    
- <span data-ttu-id="6dc0e-161">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="6dc0e-161">fnevObjectCopied</span></span>
    
- <span data-ttu-id="6dc0e-162">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="6dc0e-162">fnevSearchComplete</span></span>
    
<span data-ttu-id="6dc0e-163">L’événement complete de recherche, représenté par le type d’événement fnevSearchComplete, indique que la recherche initiale du domaine pour un dossier de recherche est terminée.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-163">The search complete event, represented by the fnevSearchComplete event type, indicates that the initial search of the domain for one search folder has completed.</span></span>
  
<span data-ttu-id="6dc0e-164">Les membres suivants qui contiennent des informations sur l’objet d’origine sont utilisés uniquement dans les événements de déplacement et de copie.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-164">The following members that contain information about the original object are used only in move and copy events.</span></span> 
  
- <span data-ttu-id="6dc0e-165">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="6dc0e-165">**cbOldID**</span></span>
    
- <span data-ttu-id="6dc0e-166">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="6dc0e-166">**lpOldID**</span></span>
    
- <span data-ttu-id="6dc0e-167">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="6dc0e-167">**cbOldParentID**</span></span>
    
- <span data-ttu-id="6dc0e-168">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="6dc0e-168">**lpOldParentID**</span></span>
    
<span data-ttu-id="6dc0e-169">Ces membres ne s’appliquent pas aux autres types d’événements.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-169">These members do not apply to the other types of events.</span></span>
  
<span data-ttu-id="6dc0e-170">Pour plus d’informations sur la notification, consultez les rubriques décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="6dc0e-171">**Rubrique**</span><span class="sxs-lookup"><span data-stu-id="6dc0e-171">**Topic**</span></span>|<span data-ttu-id="6dc0e-172">**Description**</span><span class="sxs-lookup"><span data-stu-id="6dc0e-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6dc0e-173">Notification d’événement MAPI</span><span class="sxs-lookup"><span data-stu-id="6dc0e-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="6dc0e-174">Vue d’ensemble des notifications et les événements de notification.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="6dc0e-175">Gérer les Notifications</span><span class="sxs-lookup"><span data-stu-id="6dc0e-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="6dc0e-176">Étude de la façon dont les clients doivent gérer les notifications.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="6dc0e-177">Prise en charge de la Notification d’événement</span><span class="sxs-lookup"><span data-stu-id="6dc0e-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="6dc0e-178">Étude de comment les fournisseurs de services peuvent utiliser la méthode [IMAPISupport](imapisupportiunknown.md) pour générer des notifications.</span><span class="sxs-lookup"><span data-stu-id="6dc0e-178">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6dc0e-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6dc0e-179">See also</span></span>



[<span data-ttu-id="6dc0e-180">Notification</span><span class="sxs-lookup"><span data-stu-id="6dc0e-180">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="6dc0e-181">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="6dc0e-181">SPropTagArray</span></span>](sproptagarray.md)


[<span data-ttu-id="6dc0e-182">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="6dc0e-182">MAPI Structures</span></span>](mapi-structures.md)

