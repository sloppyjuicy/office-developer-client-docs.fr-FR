---
title: SCurrencyArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCurrencyArray
api_type:
- COM
ms.assetid: d28852ab-b542-40e1-b2ec-85d20a2eddfd
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e9468d0c7fc7e46475afe19f12f225e53196639e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439400"
---
# <a name="scurrencyarray"></a>SCurrencyArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de valeurs monétaires qui sont utilisées pour décrire une propriété de type PT_MV_CURRENCY. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Nombre de valeurs dans le tableau vers lequel pointe le membre **lpcur** . 
    
 **lpcur**
  
> Pointeur vers un tableau de [](currency.md) structures monétaires qui contiennent les valeurs monétaires. 
    
## <a name="remarks"></a>Remarques

Pour plus d'informations sur PT_MV_CURRENCY, consultez la [liste des types de propriétés](property-types.md). 
  
## <a name="see-also"></a>Voir aussi



[CURRENCY](currency.md)
  
[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

