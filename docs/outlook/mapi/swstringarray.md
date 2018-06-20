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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1578e26ec96f69975c2304cb185f352193a52c2d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787307"
---
# <a name="swstringarray"></a>SWStringArray

  
  
**S’applique à**: Outlook 
  
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

## <a name="members"></a>Membres

 **cValues**
  
> Nombre de chaînes dans le tableau indiqué par le membre **lppszW** . 
    
 **lppszW**
  
> Pointeur vers un tableau de chaînes de caractères Unicode terminée-null.
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur PT_MV_UNICODE, reportez-vous à [Types de propriété](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

