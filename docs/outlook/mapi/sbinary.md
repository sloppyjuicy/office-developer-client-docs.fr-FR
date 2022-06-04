---
title: SBinary
description: Décrit SBinary, y compris une description du type de propriété PT_BINARY. Cela s’applique à Outlook 2013 et Outlook 2016.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SBinary
api_type:
- COM
ms.assetid: f21b5e6c-7a63-46bf-acbf-0e042e3519f7
ms.openlocfilehash: 751c4afcbe5be6d55fae4400eb3aa01eb4deee43
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894102"
---
# <a name="sbinary"></a>SBinary

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une propriété de type PT_BINARY.
  
|Propriété |Valeur |
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
    
 **lpb**
  
> Pointeur vers la valeur de la propriété PT_BINARY.
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur les types de propriétés, consultez [vue d’ensemble du type de propriété MAPI](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

