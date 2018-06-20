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
description: Contient des x et y-coordonnées d’un arc elliptique point de terminaison, x et y-coordonnées des points de contrôle sur l’arc, l’angle de la x-axe du grand axe et de rapport entre les axes principaux et secondaires de l’ellipse.
ms.openlocfilehash: 9a356429f14a20b72a8bd55689855e2954d4a807
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788548"
---
# <a name="ellipticalarcto-row-geometry-section"></a>EllipticalArcTo, ligne (section Geometry)

Contient des *x* et *y* - coordonnées du point de terminaison d’un arc elliptique, *x* - et *y* -coordonnées des points de contrôle sur l’arc, l’angle de la *x* -axe du grand axe et de rapport entre l’ellipse et minor axes r. 
  
La ligne EllipticalArcTo contient les cellules suivantes.
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -coordonnées du sommet de fin d’un arc.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |La valeur *y* -coordonnées du sommet de fin d’un arc.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |*X* -coordonnées du point de contrôle de l’arc ; un point sur l’arc. Le point de contrôle se trouve mieux sur à mi-chemin entre le début et fin sommets de l’arc. Sinon, l’arc peut atteindre une taille extrême afin de passer par le point de contrôle, avec des résultats imprévisibles.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |La valeur *y* -coordonnées du point de contrôle d’un arc.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |L’angle de l’axe de principal d’un arc par rapport à *x* -axe de son parent.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Rapport entre l'axe majeur de l'arc et son axe mineur. Contrairement à la signification réelle de ces termes, l'axe « majeur » ne doit pas forcément être plus grand que l'axe « mineur ». Ce rapport peut donc être inférieur à 1. Si cette cellule a une valeur inférieure ou égale à 0, ou supérieure à 1000, les résultats sont imprévisibles.  <br/> |
   

