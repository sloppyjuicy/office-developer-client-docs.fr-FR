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
ms.openlocfilehash: afa13bddd5cbbc53081f6ae7ddcc1671d1c40303
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419547"
---
# <a name="isocialprovidergetsession"></a><span data-ttu-id="54faf-103">ISocialProvider::GetSession</span><span class="sxs-lookup"><span data-stu-id="54faf-103">ISocialProvider::GetSession</span></span>

<span data-ttu-id="54faf-104">Obtient une interface [ISocialSession.](isocialsessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="54faf-104">Gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
  
```cpp
HRESULT _stdcall GetSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a><span data-ttu-id="54faf-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54faf-105">Parameters</span></span>

<span data-ttu-id="54faf-106">_session_</span><span class="sxs-lookup"><span data-stu-id="54faf-106">_session_</span></span>
  
> <span data-ttu-id="54faf-107">[out] Une interface **ISocialSession**.</span><span class="sxs-lookup"><span data-stu-id="54faf-107">[out] An **ISocialSession** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="54faf-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="54faf-108">Remarks</span></span>

<span data-ttu-id="54faf-109">Outlook Social Connector (OSC) utilise l’interface **ISocialSession** pour se connecter au réseau social.</span><span class="sxs-lookup"><span data-stu-id="54faf-109">The Outlook Social Connector (OSC) uses the **ISocialSession** interface to log on to the social network.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="54faf-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54faf-110">See also</span></span>

- [<span data-ttu-id="54faf-111">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="54faf-111">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

