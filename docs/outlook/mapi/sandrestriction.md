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
ms.openlocfilehash: 1437130caecd57344fc171d234c5391ea92e1d4b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787058"
---
# <a name="sandrestriction"></a>SAndRestriction

  
  
**S’applique à**: Outlook 
  
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

## <a name="members"></a>Membres

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

