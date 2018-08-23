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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 84fb79b1922669db9c8e5d518a833a6866f11cea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589181"
---
# <a name="scommentrestriction"></a>SCommentRestriction

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Décrit une restriction de commentaire, qui sert à annoter une restriction. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
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
  
> Nombre de valeurs de propriété dans le tableau indiqué par le membre **lpProp** . 
    
 **lpRes**
  
> Pointeur vers une structure [SRestriction](srestriction.md) . 
    
 **lpProp**
  
> Pointeur vers un tableau de structures [SPropValue](spropvalue.md) , chacun contenant la balise de propriété et la valeur d’une propriété nommée. 
    
## <a name="remarks"></a>Remarques

La structure **SCommentRestriction** associe un objet avec un ensemble de propriétés nommées. Restrictions de commentaire sont Contrairement à d’autres restrictions, car ils ne sont pas évaluées. Autrement dit, ils sont ignorés par la méthode [IMAPITable](imapitable-restrict.md) . Il n’existe aucun effet sur les lignes renvoyées par la méthode [IMAPITable::QueryRows](imapitable-queryrows.md) après qu’un appel **IMAPITable** a été effectué. 
  
La structure **SCommentRestriction** peut être utilisée pour conserver les informations spécifiques à l’application avec une restriction lorsqu’il est enregistré sur le disque. Par exemple, un client de l’enregistrement du nom d’une propriété nommée utilisé dans une restriction de propriété permettre le faire dans une structure **SCommentRestriction** . L’enregistrement d’un nom de propriété n’est pas possible dans une restriction de propriété car la structure [SPropertyRestriction](spropertyrestriction.md) associée conserve uniquement la balise de propriété. 
  
Pour plus d’informations sur les restrictions de structure **SCommentRestriction** en général, voir [à propos des Restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)
  
[SRestriction](srestriction.md)
  
[SPropertyRestriction](spropertyrestriction.md)


[Structures MAPI](mapi-structures.md)

