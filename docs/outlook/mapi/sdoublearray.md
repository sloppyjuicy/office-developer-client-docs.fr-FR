---
title: SDoubleArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SDoubleArray
api_type:
- COM
ms.assetid: b63b26de-faf9-453c-ab8b-fb703ed09ae8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 160fdc7ecc27a2a2a14882090f674441655540f5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609494"
---
# <a name="sdoublearray"></a>SDoubleArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de doubles utilisé pour décrire une propriété de type PT_MV_DOUBLE.
  
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
  
> Nombre de valeurs dans le tableau pointées par **le membre lpdbl.** 
    
 **lpdbl**
  
> Pointeur vers un tableau de valeurs doubles.
    
## <a name="remarks"></a>Remarques

Pour plus d’informations PT_MV_DOUBLE, voir [Liste des types de propriétés.](property-types.md)
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

