---
title: SGuidArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SGuidArray
api_type:
- COM
ms.assetid: 2091e5fc-75c8-4ea4-87e9-a9bf508e9c58
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 156234b52f092c25314603f7f65da2b20bdbbbc5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550008"
---
# <a name="sguidarray"></a>SGuidArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de structures [GUID](guid.md) utilisées pour décrire une propriété de type PT_MV_CLSID. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SGuidArray
{
  ULONG cValues;
  GUID FAR *lpguid;
} SGuidArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Nombre de valeurs dans le tableau pointées par **le membre lpguid.** 
    
 **lpguid**
  
> Pointeur vers un tableau de structures **GUID** qui contient les valeurs d’identificateur de classe. 
    
## <a name="remarks"></a>Remarques

Pour plus d’informations PT_MV_CLSID, voir [Liste des types de propriétés.](property-types.md)
  
## <a name="see-also"></a>Voir aussi



[GUID](guid.md)
  
[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

