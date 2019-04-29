---
title: ISocialSessionGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6546be99-aee4-41a6-8297-ace378776503
description: Cette méthode a été déconseillée dans OSC 1,1.
ms.openlocfilehash: 29a7cdc9895dcfa2bd926d95dbd2089b7a5dc778
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439295"
---
# <a name="isocialsessiongetactivities"></a>ISocialSession::GetActivities

Cette méthode a été déconseillée dans OSC 1,1.
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a>Remarques

À partir du OSC 1,1, le OSC n'appelle plus **GetActivities**. Le OSC ignore la valeur de **dynamicActivitiesLookup**. Pour prendre en charge la recherche dynamique d'activités, implémentez la méthode [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) . Définissez **cacheActivities** sur **false**et **GetActivities** et **dynamicActivitiesLookupEx** sur **true**, ce qui invite l'OSC à appeler **ISocialSession2:: GetActivitiesEx** . 
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

