---
title: Forcer une Notification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9c7d6605-73ee-468c-981b-e0853106c9ba
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 40fc763071f7113e222c6987dfd70fb7d89bab4b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783337"
---
# <a name="forcing-a-notification"></a><span data-ttu-id="504cd-103">Forcer une Notification</span><span class="sxs-lookup"><span data-stu-id="504cd-103">Forcing a Notification</span></span>

  
  
<span data-ttu-id="504cd-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="504cd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="504cd-105">Lorsque fournisseurs de services utilisent la [IMAPISupport : IUnknown](imapisupportiunknown.md) méthodes de notification, MAPI fournit des notifications à l’aide d’une fenêtre masquée et sa procédure de fenêtre correspondante.</span><span class="sxs-lookup"><span data-stu-id="504cd-105">When service providers use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods for notification, MAPI delivers notifications using a hidden window and its corresponding window procedure.</span></span> <span data-ttu-id="504cd-106">Pour chaque processus recevoir une notification, MAPI publie un message spécial dans la fenêtre masquée.</span><span class="sxs-lookup"><span data-stu-id="504cd-106">For each process to receive a notification, MAPI posts a special message to the hidden window.</span></span> <span data-ttu-id="504cd-107">Ce message est nommé avec la constante **szMAPINotificationMsg** est défini dans MAPIDEFS. H.</span><span class="sxs-lookup"><span data-stu-id="504cd-107">This message is named with the constant **szMAPINotificationMsg** which is defined in MAPIDEFS.H.</span></span> 
  
<span data-ttu-id="504cd-108">Vous recevez ces notifications lors de la procédure de fenêtre de la fenêtre masquée traite le message **szMAPINotificationMsg** .</span><span class="sxs-lookup"><span data-stu-id="504cd-108">You receive these notifications when the hidden window's window procedure processes the **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="504cd-109">Pour garantir que les notifications sont envoyées, il est nécessaire pour attendre et distribuer ce message **szMAPINotificationMsg** .</span><span class="sxs-lookup"><span data-stu-id="504cd-109">To guarantee that notifications are delivered, it is necessary to wait for and dispatch this **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="504cd-110">L’implémentation de la logique pour effectuer cette opération peut être effectuée assez simple, mais MAPI fournit un point d’entrée dans la DLL MAPI appelé [HrDispatchNotifications](hrdispatchnotifications.md) pour rendre le traitement encore plus simple.</span><span class="sxs-lookup"><span data-stu-id="504cd-110">Implementing the logic to achieve this can be done fairly simply, but MAPI provides an entry point into the MAPI DLL called [HrDispatchNotifications](hrdispatchnotifications.md) to make processing even simpler.</span></span> <span data-ttu-id="504cd-111">Appel **HrDispatchNotifications** comme suit pour recevoir des notifications dans votre client :</span><span class="sxs-lookup"><span data-stu-id="504cd-111">Call **HrDispatchNotifications** as follows to receive notifications in your client:</span></span> 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


