---
title: SizedSPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedSPropProblemArray
api_type:
- COM
ms.assetid: 2fc3febb-8c69-4315-a112-a28eee98013d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 691df04d46b8f211f6befd367cc63a388298090e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586704"
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

## <a name="parameters"></a>Paramètres

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

