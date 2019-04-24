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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a2a6d273495df52adb83393dc5549b0872c8f6f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341740"
---
# <a name="srestriction"></a>SRestriction

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit un filtre permettant de limiter l'affichage d'un tableau à des lignes spécifiques. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
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

 **transcriptase**
  
> Type de restriction. Les valeurs possibles sont les suivantes: 
    
RES_AND 
  
> Une restriction **and** , qui applique une opération **** and au niveau du bit à une restriction. 
    
RES_BITMASK 
  
> Une restriction de masque de masques, qui applique un masque de à une valeur de propriété.
    
RES_COMMENT 
  
> Restriction de commentaire, qui associe un commentaire à une restriction.
    
RES_COMPAREPROPS 
  
> Une restriction de comparaison de propriétés, qui compare deux valeurs de propriété.
    
RES_CONTENT 
  
> Une restriction de contenu, qui recherche une valeur de propriété pour un contenu spécifique.
    
RES_EXIST 
  
> Une restriction Exists, qui détermine si une propriété est prise en charge.
    
RES_NOT 
  
> Aucune **** restriction, qui applique une opération **not** logique à une restriction. 
    
RES_OR 
  
> Une restriction **or** , qui applique une opération **or** logique à une restriction. 
    
RES_PROPERTY 
  
> Une restriction de propriété, qui détermine si une valeur de propriété correspond à une valeur spécifique.
    
RES_SIZE 
  
> Une restriction de taille, qui détermine si une valeur de propriété correspond à une taille particulière.
    
RES_SUBRESTRICTION 
  
> Une restriction de sous-objet, qui applique une restriction aux pièces jointes ou aux destinataires d'un message.
    
 **serv**
  
> Union des structures de restriction décrivant le filtre à appliquer. La structure spécifique incluse dans le membre **res** dépend de la valeur du membre **RT** . Le mappage entre le type de restriction et la structure est illustré dans le tableau suivant. 
    
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

Les clients utilisent une structure **SRestriction** pour limiter le nombre et le type de lignes dans leur affichage d'un tableau et Rechercher des messages spécifiques dans un dossier. Pour imposer la limitation sur une table, les clients appellent soit une fonction [IMAPITable:: Restrict](imapitable-restrict.md) ou [IMAPITable:: FindRow](imapitable-findrow.md). Pour imposer la limitation sur un dossier, les clients appellent la méthode [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) du dossier. 
  
Pour plus d'informations sur l'utilisation des restrictions avec des tableaux, voir [about restrictions](about-restrictions.md). 
  
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

