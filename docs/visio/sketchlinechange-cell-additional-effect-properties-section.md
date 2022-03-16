---
title: SketchLineChange Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: Détermine la quantité de randomisation de la ligne de la forme à partir de la géométrie de la forme lors de l’utilisation d’un effet de croquis, sous la forme d’un pourcentage de la longueur d’une section. Si la valeur de la cellule SketchLineChange est définie sur 0 %, la géométrie du trait de la forme correspond à la géométrie de la forme. Si la valeur est 100 %, la géométrie de la ligne de la forme ne suit pas la géométrie de la forme.
ms.openlocfilehash: a7ecd7de377d4120cb3b1c561f42b9647be11cea
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63506596"
---
# <a name="sketchlinechange-cell-additional-effect-properties-section"></a>SketchLineChange Cell (Additional Effect Properties Section)

Détermine la quantité de randomisation de la ligne de la forme à partir de la géométrie de la forme lors de l’utilisation d’un effet de croquis, sous la forme d’un pourcentage de la longueur d’une section. Si la valeur de la **cellule SketchLineChange** est définie sur 0 %, la géométrie du trait de la forme correspond à la géométrie de la forme. Si la valeur est 100 %, la géométrie de la ligne de la forme ne suit pas la géométrie de la forme. 
  
## <a name="remarks"></a>Remarques

Pour de meilleurs résultats, la plage idéale de valeurs pour la cellule **SketchLineChange** est entre 15 et 50 %. Une valeur inférieure à 15 % est à peine perceptible . une valeur supérieure à 50 % peut aléatoirer trop la ligne. 
  
Pour obtenir une référence à la cellule **SketchLineChange** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | SketchLineChange  <br/> |
   
Pour obtenir une référence à la **cellule SketchLineChange** à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowOtherEffectProperties** <br/> |
| **Index de la cellule :**  <br/> |**visSketchLineChange** <br/> |
   

