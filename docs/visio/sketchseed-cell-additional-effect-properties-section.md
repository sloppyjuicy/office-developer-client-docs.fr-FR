---
title: SketchSeed Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6f62650d-36f8-4c6e-b79f-c9c397a5954d
description: Représente une valeur de randomisation utilisée pour déterminer la géométrie d’un effet de croquis, sous la forme d’un nombre d’caractères positif. La valeur de la cellule SketchSeed est créée de manière aléatoire lorsqu’un effet de croquis est appliqué à la forme.
ms.openlocfilehash: 9b7edab031427e34dbff0aac02a4f72110a0821f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549587"
---
# <a name="sketchseed-cell-additional-effect-properties-section"></a>SketchSeed Cell (Additional Effect Properties Section)

Représente une valeur de randomisation utilisée pour déterminer la géométrie d’un effet de croquis, sous la forme d’un nombre d’caractères positif. La valeur de la **cellule SketchSeed** est créée de manière aléatoire lorsqu’un effet de croquis est appliqué à la forme. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **SketchSeed** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | SketchSeed  <br/> |
   
Pour obtenir une référence à la cellule **SketchSeed** à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowOtherEffectProperties** <br/> |
| Index de la cellule :  <br/> |**visSketchSeed** <br/> |
   

