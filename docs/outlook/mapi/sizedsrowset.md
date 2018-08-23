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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b8c70c8b13025f196fdebb2956939bec840a96f5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583938"
---
# <a name="sizedsrowset"></a>SizedSRowSet

**S’applique à**: Outlook 2013 | Outlook 2016 
  
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
- [Macros liées aux structures](macros-related-to-structures.md)

