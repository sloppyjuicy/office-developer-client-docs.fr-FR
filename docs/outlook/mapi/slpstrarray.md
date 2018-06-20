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
ms.openlocfilehash: 6d2bb6bdb934e0b02831b813b1246a3df4193e0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787195"
---
# <a name="slpstrarray"></a>SLPSTRArray

  
  
**S’applique à**: Outlook 
  
Contient un tableau de valeurs de chaîne qui sont utilisés pour décrire une propriété de type PT_MV_STRING8.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a>Membres

 **cValues**
  
> Nombre de valeurs dans le tableau indiqué par le membre **lppszA** . 
    
 **lppszA**
  
> Pointeur vers un tableau de chaînes de caractères de 8 bits fin à la valeur null.
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur PT_MV_STRING8, voir la [Liste des Types de propriété](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

