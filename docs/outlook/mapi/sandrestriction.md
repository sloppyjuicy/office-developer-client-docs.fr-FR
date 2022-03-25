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
description: Décrit une restriction AND, qui est utilisée pour joindre un groupe de restrictions à l’aide d’une opération LOGIQUE AND.
ms.openlocfilehash: 756d88535371c4399db47eb4c8241673f93bcfb5
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64406266"
---
# <a name="sandrestriction"></a>SAndRestriction

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une restriction **AND** , qui est utilisée pour joindre un groupe de restrictions à l’aide d’une **opération LOGIQUE AND** . 
  
|Propriété |Valeur |
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
  
> Nombre de restrictions de recherche dans le tableau pointés par **le membre lpRes** . 
    
 **lpRes**
  
> Pointeur vers un tableau de structures [SRestriction](srestriction.md) qui seront combinées avec une opération **LOGIQUE AND** . 
    
## <a name="remarks"></a>Remarques

Le résultat de **la SAndRestriction** est TRUE si toutes ses restrictions enfants sont évaluées à TRUE. Elle est FALSE si une restriction enfant est évaluée à FALSE. 
  
Pour obtenir une description des types de restrictions, comment les créer et un exemple de code, voir [À propos des restrictions](about-restrictions.md).
  
## <a name="see-also"></a>Voir aussi



[SRestriction](srestriction.md)


[Structures MAPI](mapi-structures.md)

