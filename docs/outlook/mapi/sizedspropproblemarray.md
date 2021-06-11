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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b3818e5e1429c7e2b7d5f7533db733ba29e672c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418112"
---
# <a name="sizedspropproblemarray"></a>SizedSPropProblemArray

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une structure [nommée SPropProblemArray](spropproblemarray.md) qui contient un nombre spécifié de structures [SPropProblem.](spropproblem.md) 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**SPropProblemArray** <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a>Parameters

_ _cprob_
  
> Nombre de structures **SPropProblem** à inclure dans la nouvelle structure. 
    
_ _name_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

Utilisez la macro **SizedSPropProblemArray** pour créer un tableau de problèmes de propriétés avec des limites explicites. Pour utiliser la nouvelle structure qui résulte de la macro **SizedSPropProblemArray** comme pointeur vers une structure **SPropProblemArray,** effectuez la distribution suivante : 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a>Voir aussi

- [SPropProblemArray](spropproblemarray.md)
- [SPropProblem](spropproblem.md)
- [Macros liées aux structures](macros-related-to-structures.md)

