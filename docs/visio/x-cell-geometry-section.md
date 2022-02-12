---
title: X, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1135
ms.localizationpriority: medium
ms.assetid: 2416b323-e084-18e1-c9be-a797078dfab9
description: Représente une coordonnée x sur une forme en coordonnées locales. Ce tableau décrit la cellule X suivant la ligne sur laquelle elle se trouve.
ms.openlocfilehash: be46967ab4294ab0334868b8fcc17508043cc772
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773816"
---
# <a name="x-cell-geometry-section"></a>X, cellule (section Geometry)

Représente une  *coordonnée x*  sur une forme en coordonnées locales. Ce tableau décrit la cellule X suivant la ligne sur laquelle elle se trouve. 
  
|Ligne|Description|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> | Si la ligne MoveTo est la première ligne de la section, la cellule X représente la coordonnée  *x*  du premier sommet d’un chemin d’accès. Si la ligne MoveTo apparaît entre deux lignes, la cellule X représente la coordonnée  *x*  du premier vertex après la rupture du chemin d’accès. |
|[LineTo](lineto-row-geometry-section.md) <br/> | Coordonnée *x*  du sommet de fin d’un segment de ligne droite. |
|[ArcTo](arcto-row-geometry-section.md) <br/> | Coordonnée *x*  du sommet de fin d’un arc. |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Coordonnée *x*  du sommet de fin d’un arc elliptique. |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Coordonnée *x*  du sommet de fin d’une polyligne. |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Coordonnée *x*  du dernier point de contrôle d’une ligne B-spline rationnelle nonuniforme (NURBS). |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Coordonnée *x*  du deuxième point de contrôle d’une spline. |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Coordonnée *x*  d’un point de contrôle. |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Coordonnée  *x*  d’un point sur la ligne infinie. |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Coordonnée *x*  du centre de l’ellipse. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule X à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | Geometry  *i*  . X  *j*            où  *i*  et  *j*  = <1>, 2, 3... |
|| Geometry  *i*  . X1 (lignes InfiniteLine et Ellipse) où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule X à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionFirstComponent** +   *i* où *i* = 0, 1, 2... |
| Index de la ligne :  <br/> |**visRowVertex** +   *j* où *j* = 0, 1, 2... |
||**visRowVertex** (lignes InfiniteLine et Ellipse)  <br/> |
| Index de la cellule :  <br/> |**visX** (lignes MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart et SplineKnot)  <br/> |
||**visInfiniteLineX1** (ligne InfiniteLine)  <br/> |
||**visEllipseCenterX** (ligne Ellipse)  <br/> |
   

