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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 86fe4b0a1a7521c310788505b99f53bc8657de75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783266"
---
# <a name="errornotification"></a><span data-ttu-id="b3c33-103">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b3c33-103">ERROR_NOTIFICATION</span></span>

  
  
<span data-ttu-id="b3c33-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b3c33-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b3c33-105">Décrit les informations qui sont associées à une erreur critique.</span><span class="sxs-lookup"><span data-stu-id="b3c33-105">Describes information that relate to a critical error.</span></span> <span data-ttu-id="b3c33-106">Cela entraîne une notification d’erreur à générer.</span><span class="sxs-lookup"><span data-stu-id="b3c33-106">This causes an error notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b3c33-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b3c33-107">Header file:</span></span>  <br/> |<span data-ttu-id="b3c33-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b3c33-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="b3c33-109">Membres</span><span class="sxs-lookup"><span data-stu-id="b3c33-109">Members</span></span>

 <span data-ttu-id="b3c33-110">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="b3c33-110">**cbEntryID**</span></span>
  
> <span data-ttu-id="b3c33-111">Nombre d’octets de l’identificateur d’entrée désignés par **lpEntryID**.</span><span class="sxs-lookup"><span data-stu-id="b3c33-111">Count of bytes in the entry identifier pointed to by **lpEntryID**.</span></span> 
    
 <span data-ttu-id="b3c33-112">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="b3c33-112">**lpEntryID**</span></span>
  
> <span data-ttu-id="b3c33-113">Pointeur vers l’identificateur d’entrée de l’objet qui provoque l’erreur.</span><span class="sxs-lookup"><span data-stu-id="b3c33-113">Pointer to the entry identifier of the object that causes the error.</span></span>
    
 <span data-ttu-id="b3c33-114">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="b3c33-114">**scode**</span></span>
  
> <span data-ttu-id="b3c33-115">Valeur d’erreur pour l’erreur critique.</span><span class="sxs-lookup"><span data-stu-id="b3c33-115">Error value for the critical error.</span></span> 
    
 <span data-ttu-id="b3c33-116">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="b3c33-116">**ulFlags**</span></span>
  
> <span data-ttu-id="b3c33-117">Masque de bits d’indicateurs utilisés pour désigner le format du texte vers laquelle pointe le membre **lpszError** dans la structure désigné par **lpMAPIError**.</span><span class="sxs-lookup"><span data-stu-id="b3c33-117">Bitmask of flags used to designate the format of the text pointed to by the **lpszError** member in the structure pointed to by **lpMAPIError**.</span></span> <span data-ttu-id="b3c33-118">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="b3c33-118">The following flag can be set:</span></span>
    
<span data-ttu-id="b3c33-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b3c33-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b3c33-120">Les chaînes passée sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="b3c33-120">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="b3c33-121">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="b3c33-121">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="b3c33-122">**lpMAPIError**</span><span class="sxs-lookup"><span data-stu-id="b3c33-122">**lpMAPIError**</span></span>
  
> <span data-ttu-id="b3c33-123">Pointeur vers une structure [MAPIERROR](mapierror.md) décrivant l’erreur.</span><span class="sxs-lookup"><span data-stu-id="b3c33-123">Pointer to a [MAPIERROR](mapierror.md) structure describing the error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b3c33-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="b3c33-124">Remarks</span></span>

<span data-ttu-id="b3c33-125">La structure **ERROR_NOTIFICATION** est un des membres de l’union de structures inclus dans le membre **info** de la structure de [NOTIFICATION](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="b3c33-125">The **ERROR_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="b3c33-126">Lorsque le membre **info** d’une structure **NOTIFICATION** contient une structure **ERROR_NOTIFICATION** , le membre **ulEventType** de la structure de **NOTIFICATION** est défini sur _fnevCriticalError_.</span><span class="sxs-lookup"><span data-stu-id="b3c33-126">When the **info** member of a **NOTIFICATION** structure contains an **ERROR_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevCriticalError_.</span></span>
  
<span data-ttu-id="b3c33-127">La valeur du membre **cbEntryID** et le membre **lpEntryID** peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="b3c33-127">The value of the **cbEntryID** member and the **lpEntryID** member can be NULL.</span></span> 
  
<span data-ttu-id="b3c33-128">Pour plus d’informations sur la notification, consultez les rubriques décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b3c33-128">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="b3c33-129">**Rubrique**</span><span class="sxs-lookup"><span data-stu-id="b3c33-129">**Topic**</span></span>|<span data-ttu-id="b3c33-130">**Description**</span><span class="sxs-lookup"><span data-stu-id="b3c33-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b3c33-131">Notification d’événement MAPI</span><span class="sxs-lookup"><span data-stu-id="b3c33-131">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="b3c33-132">Vue d’ensemble des notifications et les événements de notification.</span><span class="sxs-lookup"><span data-stu-id="b3c33-132">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="b3c33-133">Gérer les Notifications</span><span class="sxs-lookup"><span data-stu-id="b3c33-133">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="b3c33-134">Étude de la façon dont les clients doivent gérer les notifications.</span><span class="sxs-lookup"><span data-stu-id="b3c33-134">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="b3c33-135">Prise en charge de la Notification d’événement</span><span class="sxs-lookup"><span data-stu-id="b3c33-135">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="b3c33-136">Étude de comment les fournisseurs de services peuvent utiliser la méthode **IMAPISupport** pour générer des notifications.</span><span class="sxs-lookup"><span data-stu-id="b3c33-136">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b3c33-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3c33-137">See also</span></span>



[<span data-ttu-id="b3c33-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="b3c33-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="b3c33-139">Notification</span><span class="sxs-lookup"><span data-stu-id="b3c33-139">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="b3c33-140">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="b3c33-140">MAPI Structures</span></span>](mapi-structures.md)

