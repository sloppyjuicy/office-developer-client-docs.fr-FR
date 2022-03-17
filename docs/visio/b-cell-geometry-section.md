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
ms.openlocfilehash: 27edd6acd8628510657fcde348b1eb085ad9dca5
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63520979"
---
# <a name="b-cell-geometry-section"></a>B, cellule (section Geometry)

Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule B pour chaque ligne.
  
|Ligne|Description|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Coordonnée *y* du point de contrôle d’un arc. |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Dernière épaisseur de la courbe B-spline rationnelle non uniforme (NURBS). |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Premier nœud d’une spline |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Coordonnée *y* d’un point sur une ligne infinie ; associé à *la coordonnée x* représentée par la [cellule A](a-cell-geometry-section.md) . |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Coordonnée *y* d’un point sur une ellipse ; associé à *la coordonnée x* représentée par la [cellule A](a-cell-geometry-section.md) . |

## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule B par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Geometry *i* . B *j*           où *i* et *j* = <1>, 2, 3... |
| **Nom de cellule :**  <br/> | Geometry *i* . B1 (lignes InfiniteLine et Ellipse)  <br/> |

Pour obtenir une référence à la cellule B à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2... |
| **Index de la ligne :**  <br/> |**visRowVertex** +  *j* où *j* = 0, 1, 2... |
| **Index de la ligne :**  <br/> |**visRowVertex** (lignes InfiniteLine et Ellipse)  <br/> |
| **Index de la cellule :**  <br/> |**visControlX** (ligne EllipticalArcTo)  <br/> |
| **Index de la cellule :**  <br/> |**visControlY** (ligne EllipticalArcTo)  <br/> |
| **Index de la cellule :**  <br/> |**visNURBSWeight** (ligne NURBSTo)  <br/> |
| **Index de la cellule :**  <br/> |**visSplineKnot2** (ligne SplineStart)  <br/> |
| **Index de la cellule :**  <br/> |**visInfiniteLineY2** (ligne InfiniteLine)  <br/> |
| **Index de la cellule :**  <br/> |**visEllipseMajorY** (ligne Ellipse)  <br/> |
