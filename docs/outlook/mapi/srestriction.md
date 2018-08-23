---
title: SRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRestriction
api_type:
- COM
ms.assetid: c12b4409-da6f-480b-87af-1e5baea2e8bd
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 5f8a76cb317ac9bf1b6a4dc4a92b6d6f0098e1d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577400"
---
# <a name="srestriction"></a>SRestriction

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Décrit un filtre pour limiter l’affichage d’une table aux lignes particuliers. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SRestriction
{
  ULONG rt;
  union
  {
    SComparePropsRestriction resCompareProps;
    SAndRestriction resAnd;
    SOrRestriction resOr;
    SNotRestriction resNot;
    SContentRestriction resContent;
    SPropertyRestriction resProperty;
    SBitMaskRestriction resBitMask;
    SSizeRestriction resSize;
    SExistRestriction resExist;
    SSubRestriction resSub;
    SCommentRestriction resComment;
  } res;
} SRestriction;

```

## <a name="members"></a>Members

 **RT**
  
> Le type de restriction. Les valeurs possibles sont les suivantes : 
    
RES_AND 
  
> Une restriction **et** , qui applique une opération de bits **AND** à une restriction. 
    
RES_BITMASK 
  
> Une restriction de masque de bits, qui applique un masque de bits pour une valeur de propriété.
    
RES_COMMENT 
  
> Une restriction de commentaire, qui associe un commentaire à une restriction.
    
RES_COMPAREPROPS 
  
> Restriction de comparaison de propriété, qui permet de comparer deux valeurs de propriété.
    
RES_CONTENT 
  
> Une restriction de contenu, qui recherche une valeur de propriété pour un contenu spécifique.
    
RES_EXIST 
  
> Une restriction existe, qui détermine si une propriété est prise en charge.
    
RES_NOT 
  
> **Pas** restriction, qui applique une opération **NOT** logique à une restriction. 
    
RES_OR 
  
> Une restriction **ou** , qui applique une opération **ou** logique à une restriction. 
    
RES_PROPERTY 
  
> Une restriction de propriété, qui détermine si une valeur de propriété correspond à une valeur particulière.
    
RES_SIZE 
  
> Une restriction de taille, qui détermine si une valeur de propriété est une taille spécifique.
    
RES_SUBRESTRICTION 
  
> Une restriction objet secondaire, qui applique une restriction aux pièces jointes d’un message ou des destinataires.
    
 **res**
  
> Union de structures de restriction décrivant le filtre à appliquer. La structure spécifique incluse dans le membre **res** dépend de la valeur du membre **rt** . Le mappage entre le type de restriction et la structure est répertorié dans le tableau suivant. 
    
|||
|:-----|:-----|
|**Type de restriction** <br/> |**Structure de restriction** <br/> |
|RES_AND  <br/> |[SAndRestriction](sandrestriction.md) <br/> |
|RES_BITMASK  <br/> |[SBitMaskRestriction](sbitmaskrestriction.md) <br/> |
|RES_COMMENT  <br/> |[SCommentRestriction](scommentrestriction.md) <br/> |
|RES_COMPAREPROPS  <br/> |[SComparePropsRestriction](scomparepropsrestriction.md) <br/> |
|RES_CONTENT  <br/> |[SContentRestriction](scontentrestriction.md) <br/> |
|RES_EXIST  <br/> |[SExistRestriction](sexistrestriction.md) <br/> |
|RES_NOT  <br/> |[SNotRestriction](snotrestriction.md) <br/> |
|RES_OR  <br/> |[SOrRestriction](sorrestriction.md) <br/> |
|RES_PROPERTY  <br/> |[SPropertyRestriction](spropertyrestriction.md) <br/> |
|RES_SIZE  <br/> |[SSizeRestriction](ssizerestriction.md) <br/> |
|RES_SUBRESTRICTION  <br/> |[SSubRestriction](ssubrestriction.md) <br/> |
   
## <a name="remarks"></a>Remarques

Clients utilisent une structure **SRestriction** pour limiter le nombre et le type de lignes dans leur vue d’une table et pour rechercher des messages spécifiques dans un dossier. Pour imposer la limitation sur une table, les clients appellent [IMAPITable](imapitable-restrict.md) ou [IMAPITable::FindRow](imapitable-findrow.md). Pour imposer la limite d’un dossier, les clients appellent [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) méthode du dossier. 
  
Pour plus d’informations sur l’utilisation des restrictions des tableaux, voir [à propos des Restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Voir aussi



[SAndRestriction](sandrestriction.md)
  
[SBitMaskRestriction](sbitmaskrestriction.md)
  
[SCommentRestriction](scommentrestriction.md)
  
[SComparePropsRestriction](scomparepropsrestriction.md)
  
[SContentRestriction](scontentrestriction.md)
  
[SExistRestriction](sexistrestriction.md)
  
[SNotRestriction](snotrestriction.md)
  
[SOrRestriction](sorrestriction.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SSizeRestriction](ssizerestriction.md)
  
[SSubRestriction](ssubrestriction.md)


[Structures MAPI](mapi-structures.md)

