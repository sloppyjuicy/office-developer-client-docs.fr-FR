---
title: SWStringArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SWStringArray
api_type:
- COM
ms.assetid: c1ae24ad-1bbb-4dee-b414-b5226593b6fa
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 68a90d4bcc0b52cfa312fcaa60add644ea835ce0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609486"
---
# <a name="swstringarray"></a>SWStringArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
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
  
> Nombre de chaînes dans le tableau pointées par **le membre lppszW.** 
    
 **lppszW**
  
> Pointeur vers un tableau de chaînes de caractères Unicode terminées par null.
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur PT_MV_UNICODE, voir [Types de propriétés.](property-types.md)
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

