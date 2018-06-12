---
title: D, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251753
localization_priority: Normal
ms.assetid: 5f1fdf59-db58-561c-e187-1af72a8b87f2
description: Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule D pour chaque ligne.
ms.openlocfilehash: ed67197e46ee159ba2175b0e86623fe1704992d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788386"
---
# <a name="d-cell-geometry-section"></a>D, cellule (section Geometry)

Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule D pour chaque ligne.
  
|**Row**|**Description**|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Rapport entre l'axe majeur de l'arc et son axe mineur. Contrairement à la signification réelle de ces termes, l'axe « majeur » ne doit pas forcément être plus grand que l'axe « mineur ». Ce rapport peut donc être inférieur à 1. Si cette cellule a une valeur inférieure ou égale à 0, ou supérieure à 1000, les résultats sont imprévisibles.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Première épaisseur de la courbe B-spline rationnelle non uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Degré d'une spline (entier compris entre 1 et 25).  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | *Y* -coordonnées d’un point sur une ellipse ; associée à l' *x* -coordonnée représentée par la cellule [C](c-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule D par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Géométrie *i* . D *j* où *i* et *j* = < 1 >, 2, 3...  <br/> |
|| Géométrie *i* . D1 (ligne Ellipse) où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule D par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la ligne :  <br/> |**visRowVertex** +  *j* où *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (Ligne ellipse)  <br/> |
| Index de la cellule :  <br/> |**visAspectRatio** (Ligne EllipticalArcTo)  <br/> |
||**visNURBSWeightPrev** (Ligne NURBSTo)  <br/> |
||**visSplineDegree** (Ligne SplineStart)  <br/> |
||**visEllipseMinorY** (Ligne ellipse)  <br/> |
   

