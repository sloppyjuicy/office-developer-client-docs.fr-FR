---
title: SBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinary
api_type:
- COM
ms.assetid: f21b5e6c-7a63-46bf-acbf-0e042e3519f7
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f54ef96443e5c9fc5fb587f5a9c25388c1ff9cdb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577421"
---
# <a name="sbinary"></a>SBinary

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Décrit une propriété de type PT_BINARY.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SBinary
{
  ULONG      cb;
  LPBYTE     lpb;
} SBinary, FAR *LPSBinary;

```

## <a name="members"></a>Members

 **cb**
  
> Nombre d’octets dans le membre **lpb** . 
    
 **LPB**
  
> Pointeur vers la valeur de la propriété PT_BINARY.
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur les types de propriété, voir [Vue d’ensemble des types de propriété MAPI](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

