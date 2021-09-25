---
title: SLongArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SLongArray
api_type:
- COM
ms.assetid: 57435634-202d-4998-9931-4562f1a66f5f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d1f987f87fb07912115057aed82c0e592e0695c5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619735"
---
# <a name="slongarray"></a>SLongArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de types de valeur LONG utilisés pour décrire une propriété de type PT_MV_LONG. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Nombre de valeurs dans le tableau pointées par le **membre lpl.** 
    
 **lpl**
  
> Pointeur vers un tableau de valeurs LONG.
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur PT_MV_LONG, voir [Liste des types de propriétés.](property-types.md)
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

