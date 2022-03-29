---
title: SLongArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SLongArray
api_type:
- COM
ms.assetid: 57435634-202d-4998-9931-4562f1a66f5f
description: Contient un tableau de types de valeur LONG utilisés pour décrire une propriété de type PT_MV_LONG.
ms.openlocfilehash: e5598ce83cade0df1337596e1add17d65e0b77a6
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455222"
---
# <a name="slongarray"></a>SLongArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de types de valeur LONG utilisés pour décrire une propriété de type PT_MV_LONG. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Nombre de valeurs dans le tableau pointées par le **membre lpl** . 
    
 **lpl**
  
> Pointeur vers un tableau de valeurs LONG.
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur PT_MV_LONG, voir [Liste des types de propriétés](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

