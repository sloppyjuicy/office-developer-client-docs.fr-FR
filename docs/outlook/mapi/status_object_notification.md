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
ms.openlocfilehash: ba93cd0343121751ab12514fe3f09e5a480d5b23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582272"
---
# <a name="statusobjectnotification"></a><span data-ttu-id="98da4-103">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="98da4-103">STATUS_OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="98da4-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98da4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98da4-105">Décrit un objet état qui a été affecté par une modification.</span><span class="sxs-lookup"><span data-stu-id="98da4-105">Describes a status object that has been affected by a change.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="98da4-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="98da4-106">Header file:</span></span>  <br/> |<span data-ttu-id="98da4-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="98da4-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cValues;
  LPSPropValue lpPropVals;
} STATUS_OBJECT_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="98da4-108">Members</span><span class="sxs-lookup"><span data-stu-id="98da4-108">Members</span></span>

 <span data-ttu-id="98da4-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="98da4-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="98da4-110">Nombre d’octets de l’identificateur d’entrée vers laquelle pointe le membre **lpEntryID** .</span><span class="sxs-lookup"><span data-stu-id="98da4-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="98da4-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="98da4-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="98da4-112">Pointeur vers l’identificateur d’entrée de l’objet état modifié.</span><span class="sxs-lookup"><span data-stu-id="98da4-112">Pointer to the entry identifier of the changed status object.</span></span>
    
 <span data-ttu-id="98da4-113">**cValues**</span><span class="sxs-lookup"><span data-stu-id="98da4-113">**cValues**</span></span>
  
> <span data-ttu-id="98da4-114">Nombre de structures [SPropValue](spropvalue.md) dans le tableau indiqué par le membre **lpPropVals** .</span><span class="sxs-lookup"><span data-stu-id="98da4-114">Count of [SPropValue](spropvalue.md) structures in the array pointed to by the **lpPropVals** member.</span></span> 
    
 <span data-ttu-id="98da4-115">**lpPropVals**</span><span class="sxs-lookup"><span data-stu-id="98da4-115">**lpPropVals**</span></span>
  
> <span data-ttu-id="98da4-116">Pointeur vers un tableau de structures **SPropValue** qui décrivent les propriétés de l’objet état modifié.</span><span class="sxs-lookup"><span data-stu-id="98da4-116">Pointer to an array of **SPropValue** structures that describe the properties of the changed status object.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="98da4-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="98da4-117">Remarks</span></span>

<span data-ttu-id="98da4-118">La structure **STATUS_OBJECT_NOTIFICATION** est un des membres de l’union de structures inclus dans le membre **info** de la structure de [NOTIFICATION](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="98da4-118">The **STATUS_OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="98da4-119">La structure **STATUS_OBJECT_NOTIFICATION** est incluse dans une notification d’objet état pour un événement de type _fnevStatusObjectModified_.</span><span class="sxs-lookup"><span data-stu-id="98da4-119">The **STATUS_OBJECT_NOTIFICATION** structure is included with a status object notification for an event of type  _fnevStatusObjectModified_.</span></span> <span data-ttu-id="98da4-120">Notification d’état d’objet est une notification MAPI interne ; clients et fournisseurs de services ne peut pas inscrire pour qu’il et il ne peut pas générer des fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="98da4-120">Status object notification is an internal MAPI notification; clients and service providers cannot register for it and service providers cannot generate it.</span></span>
  
<span data-ttu-id="98da4-121">Pour plus d’informations sur la notification, consultez les rubriques décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="98da4-121">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="98da4-122">**Rubrique**</span><span class="sxs-lookup"><span data-stu-id="98da4-122">**Topic**</span></span>|<span data-ttu-id="98da4-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="98da4-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="98da4-124">Notification d’événement dans MAPI</span><span class="sxs-lookup"><span data-stu-id="98da4-124">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="98da4-125">Vue d’ensemble des notifications et les événements de notification.</span><span class="sxs-lookup"><span data-stu-id="98da4-125">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="98da4-126">Gestion des notifications</span><span class="sxs-lookup"><span data-stu-id="98da4-126">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="98da4-127">Étude de la façon dont les clients doivent gérer les notifications.</span><span class="sxs-lookup"><span data-stu-id="98da4-127">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="98da4-128">Prise en charge des notifications d’événements</span><span class="sxs-lookup"><span data-stu-id="98da4-128">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="98da4-129">Étude de comment les fournisseurs de services peuvent utiliser la méthode **IMAPISupport** pour générer des notifications.</span><span class="sxs-lookup"><span data-stu-id="98da4-129">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="98da4-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98da4-130">See also</span></span>



[<span data-ttu-id="98da4-131">Notification</span><span class="sxs-lookup"><span data-stu-id="98da4-131">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="98da4-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="98da4-132">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="98da4-133">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="98da4-133">MAPI Structures</span></span>](mapi-structures.md)

