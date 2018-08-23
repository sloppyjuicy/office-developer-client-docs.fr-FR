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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 9f8da0902ea4c4a862d279ee80ba566c0473c44e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592324"
---
# <a name="sandrestriction"></a>SAndRestriction

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Décrit une restriction **AND** , qui est utilisée pour participer à un groupe de restrictions à l’aide d’une opération **AND** logique. 
  
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
  
> Nombre de restrictions de recherche dans le tableau indiqué par le membre **lpRes** . 
    
 **lpRes**
  
> Pointeur vers un tableau de structures [SRestriction](srestriction.md) vont être combinées avec une opération **AND** logique. 
    
## <a name="remarks"></a>Remarques

Le résultat de la **SAndRestriction** a la valeur TRUE si toutes les restrictions de ses enfants ont la valeur TRUE. Elle a la valeur FALSE si aucune restriction enfant a la valeur FALSE. 
  
Pour obtenir une description des types de restrictions, comment les créer et exemple de code, voir [à propos des Restrictions](about-restrictions.md).
  
## <a name="see-also"></a>Voir aussi



[SRestriction](srestriction.md)


[Structures MAPI](mapi-structures.md)

