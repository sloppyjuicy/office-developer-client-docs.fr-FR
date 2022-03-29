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
description: Contient un tableau de valeurs d’heure utilisées pour décrire une propriété de type PT_MV_SYSTIME pour Outlook 2013 ou Outlook 2016.
ms.openlocfilehash: 067b218891d1e3cf65cd1414c882880c069e4ddd
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64454711"
---
# <a name="sdatetimearray"></a>SDateTimeArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de valeurs d’heure utilisées pour décrire une propriété de type PT_MV_SYSTIME.
  
|Propriété |Valeur |
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
  
> Nombre de valeurs dans le tableau pointées par **le membre lpft** . 
    
 **lpft**
  
> Pointeur vers un tableau de structures [FILETIME](filetime.md) qui contiennent les valeurs d’heure. 
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur PT_MV_SYSTIME, voir [Liste des types de propriétés](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[FILETIME](filetime.md)
  
[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

