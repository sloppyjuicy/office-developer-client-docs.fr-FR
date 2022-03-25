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
description: Contient un tableau de structures GUID utilisées pour décrire une propriété de type PT_MV_CLSID.
ms.openlocfilehash: a087e4b0d1c1df59a8a0e7aed1ee59ad9dfd107f
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63782621"
---
# <a name="sguidarray"></a>SGuidArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de structures [GUID](guid.md) utilisées pour décrire une propriété de type PT_MV_CLSID. 
  
|Propriété |Valeur |
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
  
> Nombre de valeurs dans le tableau pointées par **le membre lpguid** . 
    
 **lpguid**
  
> Pointeur vers un tableau de structures **GUID** qui contient les valeurs d’identificateur de classe. 
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur PT_MV_CLSID, voir [Liste des types de propriétés](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[GUID](guid.md)
  
[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

