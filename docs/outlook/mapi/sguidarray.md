---
title: SGuidArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SGuidArray
api_type:
- COM
ms.assetid: 2091e5fc-75c8-4ea4-87e9-a9bf508e9c58
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: bc0ae6d69db6077c17d2efa66d04a5366f2395a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585569"
---
# <a name="sguidarray"></a>SGuidArray

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un tableau de [GUID](guid.md) structures qui sont utilisées pour décrire une propriété de type PT_MV_CLSID. 
  
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
  
> Nombre de valeurs dans le tableau indiqué par le membre **lpguid** . 
    
 **lpguid**
  
> Pointeur vers un tableau de structures **GUID** qui contient les valeurs d’identificateur de classe. 
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur PT_MV_CLSID, voir la [Liste des Types de propriété](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[GUID](guid.md)
  
[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

