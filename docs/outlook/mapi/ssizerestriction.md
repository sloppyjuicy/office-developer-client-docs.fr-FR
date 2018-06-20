---
title: SSizeRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSizeRestriction
api_type:
- COM
ms.assetid: 4e7340d1-3cb9-4276-b83f-1c8f94acb909
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 134eb844ef7b72d396c300b27a87a3a7ae320cf1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787258"
---
# <a name="ssizerestriction"></a>SSizeRestriction

  
  
**S’applique à**: Outlook 
  
Décrit une restriction de taille qui est utilisée pour tester la taille d’une valeur de propriété. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SSizeRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  ULONG cb;
} SSizeRestriction;

```

## <a name="members"></a>Membres

 **RelOp**
  
> Opérateur de relation qui est utilisé dans la comparaison de taille. Les valeurs possibles sont les suivantes : 
    
RELOP_GE 
  
> La comparaison est effectuée en fonction d’une première valeur supérieure ou égale.
    
RELOP_GT 
  
> La comparaison est effectuée en fonction d’une première valeur supérieure.
    
RELOP_LE 
  
> La comparaison est effectuée en fonction d’une première valeur inférieur ou égale.
    
RELOP_LT 
  
> La comparaison est effectuée en fonction d’une première valeur plus faible.
    
RELOP_NE 
  
> La comparaison est effectuée en fonction de comparaison.
    
RELOP_RE 
  
> La comparaison est effectuée en fonction de comme valeurs (expression régulière).
    
RELOP_EQ 
  
> La comparaison est effectuée en fonction des valeurs égales.
    
 **ulPropTag**
  
> Balise de propriété qui identifie la propriété à tester.
    
 **cb**
  
> Nombre d’octets de la valeur de propriété.
    
## <a name="remarks"></a>Remarques

Pour une présentation générale du fonctionnement des restrictions, voir [à propos des Restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Voir aussi



[SRestriction](srestriction.md)


[Structures MAPI](mapi-structures.md)

