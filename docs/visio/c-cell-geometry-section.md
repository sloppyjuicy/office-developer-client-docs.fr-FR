---
title: C, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm140
ms.localizationpriority: medium
ms.assetid: d51a1dd8-678a-a34d-658d-bd7a027dd379
description: Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule C pour chaque ligne.
ms.openlocfilehash: 19a197f827292a5063f153225bc17f6ddb0a40b8
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63508150"
---
# <a name="c-cell-geometry-section"></a>C, cellule (section Geometry)

Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule C pour chaque ligne.
  
|Ligne|Description|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Angle de l’axe principal d’un arc par rapport à *l’axe x* de son parent. |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Premier nœud de la courbe B-spline rationnelle non uniforme (NURBS). |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Dernier nœud d’une spline |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Coordonnée *x* d’un point sur une ellipse ; couplée à la *coordonnée y* représentée par la cellule [D](d-cell-geometry-section.md) . |

## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule C par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Geometry *i* . C *j*           où *i* et *j* = <1>, 2, 3... |
| **Nom de cellule :**  <br/> | Geometry *i* . C1 (ligne Ellipse)  <br/> |

Pour obtenir une référence à la cellule C à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2... |
| **Index de la ligne :**  <br/> |**visRowVertex** +  *j* où *j* = 0, 1, 2... |
| **Index de la ligne :**  <br/> |**visRowVertex** (ligne Ellipse)  <br/> |
| **Index de la cellule :**  <br/> |**visEccentricityAngle** (ligne EllipticalArcTo)  <br/> |
| **Index de la cellule :**  <br/> |**visNURBSKnotPrev** (ligne NURBSTo)  <br/> |
| **Index de la cellule :**  <br/> |**visSplineKnot3** (ligne SplineStart)  <br/> |
| **Index de la cellule :**  <br/> |**visEllipseMinorX** (ligne Ellipse)  <br/> |
