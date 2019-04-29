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
ms.openlocfilehash: ff032b5af2918ec9865360ede5c3d76e8e872e9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423306"
---
# <a name="b-cell-geometry-section"></a>B, cellule (section Geometry)

Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule B pour chaque ligne.
  
|**Ligne**|**Description**|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Coordonnée *y* du point de contrôle d'un arc.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Dernière épaisseur de la courbe B-spline rationnelle non uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Premier nœud d’une spline  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Coordonnée *y* d'un point sur une ligne infinie; associée à la coordonnée *x* représentée par la cellule [A](a-cell-geometry-section.md) .  <br/> |
|[Sélection](ellipse-row-geometry-section.md) <br/> | Coordonnée *y* d'un point sur une ellipse; associée à la coordonnée *x* représentée par la cellule [A](a-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule B par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Géométrie *i* . B *j* où *i* et *j* = <1>, 2, 3...  <br/> |
|| Géométrie *i* . B1 (lignes InfiniteLine et ellipse)  <br/> |
   
Pour obtenir une référence à la cellule B à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la ligne :  <br/> |**visRowVertex** +  *j* où *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (lignes InfiniteLine et Ellipse)  <br/> |
| Index de la cellule :  <br/> |**visControlX** (ligne EllipticalArcTo)  <br/> |
||**visControlY** (ligne EllipticalArcTo)  <br/> |
||**visNURBSWeight** (ligne NURBSTo)  <br/> |
||**visSplineKnot2** (ligne SplineStart)  <br/> |
||**visInfiniteLineY2** (ligne InfiniteLine)  <br/> |
||**visEllipseMajorY** (ligne Ellipse)  <br/> |
   

