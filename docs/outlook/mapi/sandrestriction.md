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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: da35c9c72f4cf3f076715a7a35a3e3514c672ceb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344659"
---
# <a name="sandrestriction"></a>SAndRestriction

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une restriction **et** , utilisée pour joindre un groupe de restrictions à l'aide d'une opération **and** logique. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a>Members

 **cRes**
  
> Nombre de restrictions de recherche dans le tableau vers lequel pointe le membre **lpRes** . 
    
 **lpRes**
  
> Pointeur vers un tableau de structures [SRestriction](srestriction.md) qui seront combinées avec une opération **and** logique. 
    
## <a name="remarks"></a>Remarques

Le résultat de l' **SAndRestriction** est true si toutes ses restrictions enfants ont la valeur true. Elle a la valeur FALSe si une restriction enfant prend la valeur FALSe. 
  
Pour obtenir une description des types de restrictions, de leur création et de l'exemple de code, reportez-vous à la rubrique [à propos des restrictions](about-restrictions.md).
  
## <a name="see-also"></a>Voir aussi



[SRestriction](srestriction.md)


[Structures MAPI](mapi-structures.md)

