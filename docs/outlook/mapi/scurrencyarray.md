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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 1b262ba9c83e9890719f716a373c566be172ae73
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572451"
---
# <a name="scurrencyarray"></a>SCurrencyArray

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un tableau de valeurs monétaires qui sont utilisées pour décrire une propriété de type PT_MV_CURRENCY. 
  
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
  
> Nombre de valeurs dans le tableau indiqué par le membre **lpcur** . 
    
 **lpcur**
  
> Pointeur vers un tableau de structures de [devise](currency.md) qui contiennent les valeurs monétaires. 
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur PT_MV_CURRENCY, voir la [Liste des Types de propriété](property-types.md). 
  
## <a name="see-also"></a>Voir aussi



[CURRENCY](currency.md)
  
[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

