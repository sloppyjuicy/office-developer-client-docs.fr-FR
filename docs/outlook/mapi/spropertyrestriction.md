---
title: SPropertyRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropertyRestriction
api_type:
- COM
ms.assetid: 2bbf13e9-05b3-4498-8e08-d9e07505190d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 29d392eba530126e06a672c10044c5b4df0618c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406086"
---
# <a name="spropertyrestriction"></a>SPropertyRestriction

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une restriction de propriété qui est utilisée pour faire correspondre une constante à la valeur d'une propriété.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SPropertyRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  LPSPropValue lpProp;
} SPropertyRestriction;

```

## <a name="members"></a>Members

**RelOp**
  
> Opérateur relationnel qui sera utilisé dans la recherche. Les valeurs possibles sont les suivantes:
    
  - RELOP_GE: la comparaison est effectuée en fonction d'une première valeur supérieure ou égale.
        
  - RELOP_GT: la comparaison est effectuée en fonction d'une valeur supérieure.
        
  - RELOP_LE: la comparaison est effectuée en fonction d'une valeur inférieure ou égale à la première valeur.
        
  - RELOP_LT: la comparaison est effectuée en fonction d'une valeur inférieure.
        
  - RELOP_NE: la comparaison est effectuée en fonction de valeurs inégales.
        
  - RELOP_RE: la comparaison est effectuée en fonction des valeurs LIKE (expression régulière).
        
  - RELOP_EQ: la comparaison est effectuée en fonction de valeurs égales.
    
**ulPropTag**
  
> Balise de propriété identifiant la propriété à comparer. 
    
**lpProp**
  
> Pointeur vers une structure [SPropValue](spropvalue.md) qui contient la valeur de constante qui sera utilisée dans la comparaison. 
    
## <a name="remarks"></a>Remarques

Il existe deux balises de propriété dans une structure **SPropertyRestriction** . L'une se trouve dans le membre **ulPropTag** et l'autre dans le membre **ulPropTag** de la structure **SPropValue** pointée par **lpProp**. MAPI nécessite le champ identificateur de propriété et le champ type de propriété. Le **ulPropTag** dans **SPropertyRestriction** est la propriété à mettre en correspondance et le pointeur **lpProp** de l' **SPropertyRestriction** au type de **ulPropTag**de l' **SPropValue** indique comment la valeur des membres de l' **lpProp** Union sont interprétées. Les deux types de propriété doivent correspondre, sinon la valeur d'erreur MAPI_E_TOO_COMPLEX est renvoyée lorsque la restriction est utilisée dans un appel de [IMAPITable:: Restrict](imapitable-restrict.md) ou [IMAPITable:: FindRow](imapitable-findrow.md). 
  
L'ordre de comparaison est _(valeur de la propriété) (opérateur relationnel) (valeur constante)_.
  
Lorsqu'une restriction de propriété est transmise à une opération **IMAPITable** :: restrict ou **IMAPITable:: FindRow** et la propriété cible n'existe pas, les résultats de la restriction ne sont pas définis. En créant une restriction **et** qui rejoint la restriction de propriété avec une restriction **existante** , un appelant peut être assuré de résultats précis. Utilisez une structure [SExistRestriction](sexistrestriction.md) pour définir la restriction **exist** et une structure [SAndRestriction](sandrestriction.md) pour définir la restriction **et** . 
  
Les balises de propriété à valeurs multiples peuvent être utilisées dans les restrictions de propriété si le fournisseur de services implémentant le tableau les prend en charge. S'il est pris en charge, les balises de propriétés à valeurs multiples peuvent être utilisées partout où des balises de propriété à valeur unique peuvent être utilisées. 
  
Les balises de propriété à valeurs multiples peuvent être utilisées dans les méthodes suivantes:
  
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::GetProps](imapiprop-getprops.md)
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [IMAPITable::Restrict](imapitable-restrict.md)
    
> [!IMPORTANT]
> Un cas notable lorsque les deux balises de propriété ne correspondent pas s'il s'agit d'une restriction sur une propriété à valeurs multiples. Dans ce cas, les éléments suivants doivent être vrais. > si le type de propriété de l' **ulPropTag** de **SPropertyRestriction** contient le type de propriété à valeurs multiples indicateur binaire MV_FLAG (0x1000), le type de propriété de l' **ulPropTag** de **SPropValue** doit correspondre à l'ancien moins le MV_ Indicateur bit Flag, c'est-à-dire son inverse. > par exemple, pour limiter l'utilisation d'une propriété de chaîne personnalisée à valeurs multiples, telle qu'une catégorie avec une balise de propriété pour la propriété 0x8012101f, c'est-à-dire PROP_TAG (MV_FLAG | PT_UNICODE, 0x8012)), le **SPropertyRestriction** correspondant apparaîtra comme -. >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> Notez que si le type de propriété de l' **ulPropTag** de **SPropValue** contient l'indicateur de bit MV_FLAG, le retour probable est MAPI_E_TOO_COMPLEX. 
  
Pour plus d'informations sur la structure **SPropertyRestriction** , consultez la rubrique [à propos des restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Voir aussi

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)
- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [IMAPITable::FindRow](imapitable-findrow.md)
- [IMAPITable::Restrict](imapitable-restrict.md)
- [Structures MAPI](mapi-structures.md)

