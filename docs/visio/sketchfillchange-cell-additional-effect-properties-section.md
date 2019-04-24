---
title: SketchFillChange Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: Détermine le degré de randomisation du remplissage de la forme à partir de la géométrie de la forme lors de l'utilisation d'un effet d'esquisse, sous la forme d'un pourcentage de la longueur d'une section. Si la valeur de la cellule SketchFillChange est définie sur 0%, la géométrie de délimitation du remplissage d'une forme correspond à la géométrie de la forme. Si la valeur est 100%, la géométrie de délimitation du remplissage de la forme ne suit pas la géométrie de la forme.
ms.openlocfilehash: 8726e9dd6ca6257fb8dbbbef3dce1d4ec344e28b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339810"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a>SketchFillChange Cell (Additional Effect Properties Section)

Détermine le degré de randomisation du remplissage de la forme à partir de la géométrie de la forme lors de l'utilisation d'un effet d'esquisse, sous la forme d'un pourcentage de la longueur d'une section. Si la valeur de la cellule **SketchFillChange** est définie sur 0%, la géométrie de délimitation du remplissage d'une forme correspond à la géométrie de la forme. Si la valeur est 100%, la géométrie de délimitation du remplissage de la forme ne suit pas la géométrie de la forme. 
  
## <a name="remarks"></a>Remarques

Pour obtenir de meilleurs résultats, la plage de valeurs idéale pour la cellule **SketchFillChange** est comprise entre 15% et 50%. Une valeur inférieure à 15% est à peine perceptible; une valeur supérieure à 50% est de plus en plus aléatoire. 
  
Pour obtenir une référence à la cellule **SketchFillChange** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez: 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | SketchFillChange  <br/> |
   
Pour obtenir une référence à la cellule **SketchFillChange** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants: 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowOtherEffectProperties** <br/> |
| Index de la cellule :  <br/> |**visSketchFillChange** <br/> |
   

