---
title: MAPIOFFLINE_AGGREGATEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2e502d28-ae09-49d9-a35a-5d77acdcd6f4
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 4775de0707eb90549f07525e3aa54ec5842f6050
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357133"
---
# <a name="mapiofflineaggregateinfo"></a>MAPIOFFLINE_AGGREGATEINFO

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La structure est utilisée avec [HrCreateOfflineObj](hrcreateofflineobj.md). 
  
```cpp
typedef struct
{
  ULONG            ulSize;
  IUnknown*          pOuterObj;
  IUnknown*          pRefTrackRoot;
} MAPIOFFLINE_AGGREGATEINFO;
```

## <a name="members"></a>Members

 **ulSize**
  
> Taille de la structure.
    
 **pOuterObj**
  
> Pointeur vers l'objet IUnknown sur lequel cet objet est regroupé. Cela permet aux appels QueryInterface de passer par l'objet créé.
    
 **pRefTrackRoot**
  
> Doit être NULL.
    
## <a name="see-also"></a>Voir aussi



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_CREATEINFO](mapioffline_createinfo.md)

