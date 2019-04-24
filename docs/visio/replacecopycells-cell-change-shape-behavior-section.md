---
title: ReplaceCopyCells Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f36aefd-da49-47ea-9b90-2fa1a2298849
description: Indique la liste des cellules de la feuille ShapeSheet qui sont copiées d'une ancienne forme à la forme de remplacement pendant une opération de remplacement de forme.
ms.openlocfilehash: f2a7908a623c861d0284821b2d8ae5fc71690685
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320173"
---
# <a name="replacecopycells-cell-change-shape-behavior-section"></a>ReplaceCopyCells Cell (Change Shape Behavior Section)

Indique la liste des cellules de la feuille ShapeSheet qui sont copiées d'une ancienne forme à la forme de remplacement pendant une opération de remplacement de forme. 
  
## <a name="remarks"></a>Remarques

La forme de base du remplacement doit contenir un appel de fonction **DependsOn** dans la cellule **ReplaceCopyCells** , où chaque argument de la fonction est une référence à une cellule. Ces cellules sont copiées de l'ancienne forme à la forme qui résulte d'une opération de remplacement de forme, quel que soit l'emplacement où elles se trouvent dans la feuille ShapeSheet. 
  
Les valeurs et/ou les formules qui font référence à d'autres cellules sont copiées dans la forme obtenue. Si la forme obtenue n'a pas la cellule référencée, la cellule copiée contient la valeur uniquement. 
  
Les références dans le jeu de protection des substitutions de cellule **ReplaceCopyCells** sur les cellules définies dans la section **protection** et les cellules **ReplaceLockFormat**, **ReplaceLockShapeData**et **ReplaceLockText** . 
  
Pour obtenir une référence à la cellule **ReplaceCopyCells** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez: 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | ReplaceCopyCells  <br/> |
   
Pour obtenir une référence à la cellule **ReplaceCopyCells** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants: 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowReplaceBehaviors** <br/> |
| Index de la cellule :  <br/> |**visReplaceCopyCells** <br/> |
   

