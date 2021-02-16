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
  
Décrit une restriction de propriété de comparaison, qui teste deux propriétés à l’aide d’un opérateur relationnel. 
  
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

## <a name="members"></a>Members

**relop**
  
> Opérateur relationnel à utiliser pour comparer les deux propriétés. Les valeurs possibles sont les suivantes :
    
  - RELOP_GE : la comparaison est réalisée en fonction d’une première valeur supérieure ou égale.
      
  - RELOP_GT : la comparaison est réalisée en fonction d’une première valeur supérieure.
      
  - RELOP_LE : la comparaison est réalisée en fonction d’une première valeur inférieure ou égale.
      
  - RELOP_LT : la comparaison est réalisée en fonction d’une première valeur inférieure.
      
  - RELOP_NE : la comparaison est réalisée en fonction de valeurs différentes.
      
  - RELOP_RE : la comparaison est réalisée en fonction des valeurs LIKE (expression régulière).
      
  - RELOP_EQ : la comparaison est réalisée sur la base de valeurs égales.
    
**ulPropTag1**
  
> Balise de propriété de la première propriété à comparer. 
    
**ulPropTag2**
  
> Balise de propriété de la deuxième propriété à comparer.
    
## <a name="remarks"></a>Remarques

L’ordre de comparaison _est (balise de propriété 1) (opérateur relationnel) (balise de propriété 2)._ Les propriétés à comparer doivent être du même type. Si vous essayez de comparer des propriétés de différents types, MAPI ou le fournisseur de services retourne la valeur d’erreur MAPI_E_TOO_COMPLEX à partir de la méthode [IMAPITable](imapitableiunknown.md) à laquelle la structure est passée en tant que paramètre. 
  
Le résultat d’une restriction de valeur de propriété de comparaison n’est pas définie lorsqu’une ou les deux propriétés n’existent pas. Lorsqu’un client nécessite un comportement bien défini pour une telle restriction et qu’il n’est pas sûr que la propriété existe (par exemple, il ne s’agit pas d’une colonne obligatoire d’une table), il doit créer une restriction **AND** pour joindre la restriction de comparaison de propriétés à une restriction existante. Utilisez une structure [SExistRestriction](sexistrestriction.md) pour définir la restriction existante et une structure [SAndRestriction](sandrestriction.md) pour définir la restriction **AND.** 
  
Les propriétés spécifiées dans les membres **ulPropTag1** et **ulPropTag2** peuvent avoir plusieurs valeurs si le fournisseur de services la prend en charge. 
  
Pour plus d’informations sur la structure et les restrictions **SComparePropsRestriction** en général, voir [à propos des restrictions](about-restrictions.md).
  
## <a name="see-also"></a>Voir aussi

- [SBitMaskRestriction](sbitmaskrestriction.md)
- [SRestriction](srestriction.md)
- [Structures MAPI](mapi-structures.md)

