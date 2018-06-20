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
description: Représente une y-coordonnées d’une forme dans le système de coordonnées local. Le tableau suivant décrit la cellule Y basée sur la ligne où elle se trouve.
ms.openlocfilehash: 461fd0ec41d34132f469c811292550d2f7e094f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790087"
---
# <a name="y-cell-geometry-section"></a>Y, cellule (section Geometry)

Représente une *y* -coordonnées d’une forme dans le système de coordonnées local. Le tableau suivant décrit la cellule Y basée sur la ligne où elle se trouve. 
  
|**Row**|**Description**|
|:-----|:-----|
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Si la ligne MoveTo est la première ligne dans la section, la cellule Y représente la valeur *y* -coordonnées du premier sommet d’un chemin d’accès. Si la ligne MoveTo apparaît entre deux lignes, la cellule Y représente la valeur *y* -coordonnées du premier sommet après la rupture du chemin d’accès.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | La valeur *y* -coordonnées du sommet de fin d’un segment de trait droit.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | La valeur *y* -coordonnées du sommet de fin d’un arc.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | La valeur *y* -coordonnées du sommet de fin d’un arc elliptique.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | La valeur *y* -coordonnées du sommet de fin d’une polyligne.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | La valeur *y* -coordonnées du dernier point de contrôle d’une courbe B-spline rationnelle (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | La valeur *y* -coordonnées du deuxième point de contrôle d’une spline.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | La valeur *y* -coordonnées d’un point de contrôle.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Une coordonnée *y* d’un point sur une ligne infinie.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | La valeur *y* -coordonnée du centre de l’ellipse.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Y par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Géométrie *i* . Y *j* où *i* et *j* = < 1 >, 2, 3...  <br/> |
|| Géométrie *i* . Y1 (lignes InfiniteLine et Ellipse) où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Y par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la ligne :  <br/> |**visRowVertex** +  *j* où *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (Lignes InfiniteLine et Ellipse)  <br/> |
| Index de la cellule :  <br/> |**visY** (Lignes MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart et SplineKnot)  <br/> |
||**visInfiniteLineY1** (Ligne InfiniteLine)  <br/> |
||**visEllipseCenterY** (Ligne ellipse)  <br/> |
   

