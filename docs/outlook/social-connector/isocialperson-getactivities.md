---
title: ISocialPersonGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: cf727140-f6e7-4718-bd74-1f8feeccf70c
description: Cette méthode a été Outlook Social Connector 2013.
ms.openlocfilehash: c225cd19c2e3d02ebddae70ccd98ad5d59f783ed
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563244"
---
# <a name="isocialpersongetactivities"></a>ISocialPerson::GetActivities

Cette méthode a été Outlook Social Connector 2013.
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a>Remarques

À compter de Outlook Social Connector 2013, OSC prend en charge uniquement la synchronisation à la demande des activités et non la synchronisation hybride ou mise en cache des activités. L’OSC ignore le **paramètre cacheActivities** dans le XML de fonctionnalités et n’appelle pas cette méthode. Pour prendre en charge la recherche d’activités dynamiques, implémentez la méthode [ISocialSession2::GetActivitiesEx.](isocialsession2-getactivitiesex.md) Définissez **cacheActivities** sur **false**, **getActivities** et **dynamicActivitiesLookupEx** comme **true**, ce qui invite l’OSC à appeler **ISocialSession2::GetActivitiesEx** à la place. 
  
Pour plus d’informations sur la façon dont OSC obtient les activités des amis, voir [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Voir aussi

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

