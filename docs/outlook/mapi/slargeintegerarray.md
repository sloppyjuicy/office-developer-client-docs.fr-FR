---
title: SLargeIntegerArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLargeIntegerArray
api_type:
- COM
ms.assetid: 9ec9a674-c1a2-4137-856f-6cabe6f0eb9f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ab82fff2645a5e1861523eb3f1866e0ddc7d13a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331387"
---
# <a name="slargeintegerarray"></a>SLargeIntegerArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de structures [LARGE_INTEGER](https://go.microsoft.com/fwlink/?LinkId=132130) utilisées pour décrire une propriété de type PT_MV_I8. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SLargeIntegerArray
{
  ULONG cValues;
  LARGE_INTEGER FAR *lpli;
} SLargeIntegerArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Nombre de valeurs dans le tableau vers lequel pointe le membre **lpli** . 
    
 **lpli**
  
> Pointeur vers un tableau de structures **LARGE_INTEGER** contenant les valeurs entières. 
    
## <a name="remarks"></a>Remarques

Pour plus d'informations sur PT_MV_18, consultez la rubrique [liste des types de propriétés](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

