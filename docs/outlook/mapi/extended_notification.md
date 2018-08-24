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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: de9b5e377840b1fbfa3b6dd73fd952c0c72efeb7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580641"
---
# <a name="extendednotification"></a><span data-ttu-id="34c3c-103">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="34c3c-103">EXTENDED_NOTIFICATION</span></span>

  
  
<span data-ttu-id="34c3c-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34c3c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34c3c-105">Décrit les informations relatives à un événement qui est spécifique au fournisseur de service.</span><span class="sxs-lookup"><span data-stu-id="34c3c-105">Describes information that relates to an event that is service provider-specific.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="34c3c-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="34c3c-106">Header file:</span></span>  <br/> |<span data-ttu-id="34c3c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="34c3c-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _EXTENDED_NOTIFICATION
{
  ULONG ulEvent;
  ULONG cb;
  LPBYTE pbEventParameters;
} EXTENDED_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="34c3c-108">Members</span><span class="sxs-lookup"><span data-stu-id="34c3c-108">Members</span></span>

 <span data-ttu-id="34c3c-109">**ulEvent**</span><span class="sxs-lookup"><span data-stu-id="34c3c-109">**ulEvent**</span></span>
  
> <span data-ttu-id="34c3c-110">Code d’événement étendue définie par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="34c3c-110">Extended event code that is defined by the provider.</span></span>
    
 <span data-ttu-id="34c3c-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="34c3c-111">**cb**</span></span>
  
> <span data-ttu-id="34c3c-112">Nombre d’octets dans les paramètres spécifiques à l’événement indiqué par **pbEventParameters**.</span><span class="sxs-lookup"><span data-stu-id="34c3c-112">Count of bytes in the event-specific parameters pointed to by **pbEventParameters**.</span></span> 
    
 <span data-ttu-id="34c3c-113">**pbEventParameters**</span><span class="sxs-lookup"><span data-stu-id="34c3c-113">**pbEventParameters**</span></span>
  
> <span data-ttu-id="34c3c-114">Pointeur vers les paramètres spécifiques à l’événement.</span><span class="sxs-lookup"><span data-stu-id="34c3c-114">Pointer to event-specific parameters.</span></span> <span data-ttu-id="34c3c-115">Le type de paramètres qui sont utilisés dépend de la valeur du membre **ulEvent** ; Ces paramètres sont décrits par le fournisseur qui a émis l’événement.</span><span class="sxs-lookup"><span data-stu-id="34c3c-115">The type of parameters that are used depends on the value of the **ulEvent** member; these parameters are documented by the provider that issued the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="34c3c-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="34c3c-116">Remarks</span></span>

<span data-ttu-id="34c3c-117">La structure **EXTENDED_NOTIFICATION** est un des membres de l’union de structures inclus dans le membre **info** de la structure de [NOTIFICATION](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="34c3c-117">The **EXTENDED_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="34c3c-118">Lorsque le membre **info** d’une structure **NOTIFICATION** contient une structure **EXTENDED_NOTIFICATION** , le membre **ulEventType** de la structure de **NOTIFICATION** est défini sur _fnevExtended_.</span><span class="sxs-lookup"><span data-stu-id="34c3c-118">When the **info** member of a **NOTIFICATION** structure contains an **EXTENDED_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevExtended_.</span></span>
  
<span data-ttu-id="34c3c-119">L’événement étendue est définie par un fournisseur de services pour représenter un type de modification qui ne peuvent pas être couvertes par les autres événements prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="34c3c-119">The extended event is defined by a service provider to represent a type of change that cannot be covered by any of the other predefined events.</span></span> <span data-ttu-id="34c3c-120">Seuls les clients qui savoir avant qu’ils inscrivent qu’un fournisseur de services prend en charge un événement étendu peuvent s’inscrire pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="34c3c-120">Only clients that know before they register that a service provider supports an extended event can register for that event.</span></span> <span data-ttu-id="34c3c-121">Il n’est pas possible pour les clients déterminer sans connaissances avancées si un fournisseur de services prend en charge un événement étendu.</span><span class="sxs-lookup"><span data-stu-id="34c3c-121">It is not possible for clients to determine without advanced knowledge if a service provider supports an extended event.</span></span> <span data-ttu-id="34c3c-122">Si un fournisseur de services prend en charge un événement étendu, il montre comment gérer un événement lorsqu’il est reçu.</span><span class="sxs-lookup"><span data-stu-id="34c3c-122">If a service provider supports an extended event, it shows how to handle such an event when it is received.</span></span>
  
<span data-ttu-id="34c3c-123">Une étendue est envoyé à la session quand un client se déconnecte.</span><span class="sxs-lookup"><span data-stu-id="34c3c-123">An extended notification is sent by the session when a client logs off.</span></span> <span data-ttu-id="34c3c-124">Enregistrer cette notification en appelant [IMAPISession::Advise](imapisession-advise.md) avec le paramètre _lpEntryID_ défini sur NULL et le paramètre _cbEntryID_ définir sur zéro.</span><span class="sxs-lookup"><span data-stu-id="34c3c-124">Register for this notification by calling [IMAPISession::Advise](imapisession-advise.md) with the  _lpEntryID_ parameter set to NULL and the  _cbEntryID_ parameter set to zero.</span></span> 
  
<span data-ttu-id="34c3c-125">Pour plus d’informations sur la notification, consultez les rubriques décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="34c3c-125">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="34c3c-126">**Rubrique**</span><span class="sxs-lookup"><span data-stu-id="34c3c-126">**Topic**</span></span>|<span data-ttu-id="34c3c-127">**Description**</span><span class="sxs-lookup"><span data-stu-id="34c3c-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="34c3c-128">Notification d’événement dans MAPI</span><span class="sxs-lookup"><span data-stu-id="34c3c-128">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="34c3c-129">Vue d’ensemble des notifications et les événements de notification.</span><span class="sxs-lookup"><span data-stu-id="34c3c-129">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="34c3c-130">Gestion des notifications</span><span class="sxs-lookup"><span data-stu-id="34c3c-130">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="34c3c-131">Étude de la façon dont les clients doivent gérer les notifications.</span><span class="sxs-lookup"><span data-stu-id="34c3c-131">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="34c3c-132">Prise en charge des notifications d’événements</span><span class="sxs-lookup"><span data-stu-id="34c3c-132">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="34c3c-133">Étude de comment les fournisseurs de services peuvent utiliser les méthodes [IMAPISupport](imapisupportiunknown.md) pour générer des notifications.</span><span class="sxs-lookup"><span data-stu-id="34c3c-133">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) methods to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="34c3c-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34c3c-134">See also</span></span>



[<span data-ttu-id="34c3c-135">Notification</span><span class="sxs-lookup"><span data-stu-id="34c3c-135">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="34c3c-136">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="34c3c-136">MAPI Structures</span></span>](mapi-structures.md)

