---
title: SCommentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCommentRestriction
api_type:
- COM
ms.assetid: 07631ae1-981e-4c8e-a30b-1213904fe079
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3f66f513cc16bc479dd24c53804d751a396141f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351414"
---
# <a name="scommentrestriction"></a>SCommentRestriction

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une restriction de commentaire, utilisée pour annoter une restriction. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SCommentRestriction
{
  ULONG          cValues;
  LPSRestriction lpRes;
  LPSPropValue   lpProp;
} SCommentRestriction;

```

## <a name="members"></a>Members

 **cValues**
  
> Nombre de valeurs de propriété dans le tableau vers lequel pointe le membre **lpProp** . 
    
 **lpRes**
  
> Pointeur vers une structure [SRestriction](srestriction.md) . 
    
 **lpProp**
  
> Pointeur vers un tableau de structures [SPropValue](spropvalue.md) , chacune contenant la balise de propriété et la valeur d'une propriété nommée. 
    
## <a name="remarks"></a>Remarques

La structure **SCommentRestriction** associe un objet à un ensemble de propriétés nommées. Les restrictions de commentaire sont à la différence des autres restrictions car elles ne sont pas évaluées. Autrement dit, ils sont ignorés par la méthode [IMAPITable:: Restrict](imapitable-restrict.md) . Il n'y a aucun effet sur les lignes renvoyées par la méthode [IMAPITable:: QueryRows](imapitable-queryrows.md) après l'appel de la méthode IMAPITable: **: Restrict** . 
  
La structure **SCommentRestriction** peut être utilisée pour conserver les informations spécifiques à l'application à l'aide d'une restriction lorsqu'elle est enregistrée sur le disque. Par exemple, un client enregistrant le nom d'une propriété nommée utilisée dans une restriction de propriété peut le faire dans une structure **SCommentRestriction** . L'enregistrement d'un nom de propriété n'est pas possible dans une restriction de propriété car la structure [SPropertyRestriction](spropertyrestriction.md) associée contient uniquement la balise de propriété. 
  
Pour plus d'informations sur la structure **SCommentRestriction** et les restrictions en général, consultez la rubrique [à propos des restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)
  
[SRestriction](srestriction.md)
  
[SPropertyRestriction](spropertyrestriction.md)


[Structures MAPI](mapi-structures.md)

