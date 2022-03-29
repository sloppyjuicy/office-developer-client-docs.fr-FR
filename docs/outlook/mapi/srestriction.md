---
title: SRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SRestriction
api_type:
- COM
ms.assetid: c12b4409-da6f-480b-87af-1e5baea2e8bd
description: Décrit un filtre pour limiter l’affichage d’un tableau à des lignes particulières pour Outlook 2013 et Outlook 2016.
ms.openlocfilehash: 4e39e6e202c3b9cbe4a48eba44489ad68c8dbf1f
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64456251"
---
# <a name="srestriction"></a>SRestriction

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit un filtre pour limiter l’affichage d’un tableau à des lignes particulières. 
  
|Propriété |Valeur |
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

 **rt**
  
> Type de restriction. Les valeurs possibles sont les suivantes : 
    
RES_AND 
  
> Une restriction **AND** , qui applique une opération **AND** au bit à une restriction. 
    
RES_BITMASK 
  
> Restriction de masque de bits, qui applique un masque de bits à une valeur de propriété.
    
RES_COMMENT 
  
> Restriction de commentaire, qui associe un commentaire à une restriction.
    
RES_COMPAREPROPS 
  
> Restriction de comparaison de propriété, qui compare deux valeurs de propriété.
    
RES_CONTENT 
  
> Restriction de contenu qui recherche une valeur de propriété pour un contenu spécifique.
    
RES_EXIST 
  
> Restriction existante, qui détermine si une propriété est prise en charge.
    
RES_NOT 
  
> Restriction **NOT** , qui applique une opération **LOGIQUE NOT** à une restriction. 
    
RES_OR 
  
> Une restriction **OR** , qui applique une opération **LOGIQUE OR** à une restriction. 
    
RES_PROPERTY 
  
> Restriction de propriété, qui détermine si une valeur de propriété correspond à une valeur particulière.
    
RES_SIZE 
  
> Restriction de taille, qui détermine si une valeur de propriété est une taille particulière.
    
RES_SUBRESTRICTION 
  
> Restriction de sous-objet, qui applique une restriction aux pièces jointes ou aux destinataires d’un message.
    
 **res**
  
> Union des structures de restriction décrivant le filtre à appliquer. La structure spécifique incluse dans le **membre res** dépend de la valeur du membre **rt** . Le mappage entre le type de restriction et la structure est répertorié dans le tableau suivant. 
    
|Propriété |Valeur |
|:-----|:-----|
|**Type de restriction** <br/> |**Structure des restrictions** <br/> |
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

Les clients utilisent **une structure SRestriction** pour limiter le nombre et le type de lignes dans leur vue d’une table et pour rechercher des messages spécifiques dans un dossier. Pour imposer la limitation à une table, les clients appellent [IMAPITable::Restrict](imapitable-restrict.md) ou [IMAPITable::FindRow](imapitable-findrow.md). Pour imposer la limitation à un dossier, les clients appellent la méthode [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) du dossier. 
  
Pour plus d’informations sur l’utilisation des restrictions avec des tableaux, voir [À propos des restrictions](about-restrictions.md). 
  
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

