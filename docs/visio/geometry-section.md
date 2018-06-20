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
description: Contient des lignes qui répertorient les coordonnées des sommets des traits et des arcs qui constituent la forme.
ms.openlocfilehash: 59f85c512b7038f6cfddcb657435730a2e724bd6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788708"
---
# <a name="geometry-section"></a>Geometry, section

Contient des lignes qui répertorient les coordonnées des sommets des traits et des arcs qui constituent la forme. 
  
La géométrie d’une forme peut être exprimée en plusieurs sections **Geometry** . Plusieurs chemins d’accès peuvent être utiles lorsque plusieurs chemins d’accès sont différentes propriétés (par exemple, les chemins d’accès de [capture d’image](clippingpath-cell-foreign-image-info-section.md) ). 
  
## <a name="remarks"></a>Remarques

La section **Geometry** contient les types suivants de la ligne. Pour plus d’informations, consultez les rubriques de la ligne. 
  
|**Row**|**Description**|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> |Déplace vers une coordonnée.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> |Trace un trait jusqu’à une coordonnée.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> |Trace un arc de cercle jusqu’à une coordonnée.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> |Trace un arc elliptique jusqu’à une coordonnée.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> |Trace une polyligne ou des lignes consécutives jusqu’à une coordonnée.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> |Trace une non-uniform rational B-spline (NURBS) jusqu'à une coordonnée.  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> |Débute une spline.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> |Trace un segment de spline jusqu’à une coordonnée de nœud.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> |Trace une ligne infinie d’une coordonnée à une autre.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> |Trace une ellipse à partir de la coordonnée du centre et d’un grand/petit axe.  <br/> |
|[RelCubBezTo](relcubbezto-row-geometry-section.md) <br/> |Trace une courbe de Bézier cube par rapport à la largeur et la hauteur de la forme.  <br/> |
|[RelEllipticalArcTo](relellipticalarcto-row-geometry-section.md) <br/> |Trace un arc elliptique jusqu'à une coordonnée par rapport à la hauteur et la largeur de la forme.  <br/> |
|[RelLineTo](rellineto-row-geometry-section.md) <br/> |Trace un trait jusqu'à une coordonnée relative de la hauteur et la largeur d’une forme.  <br/> |
|[RelMoveTo](relmoveto-row-geometry-section.md) <br/> |Déplacer vers une coordonnée par rapport à la largeur et la hauteur de la forme.  <br/> |
|[RelQuadBezTo](relquadbezto-row-geometry-section.md) <br/> |Dessine une courbe de Bézier quadratique par rapport à la largeur et la hauteur de la forme.  <br/> |
   
Pour modifier un type de ligne dans cette section, avec le bouton droit de la ligne, puis cliquez sur **Modifier le Type de ligne** dans le menu contextuel. 
  

