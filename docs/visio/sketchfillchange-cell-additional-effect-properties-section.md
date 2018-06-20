---
title: SketchFillChange, cellule (Section Propriétés de l’effet supplémentaires)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: Détermine la quantité de randomisation de remplissage d’une forme à partir de la géométrie de lors de l’utilisation d’un effet esquisse, sous forme de pourcentage de la longueur d’une section. Si la valeur de la cellule SketchFillChange est définie sur 0 %, la géométrie de délimitation de remplissage d’une forme correspond à la géométrie d’une forme. Si la valeur est 100 %, la géométrie de remplissage de la forme de délimitation ne suit pas la géométrie de la forme.
ms.openlocfilehash: 8dda34e03188909e167a4abda6f62da3d43c4dd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789756"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a>SketchFillChange, cellule (Section Propriétés de l’effet supplémentaires)

Détermine la quantité de randomisation de remplissage d’une forme à partir de la géométrie de lors de l’utilisation d’un effet esquisse, sous forme de pourcentage de la longueur d’une section. Si la valeur de la cellule **SketchFillChange** est définie sur 0 %, la géométrie de délimitation de remplissage d’une forme correspond à la géométrie d’une forme. Si la valeur est 100 %, la géométrie de remplissage de la forme de délimitation ne suit pas la géométrie de la forme. 
  
## <a name="remarks"></a>Remarques

Pour obtenir les meilleurs résultats, la plage de valeurs de la cellule **SketchFillChange** idéale est comprise entre 15 et 50 %. Une valeur inférieure à 15 % est à peine visible ; une valeur supérieure à 50 % est plus plus aléatoire. 
  
Pour obtenir une référence à la cellule **SketchFillChange** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | SketchFillChange  <br/> |
   
Pour obtenir une référence à la cellule **SketchFillChange** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowOtherEffectProperties** <br/> |
| Index de la cellule :  <br/> |**visSketchFillChange** <br/> |
   

