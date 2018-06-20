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
ms.openlocfilehash: af952b6d57325e1b52093fcf655e6fdc271ca34f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787586"
---
# <a name="isocialpersongetactivities"></a>ISocialPerson::GetActivities

Cette méthode a été déconseillée dans Outlook Social Connector 2013.
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a>Remarques

Démarrage dans Outlook Social Connector 2013, l’OSC prend en charge la synchronisation des activités uniquement sur demande et non mis en cache ou synchronisation hybride des activités. L’OSC ignore le paramètre **cacheActivities** dans le XML des fonctionnalités et n’appelle pas cette méthode. Pour prendre en charge la recherche d’activités dynamique, implémentez la méthode [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) . Définir **cacheActivities** comme **faux**, **getActivities** et **dynamicActivitiesLookupEx** en tant que **la valeur true**, ce qui vous invite à l’OSC à appeler **ISocialSession2::GetActivitiesEx** à la place. 
  
Pour plus d’informations sur comment l’OSC Obtient les activités de vos amis, voir [synchronisation des amis et des activités](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Voir aussi

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

