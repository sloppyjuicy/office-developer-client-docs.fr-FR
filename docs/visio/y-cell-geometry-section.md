---
title: Y, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251750
ms.localizationpriority: medium
ms.assetid: a53b5787-f419-7a36-3c04-c63b3c173ac7
description: Représente une coordonnée y sur une forme en coordonnées locales. Ce tableau décrit la cellule Y suivant la ligne sur laquelle elle se trouve.
ms.openlocfilehash: b5e6c673a15acac5c0effdbc34d6a46e48511e51
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63519746"
---
# <a name="y-cell-geometry-section"></a>Y, cellule (section Geometry)

Représente une  *coordonnée y*  sur une forme en coordonnées locales. Ce tableau décrit la cellule Y suivant la ligne sur laquelle elle se trouve.
  
|Ligne|Description|
|:-----|:-----|
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Si la ligne MoveTo est la première ligne de la section, la cellule Y représente la coordonnée *y* du premier sommet d’un chemin d’accès. Si la ligne MoveTo apparaît entre deux lignes, la cellule Y représente la coordonnée *y* du premier sommet après la coupure du chemin d’accès. |
|[LineTo](lineto-row-geometry-section.md) <br/> | Coordonnée *y* du sommet de fin d’un segment de ligne droite. |
|[ArcTo](arcto-row-geometry-section.md) <br/> | Coordonnée *y* du sommet de fin d’un arc. |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Coordonnée *y* du sommet de fin d’un arc elliptique. |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Coordonnée *y* du sommet de fin d’une polyligne. |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Coordonnée *y* du dernier point de contrôle d’une ligne B-spline rationnelle nonuniforme (NURBS). |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Coordonnée *y* du deuxième point de contrôle d’une spline. |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Coordonnée *y* d’un point de contrôle. |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Coordonnée *y* d’un point sur la ligne infinie. |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Coordonnée *y* du centre de l’ellipse. |

## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Y à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez :
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Geometry *i* . Y  *j*            où *i* et *j* = <1>, 2, 3... |
| **Nom de cellule :**  <br/> | Geometry *i* . Y1 (lignes InfiniteLine et Ellipse) où *i* = <1>, 2, 3... |

Pour obtenir une référence à la cellule Y à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionFirstComponent** +   *i* où *i* = 0, 1, 2... |
| **Index de la ligne :**  <br/> |**visRowVertex** +  *j* où *j* = 0, 1, 2... |
| **Index de la ligne :**  <br/> |**visRowVertex** (lignes InfiniteLine et Ellipse)  <br/> |
| **Index de la cellule :**  <br/> |**visY** (lignes MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart et SplineKnot)  <br/> |
| **Index de la cellule :**  <br/> |**visInfiniteLineY1** (ligne InfiniteLine)  <br/> |
| **Index de la cellule :**  <br/>|**visEllipseCenterY** (ligne Ellipse)  <br/> |
