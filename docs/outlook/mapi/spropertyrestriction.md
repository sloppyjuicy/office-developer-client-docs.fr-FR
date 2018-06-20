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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f59b0041f271010e56dda2f73d2248f133bc1325
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787224"
---
# <a name="spropertyrestriction"></a>SPropertyRestriction

**S’applique à**: Outlook 
  
Décrit une restriction de propriété qui est utilisée pour la correspondance d’une constante avec la valeur d’une propriété.
  
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

## <a name="members"></a>Membres

**RelOp**
  
> Opérateur relationnel qui sera utilisé dans la recherche. Les valeurs possibles sont les suivantes :
    
  - RELOP_GE : La comparaison est effectuée en fonction d’une première valeur supérieure ou égale.
        
  - RELOP_GT : La comparaison est effectuée en fonction d’une première valeur supérieure.
        
  - RELOP_LE : La comparaison est effectuée en fonction d’une première valeur inférieur ou égale.
        
  - RELOP_LT : La comparaison est effectuée en fonction d’une première valeur plus faible.
        
  - RELOP_NE : La comparaison est effectuée en fonction de comparaison.
        
  - RELOP_RE : La comparaison est effectuée en fonction de comme valeurs (expression régulière).
        
  - RELOP_EQ : La comparaison est effectuée en fonction de des valeurs égales.
    
**ulPropTag**
  
> Balise de propriété qui identifie la propriété à comparer. 
    
**lpProp**
  
> Pointeur vers une structure [SPropValue](spropvalue.md) qui contient la valeur de constante qui sera utilisée lors de la comparaison. 
    
## <a name="remarks"></a>Remarques

Il existe deux balises de propriété dans une structure **SPropertyRestriction** . Est le membre **ulPropTag** et l’autre dans le membre **ulPropTag** de la structure **SPropValue** désigné par **lpProp**. MAPI nécessite le champ d’identificateur de propriété et le champ de type de propriété. **ulPropTag** dans **SPropertyRestriction** est la propriété à mettre en correspondance, et le pointeur **lpProp** de l' **SPropertyRestriction** au type de **ulPropTag**d' de la **SPropValue** indique comment la valeur de membres de la union **lpProp** sont interprétées. Les types de deux propriété doivent correspondre, sinon la valeur d’erreur MAPI_E_TOO_COMPLEX est renvoyée lorsque la restriction est utilisée dans un appel à [IMAPITable](imapitable-restrict.md) ou [IMAPITable::FindRow](imapitable-findrow.md). 
  
L’ordre de comparaison est _(valeur de la propriété) (opérateur relationnel) (constante)_.
  
Lorsqu’une restriction de propriété est transmise à **IMAPITable** ou **IMAPITable::FindRow** et la propriété cible n’existe pas, les résultats de la restriction ne sont pas définis. En créant une restriction **et** qui rejoint la restriction de propriété avec une restriction **existe** , l’appelant peut être garanti des résultats précis. Utilisez une structure [SExistRestriction](sexistrestriction.md) pour définir la restriction **existent** et une structure [SAndRestriction](sandrestriction.md) pour définir la restriction **et** . 
  
Balises de propriété à valeurs multiples peuvent être utilisées dans les restrictions de propriété si le fournisseur de services l’implémentation de la table les prend en charge. Si prise en charge, propriété à valeurs multiples balises peut être utilisées n’importe où les balises de propriété à valeur unique peuvent être utilisées. 
  
Balises de propriété à valeurs multiples peuvent être utilisées dans les méthodes suivantes :
  
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::GetProps](imapiprop-getprops.md)
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [IMAPITable](imapitable-restrict.md)
    
> [!IMPORTANT]
> Un cas notable lorsque les balises de deux propriété ne correspondront pas se restriction sur une propriété à valeurs multiples. Dans ce cas, les informations suivantes doivent être vérifiées. > Si le type de propriété de **ulPropTag** de **SPropertyRestriction** contient le type de propriété à valeurs multiples bit indicateur MV_FLAG (0 x 1000), le type de propriété de **ulPropTag** de **SPropValue** doit correspondre à l’ancienne moins le MV_ INDICATEUR bit indicateur, autrement dit, son inverse. > Par exemple, pour limiter à l’aide d’une propriété de type chaîne à valeurs multiples comme une catégorie avec une balise de propriété pour la propriété 0x8012101f, c'est-à-dire PROP_TAG (MV_FLAG | PT_UNICODE, 0x8012)), le correspondant **SPropertyRestriction** apparaît sous la forme suit. >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> Notez que si le type de propriété de **ulPropTag** de **SPropValue** contient l’indicateur de bit MV_FLAG, le retour est MAPI_E_TOO_COMPLEX. 
  
Pour plus d’informations sur la structure **SPropertyRestriction** , voir [à propos des Restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Voir aussi

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)
- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [IMAPITable::FindRow](imapitable-findrow.md)
- [IMAPITable](imapitable-restrict.md)
- [Structures MAPI](mapi-structures.md)

