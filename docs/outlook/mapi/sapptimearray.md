---
title: SAppTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SAppTimeArray
api_type:
- COM
ms.assetid: 5a1ff95a-9862-4165-8a70-bd2eeb7fe683
description: Contient un tableau de valeurs d’heure. La structure SAppTimeArray permet de définir des propriétés de type PT_MV_APPTIME.
ms.openlocfilehash: 0ffbb4544281c73fbaa28c69ff4a56d2fa4e7916
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64406378"
---
# <a name="sapptimearray"></a>SAppTimeArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de valeurs d’heure.
  
|Propriété |Valeur |
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
  
> Nombre de valeurs dans le tableau pointées par **le membre lpat** . 
    
 **lpat**
  
> Pointeur vers un tableau de valeurs d’heure d’application. 
    
## <a name="remarks"></a>Remarques

La structure **SAppTimeArray permet** de définir des propriétés de type PT_MV_APPTIME. Pour plus d’informations sur PT_MV_APPTIME, voir [Liste des types de propriétés](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[Structures MAPI](mapi-structures.md)

