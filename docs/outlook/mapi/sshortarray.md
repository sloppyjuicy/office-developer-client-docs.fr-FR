---
title: SShortArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SShortArray
api_type:
- COM
ms.assetid: 201ceb76-41bc-4d7b-835d-5196bf3dc234
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 99d2cfb9b4d460ed6a86235a011f9bf244aac0a2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566464"
---
# <a name="sshortarray"></a>SShortArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de valeurs d’un nombre integer non signé qui sont utilisées pour décrire une propriété de type PT_MV_SHORT.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Nombre de valeurs dans le tableau pointées par le **membre lpi.** 
    
 **lpi**
  
> Pointeur vers un tableau de valeurs d’un nombre integer non signé.
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur PT_MV_SHORT types de propriétés et d’autres types de propriétés, voir [Types de propriétés.](property-types.md) 
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

