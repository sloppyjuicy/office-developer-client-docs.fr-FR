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
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a>ISocialProfile::GetActivitiesOfFriendsAndColleagues

Cette méthode a été déconseillée dans Outlook Social Connector 2013.
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a>Remarques

À partir d'Outlook Social Connector 2013, le OSC prend uniquement en charge la synchronisation à la demande des activités et n'est pas mise en cache ni synchronisation hybride des activités. Le fichier OSC ignore le paramètre **cacheActivities** dans le code XML des fonctionnalités et n'appelle plus cette méthode. Pour prendre en charge la recherche dynamique d'activités, implémentez la méthode [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) . Définissez **GetActivities** et **dynamicActivitiesLookupEx** sur **true**, ce qui entraîne l'invite de la propriété OSC à appeler **ISocialSession2:: GetActivitiesEx** . 
  
Pour plus d'informations sur la façon dont l'OSC Obtient les activités des amis, consultez la rubrique [synchronisation des amis et des activités](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Voir aussi

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

