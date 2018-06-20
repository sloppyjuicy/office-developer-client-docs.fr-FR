---
title: SRealArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRealArray
api_type:
- COM
ms.assetid: 95be07bf-5732-4775-9e0f-fec47e99d9b7
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c64e9a7497a70ea34dc09a5749dd281a24f9413d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787238"
---
# <a name="srealarray"></a>SRealArray

  
  
**S’applique à**: Outlook 
  
Contient un tableau de valeurs float qui sont utilisées pour décrire une propriété de type PT_MV_R4. 
  
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

## <a name="members"></a>Membres

 **cValues**
  
> Nombre de valeurs dans le tableau indiqué par le membre **lpflt** . 
    
 **lpflt**
  
> Pointeur vers un tableau de valeurs float.
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur le type de propriété PT_MV_R4, voir [Types de propriété](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

