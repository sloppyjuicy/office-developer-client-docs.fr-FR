---
title: ISocialSessionGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 6546be99-aee4-41a6-8297-ace378776503
description: Cette méthode a été dépréciée dans OSC 1.1.
ms.openlocfilehash: 6cc6137091ec1c10cd2e92f904149597935b094a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608812"
---
# <a name="isocialsessiongetactivities"></a>ISocialSession::GetActivities

Cette méthode a été dépréciée dans OSC 1.1.
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a>Remarques

À compter d’OSC 1.1, l’OSC n’appelle plus **GetActivities.** L’OSC ignore la valeur **de dynamicActivitiesLookup**. Pour prendre en charge la recherche d’activités dynamiques, implémentez la méthode [ISocialSession2::GetActivitiesEx.](isocialsession2-getactivitiesex.md) Définissez **cacheActivities** sur **false** et **getActivities** et **dynamicActivitiesLookupEx** sur **true,** ce qui invite l’OSC à appeler **ISocialSession2::GetActivitiesEx** à la place. 
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

