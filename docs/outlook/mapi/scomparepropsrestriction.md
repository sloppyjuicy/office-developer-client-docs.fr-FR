---
title: SComparePropsRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SComparePropsRestriction
api_type:
- COM
ms.assetid: 3231a91a-1ef2-4dd8-9f3e-79ca56d2eae9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 513ec0db4e99e687d8aeb9e1d6acdef73df4d158
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33440002"
---
# <a name="scomparepropsrestriction"></a>SComparePropsRestriction

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une restriction de propriété compare, qui teste deux propriétés à l'aide d'un opérateur relationnel. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SComparePropsRestriction
{
  ULONG relop;
  ULONG ulPropTag1;
  ULONG ulPropTag2;
} SComparePropsRestriction;

```

## <a name="members"></a>Members

**RelOp**
  
> Opérateur relationnel à utiliser pour comparer les deux propriétés. Les valeurs possibles sont les suivantes:
    
  - RELOP_GE: la comparaison est effectuée en fonction d'une première valeur supérieure ou égale.
      
  - RELOP_GT: la comparaison est effectuée en fonction d'une valeur supérieure.
      
  - RELOP_LE: la comparaison est effectuée en fonction d'une valeur inférieure ou égale à la première valeur.
      
  - RELOP_LT: la comparaison est effectuée en fonction d'une valeur inférieure.
      
  - RELOP_NE: la comparaison est effectuée en fonction de valeurs inégales.
      
  - RELOP_RE: la comparaison est effectuée en fonction des valeurs LIKE (expression régulière).
      
  - RELOP_EQ: la comparaison est effectuée en fonction de valeurs égales.
    
**ulPropTag1**
  
> Balise de propriété de la première propriété à comparer. 
    
**ulPropTag2**
  
> Balise de propriété de la deuxième propriété à comparer.
    
## <a name="remarks"></a>Remarques

L'ordre de comparaison est _(balise de propriété 1) (opérateur relationnel) (balise de propriété 2)_. Les propriétés à comparer doivent être du même type. Si vous tentez de comparer des propriétés de types différents, MAPI ou le fournisseur de services renvoie la valeur d'erreur MAPI_E_TOO_COMPLEX à partir de la méthode [IMAPITable](imapitableiunknown.md) que la structure est transmise en tant que paramètre. 
  
Le résultat d'une restriction de valeur de la propriété compare n'est pas défini lorsque l'une ou les deux propriétés n'existent pas. Lorsqu'un client a besoin d'un comportement bien défini pour une restriction de ce type et qu'il n'est pas certain que la propriété existe, (par exemple, il ne s'agit pas d'une colonne obligatoire d'un tableau), il doit créer une restriction **et** rejoigne la restriction de propriété compare existante. restreindre. Utilisez une structure [SExistRestriction](sexistrestriction.md) pour définir la restriction exist et une structure [SAndRestriction](sandrestriction.md) pour définir la restriction **et** . 
  
Les propriétés spécifiées dans les membres **ulPropTag1** et **ulPropTag2** peuvent être à valeurs multiples si le fournisseur de services le prend en charge. 
  
Pour plus d'informations sur la structure **SComparePropsRestriction** et les restrictions en général, consultez la rubrique [à propos des restrictions](about-restrictions.md).
  
## <a name="see-also"></a>Voir aussi

- [SBitMaskRestriction](sbitmaskrestriction.md)
- [SRestriction](srestriction.md)
- [Structures MAPI](mapi-structures.md)

