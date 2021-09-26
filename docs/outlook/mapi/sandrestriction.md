---
title: SAndRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SAndRestriction
api_type:
- COM
ms.assetid: 1b7dfe87-f87f-43e3-8332-a0d9c3f70d16
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c31fb0a70dc2458f4db62135d6b371996e2b5dab
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599101"
---
# <a name="sandrestriction"></a>SAndRestriction

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une restriction **AND,** qui est utilisée pour joindre un groupe de restrictions à l’aide d’une **opération LOGIQUE AND.** 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a>Members

 **cRes**
  
> Nombre de restrictions de recherche dans le tableau pointées par le membre **lpRes.** 
    
 **lpRes**
  
> Pointeur vers un tableau de structures [SRestriction](srestriction.md) qui seront combinées avec une opération **LOGIQUE AND.** 
    
## <a name="remarks"></a>Remarques

Le résultat de **la SAndRestriction** est TRUE si toutes ses restrictions enfants sont évaluées à TRUE. Elle est FALSE si une restriction enfant est évaluée à FALSE. 
  
Pour obtenir une description des types de restrictions, comment les créer et un exemple de code, voir [à propos des restrictions.](about-restrictions.md)
  
## <a name="see-also"></a>Voir aussi



[SRestriction](srestriction.md)


[Structures MAPI](mapi-structures.md)

