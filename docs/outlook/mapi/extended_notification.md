---
title: EXTENDED_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.EXTENDED_NOTIFICATION
api_type:
- COM
ms.assetid: f01fce7b-a038-4002-8bad-0e6a51ae9d05
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a8b49d0b80102f6295f3f717fb123a6581854d5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341117"
---
# <a name="extendednotification"></a><span data-ttu-id="39282-103">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="39282-103">EXTENDED_NOTIFICATION</span></span>

  
  
<span data-ttu-id="39282-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39282-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39282-105">Décrit les informations relatives à un événement qui est spécifique au fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="39282-105">Describes information that relates to an event that is service provider-specific.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="39282-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="39282-106">Header file:</span></span>  <br/> |<span data-ttu-id="39282-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="39282-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _EXTENDED_NOTIFICATION
{
  ULONG ulEvent;
  ULONG cb;
  LPBYTE pbEventParameters;
} EXTENDED_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="39282-108">Members</span><span class="sxs-lookup"><span data-stu-id="39282-108">Members</span></span>

 <span data-ttu-id="39282-109">**ulEvent**</span><span class="sxs-lookup"><span data-stu-id="39282-109">**ulEvent**</span></span>
  
> <span data-ttu-id="39282-110">Code d'événement étendu défini par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="39282-110">Extended event code that is defined by the provider.</span></span>
    
 <span data-ttu-id="39282-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="39282-111">**cb**</span></span>
  
> <span data-ttu-id="39282-112">Nombre d'octets dans les paramètres spécifiques de l'événement pointés par **pbEventParameters**.</span><span class="sxs-lookup"><span data-stu-id="39282-112">Count of bytes in the event-specific parameters pointed to by **pbEventParameters**.</span></span> 
    
 <span data-ttu-id="39282-113">**pbEventParameters**</span><span class="sxs-lookup"><span data-stu-id="39282-113">**pbEventParameters**</span></span>
  
> <span data-ttu-id="39282-114">Pointeur vers des paramètres spécifiques à l'événement.</span><span class="sxs-lookup"><span data-stu-id="39282-114">Pointer to event-specific parameters.</span></span> <span data-ttu-id="39282-115">Le type de paramètres utilisés dépend de la valeur du membre **ulEvent** ; ces paramètres sont documentés par le fournisseur qui a émis l'événement.</span><span class="sxs-lookup"><span data-stu-id="39282-115">The type of parameters that are used depends on the value of the **ulEvent** member; these parameters are documented by the provider that issued the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="39282-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="39282-116">Remarks</span></span>

<span data-ttu-id="39282-117">La structure **EXTENDED_NOTIFICATION** est l'un des membres de l'Union des structures incluses dans le membre **info** de la structure de [notification](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="39282-117">The **EXTENDED_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="39282-118">Lorsque le membre **info** d'une structure de **notification** contient une structure **EXTENDED_NOTIFICATION** , le membre **ulEventType** de la structure de **notification** est défini sur _fnevExtended_.</span><span class="sxs-lookup"><span data-stu-id="39282-118">When the **info** member of a **NOTIFICATION** structure contains an **EXTENDED_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevExtended_.</span></span>
  
<span data-ttu-id="39282-119">L'événement étendu est défini par un fournisseur de services pour représenter un type de modification qui ne peut pas être couvert par les autres événements prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="39282-119">The extended event is defined by a service provider to represent a type of change that cannot be covered by any of the other predefined events.</span></span> <span data-ttu-id="39282-120">Seuls les clients qui connaissent qu'un fournisseur de services prend en charge un événement étendu peuvent s'inscrire à cet événement.</span><span class="sxs-lookup"><span data-stu-id="39282-120">Only clients that know before they register that a service provider supports an extended event can register for that event.</span></span> <span data-ttu-id="39282-121">Il n'est pas possible pour les clients de déterminer sans connaissances avancées si un fournisseur de services prend en charge un événement étendu.</span><span class="sxs-lookup"><span data-stu-id="39282-121">It is not possible for clients to determine without advanced knowledge if a service provider supports an extended event.</span></span> <span data-ttu-id="39282-122">Si un fournisseur de services prend en charge un événement étendu, il montre comment gérer ce type d'événement lors de sa réception.</span><span class="sxs-lookup"><span data-stu-id="39282-122">If a service provider supports an extended event, it shows how to handle such an event when it is received.</span></span>
  
<span data-ttu-id="39282-123">Une notification étendue est envoyée par la session lorsqu'un client se déconnecte.</span><span class="sxs-lookup"><span data-stu-id="39282-123">An extended notification is sent by the session when a client logs off.</span></span> <span data-ttu-id="39282-124">Inscrivez-vous à cette notification en appelant [IMAPISession:: Advise](imapisession-advise.md) avec le paramètre _LPENTRYID_ défini sur null et le paramètre _cbEntryID_ défini sur zéro.</span><span class="sxs-lookup"><span data-stu-id="39282-124">Register for this notification by calling [IMAPISession::Advise](imapisession-advise.md) with the  _lpEntryID_ parameter set to NULL and the  _cbEntryID_ parameter set to zero.</span></span> 
  
<span data-ttu-id="39282-125">Pour plus d'informations sur la notification, reportez-vous aux rubriques décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="39282-125">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="39282-126">**Rubrique**</span><span class="sxs-lookup"><span data-stu-id="39282-126">**Topic**</span></span>|<span data-ttu-id="39282-127">**Description**</span><span class="sxs-lookup"><span data-stu-id="39282-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39282-128">Notification d'événement dans MAPI</span><span class="sxs-lookup"><span data-stu-id="39282-128">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="39282-129">Vue d'ensemble générale des événements de notification et de notification.</span><span class="sxs-lookup"><span data-stu-id="39282-129">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="39282-130">Gestion des notifications</span><span class="sxs-lookup"><span data-stu-id="39282-130">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="39282-131">Présentation de la façon dont les clients doivent gérer les notifications.</span><span class="sxs-lookup"><span data-stu-id="39282-131">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="39282-132">Notification d'événement de prise en charge</span><span class="sxs-lookup"><span data-stu-id="39282-132">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="39282-133">Présentation de la façon dont les fournisseurs de services peuvent utiliser les méthodes [IMAPISupport](imapisupportiunknown.md) pour générer des notifications.</span><span class="sxs-lookup"><span data-stu-id="39282-133">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) methods to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="39282-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39282-134">See also</span></span>



[<span data-ttu-id="39282-135">Notification</span><span class="sxs-lookup"><span data-stu-id="39282-135">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="39282-136">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="39282-136">MAPI Structures</span></span>](mapi-structures.md)

