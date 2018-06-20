---
title: SDateTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDateTimeArray
api_type:
- COM
ms.assetid: 6a0dff65-1055-487c-9d15-4cfe336f2ad7
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9734adff9c9c7526fc8ff46d17ca913752e104b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787087"
---
# <a name="sdatetimearray"></a>SDateTimeArray

  
  
**S’applique à**: Outlook 
  
Contient un tableau de valeurs de temps qui sont utilisés pour décrire une propriété de type PT_MV_SYSTIME.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SDateTimeArray
{
  ULONG cValues;
  FILETIME FAR *lpft;
} SDateTimeArray;

```

## <a name="members"></a>Membres

 **cValues**
  
> Nombre de valeurs dans le tableau indiqué par le membre **lpft** . 
    
 **lpft**
  
> Pointeur vers un tableau de structures [FILETIME](filetime.md) qui contiennent les valeurs d’heure. 
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur PT_MV_SYSTIME, voir la [Liste des Types de propriété](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[FILETIME](filetime.md)
  
[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

