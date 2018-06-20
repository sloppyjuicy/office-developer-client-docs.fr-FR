---
title: SketchLineChange, cellule (Section Propriétés de l’effet supplémentaires)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: Détermine la quantité de randomisation de ligne de la forme de géométrie de la forme lors de l’utilisation d’un effet esquisse, sous forme de pourcentage de la longueur d’une section. Si la valeur de la cellule SketchLineChange est définie sur 0 %, la géométrie d’une ligne de la forme correspond à la géométrie d’une forme. Si la valeur est 100 %, la géométrie d’une ligne de la forme ne suit pas la géométrie de la forme.
ms.openlocfilehash: 57d2af1a914710d7e5a58686b577014ceb7af424
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789751"
---
# <a name="sketchlinechange-cell-additional-effect-properties-section"></a>SketchLineChange, cellule (Section Propriétés de l’effet supplémentaires)

Détermine la quantité de randomisation de ligne de la forme de géométrie de la forme lors de l’utilisation d’un effet esquisse, sous forme de pourcentage de la longueur d’une section. Si la valeur de la cellule **SketchLineChange** est définie sur 0 %, la géométrie d’une ligne de la forme correspond à la géométrie d’une forme. Si la valeur est 100 %, la géométrie d’une ligne de la forme ne suit pas la géométrie de la forme. 
  
## <a name="remarks"></a>Remarques

Pour obtenir les meilleurs résultats, la plage de valeurs de la cellule **SketchLineChange** idéale est comprise entre 15 et 50 %. Une valeur inférieure à 15 % est à peine visible ; une valeur supérieure à 50 % pourrait randomize trop la ligne. 
  
Pour obtenir une référence à la cellule **SketchLineChange** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | SketchLineChange  <br/> |
   
Pour obtenir une référence à la cellule **SketchLineChange** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowOtherEffectProperties** <br/> |
| Index de la cellule :  <br/> |**visSketchLineChange** <br/> |
   

