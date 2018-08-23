---
title: SPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropTagArray
api_type:
- COM
ms.assetid: 4a9e1579-bebe-4a51-8ced-6dba9c3bcb63
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 5237a5c2767920bdb604bfe86603cea4fca56b84
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572773"
---
# <a name="sproptagarray"></a>SPropTagArray

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un tableau de balises de propriété. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macros connexes :  <br/> |[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md) <br/> |
   
```cpp
typedef struct _SPropTagArray
{
  ULONG cValues;
  ULONG aulPropTag[MAPI_DIM];
} SPropTagArray, FAR *LPSPropTagArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Nombre de balises de propriété dans le tableau indiqué par le membre **aulPropTag** . 
    
 **aulPropTag**
  
> Tableau de balises de propriété.
    
## <a name="remarks"></a>Remarques

Une balise de propriété est un entier non signé 32 bits qui se compose de deux parties : 
  
- Un identificateur dans l’ordre de haut niveau 16 bits.
    
- Un type dans les 16 bits de poids faible.
    
L’identificateur est une valeur numérique dans une plage spécifique. MAPI définit les plages pour les identificateurs décrire la propriété qui est utilisée pour et qui est chargé de maintenance. MAPI définit des contraintes pour chacune des balises de propriété pris en charge dans le fichier d’en-tête Mapitags.h.
  
Le type indique le format de la valeur de propriété. MAPI définit des constantes pour chacun des types de propriété pris en charge dans le fichier d’en-tête Mapidefs.h. 
  
Pour plus d’informations sur les balises de propriétés et leurs composants, consultez les rubriques suivantes : 
  
[Balises de propriété MAPI](mapi-property-tags.md)
  
[Vue d’ensemble d’identificateur de propriété MAPI](mapi-property-identifier-overview.md)
  
[Vue d’ensemble des types de propriété MAPI](mapi-property-type-overview.md)
  
Pour obtenir une liste complète des types de propriété à valeur unique et à valeurs multiples, voir l’annexe, [les Types et les identificateurs de propriété](property-identifiers-and-types.md). 
  
## <a name="see-also"></a>Voir aussi



[Structures MAPI](mapi-structures.md)

