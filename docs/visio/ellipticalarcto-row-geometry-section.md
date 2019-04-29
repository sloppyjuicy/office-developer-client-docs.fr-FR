---
title: EllipticalArcTo, ligne (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3015
localization_priority: Normal
ms.assetid: 7ceb30a8-1d05-feff-35d8-08a198784a27
description: Contient les coordonnées x et y du point de terminaison d'un arc elliptique, les coordonnées x et y des points de contrôle de l'arc, l'angle entre l'axe x et l'axe principal de l'ellipse, ainsi que le rapport entre les axes principal et secondaire de l'ellipse.
ms.openlocfilehash: c6db7560a05652ca3bfcadb2fd4857ac39370562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421402"
---
# <a name="ellipticalarcto-row-geometry-section"></a>EllipticalArcTo, ligne (section Geometry)

Contient les coordonnées *x* et *y* du point de terminaison d'un arc elliptique, les coordonnées *x* et *y* des points de contrôle de l'arc, l'angle entre l'axe *x* et l'axe principal de l'ellipse, ainsi que le rapport entre les principales et les Mino de l'ellipse axes des ordonnées. 
  
La ligne EllipticalArcTo contient les cellules suivantes.
  
|**Cellule**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordonnée *x* du sommet de fin sur un arc.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Coordonnée *y* du sommet de fin d'un arc.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Coordonnée *x* du point de contrôle de l'arc; point sur l'arc. Le point de contrôle est le mieux situé à mi-chemin entre les sommets de début et de fin de l'arc. Dans le cas contraire, l'ARC peut se développer à une taille extrême afin de passer par le point de contrôle, avec des résultats imprévisibles.  <br/> |
|[Point](b-cell-geometry-section.md) <br/> |Coordonnée *y* du point de contrôle d'un arc.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Angle de l'axe principal d'un arc par rapport à l'axe *x* de son parent.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Rapport entre l'axe majeur de l'arc et son axe mineur. Contrairement à la signification réelle de ces termes, l'axe « majeur » ne doit pas forcément être plus grand que l'axe « mineur ». Ce rapport peut donc être inférieur à 1. Si cette cellule a une valeur inférieure ou égale à 0, ou supérieure à 1000, les résultats sont imprévisibles.  <br/> |
   

