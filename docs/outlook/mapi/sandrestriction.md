---
title: SAndRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAndRestriction
api_type:
- COM
ms.assetid: 1b7dfe87-f87f-43e3-8332-a0d9c3f70d16
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: da35c9c72f4cf3f076715a7a35a3e3514c672ceb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438882"
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
  
> Nombre de restrictions de recherche dans le tableau pointés par le membre **lpRes.** 
    
 **lpRes**
  
> Pointeur vers un tableau de structures [SRestriction](srestriction.md) qui seront combinées avec une opération **LOGIQUE AND.** 
    
## <a name="remarks"></a>Remarques

Le résultat de **la SAndRestriction** est TRUE si toutes ses restrictions enfants sont évaluées à TRUE. Elle est FALSE si une restriction enfant est évaluée à FALSE. 
  
Pour obtenir une description des types de restrictions, comment les créer et un exemple de code, voir [à propos des restrictions.](about-restrictions.md)
  
## <a name="see-also"></a>Voir aussi



[SRestriction](srestriction.md)


[Structures MAPI](mapi-structures.md)

