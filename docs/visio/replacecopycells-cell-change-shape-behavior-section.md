---
title: ReplaceCopyCells, cellule (Section de comportement de forme modification)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f36aefd-da49-47ea-9b90-2fa1a2298849
description: Indique une liste des cellules dans la feuille ShapeSheet qui sont copiés à partir d’une ancienne forme à la forme de remplacement lors d’une opération de remplacement de forme.
ms.openlocfilehash: 1e3b5e4dbc29372f75b7a7ed8013a7dd82d94e1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789435"
---
# <a name="replacecopycells-cell-change-shape-behavior-section"></a>ReplaceCopyCells, cellule (Section de comportement de forme modification)

Indique une liste des cellules dans la feuille ShapeSheet qui sont copiés à partir d’une ancienne forme à la forme de remplacement lors d’une opération de remplacement de forme. 
  
## <a name="remarks"></a>Remarques

La forme de base du remplacement doit contenir un appel de fonction **DEPENDSON** dans la cellule **ReplaceCopyCells** , où chaque argument de la fonction est une référence à une cellule. Ces cellules sont copiés à la forme qui résulte d’une opération de remplacement de forme, où qu’ils soient dans la feuille ShapeSheet de la forme ancienne. 
  
Les valeurs et les formules qui référencent d’autres cellules sont copiés à la forme obtenue. Si la forme obtenue ne dispose pas de la cellule référencée, la cellule contient la valeur uniquement. 
  
Références de la cellule **ReplaceCopyCells** remplacent défini de protection sur cellules telle que définie dans la section **Protection** et les cellules **ReplaceLockText** , **ReplaceLockFormat**et **ReplaceLockShapeData**. 
  
Pour obtenir une référence à la cellule **ReplaceCopyCells** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | ReplaceCopyCells  <br/> |
   
Pour obtenir une référence à la cellule **ReplaceCopyCells** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowReplaceBehaviors** <br/> |
| Index de la cellule :  <br/> |**visReplaceCopyCells** <br/> |
   

