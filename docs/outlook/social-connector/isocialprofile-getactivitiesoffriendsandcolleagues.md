---
title: ISocialProfileGetActivitiesOfFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4aaf7417-0a03-42a4-a282-599327ec5381
description: Cette méthode a été déconseillée dans Outlook Social Connector 2013.
ms.openlocfilehash: c02cf0e8a6d2da3f9fb7704c92e10e0409042393
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285963"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a><span data-ttu-id="d274e-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="d274e-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span></span>

<span data-ttu-id="d274e-104">Cette méthode a été déconseillée dans Outlook Social Connector 2013.</span><span class="sxs-lookup"><span data-stu-id="d274e-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a><span data-ttu-id="d274e-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="d274e-105">Remarks</span></span>

<span data-ttu-id="d274e-106">À partir d'Outlook Social Connector 2013, le OSC prend uniquement en charge la synchronisation à la demande des activités et n'est pas mise en cache ni synchronisation hybride des activités.</span><span class="sxs-lookup"><span data-stu-id="d274e-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="d274e-107">Le fichier OSC ignore le paramètre **cacheActivities** dans le code XML des fonctionnalités et n'appelle plus cette méthode.</span><span class="sxs-lookup"><span data-stu-id="d274e-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and no longer calls this method.</span></span> <span data-ttu-id="d274e-108">Pour prendre en charge la recherche dynamique d'activités, implémentez la méthode [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) .</span><span class="sxs-lookup"><span data-stu-id="d274e-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="d274e-109">Définissez **GetActivities** et **dynamicActivitiesLookupEx** sur **true**, ce qui entraîne l'invite de la propriété OSC à appeler **ISocialSession2:: GetActivitiesEx** .</span><span class="sxs-lookup"><span data-stu-id="d274e-109">Set **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="d274e-110">Pour plus d'informations sur la façon dont l'OSC Obtient les activités des amis, consultez la rubrique [synchronisation des amis et des activités](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="d274e-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d274e-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d274e-111">See also</span></span>

- [<span data-ttu-id="d274e-112">ISocialProfile : ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="d274e-112">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)

