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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e3f53a894b7f7cdaa68e66530c7bd99bf49b9ed0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581355"
---
# <a name="swstringarray"></a>SWStringArray

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un tableau de chaînes de caractères qui sont utilisées pour décrire une propriété de type PT_MV_UNICODE. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Nombre de chaînes dans le tableau indiqué par le membre **lppszW** . 
    
 **lppszW**
  
> Pointeur vers un tableau de chaînes de caractères Unicode terminée-null.
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur PT_MV_UNICODE, reportez-vous à [Types de propriété](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

