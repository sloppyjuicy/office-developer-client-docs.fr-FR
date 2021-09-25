---
title: SOrRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SOrRestriction
api_type:
- COM
ms.assetid: 6fee29ce-9a34-4e0c-bb71-03120c3f1117
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 20d34d3cdb6eb43ef28b829d7d4a987b8525491b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578570"
---
# <a name="sorrestriction"></a>SOrRestriction

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une restriction **OR** qui est utilisée pour appliquer une opération **LOGIQUE OR** à une restriction. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SOrRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SOrRestriction;

```

## <a name="members"></a>Members

 **cRes**
  
> Nombre de structures dans le tableau pointées par **le membre lpRes.** 
    
 **lpRes**
  
> Pointeur vers la structure [SRestriction](srestriction.md) décrivant la restriction à joindre à l’aide de l’opération **logique OR.** 
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur la structure **SOrRestriction,** voir [À propos des restrictions.](about-restrictions.md) 
  
## <a name="see-also"></a>Voir aussi



[SRestriction](srestriction.md)


[Structures MAPI](mapi-structures.md)

