---
title: MAPIOFFLINE_AGGREGATEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 2e502d28-ae09-49d9-a35a-5d77acdcd6f4
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: df8b5dd061613b75627e6c1c9208efb81a531cdd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616753"
---
# <a name="mapioffline_aggregateinfo"></a>MAPIOFFLINE_AGGREGATEINFO

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La structure est utilisée [avec HrCreateOfflineObj](hrcreateofflineobj.md). 
  
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
  
> Pointeur vers l’objet IUnknown sur lequel cet objet est agrégé. Cela permet à tous les appels QueryInterface de passer à l’objet créé.
    
 **pRefTrackRoot**
  
> Doit être NULL.
    
## <a name="see-also"></a>Voir aussi



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_CREATEINFO](mapioffline_createinfo.md)

