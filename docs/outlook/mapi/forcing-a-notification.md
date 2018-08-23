---
title: Forçage d’une notification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9c7d6605-73ee-468c-981b-e0853106c9ba
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5affce8ab7a8b08019816ad9485641c401dd80c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578772"
---
# <a name="forcing-a-notification"></a><span data-ttu-id="b33ba-103">Forçage d’une notification</span><span class="sxs-lookup"><span data-stu-id="b33ba-103">Forcing a Notification</span></span>

  
  
<span data-ttu-id="b33ba-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b33ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b33ba-105">Lorsque fournisseurs de services utilisent la [IMAPISupport : IUnknown](imapisupportiunknown.md) méthodes de notification, MAPI fournit des notifications à l’aide d’une fenêtre masquée et sa procédure de fenêtre correspondante.</span><span class="sxs-lookup"><span data-stu-id="b33ba-105">When service providers use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods for notification, MAPI delivers notifications using a hidden window and its corresponding window procedure.</span></span> <span data-ttu-id="b33ba-106">Pour chaque processus recevoir une notification, MAPI publie un message spécial dans la fenêtre masquée.</span><span class="sxs-lookup"><span data-stu-id="b33ba-106">For each process to receive a notification, MAPI posts a special message to the hidden window.</span></span> <span data-ttu-id="b33ba-107">Ce message est nommé avec la constante **szMAPINotificationMsg** est défini dans MAPIDEFS. H.</span><span class="sxs-lookup"><span data-stu-id="b33ba-107">This message is named with the constant **szMAPINotificationMsg** which is defined in MAPIDEFS.H.</span></span> 
  
<span data-ttu-id="b33ba-108">Vous recevez ces notifications lors de la procédure de fenêtre de la fenêtre masquée traite le message **szMAPINotificationMsg** .</span><span class="sxs-lookup"><span data-stu-id="b33ba-108">You receive these notifications when the hidden window's window procedure processes the **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="b33ba-109">Pour garantir que les notifications sont envoyées, il est nécessaire pour attendre et distribuer ce message **szMAPINotificationMsg** .</span><span class="sxs-lookup"><span data-stu-id="b33ba-109">To guarantee that notifications are delivered, it is necessary to wait for and dispatch this **szMAPINotificationMsg** message.</span></span> <span data-ttu-id="b33ba-110">L’implémentation de la logique pour effectuer cette opération peut être effectuée assez simple, mais MAPI fournit un point d’entrée dans la DLL MAPI appelé [HrDispatchNotifications](hrdispatchnotifications.md) pour rendre le traitement encore plus simple.</span><span class="sxs-lookup"><span data-stu-id="b33ba-110">Implementing the logic to achieve this can be done fairly simply, but MAPI provides an entry point into the MAPI DLL called [HrDispatchNotifications](hrdispatchnotifications.md) to make processing even simpler.</span></span> <span data-ttu-id="b33ba-111">Appel **HrDispatchNotifications** comme suit pour recevoir des notifications dans votre client :</span><span class="sxs-lookup"><span data-stu-id="b33ba-111">Call **HrDispatchNotifications** as follows to receive notifications in your client:</span></span> 
  
```cpp
HRESULT hr = HrDispatchNotifications(0);
 
```


