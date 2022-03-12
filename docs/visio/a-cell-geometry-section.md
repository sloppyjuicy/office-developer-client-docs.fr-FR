---
title: A, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm51215
ms.localizationpriority: medium
ms.assetid: 6853df0f-d22e-89ca-7d34-342b9c0bea23
description: Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule A pour chaque ligne.
ms.openlocfilehash: 48a1c51fe0ce92ea52b511c2b444928b81407bfb
ms.sourcegitcommit: 7b410a51d1e8c97e9cce8d4aa75074162b7d9485
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2022
ms.locfileid: "63448383"
---
# <a name="a-cell-geometry-section"></a>A, cellule (section Geometry)

Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule A pour chaque ligne.
  
|Ligne|Description|
|:-----|:-----|
|[ArcTo](arcto-row-geometry-section.md) <br/> | Distance entre le milieu de l’arc et le milieu de sa corde. |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Coordonnée *x*  du point de contrôle de l’arc, un point sur l’arc. Le point de contrôle est mieux situé à mi-chemin entre les vertex de début et de fin de l’arc. Dans le cas contraire, l’arc peut atteindre une taille extrême afin de passer par le point de contrôle, avec des résultats imprévisibles. |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Formule de la polyligne |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Avant-dernier nœud de la courbe B-spline rationnelle non uniforme (NURBS). |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Deuxième nœud de la spline |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Un des nœuds de la spline (autre que le dernier ou les deux premiers) |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Coordonnée  *x*  d’un point sur la ligne infinie ; associé à  *la coordonnée y*  représentée par la [cellule B](b-cell-geometry-section.md) . |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Coordonnée  *x*  d’un point sur l’ellipse ; associé à  *la coordonnée y*  représentée par la [cellule B](b-cell-geometry-section.md) . |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule A par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Geometry  *i*  . A  *j*            where  *i*  and  *j*  = <1>, 2, 3... |
| **Nom de cellule :**  <br/> | Geometry  *i*  . A1 (lignes InfiniteLine et Ellipse) où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule A à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionFirstComponent** +   *i* où *i* = 0, 1, 2... |
| **Index de la ligne :**  <br/> |**visRowVertex** +   *j* où *j* = 0, 1, 2... |
| **Index de la ligne :**  <br/> |**visRowVertex** (lignes InfiniteLine et Ellipse)  <br/> |
| **Index de la cellule :**  <br/> |**visBow** (ligne ArcTo)  <br/> |
| **Index de la cellule :**  <br/> |**visControlX** (ligne EllipticalArcTo)  <br/> |
| **Index de la cellule :**  <br/> |**visControlY** (ligne EllipticalArcTo)  <br/> |
| **Index de la cellule :**  <br/> |**visPolylineData** (ligne Polyline)  <br/> |
| **Index de la cellule :**  <br/> |**visNURBSKnot** (ligne NURBSTo)  <br/> |
| **Index de la cellule :**  <br/> |**visSplineKnot** (lignes SplineStart et SplineKnot)  <br/> |
| **Index de la cellule :**  <br/> |**visInfiniteLineX2** (ligne InfiniteLine)  <br/> |
| **Index de la cellule :**  <br/> |**visEllipseMajorX** (ligne Ellipse)  <br/> |
   

