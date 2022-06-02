---
title: ISocialPersonGetActivities
description: ISocialPersonGetActivities a été déprécié dans Outlook Social Connector 2013. Fournit des références à la synchronisation d’amis et d’activités.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: cf727140-f6e7-4718-bd74-1f8feeccf70c
ms.openlocfilehash: 8184c4e4f9185fd0490ba8c78314e7c6e736a2e8
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65852564"
---
# <a name="isocialpersongetactivities"></a>ISocialPerson::GetActivities

Cette méthode a été déconseillée dans Outlook Social Connector 2013.
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a>Remarques

À compter de Outlook Social Connector 2013, osc prend en charge uniquement la synchronisation à la demande des activités et non la synchronisation hybride ou mise en cache des activités. L’OSC ignore le paramètre **cacheActivities** dans le code XML des fonctionnalités et n’appelle pas cette méthode. Pour prendre en charge la recherche d’activités dynamiques, implémentez la méthode [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) . Définissez **cacheActivities** comme **false**, **getActivities** et **dynamicActivitiesLookupEx** comme **true**, ce qui invite l’OSC à appeler **ISocialSession2::GetActivitiesEx** à la place. 
  
Pour plus d’informations sur la façon dont la OSC obtient les activités des amis, consultez [Synchroniser les amis et les activités](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Voir aussi

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

