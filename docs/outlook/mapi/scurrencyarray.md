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
description: Contient un tableau de valeurs monétaires utilisées pour décrire une propriété de type PT_MV_CURRENCY.
ms.openlocfilehash: 2b835e542285cab41feaaada44f79958068d7fd4
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64454718"
---
# <a name="scurrencyarray"></a>SCurrencyArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de valeurs monétaires utilisées pour décrire une propriété de type PT_MV_CURRENCY. 
  
|Propriété |Valeur |
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
  
> Nombre de valeurs dans le tableau pointées par **le membre lpcur** . 
    
 **lpcur**
  
> Pointeur vers un tableau de structures [CURRENCY](currency.md) qui contiennent les valeurs monétaires. 
    
## <a name="remarks"></a>Remarques

Pour plus d’informations PT_MV_CURRENCY, voir [Liste des types de propriétés](property-types.md). 
  
## <a name="see-also"></a>Voir aussi



[CURRENCY](currency.md)
  
[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

