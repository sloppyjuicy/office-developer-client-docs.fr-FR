---
title: IMAPIOfflineGetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.GetCurrentState
api_type:
- COM
ms.assetid: f3769e83-d678-1087-fc0f-b4f156386333
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 3cf8ad3966c44add3fd85b9f1adf677039bfce15
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783865"
---
# <a name="imapiofflinegetcurrentstate"></a><span data-ttu-id="ca18f-103">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="ca18f-103">IMAPIOffline::GetCurrentState</span></span>

  
  
<span data-ttu-id="ca18f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ca18f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ca18f-105">Obtient l’état en ligne ou hors connexion en cours d’un objet en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="ca18f-105">Gets the current online or offline state of an offline object.</span></span>
  
```cpp
HRESULT GetCurrentState( 
    ULONG* pulState 
);
```

## <a name="parameters"></a><span data-ttu-id="ca18f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca18f-106">Parameters</span></span>

 <span data-ttu-id="ca18f-107">_pulState_</span><span class="sxs-lookup"><span data-stu-id="ca18f-107">_pulState_</span></span>
  
> <span data-ttu-id="ca18f-108">[out] L’état de ligne ou hors connexion en cours d’un objet en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="ca18f-108">[out] The current online or offline state of an offline object.</span></span> <span data-ttu-id="ca18f-109">Il doit être une de ces deux valeurs :</span><span class="sxs-lookup"><span data-stu-id="ca18f-109">It must be one of these two values:</span></span>
    
<span data-ttu-id="ca18f-110">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="ca18f-110">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="ca18f-111">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="ca18f-111">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="ca18f-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca18f-112">See also</span></span>



[<span data-ttu-id="ca18f-113">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="ca18f-113">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="ca18f-114">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="ca18f-114">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)


[<span data-ttu-id="ca18f-115">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="ca18f-115">MAPI Constants</span></span>](mapi-constants.md)

