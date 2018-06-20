---
title: C, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm140
localization_priority: Normal
ms.assetid: d51a1dd8-678a-a34d-658d-bd7a027dd379
description: Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule C pour chaque ligne.
ms.openlocfilehash: 1b9a813be825f2deeb5c90d596ffd9f3705bcef6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788192"
---
# <a name="c-cell-geometry-section"></a>C, cellule (section Geometry)

Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule C pour chaque ligne.
  
|**Row**|**Description**|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | L’angle de l’axe de principal d’un arc par rapport à *x* -axe de son parent.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Premier nœud de la courbe B-spline rationnelle non uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Dernier nœud d’une spline  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | *X* -coordonnées d’un point sur une ellipse ; associée à la valeur *y* -coordonnée représentée par la cellule [D](d-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule C par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Géométrie *i* . C *j* où *i* et *j* = < 1 >, 2, 3...  <br/> |
|| Géométrie *i* . C1 (ligne Ellipse)  <br/> |
   
Pour obtenir une référence à la cellule C par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la ligne :  <br/> |**visRowVertex** +  *j* où *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (Ligne ellipse)  <br/> |
| Index de la cellule :  <br/> |**visEccentricityAngle** (Ligne EllipticalArcTo)  <br/> |
||**visNURBSKnotPrev** (Ligne NURBSTo)  <br/> |
||**visSplineKnot3** (Ligne SplineStart)  <br/> |
||**visEllipseMinorX** (Ligne ellipse)  <br/> |
   

