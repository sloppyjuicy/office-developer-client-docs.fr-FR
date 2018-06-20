---
title: ISocialSessionGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6546be99-aee4-41a6-8297-ace378776503
description: Cette méthode a été déconseillée dans OSC 1.1.
ms.openlocfilehash: dc5fe25e4c4f83717309d407963d0046aa6063ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787607"
---
# <a name="isocialsessiongetactivities"></a><span data-ttu-id="93f3f-103">ISocialSession::GetActivities</span><span class="sxs-lookup"><span data-stu-id="93f3f-103">ISocialSession::GetActivities</span></span>

<span data-ttu-id="93f3f-104">Cette méthode a été déconseillée dans OSC 1.1.</span><span class="sxs-lookup"><span data-stu-id="93f3f-104">This method has been deprecated in OSC 1.1.</span></span>
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a><span data-ttu-id="93f3f-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="93f3f-105">Remarks</span></span>

<span data-ttu-id="93f3f-106">À compter d’OSC 1.1, l’OSC appelle n’est plus **GetActivities**.</span><span class="sxs-lookup"><span data-stu-id="93f3f-106">Starting in OSC 1.1, the OSC no longer calls **GetActivities**.</span></span> <span data-ttu-id="93f3f-107">L’OSC ignore la valeur de **dynamicActivitiesLookup**.</span><span class="sxs-lookup"><span data-stu-id="93f3f-107">The OSC ignores the value of **dynamicActivitiesLookup**.</span></span> <span data-ttu-id="93f3f-108">Pour prendre en charge la recherche d’activités dynamique, implémentez la méthode [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) .</span><span class="sxs-lookup"><span data-stu-id="93f3f-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="93f3f-109">Définissez **cacheActivities** comme **false**et **getActivities** et **dynamicActivitiesLookupEx** en tant que **la valeur true**, ce qui vous invite à l’OSC à appeler **ISocialSession2::GetActivitiesEx** à la place.</span><span class="sxs-lookup"><span data-stu-id="93f3f-109">Set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="93f3f-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93f3f-110">See also</span></span>

- [<span data-ttu-id="93f3f-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="93f3f-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

