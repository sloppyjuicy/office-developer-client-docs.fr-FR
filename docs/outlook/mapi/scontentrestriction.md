---
title: SContentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SContentRestriction
api_type:
- COM
ms.assetid: 784c8a5a-493e-48e6-8784-ba8122c76e3d
description: Décrit une restriction de contenu, qui est utilisée pour limiter un affichage tableau aux seules lignes qui incluent une colonne dont le contenu correspond à une chaîne de recherche.
ms.openlocfilehash: 9294b9b4ce8c356d4908da975b68d68f5c43a9d5
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455250"
---
# <a name="scontentrestriction"></a>SContentRestriction
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une restriction de contenu, qui est utilisée pour limiter un affichage tableau aux seules lignes qui incluent une colonne dont le contenu correspond à une chaîne de recherche. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SContentRestriction
{
  ULONG        ulFuzzyLevel;
  ULONG        ulPropTag;
  LPSPropValue lpProp;
} SContentRestriction;

```

## <a name="members"></a>Members

**ulFuzzyLevel**
  
> Paramètres d’option définissant le niveau de précision que la restriction de contenu doit appliquer lorsque vous vérifiez la correspondance.
    
   Les **16 bits inférieurs** du membre **ulFuzzyLevel** s’appliquent aux propriétés de type PT_BINARY et PT_STRING8 et doivent être définies sur l’une des valeurs suivantes : 
    
   - FL_FULLSTRING : pour correspondre, la chaîne de recherche **lpProp** doit être contenue dans la propriété identifiée par **ulPropTag**.
        
   - FL_PREFIX : pour correspondre, la chaîne de **recherche lpProp** doit apparaître au début de la propriété identifiée par **ulPropTag**. Les deux chaînes doivent être comparées uniquement jusqu’à la longueur de la chaîne de recherche indiquée par **lpProp**. 
        
   - FL_SUBSTRING : pour correspondre, la chaîne de recherche **lpProp** doit être contenue n’importe où dans la propriété identifiée par **ulPropTag**. 
        
   Les **16 bits supérieurs** du membre **ulFuzzyLevel** s’appliquent uniquement aux propriétés de type PT_STRING8 et peuvent être définies sur les valeurs suivantes dans n’importe quelle combinaison : 
        
   - FL_IGNORECASE : la comparaison doit être réalisée sans prendre en compte la cause. 
        
   - FL_IGNORENONSPACE : la comparaison doit ignorer les caractères non définis par Unicode, tels que les signes diacritiques. 
        
   - FL_LOOSE : la comparaison doit vous donner une correspondance autant que possible, en ignorant les caractères de cas et sans espacement. 
    
**ulPropTag**
  
> Balise de propriété identifiant la propriété de chaîne à vérifier pour l’occurrence de la chaîne de recherche. 
    
**lpProp**
  
> Pointeur vers une structure de valeurs de propriété qui contient la valeur de chaîne à utiliser comme chaîne de recherche.
    
## <a name="remarks"></a>Remarques

Il existe deux balises de propriété dans une structure **SContentRestriction** : l’une dans le membre **ulPropTag** et l’autre dans le membre **ulPropTag** de la structure **SPropValue** pointée par **lpProp**. Dans les deux balises, MAPI requiert uniquement le champ de type de propriété et ignore le champ d’identificateur de propriété. Toutefois, les deux types de propriété doivent correspondre, sinon la valeur d’erreur MAPI_E_TOO_COMPLEX est renvoyée lorsque la restriction est utilisée dans un appel à [IMAPITable::Restrict](imapitable-restrict.md) ou [IMAPITable::FindRow](imapitable-findrow.md). 
  
Les valeurs FL_FULLSTRING, FL_PREFIX et FL_SUBSTRING s’excluent mutuellement. Un seul d’entre eux peut être définie, et l’un d’eux doit être définie. Leurs significations sont corrigées et le fournisseur doit les implémenter exactement comme défini. Le fournisseur doit renvoyer MAPI_E_TOO_COMPLEX s’il ne parvient pas à prendre en charge ces valeurs. 
  
Les valeurs FL_IGNORECASE, FL_IGNORENONSPACE et FL_LOOSE sont indépendantes. N’importe où entre zéro et les trois peuvent être définies. Leurs définitions sont fournies à titre indicatif uniquement et le fournisseur est libre d’implémenter sa propre signification spécifique de chaque indicateur. Le fournisseur ne doit pas renvoyer d’indication d’erreur s’il n’a pas d’implémentation d’un indicateur spécifié. 
  
Le résultat d’une restriction de contenu imposée à une propriété n’est pas définie lorsque la propriété n’existe pas. Lorsqu’un client requiert un comportement bien défini pour une telle restriction et qu’il n’est pas sûr que la propriété existe, par exemple, il ne s’agit pas d’une colonne obligatoire d’une table qu’il doit créer une restriction **AND** pour joindre la restriction de contenu avec une restriction existante. Utilisez une structure [SExistRestriction](sexistrestriction.md) pour définir la restriction existante et une structure [SAndRestriction](sandrestriction.md) pour définir la restriction **AND** . 
  
Pour plus d’informations sur la structure et les restrictions **de SContentRestriction** en général, voir [À propos des restrictions](about-restrictions.md).
  
## <a name="see-also"></a>Voir aussi

- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [Structures MAPI](mapi-structures.md)

