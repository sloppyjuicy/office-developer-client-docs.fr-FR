---
title: CURRENCY
description: CURRENCY contient un entier 64 bits signé représentant une valeur monétaire. Cet article décrit ses membres et remarques.
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
ms.openlocfilehash: dabdd170201225cae144f4a00a01dd57370bb9cf
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815904"
---
# <a name="currency"></a>CURRENCY

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un entier 64 bits signé représentant une valeur monétaire. 
  
|Propriété |Valeur |
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
  
> Ordre faible 32 bits de la valeur monétaire. 
    
 **Salut**
  
> Ordre élevé 32 bits de la valeur monétaire.
    
## <a name="remarks"></a>Remarques

La structure **CURRENCY** est une représentation entière mise à l’échelle d’un nombre décimal avec quatre chiffres à droite de la virgule décimale. Par exemple, une valeur stockée de 327500 doit être interprétée comme représentant une valeur monétaire de 32,7500. 
  
La structure **CURRENCY** est utilisée pour décrire une propriété de type PT_CURRENCY. Pour plus d’informations sur les types de propriétés, consultez [vue d’ensemble du type de propriété MAPI](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

