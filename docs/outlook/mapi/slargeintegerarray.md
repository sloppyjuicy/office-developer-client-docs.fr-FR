---
title: SLargeIntegerArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLargeIntegerArray
api_type:
- COM
ms.assetid: 9ec9a674-c1a2-4137-856f-6cabe6f0eb9f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4d6785783f69857bd93f3c5818983e832e16af05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787197"
---
# <a name="slargeintegerarray"></a>SLargeIntegerArray

  
  
**S’applique à**: Outlook 
  
Contient un tableau de structures [LARGE_INTEGER](http://go.microsoft.com/fwlink/?LinkId=132130) qui sont utilisées pour décrire une propriété de type PT_MV_I8. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SLargeIntegerArray
{
  ULONG cValues;
  LARGE_INTEGER FAR *lpli;
} SLargeIntegerArray;

```

## <a name="members"></a>Membres

 **cValues**
  
> Nombre de valeurs dans le tableau indiqué par le membre **lpli** . 
    
 **lpli**
  
> Pointeur vers un tableau de structures **LARGE_INTEGER** contenant les valeurs entières. 
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur PT_MV_18, voir la [Liste des Types de propriété](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

