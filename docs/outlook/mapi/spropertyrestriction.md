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
description: Décrit une restriction de propriété utilisée pour faire correspondre une constante à la valeur d’une propriété.
ms.openlocfilehash: f906c826595a71eb549bc53658e379ffea4a5327
ms.sourcegitcommit: a1434c24ee2b92bd0faac5f37d9baa1d05b42058
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/27/2022
ms.locfileid: "67052428"
---
# <a name="spropertyrestriction"></a>SPropertyRestriction

**S’applique à** : Outlook 2013 | Outlook 2016
  
Décrit une restriction de propriété utilisée pour faire correspondre une constante à la valeur d’une propriété.
  
|Propriété |Valeur |
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

- RELOP_GE : la comparaison est effectuée en fonction d’une première valeur supérieure ou égale.

- RELOP_GT : la comparaison est effectuée en fonction d’une première valeur supérieure.

- RELOP_LE : la comparaison est effectuée sur la base d’une première valeur inférieure ou égale.

- RELOP_LT : la comparaison est effectuée en fonction d’une première valeur inférieure.

- RELOP_NE : La comparaison est effectuée en fonction de valeurs inégales.

- RELOP_RE : la comparaison est effectuée en fonction des valeurs LIKE (expression régulière).

- RELOP_EQ : la comparaison est effectuée sur la base de valeurs égales.

**ulPropTag**
  
> Balise de propriété identifiant la propriété à comparer.

**lpProp**
  
> Pointeur vers une structure [SPropValue](spropvalue.md) qui contient la valeur constante qui sera utilisée dans la comparaison.

## <a name="remarks"></a>Remarques

Il existe deux balises de propriété dans une structure **SPropertyRestriction** . L’un se trouve dans le membre **ulPropTag** et l’autre dans le membre **ulPropTag** de la structure **SPropValue** pointée par **lpProp**. MAPI nécessite à la fois le champ d’identificateur de propriété et le champ de type de propriété. **L’ulPropTag** dans **SPropertyRestriction** est la propriété à mettre en correspondance, et le pointeur **lpProp** de **SPropertyRestriction** vers le type **ulPropTag** du **SPropValue** indique comment la valeur des membres de **l’union lpProp** est interprétée. Les deux types de propriétés doivent correspondre, sinon la valeur d’erreur MAPI_E_TOO_COMPLEX est retournée lorsque la restriction est utilisée dans un appel à [IMAPITable::Restrict](imapitable-restrict.md) ou [IMAPITable::FindRow](imapitable-findrow.md).
  
L’ordre de comparaison est _(valeur de propriété) (opérateur relationnel) (valeur constante)._
  
Lorsqu’une restriction de propriété est passée à **IMAPITable::Restrict** ou **IMAPITable::FindRow** et que la propriété cible n’existe pas, les résultats de la restriction ne sont pas définis. En créant une restriction **AND** qui joint la restriction de propriété à une restriction **EXIST** , un appelant peut obtenir des résultats précis. Utilisez une structure [SExistRestriction](sexistrestriction.md) pour définir la restriction **EXIST** et une structure [SAndRestriction](sandrestriction.md) pour définir la restriction **AND** .
  
Dans le cas spécifique de Exchange Server 2019, les comparaisons effectuées sur le serveur présentent un comportement tel que les propriétés absentes sont traitées comme si elles étaient présentes et avaient une valeur inférieure à la valeur minimale de type de données possible. En d’autres termes, si un objet MAPI qui n’a pas de propriété PR_SENSITIVITY et qui est testé avec une ``SPropertyRestriction{RELOP_LT, PR_SENSITIVITY, {PR_SENSITIVITY, 0, {.l = INT_MIN}}`` structure, la comparaison donne « true ». (Ceci est cohérent avec la spécification « is undefined » ci-dessus.)
  
Les balises de propriétés à valeurs multiples peuvent être utilisées dans les restrictions de propriétés si le fournisseur de services qui implémente la table les prend en charge. Si elles sont prises en charge, les balises de propriétés à valeurs multiples peuvent être utilisées partout où des balises de propriétés à valeur unique peuvent être utilisées.
  
Les balises de propriétés à valeurs multiples peuvent être utilisées dans les méthodes suivantes :
  
- [IMAPIProp::SetProps](imapiprop-setprops.md)

- [IMAPIProp::GetProps](imapiprop-getprops.md)

- [IMAPITable::SetColumns](imapitable-setcolumns.md)

- [IMAPITable::SortTable](imapitable-sorttable.md)

- [IMAPITable::Restrict](imapitable-restrict.md)

> [!IMPORTANT]
> Un cas notable où les deux balises de propriété ne correspondent pas est si la restriction sur une propriété à valeurs multiples. Dans ce cas, ce qui suit doit être vrai.
> Si le type de propriété de **l’ulPropTag** de **SPropertyRestriction** contient l’indicateur de bits de type de propriété à valeurs multiples MV_FLAG (0x1000), le type de propriété de **l’ulPropTag** de **SPropValue** doit correspondre à l’indicateur de bits MV_FLAG, c’est-à-dire son inverse. > Par exemple, pour restreindre l’utilisation d’une propriété de chaîne personnalisée à valeurs multiples, telle qu’une catégorie avec une balise de propriété pour la propriété 0x8012101f, c’est-à-dire PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012)), la **SPropertyRestriction** correspondante apparaît comme suit.
> `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`
> `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`> `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> Notez que si le type de propriété de **l’ulPropTag** de **SPropValue** contient l’indicateur de bits MV_FLAG, le retour probable est MAPI_E_TOO_COMPLEX.
  
Pour plus d’informations sur la structure **SPropertyRestriction** , consultez [À propos des restrictions](about-restrictions.md).
  
## <a name="see-also"></a>Voir aussi

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)
- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [IMAPITable::FindRow](imapitable-findrow.md)
- [IMAPITable::Restrict](imapitable-restrict.md)
- [Structures MAPI](mapi-structures.md)
