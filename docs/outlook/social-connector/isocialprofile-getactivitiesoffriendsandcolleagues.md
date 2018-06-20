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
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a>ISocialProfile::GetActivitiesOfFriendsAndColleagues

Cette méthode a été déconseillée dans Outlook Social Connector 2013.
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a>Remarques

Démarrage dans Outlook Social Connector 2013, l’OSC prend en charge la synchronisation des activités uniquement sur demande et non mis en cache ou synchronisation hybride des activités. L’OSC ignore le paramètre **cacheActivities** dans le XML des fonctionnalités et n’est plus appelle cette méthode. Pour prendre en charge la recherche d’activités dynamique, implémentez la méthode [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) . Définissez **getActivities** et **dynamicActivitiesLookupEx** comme **true**, ce qui vous invite à l’OSC à appeler **ISocialSession2::GetActivitiesEx** à la place. 
  
Pour plus d’informations sur comment l’OSC Obtient les activités de vos amis, voir [synchronisation des amis et des activités](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Voir aussi

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

