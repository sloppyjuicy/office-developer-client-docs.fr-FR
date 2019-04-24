---
title: SAppTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAppTimeArray
api_type:
- COM
ms.assetid: 5a1ff95a-9862-4165-8a70-bd2eeb7fe683
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: dee1de19ed61fa4f8edab69152315d77545b01b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331695"
---
# <a name="sapptimearray"></a>SAppTimeArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de valeurs d'heure.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Nombre de valeurs dans le tableau vers lequel pointe le membre **LPAT** . 
    
 **LPAT**
  
> Pointeur vers un tableau de valeurs de temps d'application. 
    
## <a name="remarks"></a>Remarques

La structure **SAppTimeArray** est utilisée pour définir les propriétés de type PT_MV_APPTIME. Pour plus d'informations sur PT_MV_APPTIME, consultez la rubrique [liste des types de propriétés](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[Structures MAPI](mapi-structures.md)

