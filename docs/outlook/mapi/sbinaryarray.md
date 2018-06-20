---
title: SBinaryArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinaryArray
api_type:
- COM
ms.assetid: 2d5b7302-cad2-4522-beb1-7c6c711f42e6
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fd9a8d731d141dbb71a204a2d20b268951bef42f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787048"
---
# <a name="sbinaryarray"></a>SBinaryArray

  
  
**S’applique à**: Outlook 
  
Contient un tableau de valeurs binaires. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a>Membres

 **cValues**
  
> Nombre de valeurs dans le tableau indiqué par le membre **lpbin** . 
    
 **lpbin**
  
> Pointeur vers un tableau de structures [SBinary](sbinary.md) qui contient les valeurs binaires. 
    
## <a name="remarks"></a>Remarques

La structure **SBinaryArray** est utilisée pour décrire les propriétés de type PT_MV_BINARY. 
  
Pour plus d’informations sur PT_MV_BINARY, voir la [Liste des Types de propriété](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[SBinary](sbinary.md)
  
[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

