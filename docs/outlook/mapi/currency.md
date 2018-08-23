---
title: CURRENCY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CURRENCY
api_type:
- COM
ms.assetid: cffc05a0-95e4-4b9f-bf8f-c4272a75afa8
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b5a2cd09942559167300d8a921987864b8c5e48f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576462"
---
# <a name="currency"></a>CURRENCY

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un entier signé de 64 bits représentant une valeur monétaire. 
  
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

 **LO**
  
> Poids faible 32 bits de la valeur monétaire. 
    
 **Salut**
  
> Ordre haut 32 bits de la valeur monétaire.
    
## <a name="remarks"></a>Remarques

La structure de **devise** est une représentation sous forme d’entier à l’échelle d’un nombre décimal avec quatre chiffres à droite du séparateur décimal. Par exemple, une valeur stockée de 327500 doit être interprété comme représentant une valeur de devise de 32.7500. 
  
La structure de la **devise** est utilisée pour décrire une propriété de type PT_CURRENCY. Pour plus d’informations sur les types de propriété, voir [Vue d’ensemble des types de propriété MAPI](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

