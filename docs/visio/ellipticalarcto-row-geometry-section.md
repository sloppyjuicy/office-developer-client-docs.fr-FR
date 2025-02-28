---
title: EllipticalArcTo, ligne (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3015
ms.localizationpriority: medium
ms.assetid: 7ceb30a8-1d05-feff-35d8-08a198784a27
description: Contient les coordonnées x et y du point de terminaison, x et y d’un arc ellipse, les coordonnées des points de contrôle sur l’arc, l’angle entre l’axe x et l’axe principal de l’ellipse, ainsi que les proportions entre les axes principal et mineur de l’ellipse.
ms.openlocfilehash: ebb921db3ef68ba82a44484b39ec87b372eb3ebc
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63382243"
---
# <a name="ellipticalarcto-row-geometry-section"></a>EllipticalArcTo, ligne (section Geometry)

Contient les coordonnées *x* et *y* du point de terminaison, *x* et *y* d’un arc ellipse, les coordonnées des points de contrôle sur l’arc, l’angle entre l’axe *x* et l’axe principal de l’ellipse, ainsi que les proportions entre les axes principal et mineur de l’ellipse.
  
La ligne EllipticalArcTo contient les cellules suivantes.
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordonnée *x*  du sommet de fin sur un arc. |
|[Y](y-cell-geometry-section.md) <br/> |Coordonnée *y*  du sommet de fin sur un arc. |
|[A](a-cell-geometry-section.md) <br/> |Coordonnée *x*  du point de contrôle de l’arc ; point sur l’arc. Le point de contrôle est mieux situé à mi-chemin entre les vertex de début et de fin de l’arc. Dans le cas contraire, l’arc peut atteindre une taille extrême afin de passer par le point de contrôle, avec des résultats imprévisibles. |
|[B](b-cell-geometry-section.md) <br/> |Coordonnée *y*  du point de contrôle d’un arc. |
|[C](c-cell-geometry-section.md) <br/> |Angle de l’axe principal d’un arc par rapport à  *l’axe x*  de son parent. |
|[D](d-cell-geometry-section.md) <br/> |Rapport entre l'axe majeur de l'arc et son axe mineur. Contrairement à la signification réelle de ces termes, l'axe « majeur » ne doit pas forcément être plus grand que l'axe « mineur ». Ce rapport peut donc être inférieur à 1. Si cette cellule a une valeur inférieure ou égale à 0, ou supérieure à 1000, les résultats sont imprévisibles. |
