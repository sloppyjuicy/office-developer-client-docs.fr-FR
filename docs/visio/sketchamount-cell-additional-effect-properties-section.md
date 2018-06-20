---
title: SketchAmount, cellule (Section Propriétés de l’effet supplémentaires)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Détermine le degré de déformation pour un effet esquisse, comme un entier compris entre 0 et 25.
ms.openlocfilehash: d5ae954f2eab48722c48c9bc4b3f640403dbb3ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789748"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a>SketchAmount, cellule (Section Propriétés de l’effet supplémentaires)

Détermine le degré de déformation pour un effet esquisse, comme un entier compris entre 0 et 25. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |La forme est sans effet esquisse appliqué.  <br/> |
|1-25  <br/> |La forme a déformation esquisse appliquée, où la valeur 1 est la plupart déformation et 25 le moins.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **SketchAmount** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | SketchAmount  <br/> |
   
Pour obtenir une référence à la cellule **SketchAmount** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowOtherEffectProperties** <br/> |
| Index de la cellule :  <br/> |**visSketchAmount** <br/> |
   

