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
ms.openlocfilehash: 54b5cd6d681aa1e8008eade024ef57783bf18ead
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787624"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a><span data-ttu-id="f0903-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="f0903-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span></span>

<span data-ttu-id="f0903-104">Cette méthode a été déconseillée dans Outlook Social Connector 2013.</span><span class="sxs-lookup"><span data-stu-id="f0903-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a><span data-ttu-id="f0903-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="f0903-105">Remarks</span></span>

<span data-ttu-id="f0903-106">Démarrage dans Outlook Social Connector 2013, l’OSC prend en charge la synchronisation des activités uniquement sur demande et non mis en cache ou synchronisation hybride des activités.</span><span class="sxs-lookup"><span data-stu-id="f0903-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="f0903-107">L’OSC ignore le paramètre **cacheActivities** dans le XML des fonctionnalités et n’est plus appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="f0903-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and no longer calls this method.</span></span> <span data-ttu-id="f0903-108">Pour prendre en charge la recherche d’activités dynamique, implémentez la méthode [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) .</span><span class="sxs-lookup"><span data-stu-id="f0903-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="f0903-109">Définissez **getActivities** et **dynamicActivitiesLookupEx** comme **true**, ce qui vous invite à l’OSC à appeler **ISocialSession2::GetActivitiesEx** à la place.</span><span class="sxs-lookup"><span data-stu-id="f0903-109">Set **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="f0903-110">Pour plus d’informations sur comment l’OSC Obtient les activités de vos amis, voir [synchronisation des amis et des activités](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="f0903-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f0903-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0903-111">See also</span></span>

- [<span data-ttu-id="f0903-112">ISocialProfile : ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="f0903-112">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)

