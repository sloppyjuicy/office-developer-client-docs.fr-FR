---
title: ISocialSessionGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6546be99-aee4-41a6-8297-ace378776503
description: Cette méthode a été déconseillée dans OSC 1.1.
ms.openlocfilehash: dc5fe25e4c4f83717309d407963d0046aa6063ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787607"
---
# <a name="isocialsessiongetactivities"></a>ISocialSession::GetActivities

Cette méthode a été déconseillée dans OSC 1.1.
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a>Remarques

À compter d’OSC 1.1, l’OSC appelle n’est plus **GetActivities**. L’OSC ignore la valeur de **dynamicActivitiesLookup**. Pour prendre en charge la recherche d’activités dynamique, implémentez la méthode [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) . Définissez **cacheActivities** comme **false**et **getActivities** et **dynamicActivitiesLookupEx** en tant que **la valeur true**, ce qui vous invite à l’OSC à appeler **ISocialSession2::GetActivitiesEx** à la place. 
  
## <a name="see-also"></a>Voir aussi

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

