---
title: SizedSPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropProblemArray
api_type:
- COM
ms.assetid: 2fc3febb-8c69-4315-a112-a28eee98013d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: bbced8412c2c3438c58af74ef072a46606b59ddc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594613"
---
# <a name="sizedspropproblemarray"></a>SizedSPropProblemArray

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Crée une structure [SPropProblemArray](spropproblemarray.md) nommée qui contient un nombre spécifié de structures [SPropProblem](spropproblem.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**SPropProblemArray** <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a>Paramètres

__cprob_
  
> Nombre de structures **SPropProblem** à inclure dans la nouvelle structure. 
    
__nom_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

Utilisez la macro **SizedSPropProblemArray** pour créer un tableau de la propriété problème avec des limites explicites. Pour utiliser la nouvelle structure de résultats de la macro **SizedSPropProblemArray** comme un pointeur vers une structure **SPropProblemArray** , effectuer le cast suivant : 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a>Voir aussi

- [SPropProblemArray](spropproblemarray.md)
- [SPropProblem](spropproblem.md)
- [Macros liées aux structures](macros-related-to-structures.md)

