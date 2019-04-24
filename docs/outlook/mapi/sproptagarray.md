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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9a5be98298ab1f9333ac1c223a6ef594e60dd86a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344435"
---
# <a name="sproptagarray"></a>SPropTagArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de balises de propriété. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Macros connexes:  <br/> |[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md) <br/> |
   
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

Une balise de propriété est un entier non signé 32 bits composé de deux parties: 
  
- Identificateur dans l'ordre décroissant de 16 bits.
    
- Un type dans les bits de poids faible 16.
    
L'identificateur est une valeur numérique dans une plage particulière. MAPI définit des plages d'identificateurs pour décrire ce à quoi la propriété est utilisée et qui est responsable de sa maintenance. MAPI définit des contraintes pour chacune des balises de propriété qu'il prend en charge dans le fichier d'en-tête Mapitags. h.
  
Le type indique le format de la valeur de la propriété. MAPI définit des constantes pour chaque type de propriété qu'il prend en charge dans le fichier d'en-tête Mapidefs. h. 
  
Pour plus d'informations sur les balises de propriétés et leurs composants, consultez l'une des rubriques suivantes: 
  
[Balises de propriété MAPI](mapi-property-tags.md)
  
[Vue d'ensemble de l'identificateur de propriété MAPI](mapi-property-identifier-overview.md)
  
[Vue d'ensemble du type de propriété MAPI](mapi-property-type-overview.md)
  
Pour obtenir la liste complète des types de propriétés à valeur unique et à valeurs multiples, consultez l'annexe, [identificateurs et types de propriétés](property-identifiers-and-types.md). 
  
## <a name="see-also"></a>Voir aussi



[Structures MAPI](mapi-structures.md)

