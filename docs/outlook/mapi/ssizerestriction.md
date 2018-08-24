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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 990fe49d39a73c5bf80b9fdda96d2e5997869edf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595418"
---
# <a name="ssizerestriction"></a>SSizeRestriction

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
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

## <a name="members"></a>Members

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

