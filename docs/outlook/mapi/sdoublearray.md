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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 6986ed7c9ab9932c5d95fcfb7f74f80088f21971
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580368"
---
# <a name="sdoublearray"></a>SDoubleArray

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un tableau de type double utilisé pour décrire une propriété de type PT_MV_DOUBLE.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SDoubleArray
{
  ULONG cValues;
  double FAR *lpdbl;
} SDoubleArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Nombre de valeurs dans le tableau indiqué par le membre **lpdbl** . 
    
 **lpdbl**
  
> Pointeur vers un tableau de valeurs de type doubles.
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur PT_MV_DOUBLE, voir la [Liste des Types de propriété](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

