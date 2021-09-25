---
title: SDateTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SDateTimeArray
api_type:
- COM
ms.assetid: 6a0dff65-1055-487c-9d15-4cfe336f2ad7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: af16c7ab02a2cc5dbc72f828d29e292547051d95
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578689"
---
# <a name="sdatetimearray"></a>SDateTimeArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de valeurs d’heure utilisées pour décrire une propriété de type PT_MV_SYSTIME.
  
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

## <a name="members"></a>Members

 **cValues**
  
> Nombre de valeurs dans le tableau pointées par **le membre lpft.** 
    
 **lpft**
  
> Pointeur vers un tableau de structures [FILETIME](filetime.md) qui contiennent les valeurs d’heure. 
    
## <a name="remarks"></a>Remarques

Pour plus d’informations PT_MV_SYSTIME, voir [Liste des types de propriétés.](property-types.md)
  
## <a name="see-also"></a>Voir aussi



[FILETIME](filetime.md)
  
[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

