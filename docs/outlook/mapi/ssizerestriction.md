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
ms.openlocfilehash: 24ceb7b5358447de3a240756227b86224d2c354c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439085"
---
# <a name="ssizerestriction"></a>SSizeRestriction

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une restriction de taille qui est utilisée pour tester la taille d'une valeur de propriété. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
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
  
> Opérateur relationnel utilisé dans la comparaison de taille. Les valeurs possibles sont les suivantes: 
    
RELOP_GE 
  
> La comparaison est effectuée en fonction d'une valeur supérieure ou égale à la première valeur.
    
RELOP_GT 
  
> La comparaison est effectuée en fonction d'une valeur supérieure.
    
RELOP_LE 
  
> La comparaison est effectuée en fonction d'une valeur inférieure ou égale à la première valeur.
    
RELOP_LT 
  
> La comparaison est effectuée en fonction d'une valeur inférieure.
    
RELOP_NE 
  
> La comparaison est effectuée en fonction de valeurs inégales.
    
RELOP_RE 
  
> La comparaison est effectuée en fonction des valeurs LIKE (expression régulière).
    
RELOP_EQ 
  
> La comparaison est effectuée en fonction de valeurs égales.
    
 **ulPropTag**
  
> Balise de propriété identifiant la propriété à tester.
    
 **cb**
  
> Nombre d'octets dans la valeur de la propriété.
    
## <a name="remarks"></a>Remarques

Pour plus d'informations sur le fonctionnement des restrictions, consultez la rubrique [à propos des restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Voir aussi



[SRestriction](srestriction.md)


[Structures MAPI](mapi-structures.md)

