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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b8521172b441bd26a6562aa28f836d453544928f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787173"
---
# <a name="sizedspropproblemarray"></a>SizedSPropProblemArray

**S’applique à**: Outlook 
  
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
- [Macros relatives aux Structures](macros-related-to-structures.md)

