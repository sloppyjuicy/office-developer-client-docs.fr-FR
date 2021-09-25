---
title: SketchLineWeight Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6cb838be-1d6d-48e1-8e9e-bd126f0c2385
description: Détermine l’épaisseur supplémentaire ajoutée à l’épaisseur de trait à la suite d’un effet d’croquis, en points de 0 à 50. L’épaisseur du trait d’une forme augmente à mesure que la valeur de la cellule SketchLineWeight augmente.
ms.openlocfilehash: 935254e6ed7618279a43fe81eda1cf6835e455f4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553815"
---
# <a name="sketchlineweight-cell-additional-effect-properties-section"></a>SketchLineWeight Cell (Additional Effect Properties Section)

Détermine l’épaisseur supplémentaire ajoutée à l’épaisseur de trait à la suite d’un effet d’croquis, en points de 0 à 50. L’épaisseur du trait d’une forme augmente à mesure que la valeur de la **cellule SketchLineWeight** augmente. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **SketchLineWeight** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | SketchLineWeight  <br/> |
   
Pour obtenir une référence à la **cellule SketchLineWeight** à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowOtherEffectProperties** <br/> |
| Index de la cellule :  <br/> |**visSketchLineWeight** <br/> |
   

