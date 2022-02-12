---
title: Geometry, section
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm2055
ms.localizationpriority: medium
ms.assetid: 75601a1e-6b1a-27ee-a2bd-69e569315982
description: Contient les lignes qui répertorient les coordonnées des sommets des traits et des arcs qui constituent la forme.
ms.openlocfilehash: 904bdc5cf045a2582f9e63b2da70b41ad170c1fc
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62778594"
---
# <a name="geometry-section"></a>Geometry, section

Contient les lignes qui répertorient les coordonnées des sommets des traits et des arcs qui constituent la forme. 
  
La géométrie d’une forme peut être exprimée dans plusieurs sections **Geometry** . Plusieurs chemins peuvent être utiles lorsque plusieurs chemins ont des propriétés différentes (par exemple, des chemins de découpage [d’image](clippingpath-cell-foreign-image-info-section.md) ). 
  
## <a name="remarks"></a>Remarques

La section **Geometry** contient les types de lignes suivants. Pour plus de détails, voir les rubriques spécifiques des lignes. 
  
|Ligne|Description|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> |Déplace vers une coordonnée. |
|[LineTo](lineto-row-geometry-section.md) <br/> |Trace un trait jusqu’à une coordonnée. |
|[ArcTo](arcto-row-geometry-section.md) <br/> |Trace un arc de cercle jusqu’à une coordonnée. |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> |Trace un arc elliptique jusqu’à une coordonnée. |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> |Trace une polyligne ou des lignes consécutives jusqu’à une coordonnée. |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> |Dessinez une ligne B-spline rationnelle non uniforme (NURBS) vers une coordonnée. |
|[SplineStart](splinestart-row-geometry-section.md) <br/> |Débute une spline. |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> |Trace un segment de spline jusqu’à une coordonnée de nœud. |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> |Trace une ligne infinie d’une coordonnée à une autre. |
|[Ellipse](ellipse-row-geometry-section.md) <br/> |Trace une ellipse à partir de la coordonnée du centre et d’un grand/petit axe. |
|[RelCubBezTo](relcubbezto-row-geometry-section.md) <br/> |Dessinez une courbe de Bézier cubique par rapport à la largeur et à la hauteur de la forme. |
|[RelEllipticalArcTo](relellipticalarcto-row-geometry-section.md) <br/> |Dessinez un arc elliptique à une coordonnée par rapport à la hauteur et à la largeur de la forme. |
|[RelLineTo](rellineto-row-geometry-section.md) <br/> |Dessinez un trait vers une coordonnée relative à la hauteur et à la largeur d’une forme. |
|[RelMoveTo](relmoveto-row-geometry-section.md) <br/> |Atteindre une coordonnée par rapport à la largeur et à la hauteur de la forme. |
|[RelQuadBezTo](relquadbezto-row-geometry-section.md) <br/> |Dessine une courbe de Bézier quadratique par rapport à la largeur et à la hauteur de la forme. |
   
Pour changer de type de ligne dans cette section, cliquez avec le bouton droit de la souris sur la ligne, puis cliquez sur **Modifier le type de ligne** dans le menu contextuel. 
  

