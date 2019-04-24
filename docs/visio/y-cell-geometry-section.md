---
title: Y, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251750
localization_priority: Normal
ms.assetid: a53b5787-f419-7a36-3c04-c63b3c173ac7
description: Représente la coordonnée y d'une forme en coordonnées locales. Ce tableau décrit la cellule Y suivant la ligne sur laquelle elle se trouve.
ms.openlocfilehash: 9e823b8d21682b419a70ce498016abf575f36f6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342811"
---
# <a name="y-cell-geometry-section"></a>Y, cellule (section Geometry)

Représente la coordonnée *y* d'une forme en coordonnées locales. Ce tableau décrit la cellule Y suivant la ligne sur laquelle elle se trouve. 
  
|**Ligne**|**Description**|
|:-----|:-----|
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Si la ligne MoveTo est la première ligne de la section, la cellule Y représente la coordonnée *y* du premier sommet d'un chemin. Si la ligne MoveTo apparaît entre deux lignes, la cellule Y représente la coordonnée *y* du premier sommet après la rupture du chemin.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | Coordonnée *y* du sommet de fin d'un segment de trait droit.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | Coordonnée *y* du sommet de fin d'un arc.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Coordonnée *y* du sommet de fin d'un arc elliptique.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Coordonnée *y* du sommet de fin d'une polyligne.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Coordonnée *y* du dernier point de contrôle d'une courbe B-spline rationnelle inuniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Coordonnée *y* du deuxième point de contrôle d'une spline.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Coordonnée *y* d'un point de contrôle.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Coordonnée *y* d'un point sur la ligne infinie.  <br/> |
|[Sélection](ellipse-row-geometry-section.md) <br/> | Coordonnée *y* du centre de l'ellipse.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Y à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | Géométrie *i* . Y *j* où *i* et *j* = <1>, 2, 3...  <br/> |
|| Géométrie *i* . Y1 (lignes InfiniteLine et ellipse) où *i* = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Y à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la ligne :  <br/> |**visRowVertex** +  *j* où *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (lignes InfiniteLine et Ellipse)  <br/> |
| Index de la cellule :  <br/> |**visY** (lignes MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart et SplineKnot)  <br/> |
||**visInfiniteLineY1** (ligne InfiniteLine)  <br/> |
||**visEllipseCenterY** (ligne Ellipse)  <br/> |
   

