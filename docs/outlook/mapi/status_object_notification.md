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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 71e0a08436c925f0d68d63111722cc01bd73cc5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787271"
---
# <a name="statusobjectnotification"></a><span data-ttu-id="44fb1-103">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="44fb1-103">STATUS_OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="44fb1-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="44fb1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="44fb1-105">Décrit un objet état qui a été affecté par une modification.</span><span class="sxs-lookup"><span data-stu-id="44fb1-105">Describes a status object that has been affected by a change.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="44fb1-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="44fb1-106">Header file:</span></span>  <br/> |<span data-ttu-id="44fb1-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="44fb1-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cValues;
  LPSPropValue lpPropVals;
} STATUS_OBJECT_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="44fb1-108">Membres</span><span class="sxs-lookup"><span data-stu-id="44fb1-108">Members</span></span>

 <span data-ttu-id="44fb1-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="44fb1-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="44fb1-110">Nombre d’octets de l’identificateur d’entrée vers laquelle pointe le membre **lpEntryID** .</span><span class="sxs-lookup"><span data-stu-id="44fb1-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="44fb1-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="44fb1-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="44fb1-112">Pointeur vers l’identificateur d’entrée de l’objet état modifié.</span><span class="sxs-lookup"><span data-stu-id="44fb1-112">Pointer to the entry identifier of the changed status object.</span></span>
    
 <span data-ttu-id="44fb1-113">**cValues**</span><span class="sxs-lookup"><span data-stu-id="44fb1-113">**cValues**</span></span>
  
> <span data-ttu-id="44fb1-114">Nombre de structures [SPropValue](spropvalue.md) dans le tableau indiqué par le membre **lpPropVals** .</span><span class="sxs-lookup"><span data-stu-id="44fb1-114">Count of [SPropValue](spropvalue.md) structures in the array pointed to by the **lpPropVals** member.</span></span> 
    
 <span data-ttu-id="44fb1-115">**lpPropVals**</span><span class="sxs-lookup"><span data-stu-id="44fb1-115">**lpPropVals**</span></span>
  
> <span data-ttu-id="44fb1-116">Pointeur vers un tableau de structures **SPropValue** qui décrivent les propriétés de l’objet état modifié.</span><span class="sxs-lookup"><span data-stu-id="44fb1-116">Pointer to an array of **SPropValue** structures that describe the properties of the changed status object.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="44fb1-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="44fb1-117">Remarks</span></span>

<span data-ttu-id="44fb1-118">La structure **STATUS_OBJECT_NOTIFICATION** est un des membres de l’union de structures inclus dans le membre **info** de la structure de [NOTIFICATION](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="44fb1-118">The **STATUS_OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="44fb1-119">La structure **STATUS_OBJECT_NOTIFICATION** est incluse dans une notification d’objet état pour un événement de type _fnevStatusObjectModified_.</span><span class="sxs-lookup"><span data-stu-id="44fb1-119">The **STATUS_OBJECT_NOTIFICATION** structure is included with a status object notification for an event of type  _fnevStatusObjectModified_.</span></span> <span data-ttu-id="44fb1-120">Notification d’état d’objet est une notification MAPI interne ; clients et fournisseurs de services ne peut pas inscrire pour qu’il et il ne peut pas générer des fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="44fb1-120">Status object notification is an internal MAPI notification; clients and service providers cannot register for it and service providers cannot generate it.</span></span>
  
<span data-ttu-id="44fb1-121">Pour plus d’informations sur la notification, consultez les rubriques décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="44fb1-121">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="44fb1-122">**Rubrique**</span><span class="sxs-lookup"><span data-stu-id="44fb1-122">**Topic**</span></span>|<span data-ttu-id="44fb1-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="44fb1-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44fb1-124">Notification d’événement MAPI</span><span class="sxs-lookup"><span data-stu-id="44fb1-124">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="44fb1-125">Vue d’ensemble des notifications et les événements de notification.</span><span class="sxs-lookup"><span data-stu-id="44fb1-125">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="44fb1-126">Gérer les Notifications</span><span class="sxs-lookup"><span data-stu-id="44fb1-126">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="44fb1-127">Étude de la façon dont les clients doivent gérer les notifications.</span><span class="sxs-lookup"><span data-stu-id="44fb1-127">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="44fb1-128">Prise en charge de la Notification d’événement</span><span class="sxs-lookup"><span data-stu-id="44fb1-128">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="44fb1-129">Étude de comment les fournisseurs de services peuvent utiliser la méthode **IMAPISupport** pour générer des notifications.</span><span class="sxs-lookup"><span data-stu-id="44fb1-129">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="44fb1-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44fb1-130">See also</span></span>



[<span data-ttu-id="44fb1-131">Notification</span><span class="sxs-lookup"><span data-stu-id="44fb1-131">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="44fb1-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="44fb1-132">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="44fb1-133">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="44fb1-133">MAPI Structures</span></span>](mapi-structures.md)

