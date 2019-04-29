---
title: SOrRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SOrRestriction
api_type:
- COM
ms.assetid: 6fee29ce-9a34-4e0c-bb71-03120c3f1117
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9b4ca4628f356142eb5303c064e3916474810fda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437930"
---
# <a name="sorrestriction"></a>SOrRestriction

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une restriction **ou** qui est utilisée pour appliquer une opération **or** logique à une restriction. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SOrRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SOrRestriction;

```

## <a name="members"></a>Members

 **cRes**
  
> Nombre de structures dans le tableau vers lequel pointe le membre **lpRes** . 
    
 **lpRes**
  
> Pointeur vers la structure [SRestriction](srestriction.md) décrivant la restriction à joindre à l'aide de l'opération **or** logique. 
    
## <a name="remarks"></a>Remarques

Pour plus d'informations sur la structure **SOrRestriction** , consultez la rubrique [à propos des restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Voir aussi



[SRestriction](srestriction.md)


[Structures MAPI](mapi-structures.md)

