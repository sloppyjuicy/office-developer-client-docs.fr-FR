---
title: SSizeRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SSizeRestriction
api_type:
- COM
ms.assetid: 4e7340d1-3cb9-4276-b83f-1c8f94acb909
description: Décrit une restriction de taille utilisée pour tester la taille d’une valeur de propriété pour Outlook 2013 et Outlook 2016.
ms.openlocfilehash: 108659ebcf80d90a408a4d7fbf0543a9fde578af
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455642"
---
# <a name="ssizerestriction"></a>SSizeRestriction

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une restriction de taille utilisée pour tester la taille d’une valeur de propriété. 
  
|Propriété |Valeur |
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

 **relop**
  
> Opérateur relationnel utilisé dans la comparaison de tailles. Les valeurs possibles sont les suivantes : 
    
RELOP_GE 
  
> La comparaison est réalisée en fonction d’une première valeur supérieure ou égale.
    
RELOP_GT 
  
> La comparaison est réalisée en fonction d’une première valeur supérieure.
    
RELOP_LE 
  
> La comparaison est réalisée sur la base d’une première valeur inférieure ou égale.
    
RELOP_LT 
  
> La comparaison est réalisée en fonction d’une première valeur inférieure.
    
RELOP_NE 
  
> La comparaison est basée sur des valeurs différentes.
    
RELOP_RE 
  
> La comparaison est réalisée en fonction des valeurs LIKE (expression régulière).
    
RELOP_EQ 
  
> La comparaison est réalisée sur la base de valeurs égales.
    
 **ulPropTag**
  
> Balise de propriété identifiant la propriété à tester.
    
 **cb**
  
> Nombre d’octets dans la valeur de la propriété.
    
## <a name="remarks"></a>Remarques

Pour une discussion générale sur le fonctionnement des restrictions, voir [À propos des restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Voir aussi



[SRestriction](srestriction.md)


[Structures MAPI](mapi-structures.md)

