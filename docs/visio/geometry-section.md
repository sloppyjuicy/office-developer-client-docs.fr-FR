---
title: Geometry, section
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm2055
localization_priority: Normal
ms.assetid: 75601a1e-6b1a-27ee-a2bd-69e569315982
description: Contient les lignes qui répertorient les coordonnées des sommets des traits et des arcs qui constituent la forme.
ms.openlocfilehash: 32a815015c7d1764399215767b674668b7235832
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345114"
---
# <a name="geometry-section"></a>Geometry, section

Contient les lignes qui répertorient les coordonnées des sommets des traits et des arcs qui constituent la forme. 
  
La géométrie d'une forme peut être exprimée dans plusieurs **** sections Geometry. Plusieurs chemins d'accès peuvent être utiles lorsque plusieurs chemins d'accès ont des propriétés différentes (par exemple, des masques d' [image](clippingpath-cell-foreign-image-info-section.md) ). 
  
## <a name="remarks"></a>Remarques

La **** section Geometry contient les types de ligne suivants. Pour plus de détails, voir les rubriques spécifiques des lignes. 
  
|**Ligne**|**Description**|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> |Déplace vers une coordonnée.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> |Trace un trait jusqu’à une coordonnée.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> |Trace un arc de cercle jusqu’à une coordonnée.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> |Trace un arc elliptique jusqu’à une coordonnée.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> |Trace une polyligne ou des lignes consécutives jusqu’à une coordonnée.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> |Dessine une courbe B-spline rationnelle non uniforme (NURBS) à une coordonnée.  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> |Débute une spline.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> |Trace un segment de spline jusqu’à une coordonnée de nœud.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> |Trace une ligne infinie d’une coordonnée à une autre.  <br/> |
|[Sélection](ellipse-row-geometry-section.md) <br/> |Trace une ellipse à partir de la coordonnée du centre et d’un grand/petit axe.  <br/> |
|[RelCubBezTo](relcubbezto-row-geometry-section.md) <br/> |Dessine une courbe de Bézier cubique par rapport à la largeur et la hauteur de la forme.  <br/> |
|[RelEllipticalArcTo](relellipticalarcto-row-geometry-section.md) <br/> |Trace un arc elliptique jusqu'à une coordonnée par rapport à la hauteur et à la largeur de la forme.  <br/> |
|[RelLineTo](rellineto-row-geometry-section.md) <br/> |Trace un trait jusqu'à une coordonnée relative à la hauteur et à la largeur d'une forme.  <br/> |
|[RelMoveTo](relmoveto-row-geometry-section.md) <br/> |Accéder à une coordonnée par rapport à la largeur et la hauteur de la forme.  <br/> |
|[RelQuadBezTo](relquadbezto-row-geometry-section.md) <br/> |Dessine une courbe de Bézier quadratique par rapport à la largeur et la hauteur de la forme.  <br/> |
   
Pour changer de type de ligne dans cette section, cliquez avec le bouton droit de la souris sur la ligne, puis cliquez sur **Modifier le type de ligne** dans le menu contextuel. 
  

