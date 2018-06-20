---
title: B, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251751
localization_priority: Normal
ms.assetid: b0fb6a47-47d8-ab9c-854d-0b0bbfdfcc27
description: Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule B pour chaque ligne.
ms.openlocfilehash: 7d6f51d037be4852c6a101ad6e576a3a13488cb7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788044"
---
# <a name="b-cell-geometry-section"></a>B, cellule (section Geometry)

Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule B pour chaque ligne.
  
|**Row**|**Description**|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | La valeur *y* -coordonnées du point de contrôle d’un arc.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Dernière épaisseur de la courbe B-spline rationnelle non uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Premier nœud d’une spline  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | *Y* -coordonnées d’un point sur la ligne infinie ; associée à la *x* -coordonnée représentée par la cellule [A](a-cell-geometry-section.md) .  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | *Y* -coordonnées d’un point sur une ellipse ; associée à la *x* -coordonnée représentée par la cellule [A](a-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule B par un nom à partir d’une autre formule ou d’un programme, utilisez la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Géométrie *i* . B *j* où *i* et *j* = < 1 >, 2, 3...  <br/> |
|| Géométrie *i* . B1 (lignes InfiniteLine et Ellipse)  <br/> |
   
Pour obtenir une référence à la cellule B par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la ligne :  <br/> |**visRowVertex** +  *j* où *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (Lignes InfiniteLine et Ellipse)  <br/> |
| Index de la cellule :  <br/> |**visControlX** (Ligne EllipticalArcTo)  <br/> |
||**visControlY** (Ligne EllipticalArcTo)  <br/> |
||**visNURBSWeight** (Ligne NURBSTo)  <br/> |
||**visSplineKnot2** (Ligne SplineStart)  <br/> |
||**visInfiniteLineY2** (Ligne InfiniteLine)  <br/> |
||**visEllipseMajorY** (Ligne ellipse)  <br/> |
   

