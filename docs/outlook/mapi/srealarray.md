---
title: SRealArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SRealArray
api_type:
- COM
ms.assetid: 95be07bf-5732-4775-9e0f-fec47e99d9b7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8c6fc32463fda6589f1cf8b2508c826bbcab1560
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566520"
---
# <a name="srealarray"></a>SRealArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de valeurs flottantes utilisées pour décrire une propriété de type PT_MV_R4. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Nombre de valeurs dans le tableau pointées par **le membre lpflt.** 
    
 **lpflt**
  
> Pointeur vers un tableau de valeurs flottantes.
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur PT_MV_R4 type de propriété, voir [Types de propriétés.](property-types.md)
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

