---
title: CURRENCY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CURRENCY
api_type:
- COM
ms.assetid: cffc05a0-95e4-4b9f-bf8f-c4272a75afa8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5da768e4d26ad76e17a1c7271405739b52a2c028
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592521"
---
# <a name="currency"></a>CURRENCY

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un integer signé 64 bits représentant une valeur monétaire. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct tagCY
{
  unsigned long Lo;
  long Hi;
} CURRENCY;

```

## <a name="members"></a>Members

 **Lo**
  
> 32 bits de bas ordre de la valeur monétaire. 
    
 **Salut**
  
> 32 bits de haut ordre de la valeur monétaire.
    
## <a name="remarks"></a>Remarques

La structure **CURRENCY** est une représentation entière à l’échelle d’un nombre décimal à quatre chiffres à droite de la virgule décimale. Par exemple, une valeur stockée de 327 500 doit être interprétée comme représentant une valeur monétaire de 32,7500. 
  
La structure **CURRENCY** est utilisée pour décrire une propriété de type PT_CURRENCY. Pour plus d’informations sur les types de propriétés, voir [MAPI Property Type Overview](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

