---
title: SAppTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAppTimeArray
api_type:
- COM
ms.assetid: 5a1ff95a-9862-4165-8a70-bd2eeb7fe683
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dee1de19ed61fa4f8edab69152315d77545b01b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430384"
---
# <a name="sapptimearray"></a>SAppTimeArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de valeurs d’heure.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Nombre de valeurs dans le tableau pointées par **le membre lpat.** 
    
 **lpat**
  
> Pointeur vers un tableau de valeurs d’heure d’application. 
    
## <a name="remarks"></a>Remarques

La structure **SAppTimeArray est** utilisée pour définir des propriétés de type PT_MV_APPTIME. Pour plus d’informations PT_MV_APPTIME, voir [Liste des types de propriétés.](property-types.md)
  
## <a name="see-also"></a>Voir aussi



[Structures MAPI](mapi-structures.md)

