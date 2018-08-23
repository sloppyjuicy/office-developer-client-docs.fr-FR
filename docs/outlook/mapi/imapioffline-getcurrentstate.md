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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5d6b1dfcd3866b0d0e7151e9d5399e1274810d14
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568202"
---
# <a name="imapiofflinegetcurrentstate"></a><span data-ttu-id="5a232-103">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="5a232-103">IMAPIOffline::GetCurrentState</span></span>

  
  
<span data-ttu-id="5a232-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a232-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a232-105">Obtient l’état en ligne ou hors connexion en cours d’un objet en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="5a232-105">Gets the current online or offline state of an offline object.</span></span>
  
```cpp
HRESULT GetCurrentState( 
    ULONG* pulState 
);
```

## <a name="parameters"></a><span data-ttu-id="5a232-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a232-106">Parameters</span></span>

 <span data-ttu-id="5a232-107">_pulState_</span><span class="sxs-lookup"><span data-stu-id="5a232-107">_pulState_</span></span>
  
> <span data-ttu-id="5a232-108">[out] L’état de ligne ou hors connexion en cours d’un objet en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="5a232-108">[out] The current online or offline state of an offline object.</span></span> <span data-ttu-id="5a232-109">Il doit être une de ces deux valeurs :</span><span class="sxs-lookup"><span data-stu-id="5a232-109">It must be one of these two values:</span></span>
    
<span data-ttu-id="5a232-110">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="5a232-110">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="5a232-111">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="5a232-111">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="5a232-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a232-112">See also</span></span>



[<span data-ttu-id="5a232-113">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="5a232-113">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="5a232-114">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="5a232-114">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)


[<span data-ttu-id="5a232-115">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="5a232-115">MAPI Constants</span></span>](mapi-constants.md)

