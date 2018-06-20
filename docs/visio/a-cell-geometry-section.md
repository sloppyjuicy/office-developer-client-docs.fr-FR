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
ms.openlocfilehash: b907552c2346292a6b14baf16481b6b40cc80fc4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787986"
---
# <a name="a-cell-geometry-section"></a>A, cellule (section Geometry)

Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule A pour chaque ligne.
  
|**Row**|**Description**|
|:-----|:-----|
|[ArcTo](arcto-row-geometry-section.md) <br/> | Distance entre le milieu de l’arc et le milieu de sa corde.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | *X* -coordonnées du point de contrôle de l’arc, un point sur l’arc. Le point de contrôle se trouve mieux sur à mi-chemin entre le début et fin sommets de l’arc. Sinon, l’arc peut atteindre une taille extrême afin de passer par le point de contrôle, avec des résultats imprévisibles.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Formule de la polyligne.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Avant-dernier nœud de la courbe B-spline rationnelle non uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Deuxième nœud de la spline.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Un des nœuds de la spline (autre que le dernier ou les deux premiers).  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | *X* -coordonnées d’un point sur la ligne infinie ; associée à *y* -coordonnée représentée par la cellule [B](b-cell-geometry-section.md) .  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | *X* -coordonnées d’un point sur l’ellipse ; associée à *y* -coordonnée représentée par la cellule [B](b-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule A par un nom à partir d’une autre formule ou d’un programme, utilisez la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Géométrie *i* . Un *j* où *i* et *j* = < 1 >, 2, 3...  <br/> |
|| Géométrie *i* . A1 (lignes InfiniteLine et Ellipse) où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule A par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la ligne :  <br/> |**visRowVertex** +  *j* où *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (Lignes InfiniteLine et Ellipse)  <br/> |
| Index de la cellule :  <br/> |**visBow** (Ligne ArcTo)  <br/> |
||**visControlX** (Ligne EllipticalArcTo)  <br/> |
||**visControlY** (Ligne EllipticalArcTo)  <br/> |
||**visPolylineData** (Ligne Polyline)  <br/> |
||**visNURBSKnot** (Ligne NURBSTo)  <br/> |
||**visSplineKnot** (Lignes SplineStart et SplineKnot)  <br/> |
||**visInfiniteLineX2** (Ligne InfiniteLine)  <br/> |
||**visEllipseMajorX** (Ligne ellipse)  <br/> |
   

