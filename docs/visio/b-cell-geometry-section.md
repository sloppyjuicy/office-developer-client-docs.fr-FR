---
title: B, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251751
ms.localizationpriority: medium
ms.assetid: b0fb6a47-47d8-ab9c-854d-0b0bbfdfcc27
description: Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule B pour chaque ligne.
ms.openlocfilehash: b0c726a2932f7f1b2324df5488bbfeb2b269bc1d
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62778607"
---
# <a name="b-cell-geometry-section"></a>B, cellule (section Geometry)

Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule B pour chaque ligne.
  
|Ligne|Description|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Coordonnée *y*  du point de contrôle d’un arc. |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Dernière épaisseur de la courbe B-spline rationnelle non uniforme (NURBS). |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Premier nœud d’une spline |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Coordonnée  *y*  d’un point sur une ligne infinie ; associé à  *la coordonnée x*  représentée par la [cellule A](a-cell-geometry-section.md) . |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Coordonnée  *y*  d’un point sur une ellipse ; associé à  *la coordonnée x*  représentée par la [cellule A](a-cell-geometry-section.md) . |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule B par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Geometry  *i*  . B  *j*            où  *i*  et  *j*  = <1>, 2, 3... |
|| Geometry  *i*  . B1 (lignes InfiniteLine et Ellipse)  <br/> |
   
Pour obtenir une référence à la cellule B à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionFirstComponent** +   *i* où *i* = 0, 1, 2... |
| Index de la ligne :  <br/> |**visRowVertex** +   *j* où *j* = 0, 1, 2... |
||**visRowVertex** (lignes InfiniteLine et Ellipse)  <br/> |
| Index de la cellule :  <br/> |**visControlX** (ligne EllipticalArcTo)  <br/> |
||**visControlY** (ligne EllipticalArcTo)  <br/> |
||**visNURBSWeight** (ligne NURBSTo)  <br/> |
||**visSplineKnot2** (ligne SplineStart)  <br/> |
||**visInfiniteLineY2** (ligne InfiniteLine)  <br/> |
||**visEllipseMajorY** (ligne Ellipse)  <br/> |
   

