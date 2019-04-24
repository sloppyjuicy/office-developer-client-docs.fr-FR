---
title: IPSTX2SetSpoolSuspendState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX2.SetSpoolSuspendState
api_type:
- COM
ms.assetid: 396db029-1d4a-203d-2256-3353d03c6767
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: e988114e8e71ad1f80d20ab0d5a30c37425f5952
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315056"
---
# <a name="ipstx2setspoolsuspendstate"></a><span data-ttu-id="06751-103">IPSTX2::SetSpoolSuspendState</span><span class="sxs-lookup"><span data-stu-id="06751-103">IPSTX2::SetSpoolSuspendState</span></span>

  
  
<span data-ttu-id="06751-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06751-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06751-105">Définit l'état suspendu sur le spouleur.</span><span class="sxs-lookup"><span data-stu-id="06751-105">Sets the suspended state on the spooler.</span></span>
  
```cpp
void SetSpoolSuspendState( 
    ULONG ulState 
);
```

## <a name="parameters"></a><span data-ttu-id="06751-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06751-106">Parameters</span></span>

 <span data-ttu-id="06751-107">_ulState_</span><span class="sxs-lookup"><span data-stu-id="06751-107">_ulState_</span></span>
  
> <span data-ttu-id="06751-108">dans État auquel définir le spouleur.</span><span class="sxs-lookup"><span data-stu-id="06751-108">[in] The state to set the spooler to.</span></span> <span data-ttu-id="06751-109">Il doit prendre la valeur de l'une des valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="06751-109">It must be one of the following values:</span></span>
    
 <span data-ttu-id="06751-110">**SS_ACTIVE**</span><span class="sxs-lookup"><span data-stu-id="06751-110">**SS_ACTIVE**</span></span>
  
> 
    
 <span data-ttu-id="06751-111">**SS_SUSPENDED**</span><span class="sxs-lookup"><span data-stu-id="06751-111">**SS_SUSPENDED**</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="06751-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06751-112">See also</span></span>



[<span data-ttu-id="06751-113">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="06751-113">MAPI Constants</span></span>](mapi-constants.md)

