---
title: ISocialProviderGetSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 371b48c5-6d77-4d2d-890c-bb234c7eaabc
description: Obtient une interface ISocialSession.
ms.openlocfilehash: 59e6f61e1954f64d875c6336b211dcb530100252
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787614"
---
# <a name="isocialprovidergetsession"></a><span data-ttu-id="52f0d-103">ISocialProvider::GetSession</span><span class="sxs-lookup"><span data-stu-id="52f0d-103">ISocialProvider::GetSession</span></span>

<span data-ttu-id="52f0d-104">Obtient une interface [ISocialSession](isocialsessioniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="52f0d-104">Gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
  
```cpp
HRESULT _stdcall GetSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a><span data-ttu-id="52f0d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="52f0d-105">Parameters</span></span>

<span data-ttu-id="52f0d-106">_session_</span><span class="sxs-lookup"><span data-stu-id="52f0d-106">_session_</span></span>
  
> <span data-ttu-id="52f0d-107">[out] Une interface **ISocialSession** .</span><span class="sxs-lookup"><span data-stu-id="52f0d-107">[out] An **ISocialSession** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="52f0d-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="52f0d-108">Remarks</span></span>

<span data-ttu-id="52f0d-109">L’Outlook Social Connector (OSC) utilise l’interface **ISocialSession** pour vous connecter au réseau social.</span><span class="sxs-lookup"><span data-stu-id="52f0d-109">The Outlook Social Connector (OSC) uses the **ISocialSession** interface to log on to the social network.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="52f0d-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52f0d-110">See also</span></span>

- [<span data-ttu-id="52f0d-111">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="52f0d-111">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

