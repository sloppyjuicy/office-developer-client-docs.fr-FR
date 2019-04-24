---
title: SketchAmount Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Détermine le degré de déformation pour un effet d'esquisse, sous la forme d'un nombre entier compris entre 0 et 25.
ms.openlocfilehash: fd9ee3390d05f24d81d9c6677160155b0f0f0d35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314769"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a>SketchAmount Cell (Additional Effect Properties Section)

Détermine le degré de déformation pour un effet d'esquisse, sous la forme d'un nombre entier compris entre 0 et 25. 
  
|**Value**|**Description**|
|:-----|:-----|
|0  <br/> |Aucun effet de croquis n'est appliqué à la forme.  <br/> |
|1-25  <br/> |La forme est dotée d'une distorsion d'esquisse, où la valeur 1 est la plus grande distorsion et 25 le moins.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **SketchAmount** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez: 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | SketchAmount  <br/> |
   
Pour obtenir une référence à la cellule **SketchAmount** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants: 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowOtherEffectProperties** <br/> |
| Index de la cellule :  <br/> |**visSketchAmount** <br/> |
   

