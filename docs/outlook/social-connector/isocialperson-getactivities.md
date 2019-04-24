---
title: ISocialPersonGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cf727140-f6e7-4718-bd74-1f8feeccf70c
description: Cette méthode a été déconseillée dans Outlook Social Connector 2013.
ms.openlocfilehash: abad4fc2a3e3aaea8a7097ac7e6f56b0aadae299
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286163"
---
# <a name="isocialpersongetactivities"></a>ISocialPerson::GetActivities

Cette méthode a été déconseillée dans Outlook Social Connector 2013.
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a>Remarques

À partir d'Outlook Social Connector 2013, le OSC prend uniquement en charge la synchronisation à la demande des activités et n'est pas mise en cache ni synchronisation hybride des activités. Le fichier OSC ignore le paramètre **cacheActivities** dans le code XML des fonctionnalités et n'appelle pas cette méthode. Pour prendre en charge la recherche dynamique d'activités, implémentez la méthode [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) . Définissez **cacheActivities** sur **false**, **GetActivities** et **dynamicActivitiesLookupEx** sur **true**, ce qui invite l'OSC à appeler **ISocialSession2:: GetActivitiesEx** . 
  
Pour plus d'informations sur la façon dont l'OSC Obtient les activités des amis, consultez la rubrique [synchronisation des amis et des activités](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Voir aussi

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

