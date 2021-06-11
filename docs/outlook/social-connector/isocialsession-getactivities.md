---
title: ISocialSessionGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6546be99-aee4-41a6-8297-ace378776503
description: Cette méthode a été dépréciée dans OSC 1.1.
ms.openlocfilehash: 29a7cdc9895dcfa2bd926d95dbd2089b7a5dc778
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439295"
---
# <a name="isocialsessiongetactivities"></a><span data-ttu-id="e913d-103">ISocialSession::GetActivities</span><span class="sxs-lookup"><span data-stu-id="e913d-103">ISocialSession::GetActivities</span></span>

<span data-ttu-id="e913d-104">Cette méthode a été dépréciée dans OSC 1.1.</span><span class="sxs-lookup"><span data-stu-id="e913d-104">This method has been deprecated in OSC 1.1.</span></span>
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a><span data-ttu-id="e913d-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="e913d-105">Remarks</span></span>

<span data-ttu-id="e913d-106">À compter d’OSC 1.1, l’OSC n’appelle plus **GetActivities.**</span><span class="sxs-lookup"><span data-stu-id="e913d-106">Starting in OSC 1.1, the OSC no longer calls **GetActivities**.</span></span> <span data-ttu-id="e913d-107">L’OSC ignore la valeur **de dynamicActivitiesLookup**.</span><span class="sxs-lookup"><span data-stu-id="e913d-107">The OSC ignores the value of **dynamicActivitiesLookup**.</span></span> <span data-ttu-id="e913d-108">Pour prendre en charge la recherche d’activités dynamiques, implémentez la méthode [ISocialSession2::GetActivitiesEx.](isocialsession2-getactivitiesex.md)</span><span class="sxs-lookup"><span data-stu-id="e913d-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="e913d-109">Définissez **cacheActivities** sur **false** et **getActivities** et **dynamicActivitiesLookupEx** sur **true,** ce qui invite l’OSC à appeler **ISocialSession2::GetActivitiesEx** à la place.</span><span class="sxs-lookup"><span data-stu-id="e913d-109">Set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e913d-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e913d-110">See also</span></span>

- [<span data-ttu-id="e913d-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e913d-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

