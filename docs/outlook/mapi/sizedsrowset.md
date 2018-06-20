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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8b7a93a9abb9a1c589ac7fdab3723c9c924eea0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787175"
---
# <a name="sizedsrowset"></a>SizedSRowSet

**S’applique à**: Outlook 
  
Crée une structure [SRowSet](srowset.md) nommée qui contient un nombre spécifié de lignes. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**SRowSet** <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a>Paramètres

__a_
  
> Comptage du nombre de lignes à inclure dans la nouvelle structure.
    
__nom_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

Pour utiliser la nouvelle structure de résultats de la macro **SizedSRowSet** comme un pointeur vers une structure **SRowSet** , effectuer le cast suivant : 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a>Voir aussi

- [SRowSet](srowset.md)
- [Macros relatives aux Structures](macros-related-to-structures.md)

