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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 06b9b6a046aaa0f16418f75d402cc5be44f845a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787220"
---
# <a name="sorrestriction"></a>SOrRestriction

  
  
**S’applique à**: Outlook 
  
Décrit une restriction **ou** qui est utilisée pour appliquer une opération **ou** logique à une restriction. 
  
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

## <a name="members"></a>Membres

 **cRes**
  
> Nombre de structures dans le tableau indiqué par le membre **lpRes** . 
    
 **lpRes**
  
> Pointeur vers la structure [SRestriction](srestriction.md) décrivant la restriction à être joint à l’aide de l’opération **OR** logique. 
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur la structure **SOrRestriction** , voir [à propos des Restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Voir aussi



[SRestriction](srestriction.md)


[Structures MAPI](mapi-structures.md)

