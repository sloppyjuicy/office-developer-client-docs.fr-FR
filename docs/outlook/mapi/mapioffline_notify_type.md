---
title: MAPIOFFLINE_NOTIFY_TYPE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a111d7b7-6e87-4958-8f9b-0f2adbeb8b63
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 65ed848907e196c315e8ddb61c4afd2fe03faa18
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270286"
---
# <a name="mapiofflinenotifytype"></a><span data-ttu-id="0dcdf-103">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="0dcdf-103">MAPIOFFLINE_NOTIFY_TYPE</span></span>

  
  
<span data-ttu-id="0dcdf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0dcdf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0dcdf-105">Le MAPIOFFLINE_NOTIFY_TYPE d'une notification indique si une modification apportée à l'état de connexion doit avoir lieu, a lieu ou s'est terminée.</span><span class="sxs-lookup"><span data-stu-id="0dcdf-105">The MAPIOFFLINE_NOTIFY_TYPE of a notification identifies if a change in the connection state is going to take place, is taking place, or has completed.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="0dcdf-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="0dcdf-106">Quick info</span></span>

<span data-ttu-id="0dcdf-107">Voir **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="0dcdf-107">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
```cpp
typedef enum { 
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START = 1,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE = 2,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE = 3  
} MAPIOFFLINE_NOTIFY_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="0dcdf-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0dcdf-108">See also</span></span>



[<span data-ttu-id="0dcdf-109">À propos de l’API d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="0dcdf-109">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="0dcdf-110">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="0dcdf-110">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="0dcdf-111">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="0dcdf-111">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

