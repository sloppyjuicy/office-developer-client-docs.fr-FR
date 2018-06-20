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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: cde59b73381458533910dc8f0a728cc4e6ca0c01
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787099"
---
# <a name="sdoublearray"></a>SDoubleArray

  
  
**S’applique à**: Outlook 
  
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

## <a name="members"></a>Membres

 **cValues**
  
> Nombre de valeurs dans le tableau indiqué par le membre **lpdbl** . 
    
 **lpdbl**
  
> Pointeur vers un tableau de valeurs de type doubles.
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur PT_MV_DOUBLE, voir la [Liste des Types de propriété](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

