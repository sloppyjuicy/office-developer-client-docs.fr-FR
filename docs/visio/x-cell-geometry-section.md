---
title: X, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1135
localization_priority: Normal
ms.assetid: 2416b323-e084-18e1-c9be-a797078dfab9
description: Représente une coordonnée x sur une forme, en coordonnées locales. Ce tableau décrit la cellule X suivant la ligne sur laquelle elle se trouve.
ms.openlocfilehash: 6554000a86a6bf27d343a5647161bbe416725e64
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423943"
---
# <a name="x-cell-geometry-section"></a>X, cellule (section Geometry)

Représente une coordonnée *x* sur une forme, en coordonnées locales. Ce tableau décrit la cellule X suivant la ligne sur laquelle elle se trouve. 
  
|**Ligne**|**Description**|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> | Si la ligne MoveTo est la première ligne de la section, la cellule X représente la coordonnée *x* du premier sommet d'un chemin. Si la ligne MoveTo apparaît entre deux lignes, la cellule X représente la coordonnée *x* du premier sommet après la rupture du chemin.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | Coordonnée *x* du sommet de fin d'un segment de ligne droite.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | Coordonnée *x* du sommet de fin d'un arc.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Coordonnée *x* du sommet de fin d'un arc elliptique.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Coordonnée *x* du sommet de fin d'une polyligne.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Coordonnée *x* du dernier point de contrôle d'une courbe B-spline rationnelle inuniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Coordonnée *x* du deuxième point de contrôle d'une spline.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Coordonnée *x* d'un point de contrôle.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Coordonnée *x* d'un point sur la ligne infinie.  <br/> |
|[Sélection](ellipse-row-geometry-section.md) <br/> | Coordonnée *x* du centre de l'ellipse.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule X à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | Géométrie *i* . X *j* où *i* et *j* = <1>, 2, 3...  <br/> |
|| Géométrie *i* . X1 (lignes InfiniteLine et ellipse) où *i* = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule X à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la ligne :  <br/> |**visRowVertex** +  *j* où *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (lignes InfiniteLine et Ellipse)  <br/> |
| Index de la cellule :  <br/> |**visX** (lignes MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart et SplineKnot)  <br/> |
||**visInfiniteLineX1** (ligne InfiniteLine)  <br/> |
||**visEllipseCenterX** (ligne Ellipse)  <br/> |
   

