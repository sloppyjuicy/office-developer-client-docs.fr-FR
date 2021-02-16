---
title: ReplaceCopyCells Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f36aefd-da49-47ea-9b90-2fa1a2298849
description: Indique la liste des cellules de la feuille ShapeSheet qui sont copiées d’une ancienne forme vers la forme de remplacement lors d’une opération de remplacement de forme.
ms.openlocfilehash: f2a7908a623c861d0284821b2d8ae5fc71690685
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409341"
---
# <a name="replacecopycells-cell-change-shape-behavior-section"></a>ReplaceCopyCells Cell (Change Shape Behavior Section)

Indique la liste des cellules de la feuille ShapeSheet qui sont copiées d’une ancienne forme vers la forme de remplacement lors d’une opération de remplacement de forme. 
  
## <a name="remarks"></a>Remarques

La forme de base du remplacement doit contenir un appel de fonction **DEPENDSON** dans la cellule **ReplaceCopyCells,** où chaque argument de la fonction est une référence à une cellule. Ces cellules sont copiées de l’ancienne forme vers la forme qui résulte d’une opération de remplacement de forme, quel que soit l’endroit où elles se trouve dans la feuille ShapeSheet. 
  
Les valeurs et/ou formules qui font référence à d’autres cellules sont copiées dans la forme résultante. Si la forme résultante ne possède pas la cellule référencé, la cellule copiée contient uniquement la valeur. 
  
Les références de la cellule **ReplaceCopyCells** remplacent la protection définie sur les cellules telles que définies dans la section **Protection** et les cellules **ReplaceLockFormat,** **ReplaceLockShapeData** et **ReplaceLockText.** 
  
Pour obtenir une référence à la cellule **ReplaceCopyCells** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | ReplaceCopyCells  <br/> |
   
Pour obtenir une référence à la **cellule ReplaceCopyCells** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowReplaceBehaviors** <br/> |
| Index de la cellule :  <br/> |**visReplaceCopyCells** <br/> |
   

