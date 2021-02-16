---
title: SizedSRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSRowSet
api_type:
- COM
ms.assetid: 419e2c6d-ac3b-46c6-9a12-33f51f6d7f12
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: cb1e19a3f3703dc4943a5f6c322f1c8b429da5fa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410930"
---
# <a name="sizedsrowset"></a>SizedSRowSet

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une structure [SRowSet nommée](srowset.md) qui contient un nombre spécifié de lignes. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**SRowSet** <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a>Paramètres

_
  
> Nombre de lignes à inclure dans la nouvelle structure.
    
_ _name_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

Pour utiliser la nouvelle structure qui résulte de la macro **SizedSRowSet** comme pointeur vers une structure **SRowSet,** effectuez la distribution suivante : 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a>Voir aussi

- [SRowSet](srowset.md)
- [Macros liées aux structures](macros-related-to-structures.md)

