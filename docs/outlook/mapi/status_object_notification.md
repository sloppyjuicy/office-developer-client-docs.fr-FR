---
title: STATUS_OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STATUS_OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: 2872130d-a36b-46ea-bfd1-4700fe3dd41b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 84b44b4b054a2b2617502a6a463a6d4a89546804
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426267"
---
# <a name="statusobjectnotification"></a><span data-ttu-id="bd7f1-103">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="bd7f1-103">STATUS_OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="bd7f1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd7f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd7f1-105">Décrit un objet Status qui a été affecté par une modification.</span><span class="sxs-lookup"><span data-stu-id="bd7f1-105">Describes a status object that has been affected by a change.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bd7f1-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="bd7f1-106">Header file:</span></span>  <br/> |<span data-ttu-id="bd7f1-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="bd7f1-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cValues;
  LPSPropValue lpPropVals;
} STATUS_OBJECT_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="bd7f1-108">Members</span><span class="sxs-lookup"><span data-stu-id="bd7f1-108">Members</span></span>

 <span data-ttu-id="bd7f1-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="bd7f1-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="bd7f1-110">Nombre d'octets dans l'identificateur d'entrée vers lequel pointe le membre **lpEntryID** .</span><span class="sxs-lookup"><span data-stu-id="bd7f1-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="bd7f1-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="bd7f1-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="bd7f1-112">Pointeur vers l'identificateur d'entrée de l'objet d'état modifié.</span><span class="sxs-lookup"><span data-stu-id="bd7f1-112">Pointer to the entry identifier of the changed status object.</span></span>
    
 <span data-ttu-id="bd7f1-113">**cValues**</span><span class="sxs-lookup"><span data-stu-id="bd7f1-113">**cValues**</span></span>
  
> <span data-ttu-id="bd7f1-114">Nombre de structures [SPropValue](spropvalue.md) dans le tableau vers lequel pointe le membre **lpPropVals** .</span><span class="sxs-lookup"><span data-stu-id="bd7f1-114">Count of [SPropValue](spropvalue.md) structures in the array pointed to by the **lpPropVals** member.</span></span> 
    
 <span data-ttu-id="bd7f1-115">**lpPropVals**</span><span class="sxs-lookup"><span data-stu-id="bd7f1-115">**lpPropVals**</span></span>
  
> <span data-ttu-id="bd7f1-116">Pointeur vers un tableau de structures **SPropValue** qui décrivent les propriétés de l'objet d'état modifié.</span><span class="sxs-lookup"><span data-stu-id="bd7f1-116">Pointer to an array of **SPropValue** structures that describe the properties of the changed status object.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="bd7f1-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="bd7f1-117">Remarks</span></span>

<span data-ttu-id="bd7f1-118">La structure **STATUS_OBJECT_NOTIFICATION** est l'un des membres de l'Union des structures incluses dans le membre **info** de la structure de [notification](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="bd7f1-118">The **STATUS_OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="bd7f1-119">La structure **STATUS_OBJECT_NOTIFICATION** est incluse avec une notification d'objet d'État pour un événement de type _fnevStatusObjectModified_.</span><span class="sxs-lookup"><span data-stu-id="bd7f1-119">The **STATUS_OBJECT_NOTIFICATION** structure is included with a status object notification for an event of type  _fnevStatusObjectModified_.</span></span> <span data-ttu-id="bd7f1-120">La notification d'objet d'État est une notification MAPI interne; les clients et les fournisseurs de services ne peuvent pas s'inscrire à l'informatique et les fournisseurs de services ne peuvent pas le générer.</span><span class="sxs-lookup"><span data-stu-id="bd7f1-120">Status object notification is an internal MAPI notification; clients and service providers cannot register for it and service providers cannot generate it.</span></span>
  
<span data-ttu-id="bd7f1-121">Pour plus d'informations sur la notification, reportez-vous aux rubriques décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="bd7f1-121">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="bd7f1-122">**Rubrique**</span><span class="sxs-lookup"><span data-stu-id="bd7f1-122">**Topic**</span></span>|<span data-ttu-id="bd7f1-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="bd7f1-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bd7f1-124">Notification d'événement dans MAPI</span><span class="sxs-lookup"><span data-stu-id="bd7f1-124">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="bd7f1-125">Vue d'ensemble générale des événements de notification et de notification.</span><span class="sxs-lookup"><span data-stu-id="bd7f1-125">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="bd7f1-126">Gestion des notifications</span><span class="sxs-lookup"><span data-stu-id="bd7f1-126">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="bd7f1-127">Présentation de la façon dont les clients doivent gérer les notifications.</span><span class="sxs-lookup"><span data-stu-id="bd7f1-127">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="bd7f1-128">Notification d'événement de prise en charge</span><span class="sxs-lookup"><span data-stu-id="bd7f1-128">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="bd7f1-129">Présentation de la façon dont les fournisseurs de services peuvent utiliser la méthode **IMAPISupport** pour générer des notifications.</span><span class="sxs-lookup"><span data-stu-id="bd7f1-129">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bd7f1-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd7f1-130">See also</span></span>



[<span data-ttu-id="bd7f1-131">Notification</span><span class="sxs-lookup"><span data-stu-id="bd7f1-131">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="bd7f1-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="bd7f1-132">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="bd7f1-133">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="bd7f1-133">MAPI Structures</span></span>](mapi-structures.md)

