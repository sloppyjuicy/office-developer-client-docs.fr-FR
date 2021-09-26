---
title: SPropertyRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SPropertyRestriction
api_type:
- COM
ms.assetid: 2bbf13e9-05b3-4498-8e08-d9e07505190d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 66ee8e34cc8c42e2ac656284d91a2f2b64c669da
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629556"
---
# <a name="spropertyrestriction"></a>SPropertyRestriction

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une restriction de propriété utilisée pour faire correspondre une constante à la valeur d’une propriété.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SPropertyRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  LPSPropValue lpProp;
} SPropertyRestriction;

```

## <a name="members"></a>Members

**relop**
  
> Opérateur relationnel qui sera utilisé dans la recherche. Les valeurs possibles sont les suivantes :
    
  - RELOP_GE : la comparaison est réalisée en fonction d’une première valeur supérieure ou égale.
        
  - RELOP_GT : la comparaison est réalisée en fonction d’une première valeur supérieure.
        
  - RELOP_LE : la comparaison est réalisée en fonction d’une première valeur inférieure ou égale.
        
  - RELOP_LT : la comparaison est réalisée en fonction d’une première valeur inférieure.
        
  - RELOP_NE : la comparaison est réalisée en fonction de valeurs différentes.
        
  - RELOP_RE : la comparaison est réalisée en fonction des valeurs LIKE (expression régulière).
        
  - RELOP_EQ : la comparaison est réalisée sur la base de valeurs égales.
    
**ulPropTag**
  
> Balise de propriété identifiant la propriété à comparer. 
    
**lpProp**
  
> Pointeur vers une structure [SPropValue](spropvalue.md) qui contient la valeur constante qui sera utilisée dans la comparaison. 
    
## <a name="remarks"></a>Remarques

Il existe deux balises de propriété dans une structure **SPropertyRestriction.** L’un se trouve dans le membre **ulPropTag** et l’autre dans le membre **ulPropTag** de la structure **SPropValue** pointée par **lpProp**. MAPI requiert à la fois le champ d’identificateur de propriété et le champ de type de propriété. **UlPropTag** dans **SPropertyRestriction** est la propriété à mettre en correspondance, et le pointeur **lpProp** du **SPropertyRestriction** vers le type **ulPropTag**'s de **la valeur SPropValue** indique comment la valeur des membres de **l’union lpProp est** interprétée. Les deux types de propriété doivent correspondre, sinon la valeur d’erreur MAPI_E_TOO_COMPLEX est renvoyée lorsque la restriction est utilisée dans un appel à [IMAPITable::Restrict](imapitable-restrict.md) ou [IMAPITable::FindRow](imapitable-findrow.md). 
  
L’ordre de comparaison _est (valeur de propriété) (opérateur relationnel) (valeur constante)._
  
Lorsqu’une restriction de propriété est transmise à **IMAPITable::Restrict** ou **IMAPITable::FindRow** et que la propriété cible n’existe pas, les résultats de la restriction ne sont pas indéfinis. En créant une restriction **AND** qui joint la restriction de propriété à une restriction **EXIST,** un appelant peut obtenir des résultats précis. Utilisez une structure [SExistRestriction](sexistrestriction.md) pour définir la restriction **EXIST** et une structure [SAndRestriction](sandrestriction.md) pour définir la restriction **AND.** 
  
Les balises de propriétés à valeurs multiples peuvent être utilisées dans les restrictions de propriété si le fournisseur de services qui implémente la table les prend en charge. Si elle est prise en charge, des balises de propriétés à valeurs multiples peuvent être utilisées partout où les balises de propriété à valeur unique peuvent être utilisées. 
  
Les balises de propriétés à valeurs multiples peuvent être utilisées dans les méthodes suivantes :
  
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::GetProps](imapiprop-getprops.md)
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [IMAPITable::Restrict](imapitable-restrict.md)
    
> [!IMPORTANT]
> Un cas notable lorsque les deux balises de propriété ne correspondent pas est si restreindre sur une propriété à valeurs multiples. Dans ce cas, les valeurs suivantes doivent être vraies. > Si le type de propriété du **ulPropTag** de **SPropertyRestriction** contient le MV_FLAG (0x1000) d’indicateur de type propriété à valeurs multiples, le type de propriété du **ulPropTag** de **SPropValue** doit correspondre à l’ancien signe moins l’indicateur de bits MV_FLAG, c’est-à-dire son inverse. > Par exemple, pour restreindre l’utilisation d’une propriété de chaîne personnalisée à valeurs multiples telle qu’une catégorie avec une balise de propriété pour la 0x8012101f de propriété, autrement dit, PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012)), la valeur **SPropertyRestriction** correspondante apparaît comme suit. >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> notez que si le type de propriété **du ulPropTag** de **SPropValue** contient l’indicateur de bits MV_FLAG, le retour probable est MAPI_E_TOO_COMPLEX. 
  
Pour plus d’informations sur la structure **SPropertyRestriction,** voir [À propos des restrictions.](about-restrictions.md) 
  
## <a name="see-also"></a>Voir aussi

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)
- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [IMAPITable::FindRow](imapitable-findrow.md)
- [IMAPITable::Restrict](imapitable-restrict.md)
- [Structures MAPI](mapi-structures.md)

