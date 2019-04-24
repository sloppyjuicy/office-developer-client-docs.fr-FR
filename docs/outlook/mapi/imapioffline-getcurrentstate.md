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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: f5170ceb443dcde075440bf84d29000afe4680c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321272"
---
# <a name="imapiofflinegetcurrentstate"></a><span data-ttu-id="db217-103">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="db217-103">IMAPIOffline::GetCurrentState</span></span>

  
  
<span data-ttu-id="db217-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db217-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db217-105">Obtient l'État en ligne ou hors connexion actuel d'un objet hors connexion.</span><span class="sxs-lookup"><span data-stu-id="db217-105">Gets the current online or offline state of an offline object.</span></span>
  
```cpp
HRESULT GetCurrentState( 
    ULONG* pulState 
);
```

## <a name="parameters"></a><span data-ttu-id="db217-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db217-106">Parameters</span></span>

 <span data-ttu-id="db217-107">_pulState_</span><span class="sxs-lookup"><span data-stu-id="db217-107">_pulState_</span></span>
  
> <span data-ttu-id="db217-108">remarquer État en ligne ou hors connexion actuel d'un objet hors connexion.</span><span class="sxs-lookup"><span data-stu-id="db217-108">[out] The current online or offline state of an offline object.</span></span> <span data-ttu-id="db217-109">Il doit s'agir de l'une des deux valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="db217-109">It must be one of these two values:</span></span>
    
<span data-ttu-id="db217-110">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="db217-110">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="db217-111">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="db217-111">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="db217-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db217-112">See also</span></span>



[<span data-ttu-id="db217-113">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="db217-113">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="db217-114">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="db217-114">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)


[<span data-ttu-id="db217-115">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="db217-115">MAPI Constants</span></span>](mapi-constants.md)

