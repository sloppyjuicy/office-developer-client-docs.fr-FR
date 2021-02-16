---
title: A, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm51215
localization_priority: Normal
ms.assetid: 6853df0f-d22e-89ca-7d34-342b9c0bea23
description: Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule A pour chaque ligne.
ms.openlocfilehash: 7009658c7a6844a5c6071f502c05114a4accd7b7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541301"
---
# <a name="a-cell-geometry-section"></a>A, cellule (section Geometry)

Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule A pour chaque ligne.
  
|Ligne|Description|
|:-----|:-----|
|[ArcTo](arcto-row-geometry-section.md) <br/> | Distance entre le milieu de l’arc et le milieu de sa corde.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Coordonnée  *x*  du point de contrôle de l’arc, un point sur l’arc. Le point de contrôle est mieux situé à mi-chemin entre les vertex de début et de fin de l’arc. Dans le cas contraire, l’arc peut atteindre une taille extrême afin de passer par le point de contrôle, avec des résultats imprévisibles.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Formule de la polyligne  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Avant-dernier nœud de la courbe B-spline rationnelle non uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Deuxième nœud de la spline  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Un des nœuds de la spline (autre que le dernier ou les deux premiers)  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Coordonnée *x* d’un point sur la ligne infinie ; associé à *la coordonnée y* représentée par la cellule [B.](b-cell-geometry-section.md)  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Coordonnée *x* d’un point sur l’ellipse ; associé à *la coordonnée y* représentée par la cellule [B.](b-cell-geometry-section.md)  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule A par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Geometry  *i*  . A  *j*            where  *i*  and  *j*  = <1>, 2, 3...  <br/> |
|| Geometry  *i*  . A1 (lignes InfiniteLine et Ellipse) où  *i*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule A à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionFirstComponent**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la ligne :  <br/> |**visRowVertex**  +   *j* où *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (lignes InfiniteLine et Ellipse)  <br/> |
| Index de la cellule :  <br/> |**visBow** (ligne ArcTo)  <br/> |
||**visControlX** (ligne EllipticalArcTo)  <br/> |
||**visControlY** (ligne EllipticalArcTo)  <br/> |
||**visPolylineData** (ligne Polyline)  <br/> |
||**visNURBSKnot** (ligne NURBSTo)  <br/> |
||**visSplineKnot** (lignes SplineStart et SplineKnot)  <br/> |
||**visInfiniteLineX2** (ligne InfiniteLine)  <br/> |
||**visEllipseMajorX** (ligne Ellipse)  <br/> |
   

