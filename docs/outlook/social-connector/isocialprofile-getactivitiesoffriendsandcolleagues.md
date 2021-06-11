---
title: ISocialProfileGetActivitiesOfFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4aaf7417-0a03-42a4-a282-599327ec5381
description: Cette méthode a été Outlook Social Connector 2013.
ms.openlocfilehash: c02cf0e8a6d2da3f9fb7704c92e10e0409042393
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406891"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a><span data-ttu-id="4030c-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="4030c-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span></span>

<span data-ttu-id="4030c-104">Cette méthode a été Outlook Social Connector 2013.</span><span class="sxs-lookup"><span data-stu-id="4030c-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a><span data-ttu-id="4030c-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="4030c-105">Remarks</span></span>

<span data-ttu-id="4030c-106">À compter de Outlook Social Connector 2013, OSC prend en charge uniquement la synchronisation à la demande des activités et non la synchronisation hybride ou mise en cache des activités.</span><span class="sxs-lookup"><span data-stu-id="4030c-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="4030c-107">L’OSC ignore le **paramètre cacheActivities** dans le XML de fonctionnalités et n’appelle plus cette méthode.</span><span class="sxs-lookup"><span data-stu-id="4030c-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and no longer calls this method.</span></span> <span data-ttu-id="4030c-108">Pour prendre en charge la recherche d’activités dynamiques, implémentez la méthode [ISocialSession2::GetActivitiesEx.](isocialsession2-getactivitiesex.md)</span><span class="sxs-lookup"><span data-stu-id="4030c-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="4030c-109">Définissez **getActivities** et **dynamicActivitiesLookupEx** sur **true,** ce qui invite l’OSC à appeler **ISocialSession2::GetActivitiesEx** à la place.</span><span class="sxs-lookup"><span data-stu-id="4030c-109">Set **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="4030c-110">Pour plus d’informations sur la façon dont OSC obtient les activités des amis, voir [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="4030c-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4030c-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4030c-111">See also</span></span>

- [<span data-ttu-id="4030c-112">ISocialProfile : ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="4030c-112">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)

