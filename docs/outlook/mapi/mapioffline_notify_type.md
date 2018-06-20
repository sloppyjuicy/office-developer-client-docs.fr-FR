---
title: MAPIOFFLINE_NOTIFY_TYPE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a111d7b7-6e87-4958-8f9b-0f2adbeb8b63
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 468dfd634c4aaf18b019d06975ec9066c9d5f7a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784758"
---
# <a name="mapiofflinenotifytype"></a><span data-ttu-id="131aa-103">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="131aa-103">MAPIOFFLINE_NOTIFY_TYPE</span></span>

  
  
<span data-ttu-id="131aa-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="131aa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="131aa-105">Le MAPIOFFLINE_NOTIFY_TYPE d’une notification identifie si une modification de l’état de connexion est sur le point d’avoir lieu, est en cours ou terminée.</span><span class="sxs-lookup"><span data-stu-id="131aa-105">The MAPIOFFLINE_NOTIFY_TYPE of a notification identifies if a change in the connection state is going to take place, is taking place, or has completed.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="131aa-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="131aa-106">Quick info</span></span>

<span data-ttu-id="131aa-107">Voir **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="131aa-107">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
```cpp
typedef enum { 
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START = 1,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE = 2,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE = 3  
} MAPIOFFLINE_NOTIFY_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="131aa-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="131aa-108">See also</span></span>



[<span data-ttu-id="131aa-109">À propos de l’API d’état en mode hors connexion</span><span class="sxs-lookup"><span data-stu-id="131aa-109">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="131aa-110">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="131aa-110">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="131aa-111">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="131aa-111">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

