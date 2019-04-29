---
title: SBinaryArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinaryArray
api_type:
- COM
ms.assetid: 2d5b7302-cad2-4522-beb1-7c6c711f42e6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 12fefbe15491837878608540006e5dd7dc3033ea
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438287"
---
# <a name="sbinaryarray"></a>SBinaryArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de valeurs binaires. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Nombre de valeurs dans le tableau vers lequel pointe le membre **lpbin** . 
    
 **lpbin**
  
> Pointeur vers un tableau de structures [SBinary](sbinary.md) qui contient les valeurs binaires. 
    
## <a name="remarks"></a>Remarques

La structure **SBinaryArray** est utilisée pour décrire les propriétés de type PT_MV_BINARY. 
  
Pour plus d'informations sur PT_MV_BINARY, consultez la rubrique [liste des types de propriétés](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[SBinary](sbinary.md)
  
[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

