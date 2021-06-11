---
title: Forcer une notification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9c7d6605-73ee-468c-981b-e0853106c9ba
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 54eaf9e67da1b520896122c937508a90700a0b84
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433282"
---
# <a name="forcing-a-notification"></a><span data-ttu-id="fff96-103">Forcer une notification</span><span class="sxs-lookup"><span data-stu-id="fff96-103">Forcing a Notification</span></span>

  
  
<span data-ttu-id="fff96-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fff96-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fff96-105">Lorsque les fournisseurs de services utilisent les méthodes [IMAPISupport : IUnknown](imapisupportiunknown.md) pour la notification, MAPI fournit des notifications à l’aide d’une fenêtre masquée et de sa procédure de fenêtre correspondante.</span><span class="sxs-lookup"><span data-stu-id="fff96-105">When service providers use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods for notification, MAPI delivers notifications using a hidden window and its corresponding window procedure.</span></span> <span data-ttu-id="fff96-106">Pour chaque processus de réception d’une notification, MAPI publie un message spécial dans la fenêtre masquée.</span><span class="sxs-lookup"><span data-stu-id="fff96-106">For each process to receive a notification, MAPI posts a special message to the hidden window.</span></span> <span data-ttu-id="fff96-107">Ce message est nommé avec la constante **szMAPINotificationMsg** définie dans MAPIDEFS.H.</span><span class="sxs-lookup"><span data-stu-id="fff96-107">This message is named with the constant **szMAPINotificationMsg** which is defined in MAPIDEFS.H.</span></span> 
  
<span data-ttu-id="fff96-108">Vous recevez ces notifications lorsque la procédure de fenêtre masquée traite le message **szMAPINotificationMsg.**</span><span class="sxs-lookup"><span data-stu-id="fff96-108">You receive these notifications when the hidden window's window procedure processes the **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="fff96-109">Pour garantir que les notifications sont remis, il est nécessaire d’attendre et de transmettre ce message **szMAPINotificationMsg.**</span><span class="sxs-lookup"><span data-stu-id="fff96-109">To guarantee that notifications are delivered, it is necessary to wait for and dispatch this **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="fff96-110">L’exécution de la logique pour y parvenir peut être effectuée assez simplement, mais MAPI fournit un point d’entrée dans la DLL MAPI appelée [HrDispatchNotifications](hrdispatchnotifications.md) pour simplifier encore le traitement.</span><span class="sxs-lookup"><span data-stu-id="fff96-110">Implementing the logic to achieve this can be done fairly simply, but MAPI provides an entry point into the MAPI DLL called [HrDispatchNotifications](hrdispatchnotifications.md) to make processing even simpler.</span></span> <span data-ttu-id="fff96-111">Appelez **HrDispatchNotifications** comme suit pour recevoir des notifications dans votre client :</span><span class="sxs-lookup"><span data-stu-id="fff96-111">Call **HrDispatchNotifications** as follows to receive notifications in your client:</span></span> 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


