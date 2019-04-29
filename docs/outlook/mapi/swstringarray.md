---
title: SWStringArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SWStringArray
api_type:
- COM
ms.assetid: c1ae24ad-1bbb-4dee-b414-b5226593b6fa
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ff69981e83d42e439936a3e4be47eabfd811b310
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413604"
---
# <a name="swstringarray"></a>SWStringArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de chaînes de caractères utilisées pour décrire une propriété de type PT_MV_UNICODE. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Nombre de chaînes dans le tableau vers lequel pointe le membre **lppszW** . 
    
 **lppszW**
  
> Pointeur vers un tableau de chaînes de caractères Unicode terminées par null.
    
## <a name="remarks"></a>Remarques

Pour plus d'informations sur PT_MV_UNICODE, consultez la rubrique [types de propriétés](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

