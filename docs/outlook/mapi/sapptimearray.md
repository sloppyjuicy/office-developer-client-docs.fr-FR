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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 834a7141f0e7150140fa27c21d88db422d6f5561
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787040"
---
# <a name="sapptimearray"></a>SAppTimeArray

  
  
**S’applique à**: Outlook 
  
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

## <a name="members"></a>Membres

 **cValues**
  
> Nombre de valeurs dans le tableau indiqué par le membre **lpat** . 
    
 **lpat**
  
> Pointeur vers un tableau de valeurs de temps d’application. 
    
## <a name="remarks"></a>Remarques

La structure **SAppTimeArray** est utilisée pour définir les propriétés de type PT_MV_APPTIME. Pour plus d’informations sur PT_MV_APPTIME, voir la [Liste des Types de propriété](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[Structures MAPI](mapi-structures.md)

