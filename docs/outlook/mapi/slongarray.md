---
title: SLongArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLongArray
api_type:
- COM
ms.assetid: 57435634-202d-4998-9931-4562f1a66f5f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c207b1db6a24cc60967735e2f4b1a4aa97007750
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787189"
---
# <a name="slongarray"></a>SLongArray

  
  
**S’applique à**: Outlook 
  
Contient un tableau de types de valeur de type LONG qui sont utilisées pour décrire une propriété de type PT_MV_LONG. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a>Membres

 **cValues**
  
> Nombre de valeurs dans le tableau indiqué par le membre **lpl** . 
    
 **LPL**
  
> Pointeur vers un tableau de valeurs de type LONG.
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur PT_MV_LONG, voir la [Liste des Types de propriété](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

