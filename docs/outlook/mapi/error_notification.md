---
title: ERROR_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ERROR_NOTIFICATION
api_type:
- COM
ms.assetid: 6c5bb383-f8e2-4d79-bcf2-aa86c130e8b1
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f8d4fb6b8cd7ad0ebf1e7660a0f3c0602274fa10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425441"
---
# <a name="errornotification"></a><span data-ttu-id="96697-103">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="96697-103">ERROR_NOTIFICATION</span></span>

  
  
<span data-ttu-id="96697-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96697-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96697-105">Décrit les informations relatives à une erreur critique.</span><span class="sxs-lookup"><span data-stu-id="96697-105">Describes information that relate to a critical error.</span></span> <span data-ttu-id="96697-106">Cela entraîne la génération d'une notification d'erreur.</span><span class="sxs-lookup"><span data-stu-id="96697-106">This causes an error notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96697-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="96697-107">Header file:</span></span>  <br/> |<span data-ttu-id="96697-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="96697-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _ERROR_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  SCODE scode;
  ULONG ulFlags;
  LPMAPIERROR lpMAPIError;
} ERROR_NOTIFICATION;
```

## <a name="members"></a><span data-ttu-id="96697-109">Members</span><span class="sxs-lookup"><span data-stu-id="96697-109">Members</span></span>

 <span data-ttu-id="96697-110">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="96697-110">**cbEntryID**</span></span>
  
> <span data-ttu-id="96697-111">Nombre d'octets dans l'identificateur d'entrée pointé par **lpEntryID**.</span><span class="sxs-lookup"><span data-stu-id="96697-111">Count of bytes in the entry identifier pointed to by **lpEntryID**.</span></span> 
    
 <span data-ttu-id="96697-112">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="96697-112">**lpEntryID**</span></span>
  
> <span data-ttu-id="96697-113">Pointeur vers l'identificateur d'entrée de l'objet à l'origine de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="96697-113">Pointer to the entry identifier of the object that causes the error.</span></span>
    
 <span data-ttu-id="96697-114">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="96697-114">**scode**</span></span>
  
> <span data-ttu-id="96697-115">Valeur d'erreur pour l'erreur critique.</span><span class="sxs-lookup"><span data-stu-id="96697-115">Error value for the critical error.</span></span> 
    
 <span data-ttu-id="96697-116">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="96697-116">**ulFlags**</span></span>
  
> <span data-ttu-id="96697-117">Masque de des indicateurs utilisé pour désigner le format du texte pointé par le membre **lpszError** dans la structure vers laquelle pointe le **lpMAPIError**.</span><span class="sxs-lookup"><span data-stu-id="96697-117">Bitmask of flags used to designate the format of the text pointed to by the **lpszError** member in the structure pointed to by **lpMAPIError**.</span></span> <span data-ttu-id="96697-118">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="96697-118">The following flag can be set:</span></span>
    
<span data-ttu-id="96697-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="96697-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="96697-120">Les chaînes transmises sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="96697-120">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="96697-121">Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="96697-121">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="96697-122">**lpMAPIError**</span><span class="sxs-lookup"><span data-stu-id="96697-122">**lpMAPIError**</span></span>
  
> <span data-ttu-id="96697-123">Pointeur vers une structure [MAPIERROR](mapierror.md) décrivant l'erreur.</span><span class="sxs-lookup"><span data-stu-id="96697-123">Pointer to a [MAPIERROR](mapierror.md) structure describing the error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="96697-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="96697-124">Remarks</span></span>

<span data-ttu-id="96697-125">La structure **ERROR_NOTIFICATION** est l'un des membres de l'Union des structures incluses dans le membre **info** de la structure de [notification](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="96697-125">The **ERROR_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="96697-126">Lorsque le membre **info** d'une structure de **notification** contient une structure **ERROR_NOTIFICATION** , le membre **ulEventType** de la structure de **notification** est défini sur _fnevCriticalError_.</span><span class="sxs-lookup"><span data-stu-id="96697-126">When the **info** member of a **NOTIFICATION** structure contains an **ERROR_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevCriticalError_.</span></span>
  
<span data-ttu-id="96697-127">La valeur du membre **cbEntryID** et du membre **LPENTRYID** peut être null.</span><span class="sxs-lookup"><span data-stu-id="96697-127">The value of the **cbEntryID** member and the **lpEntryID** member can be NULL.</span></span> 
  
<span data-ttu-id="96697-128">Pour plus d'informations sur la notification, reportez-vous aux rubriques décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="96697-128">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="96697-129">**Rubrique**</span><span class="sxs-lookup"><span data-stu-id="96697-129">**Topic**</span></span>|<span data-ttu-id="96697-130">**Description**</span><span class="sxs-lookup"><span data-stu-id="96697-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="96697-131">Notification d'événement dans MAPI</span><span class="sxs-lookup"><span data-stu-id="96697-131">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="96697-132">Vue d'ensemble générale des événements de notification et de notification.</span><span class="sxs-lookup"><span data-stu-id="96697-132">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="96697-133">Gestion des notifications</span><span class="sxs-lookup"><span data-stu-id="96697-133">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="96697-134">Présentation de la façon dont les clients doivent gérer les notifications.</span><span class="sxs-lookup"><span data-stu-id="96697-134">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="96697-135">Notification d'événement de prise en charge</span><span class="sxs-lookup"><span data-stu-id="96697-135">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="96697-136">Présentation de la façon dont les fournisseurs de services peuvent utiliser la méthode **IMAPISupport** pour générer des notifications.</span><span class="sxs-lookup"><span data-stu-id="96697-136">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="96697-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96697-137">See also</span></span>



[<span data-ttu-id="96697-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="96697-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="96697-139">Notification</span><span class="sxs-lookup"><span data-stu-id="96697-139">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="96697-140">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="96697-140">MAPI Structures</span></span>](mapi-structures.md)

