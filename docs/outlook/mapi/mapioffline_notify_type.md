---
title: MAPIOFFLINE_NOTIFY_TYPE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a111d7b7-6e87-4958-8f9b-0f2adbeb8b63
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e7120b843eae8df70cb2c4f9cbf581dcf0e09c11
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566886"
---
# <a name="mapiofflinenotifytype"></a><span data-ttu-id="84e28-103">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="84e28-103">MAPIOFFLINE_NOTIFY_TYPE</span></span>

  
  
<span data-ttu-id="84e28-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84e28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84e28-105">Le MAPIOFFLINE_NOTIFY_TYPE d’une notification identifie si une modification de l’état de connexion est sur le point d’avoir lieu, est en cours ou terminée.</span><span class="sxs-lookup"><span data-stu-id="84e28-105">The MAPIOFFLINE_NOTIFY_TYPE of a notification identifies if a change in the connection state is going to take place, is taking place, or has completed.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="84e28-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="84e28-106">Quick info</span></span>

<span data-ttu-id="84e28-107">Voir **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="84e28-107">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
```cpp
typedef enum { 
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START = 1,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE = 2,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE = 3  
} MAPIOFFLINE_NOTIFY_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="84e28-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84e28-108">See also</span></span>



[<span data-ttu-id="84e28-109">À propos de l’API d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="84e28-109">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="84e28-110">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="84e28-110">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="84e28-111">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="84e28-111">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

