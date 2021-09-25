---
title: SizedSRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedSRowSet
api_type:
- COM
ms.assetid: 419e2c6d-ac3b-46c6-9a12-33f51f6d7f12
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 19f607e1dcf705ea57abee43c49c989fea3f21e2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619742"
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

