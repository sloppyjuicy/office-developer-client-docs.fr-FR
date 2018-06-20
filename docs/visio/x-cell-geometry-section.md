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
description: Représente un x-coordonnées d’une forme dans le système de coordonnées local. Le tableau suivant décrit la cellule X en fonction de la ligne dans laquelle il se trouve.
ms.openlocfilehash: e5bc99d4f73d49741c4378009dfc2a883bb655ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790052"
---
# <a name="x-cell-geometry-section"></a>X, cellule (section Geometry)

Représente un *x* -coordonnées d’une forme dans le système de coordonnées local. Le tableau suivant décrit la cellule X en fonction de la ligne dans laquelle il se trouve. 
  
|**Row**|**Description**|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> | Si la ligne MoveTo est la première ligne dans la section, la cellule X représente la *x* -coordonnées du premier sommet d’un chemin d’accès. Si la ligne MoveTo apparaît entre deux lignes, la cellule X représente la *x* -coordonnées du premier sommet après la rupture du chemin d’accès.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | *X* -coordonnées du sommet de fin d’un segment de trait droit.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | *X* -coordonnées du sommet de fin d’un arc.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | *X* -coordonnées du sommet de fin d’un arc elliptique.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | *X* -coordonnées du sommet de fin d’une polyligne.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | *X* -coordonnées du dernier point de contrôle d’une courbe B-spline rationnelle (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | *X* -coordonnées du deuxième point de contrôle d’une spline.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | *X* -coordonnées d’un point de contrôle.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | *X* -coordonnées d’un point sur une ligne infinie.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | *X* -coordonnée du centre de l’ellipse.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule X par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Géométrie *i* . X *j* où *i* et *j* = < 1 >, 2, 3...  <br/> |
|| Géométrie *i* . X1 (lignes InfiniteLine et Ellipse) où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule X par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la ligne :  <br/> |**visRowVertex** +  *j* où *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (Lignes InfiniteLine et Ellipse)  <br/> |
| Index de la cellule :  <br/> |**visX** (Lignes MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart et SplineKnot)  <br/> |
||**visInfiniteLineX1** (Ligne InfiniteLine)  <br/> |
||**visEllipseCenterX** (Ligne ellipse)  <br/> |
   

