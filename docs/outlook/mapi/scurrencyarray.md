---
title: SCurrencyArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SCurrencyArray
api_type:
- COM
ms.assetid: d28852ab-b542-40e1-b2ec-85d20a2eddfd
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 37847a0c2d5f4dcea96e7b3a7af6094e94a78791
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586753"
---
# <a name="scurrencyarray"></a>SCurrencyArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de valeurs monétaires utilisées pour décrire une propriété de type PT_MV_CURRENCY. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Nombre de valeurs dans le tableau pointées par **le membre lpcur.** 
    
 **lpcur**
  
> Pointeur vers un tableau de structures [CURRENCY](currency.md) qui contiennent les valeurs monétaires. 
    
## <a name="remarks"></a>Remarques

Pour plus d’informations PT_MV_CURRENCY, voir [Liste des types de propriétés.](property-types.md) 
  
## <a name="see-also"></a>Voir aussi



[CURRENCY](currency.md)
  
[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

