---
title: SDoubleArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDoubleArray
api_type:
- COM
ms.assetid: b63b26de-faf9-453c-ab8b-fb703ed09ae8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 91440d619c8ad8a64b2bac7463a26d9c196a3c0f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439267"
---
# <a name="sdoublearray"></a>SDoubleArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de doubles utilisés pour décrire une propriété de type PT_MV_DOUBLE.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SDoubleArray
{
  ULONG cValues;
  double FAR *lpdbl;
} SDoubleArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Nombre de valeurs dans le tableau vers lequel pointe le membre **lpdbl** . 
    
 **lpdbl**
  
> Pointeur vers un tableau de valeurs de type double.
    
## <a name="remarks"></a>Remarques

Pour plus d'informations sur PT_MV_DOUBLE, consultez la rubrique [liste des types de propriétés](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

