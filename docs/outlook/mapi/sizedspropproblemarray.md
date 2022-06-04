---
title: SizedSPropProblemArray
description: Contours SizedSPropProblemArray, qui crée une structure nommée SPropProblemArray qui contient un nombre spécifié de structures SPropProblem.
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
ms.openlocfilehash: 25ec7d24eb95d92f9785f3b70cb18ba6c044fbb8
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894795"
---
# <a name="sizedspropproblemarray"></a>SizedSPropProblemArray

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une structure [SPropProblemArray](spropproblemarray.md) nommée qui contient un nombre spécifié de structures [SPropProblem](spropproblem.md) . 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure associée :  <br/> |**SPropProblemArray** <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a>Paramètres

_ _cprob_
  
> Nombre de structures **SPropProblem** à inclure dans la nouvelle structure. 
    
_ _name_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

Utilisez la macro **SizedSPropProblemArray** pour créer un tableau de problèmes de propriétés avec des limites explicites. Pour utiliser la nouvelle structure qui résulte de la macro **SizedSPropProblemArray** comme pointeur vers une structure **SPropProblemArray** , effectuez le cast suivant : 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a>Voir aussi

- [SPropProblemArray](spropproblemarray.md)
- [SPropProblem](spropproblem.md)
- [Macros liées aux structures](macros-related-to-structures.md)

