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
description: 'Décrit une restriction OR qui est utilisée pour appliquer une opération LOGIQUE OR à une restriction. '
ms.openlocfilehash: 2bd694d82e17665ff9b962a3eeb5a946ef045f7f
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455208"
---
# <a name="sorrestriction"></a>SOrRestriction

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une restriction **OR** qui est utilisée pour appliquer une opération **LOGIQUE OR** à une restriction. 
  
|Propriété |Valeur |
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
  
> Nombre de structures dans le tableau pointées par **le membre lpRes** . 
    
 **lpRes**
  
> Pointeur vers la structure [SRestriction](srestriction.md) décrivant la restriction à joindre à l’aide de l’opération **logique OR** . 
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur **la structure SOrRestriction** , voir [À propos des restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Voir aussi



[SRestriction](srestriction.md)


[Structures MAPI](mapi-structures.md)

