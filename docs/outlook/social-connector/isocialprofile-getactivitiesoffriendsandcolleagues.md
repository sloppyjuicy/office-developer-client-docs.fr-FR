---
title: ISocialProfileGetActivitiesOfFriendsAndColleagues
description: ISocialProfile GetActivitiesOfFriendsAndColleagues a été déprécié dans Outlook Social Connector 2013.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 4aaf7417-0a03-42a4-a282-599327ec5381
ms.openlocfilehash: 07f010f5d37d1a44ae114425364e7e2600777d8a
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65852550"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a>ISocialProfile::GetActivitiesOfFriendsAndColleagues

Cette méthode a été déconseillée dans Outlook Social Connector 2013.
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a>Remarques

À compter de Outlook Social Connector 2013, osc prend en charge uniquement la synchronisation à la demande des activités et non la synchronisation hybride ou mise en cache des activités. Le système d’exploitation ignore le paramètre **cacheActivities** dans le code XML des fonctionnalités et n’appelle plus cette méthode. Pour prendre en charge la recherche d’activités dynamiques, implémentez la méthode [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) . Définissez **getActivities** et **dynamicActivitiesLookupEx** sur **true**, ce qui invite l’OSC à appeler **ISocialSession2::GetActivitiesEx** à la place. 
  
Pour plus d’informations sur la façon dont la OSC obtient les activités des amis, consultez [Synchroniser les amis et les activités](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Voir aussi

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

