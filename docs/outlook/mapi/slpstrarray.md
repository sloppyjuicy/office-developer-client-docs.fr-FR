---
title: SLPSTRArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLPSTRArray
api_type:
- COM
ms.assetid: 5f570d9b-eb3d-4fc7-bcbe-348a0b8fe9e9
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 987020bd6fd49fcba9453075cd502bd5cea4c3a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361151"
---
# <a name="slpstrarray"></a>SLPSTRArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de valeurs de chaîne utilisées pour décrire une propriété de type PT_MV_STRING8.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Nombre de valeurs dans le tableau vers lequel pointe le membre **lppszA** . 
    
 **lppszA**
  
> Pointeur vers un tableau de chaînes de caractères 8 bits terminées par null.
    
## <a name="remarks"></a>Remarques

Pour plus d'informations sur PT_MV_STRING8, consultez la rubrique [liste des types de propriétés](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

