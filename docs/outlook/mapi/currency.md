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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0789b566eb814fe984ae78670d22ad2937b0c3a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783122"
---
# <a name="currency"></a>CURRENCY

  
  
**S’applique à**: Outlook 
  
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

## <a name="members"></a>Membres

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

