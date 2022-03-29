---
title: SCommentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SCommentRestriction
api_type:
- COM
ms.assetid: 07631ae1-981e-4c8e-a30b-1213904fe079
description: Décrit une restriction de commentaire, qui est utilisée pour annoter une restriction. Les restrictions de commentaire sont contrairement aux autres restrictions, car elles ne sont pas évaluées.
ms.openlocfilehash: 41135749216d4d4a1a370e1a9387f7dc83566c4e
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455054"
---
# <a name="scommentrestriction"></a>SCommentRestriction

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une restriction de commentaire, qui est utilisée pour annoter une restriction. 
  
|Propriété |Valeur |
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
  
> Nombre de valeurs de propriété dans le tableau pointés par **le membre lpProp** . 
    
 **lpRes**
  
> Pointeur vers une structure [SRestriction](srestriction.md) . 
    
 **lpProp**
  
> Pointeur vers un tableau de structures [SPropValue](spropvalue.md) , chacune contenant la balise de propriété et la valeur d’une propriété nommée. 
    
## <a name="remarks"></a>Remarques

La structure **SCommentRestriction** associe un objet à un ensemble de propriétés nommées. Les restrictions de commentaire sont contrairement aux autres restrictions, car elles ne sont pas évaluées. Autrement dit, ils sont ignorés par la [méthode IMAPITable::Restrict](imapitable-restrict.md) . Il n’y a aucun effet sur les lignes renvoyées par la méthode [IMAPITable::QueryRows](imapitable-queryrows.md) après qu’un **appel IMAPITable::Restrict** a été effectué. 
  
La structure **SCommentRestriction** peut être utilisée pour conserver des informations spécifiques à l’application avec une restriction lorsqu’elle est enregistrée sur le disque. Par exemple, un client qui sauvegarde le nom d’une propriété nommée utilisée dans une restriction de propriété peut le faire dans une structure **SCommentRestriction** . L’enregistrement d’un nom de propriété n’est pas possible dans une restriction de propriété, car la structure [SPropertyRestriction](spropertyrestriction.md) associée contient uniquement la balise de propriété. 
  
Pour plus d’informations sur la structure et les restrictions **SCommentRestriction** en général, voir [À propos des restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)
  
[SRestriction](srestriction.md)
  
[SPropertyRestriction](spropertyrestriction.md)


[Structures MAPI](mapi-structures.md)

