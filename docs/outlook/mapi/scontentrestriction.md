---
title: SContentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SContentRestriction
api_type:
- COM
ms.assetid: 784c8a5a-493e-48e6-8784-ba8122c76e3d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 87be6df27a3e6729cb514118438521d76a66b30c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339836"
---
# <a name="scontentrestriction"></a>SContentRestriction
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une restriction de contenu, qui est utilisée pour limiter un affichage de tableau aux lignes qui incluent une colonne avec du contenu correspondant à une chaîne de recherche. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
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
  
> Paramètres d'option définissant le niveau de précision que la restriction de contenu doit appliquer lors de la vérification d'une correspondance.
    
   Les **16 bits inférieurs** du membre **ulFuzzyLevel** s'appliquent aux propriétés de type PT_BINARY et PT_STRING8 et doivent être définis sur l'une des valeurs suivantes: 
    
   - FL_FULLSTRING: pour la correspondance, la chaîne de recherche **lpProp** doit être contenue dans la propriété identifiée par **ulPropTag**.
        
   - FL_PREFIX: pour la correspondance, la chaîne de recherche **lpProp** doit apparaître au début de la propriété identifiée par **ulPropTag**. Les deux chaînes doivent être comparées uniquement à la longueur de la chaîne de recherche indiquée par **lpProp**. 
        
   - FL_SUBSTRING: pour la correspondance, la chaîne de recherche **lpProp** doit être contenue n'importe où dans la propriété identifiée par **ulPropTag**. 
        
   Les **16 bits supérieurs** du membre **ulFuzzyLevel** s'appliquent uniquement aux propriétés de type PT_STRING8 et peuvent être définis sur les valeurs suivantes dans n'importe quelle combinaison: 
        
   - FL_IGNORECASE: la comparaison doit être effectuée sans prendre en compte la casse. 
        
   - FL_IGNORENONSPACE: la comparaison doit ignorer les caractères non-espacement définis par Unicode, tels que les signes diacritiques. 
        
   - FL_LOOSE: la comparaison doit vous donner une correspondance dès que possible, en ignorant les caractères de casse et de non-espacement. 
    
**ulPropTag**
  
> Balise de propriété identifiant la propriété de chaîne devant faire l'objet de la chaîne de recherche. 
    
**lpProp**
  
> Pointeur vers une structure de valeur de propriété qui contient la valeur de chaîne à utiliser comme chaîne de recherche.
    
## <a name="remarks"></a>Remarques

Il existe deux balises de propriété dans une structure **SContentRestriction** : une dans le membre **ulPropTag** et l'autre dans le membre **ulPropTag** de la structure **SPropValue** vers laquelle pointe **lpProp**. Dans les deux balises, MAPI requiert uniquement le champ type de propriété et ignore le champ identificateur de propriété. Toutefois, les deux types de propriété doivent correspondre, sinon la valeur d'erreur MAPI_E_TOO_COMPLEX est renvoyée lorsque la restriction est utilisée dans un appel de la fonction [IMAPITable:: Restrict](imapitable-restrict.md) ou [IMAPITable:: FindRow](imapitable-findrow.md). 
  
Les valeurs FL_FULLSTRING, FL_PREFIX et FL_SUBSTRING s'excluent mutuellement. Un seul d'entre eux peut être défini et l'un d'entre eux doit être défini. Leur signification est fixe et le fournisseur doit les implémenter exactement comme défini. Le fournisseur doit renvoyer MAPI_E_TOO_COMPLEX s'il ne parvient pas à prendre en charge ces valeurs. 
  
Les valeurs FL_IGNORECASE, FL_IGNORENONSPACE et FL_LOOSE sont indépendantes. N'importe où entre zéro et les trois peuvent être définis. Leurs définitions sont fournies à titre indicatif uniquement et le fournisseur est libre d'implémenter sa propre signification particulière de chaque indicateur. Le fournisseur ne doit pas renvoyer d'indication d'erreur s'il n'a pas d'implémentation d'un indicateur spécifié. 
  
Le résultat d'une restriction de contenu imposée à une propriété n'est pas défini lorsque la propriété n'existe pas. Lorsqu'un client a besoin d'un comportement bien défini pour une restriction de ce type et qu'il n'est pas certain que la propriété existe, par exemple, il ne s'agit pas **** d'une colonne obligatoire d'un tableau, il doit créer une restriction pour joindre la restriction de contenu à une restriction existante. Utilisez une structure [SExistRestriction](sexistrestriction.md) pour définir la restriction exist et une structure [SAndRestriction](sandrestriction.md) pour définir la restriction **et** . 
  
Pour plus d'informations sur la structure **SContentRestriction** et les restrictions en général, consultez la rubrique [à propos des restrictions](about-restrictions.md).
  
## <a name="see-also"></a>Voir aussi

- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [Structures MAPI](mapi-structures.md)

