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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c440bb7d8f3d2d3002a4d1a80ca3a671b49f4d2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787097"
---
# <a name="scurrencyarray"></a>SCurrencyArray

  
  
**S’applique à**: Outlook 
  
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

## <a name="members"></a>Membres

 **cValues**
  
> Nombre de valeurs dans le tableau indiqué par le membre **lpcur** . 
    
 **lpcur**
  
> Pointeur vers un tableau de structures de [devise](currency.md) qui contiennent les valeurs monétaires. 
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur PT_MV_CURRENCY, voir la [Liste des Types de propriété](property-types.md). 
  
## <a name="see-also"></a>Voir aussi



[DEVISE](currency.md)
  
[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

