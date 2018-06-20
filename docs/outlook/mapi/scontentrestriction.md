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
ms.openlocfilehash: 34177aee48adad7eecb40836a247705fc22d2a32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787086"
---
# <a name="scontentrestriction"></a>SContentRestriction
 
**S’applique à**: Outlook 
  
Décrit une restriction de contenu, qui est utilisée pour limiter un affichage de tableau uniquement aux lignes qui comportent une colonne correspond à une chaîne de recherche de contenu. 
  
|||
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

## <a name="members"></a>Membres

**ulFuzzyLevel**
  
> Options définissant le niveau de précision que permettent que la restriction de contenu doit appliquer lors de la vérification pour une correspondance.
    
   Les **16 bits inférieurs** du membre **ulFuzzyLevel** s’appliquent aux propriétés de type PT_BINARY et PT_STRING8 et doit être défini sur une des valeurs suivantes : 
    
   - FL_FULLSTRING : Pour faire correspondre, la chaîne de recherche **lpProp** doit être contenue dans la propriété identifiée par **ulPropTag**.
        
   - FL_PREFIX : Pour faire correspondre, la chaîne de recherche **lpProp** doit apparaître au début de la propriété identifiée par **ulPropTag**. Les deux chaînes doivent être comparées uniquement jusqu'à la longueur de la chaîne de recherche indiquée par **lpProp**. 
        
   - FL_SUBSTRING : Pour faire correspondre, la chaîne de recherche **lpProp** doit figurer n’importe où dans la propriété identifiée par **ulPropTag**. 
        
   Les **derniers 16 bits** du membre **ulFuzzyLevel** s’appliquent uniquement aux propriétés de type PT_STRING8 et peut avoir les valeurs suivantes dans n’importe quelle combinaison : 
        
   - FL_IGNORECASE : La comparaison doit être effectuée sans tenir compte des cas. 
        
   - FL_IGNORENONSPACE : La comparaison doit ignorer les caractères de sans espace définie par l’Unicode tels que diacritiques. 
        
   - FL_LOOSE : La comparaison doit vous fournir une correspondance la mesure du possible, en ignorant la casse et les caractères sans espace. 
    
**ulPropTag**
  
> Balise de propriété qui identifie la propriété de type chaîne à vérifier pour une occurrence de la chaîne de recherche. 
    
**lpProp**
  
> Pointeur vers une structure de valeur de propriété qui contient la valeur de chaîne à utiliser comme la chaîne de recherche.
    
## <a name="remarks"></a>Remarques

Il existe deux balises de propriété dans une structure **SContentRestriction** : 1 dans le membre **ulPropTag** et l’autre dans le membre **ulPropTag** de la structure **SPropValue** désignés par **lpProp**. Dans les deux balises, MAPI nécessite uniquement le champ de type de propriété et ignore le champ d’identificateur de propriété. Toutefois, les types de deux propriété doivent correspondre, sinon la valeur d’erreur MAPI_E_TOO_COMPLEX est renvoyée lorsque la restriction est utilisée dans un appel à [IMAPITable](imapitable-restrict.md) ou [IMAPITable::FindRow](imapitable-findrow.md). 
  
Les valeurs FL_FULLSTRING, FL_PREFIX et FL_SUBSTRING s’excluent mutuellement. Un seul d'entre eux peut être défini et qu’un d'entre eux doit être défini. Leurs significations sont fixes, et le fournisseur doit implémenter les exactement tel que défini. Le fournisseur doit retourner MAPI_E_TOO_COMPLEX si elle ne peut pas prendre en charge ces valeurs. 
  
Les valeurs FL_IGNORECASE, FL_IGNORENONSPACE et FL_LOOSE sont indépendants. N’importe où à partir de zéro à trois d'entre eux peut être définie. Leurs définitions sont fournies à titre indicatif uniquement, et le fournisseur est libre de mettre en œuvre son propre signification spécifique de chaque indicateur. Le fournisseur ne doit pas renvoyer toute indication de l’erreur si elle a pas d’implémentation d’un indicateur spécifié. 
  
Le résultat d’une restriction de contenu imposée par rapport à une propriété est non défini lorsque la propriété n’existe pas. Lorsqu’un client requiert un comportement bien défini pour une telle restriction et n’est pas certain que si la propriété existe par exemple, il n’est pas une colonne d’une table requise, il doit créer une restriction **et** pour participer à la restriction de contenu avec une restriction existent. Utilisez une structure [SExistRestriction](sexistrestriction.md) pour définir la restriction existent et une structure [SAndRestriction](sandrestriction.md) pour définir la restriction **et** . 
  
Pour plus d’informations sur les restrictions de structure **SContentRestriction** en général, voir [à propos des Restrictions](about-restrictions.md).
  
## <a name="see-also"></a>Voir aussi

- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [Structures MAPI](mapi-structures.md)

