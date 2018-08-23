---
title: SShortArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SShortArray
api_type:
- COM
ms.assetid: 201ceb76-41bc-4d7b-835d-5196bf3dc234
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b684309211bbc008856311158c67864d958c96a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573032"
---
# <a name="sshortarray"></a>SShortArray

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un tableau d’entiers non signés sont utilisées pour décrire une propriété de type PT_MV_SHORT.
  
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
  
> Nombre de valeurs dans le tableau indiqué par le membre **LPP** . 
    
 **LPP**
  
> Pointeur vers un tableau de valeurs de nombre entier non signé.
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur PT_MV_SHORT et d’autres types de propriété, voir [Types de propriété](property-types.md). 
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

