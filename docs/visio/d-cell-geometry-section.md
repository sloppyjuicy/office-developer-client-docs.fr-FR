---
title: D, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251753
ms.localizationpriority: medium
ms.assetid: 5f1fdf59-db58-561c-e187-1af72a8b87f2
description: Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule D pour chaque ligne.
ms.openlocfilehash: a36f021096b28e92ff9bd2d78ef089d759cef600
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586606"
---
# <a name="d-cell-geometry-section"></a>D, cellule (section Geometry)

Représente des informations différentes selon la ligne où elle se trouve. Le tableau ci-dessous décrit la cellule D pour chaque ligne.
  
|Ligne|Description|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Rapport entre l’axe majeur de l’arc et son axe mineur. Contrairement à la signification réelle de ces termes, l’axe « majeur » ne doit pas forcément être plus grand que l’axe « mineur ». Ce rapport peut donc être inférieur à 1. Si cette cellule a une valeur inférieure ou égale à 0, ou supérieure à 1000, les résultats sont imprévisibles.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Première épaisseur de la courbe B-spline rationnelle non uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Degré d’une spline (entier entre 1 et 25)  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Coordonnée *y* d’un point sur une ellipse ; couplée à la *coordonnée x* représentée par la cellule [C.](c-cell-geometry-section.md)  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule D par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Geometry  *i*  . D  *j*            où  *i*  et  *j*  = <1>, 2, 3...  <br/> |
|| Geometry  *i*  . D1 (ligne Ellipse) où  *i*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule D à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionFirstComponent**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la ligne :  <br/> |**visRowVertex**  +   *j* où *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (ligne Ellipse)  <br/> |
| Index de la cellule :  <br/> |**visAspectRatio** (ligne EllipticalArcTo)  <br/> |
||**visNURBSWeightPrev** (ligne NURBSTo)  <br/> |
||**visSplineDegree** (ligne SplineStart)  <br/> |
||**visEllipseMinorY** (ligne Ellipse)  <br/> |
   

