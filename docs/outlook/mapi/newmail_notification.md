---
title: NEWMAIL_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NEWMAIL_NOTIFICATION
api_type:
- COM
ms.assetid: 49913050-900a-4b05-84c4-c596a93ce68b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: aad4d3be8757ca4cd7719bfd7a53ae8bbf6711f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784902"
---
# <a name="newmailnotification"></a><span data-ttu-id="4b3d2-103">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4b3d2-103">NEWMAIL_NOTIFICATION</span></span>

  
  
<span data-ttu-id="4b3d2-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4b3d2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4b3d2-105">Décrit les informations qui sont associées à l’arrivée d’un nouveau message.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-105">Describes information that relate to the arrival of a new message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4b3d2-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="4b3d2-106">Header file:</span></span>  <br/> |<span data-ttu-id="4b3d2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4b3d2-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _NEWMAIL_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cbParentID;
  LPENTRYID lpParentID;
  ULONG ulFlags;
  LPSTR lpszMessageClass;
  ULONG ulMessageFlags;
} NEWMAIL_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="4b3d2-108">Membres</span><span class="sxs-lookup"><span data-stu-id="4b3d2-108">Members</span></span>

 <span data-ttu-id="4b3d2-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="4b3d2-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="4b3d2-110">Nombre d’octets de l’identificateur d’entrée vers laquelle pointe le membre **lpEntryID** .</span><span class="sxs-lookup"><span data-stu-id="4b3d2-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="4b3d2-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="4b3d2-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="4b3d2-112">Pointeur vers l’identificateur d’entrée du message qui vient d’arriver.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-112">Pointer to the entry identifier of the newly arrived message.</span></span>
    
 <span data-ttu-id="4b3d2-113">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="4b3d2-113">**cbParentID**</span></span>
  
> <span data-ttu-id="4b3d2-114">Nombre d’octets de l’identificateur d’entrée vers laquelle pointe le membre **lpParentID** .</span><span class="sxs-lookup"><span data-stu-id="4b3d2-114">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="4b3d2-115">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="4b3d2-115">**lpParentID**</span></span>
  
> <span data-ttu-id="4b3d2-116">Pointeur vers l’identificateur d’entrée du dossier de réception pour le message qui vient d’arriver.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-116">Pointer to the entry identifier of the receive folder for the newly arrived message.</span></span>
    
 <span data-ttu-id="4b3d2-117">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="4b3d2-117">**ulFlags**</span></span>
  
> <span data-ttu-id="4b3d2-118">Masque de bits d’indicateurs utilisés pour décrire le format des propriétés de chaîne inclus dans le message.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-118">Bitmask of flags used to describe the format of the string properties included with the message.</span></span> <span data-ttu-id="4b3d2-119">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="4b3d2-119">The following flag can be set:</span></span>
    
<span data-ttu-id="4b3d2-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4b3d2-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="4b3d2-121">Les chaînes passée sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-121">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="4b3d2-122">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="4b3d2-123">**lpszMessageClass**</span><span class="sxs-lookup"><span data-stu-id="4b3d2-123">**lpszMessageClass**</span></span>
  
> <span data-ttu-id="4b3d2-124">Pointeur vers la classe de message du message qui vient d’arriver.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-124">Pointer to the message class of the newly arrived message.</span></span> 
    
 <span data-ttu-id="4b3d2-125">**ulMessageFlags**</span><span class="sxs-lookup"><span data-stu-id="4b3d2-125">**ulMessageFlags**</span></span>
  
> <span data-ttu-id="4b3d2-126">Masque de bits d’indicateurs qui décrit l’état actuel du message qui vient d’arriver.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-126">Bitmask of flags that describes the current state of the newly arrived message.</span></span> <span data-ttu-id="4b3d2-127">Le membre **ulMessageFlags** est une copie de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-127">The **ulMessageFlags** member is a copy of the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4b3d2-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="4b3d2-128">Remarks</span></span>

<span data-ttu-id="4b3d2-129">La structure **NEWMAIL_NOTIFICATION** est un des membres de l’union de structures inclus dans le membre **info** de la structure de [NOTIFICATION](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="4b3d2-129">The **NEWMAIL_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="4b3d2-130">Lorsque le membre **info** d’une structure **NOTIFICATION** contient une structure **NEWMAIL_NOTIFICATION** , le membre **ulEventType** de la structure de **NOTIFICATION** est défini sur _fnevNewMail._</span><span class="sxs-lookup"><span data-stu-id="4b3d2-130">When the **info** member of a **NOTIFICATION** structure contains a **NEWMAIL_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevNewMail._</span></span>
  
<span data-ttu-id="4b3d2-131">MAPI utilise la structure **NEWMAIL_NOTIFICATION** uniquement en tant que membre de la structure **NOTIFICATION** , qui conserve des informations sur un événement de notification pour le récepteur de notifications.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-131">MAPI uses the **NEWMAIL_NOTIFICATION** structure only as a member of the **NOTIFICATION** structure, which holds information about a notification event for the advise sink.</span></span> 
  
<span data-ttu-id="4b3d2-132">Pour plus d’informations sur la notification, consultez les rubriques décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-132">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="4b3d2-133">**Rubrique**</span><span class="sxs-lookup"><span data-stu-id="4b3d2-133">**Topic**</span></span>|<span data-ttu-id="4b3d2-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="4b3d2-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4b3d2-135">Notification d’événement MAPI</span><span class="sxs-lookup"><span data-stu-id="4b3d2-135">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="4b3d2-136">Vue d’ensemble des notifications et les événements de notification.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-136">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="4b3d2-137">Gérer les Notifications</span><span class="sxs-lookup"><span data-stu-id="4b3d2-137">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="4b3d2-138">Étude de la façon dont les clients doivent gérer les notifications.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-138">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="4b3d2-139">Prise en charge de la Notification d’événement</span><span class="sxs-lookup"><span data-stu-id="4b3d2-139">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="4b3d2-140">Étude de comment les fournisseurs de services peuvent utiliser la méthode [IMAPISupport](imapisupportiunknown.md) pour générer des notifications.</span><span class="sxs-lookup"><span data-stu-id="4b3d2-140">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4b3d2-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b3d2-141">See also</span></span>



[<span data-ttu-id="4b3d2-142">Notification</span><span class="sxs-lookup"><span data-stu-id="4b3d2-142">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="4b3d2-143">Propriété canonique PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="4b3d2-143">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)


[<span data-ttu-id="4b3d2-144">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="4b3d2-144">MAPI Structures</span></span>](mapi-structures.md)

