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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6ebc4e9cbc79a71a91f1f2f3eec0d40de979ab18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787078"
---
# <a name="scomparepropsrestriction"></a>SComparePropsRestriction

**S’applique à**: Outlook 
  
Décrit une restriction de propriété de comparaison qui teste les deux propriétés à l’aide d’un opérateur relationnel. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SComparePropsRestriction
{
  ULONG relop;
  ULONG ulPropTag1;
  ULONG ulPropTag2;
} SComparePropsRestriction;

```

## <a name="members"></a>Membres

**RelOp**
  
> Opérateur de relation à utiliser pour comparer les deux propriétés. Les valeurs possibles sont les suivantes :
    
  - RELOP_GE : La comparaison est effectuée en fonction d’une première valeur supérieure ou égale.
      
  - RELOP_GT : La comparaison est effectuée en fonction d’une première valeur supérieure.
      
  - RELOP_LE : La comparaison est effectuée en fonction d’une première valeur inférieur ou égale.
      
  - RELOP_LT : La comparaison est effectuée en fonction d’une première valeur plus faible.
      
  - RELOP_NE : La comparaison est effectuée en fonction de comparaison.
      
  - RELOP_RE : La comparaison est effectuée en fonction de comme valeurs (expression régulière).
      
  - RELOP_EQ : La comparaison est effectuée en fonction de des valeurs égales.
    
**ulPropTag1**
  
> Balise de propriété de la première propriété à comparer. 
    
**ulPropTag2**
  
> Balise de propriété de la seconde propriété à comparer.
    
## <a name="remarks"></a>Remarques

L’ordre de comparaison est _(balise de propriété (1) (opérateur relationnel) (balise de propriété 2)_. Les propriétés à comparer doivent être du même type. Tentative de comparer les propriétés de différents types, MAPI ou le fournisseur de services renvoyer la valeur d’erreur MAPI_E_TOO_COMPLEX à partir de la méthode [IMAPITable](imapitableiunknown.md) à laquelle la structure est transmise en tant que paramètre. 
  
Le résultat d’une restriction de valeur de propriété de comparaison est non défini lorsqu’un ou deux des propriétés n’existent pas. Lorsqu’un client requiert un comportement bien défini pour une telle restriction et n’est pas certain que la propriété existe, (par exemple, il se n'agit pas une colonne d’une table requise) il doit créer une restriction **et** pour participer à la restriction de propriété comparer avec un existe restriction. Utilisez une structure [SExistRestriction](sexistrestriction.md) pour définir la restriction existent et une structure [SAndRestriction](sandrestriction.md) pour définir la restriction **et** . 
  
Les propriétés spécifiées dans les membres **ulPropTag1** et **ulPropTag2** peuvent être à valeurs multiples si le fournisseur de services prend en charge. 
  
Pour plus d’informations sur les restrictions de structure **SComparePropsRestriction** en général, voir [à propos des Restrictions](about-restrictions.md).
  
## <a name="see-also"></a>Voir aussi

- [SBitMaskRestriction](sbitmaskrestriction.md)
- [SRestriction](srestriction.md)
- [Structures MAPI](mapi-structures.md)

