---
title: RelEllipticalArcTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b7da082-5e55-411d-b109-7fb6fa8f6e8e
description: Contient les coordonnées x et y d'un point de terminaison d'arc elliptique par rapport à la largeur et la hauteur de la forme, les coordonnées x et y des points de contrôle de l'arc par rapport à la largeur et la hauteur de la forme, l'angle entre l'axe x et l'axe principal de l'ellipse, et le rapport entre t axes principaux et secondaires de l'ellipse.
ms.openlocfilehash: e38f5f2baf6bb9ade31c2778799a3ece968147f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359961"
---
# <a name="relellipticalarcto-row-geometry-section"></a>RelEllipticalArcTo Row (Geometry Section)

Contient les coordonnées *x* et *y* d'un point de terminaison d'un arc elliptique par rapport à la largeur et la hauteur de la forme, ainsi que les coordonnées *x* et *y* des points de contrôle de l'arc par rapport à la largeur et la hauteur de la forme, en fonction de l'angle à partir du *x*   -axe de l'axe principal de l'ellipse et ratio entre les axes principal et secondaire de l'ellipse. 
  
> [!NOTE]
> Une ligne **RelEllipticalArcTo** ne peut être conservée que dans les formats de fichier. vsdx,. VSDM,. vstx,. vstm,. vssx et. VSSM. Lorsqu'un fichier est enregistré aux formats Visio 2003-2010, la ligne **RelEllipticalArcTo** est convertie en ligne [EllipticalArcTo](ellipticalarcto-row-geometry-section.md) . 
  
Une ligne **RelEllipticalArcTo** contient les cellules suivantes. 
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordonnée *x* du sommet de fin sur un arc par rapport à la largeur de la forme.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Coordonnée *y* du sommet de fin sur un arc par rapport à la hauteur de la forme.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Coordonnée *x* du point de contrôle de l'arc par rapport à la largeur de la forme; point sur l'arc. Le point de contrôle est le mieux situé à mi-chemin entre les sommets de début et de fin de l'arc. Dans le cas contraire, l'ARC peut se développer à une taille extrême afin de passer par le point de contrôle, avec des résultats imprévisibles.  <br/> |
|[Point](b-cell-geometry-section.md) <br/> |Coordonnée *y* du point de contrôle d'un arc par rapport à la largeur de la forme.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Angle de l'axe principal d'un arc par rapport à l'axe *x* de son parent.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Rapport entre l'axe majeur de l'arc et son axe mineur. Contrairement à la signification réelle de ces termes, l'axe « majeur » ne doit pas forcément être plus grand que l'axe « mineur ». Ce rapport peut donc être inférieur à 1. Si cette cellule a une valeur inférieure ou égale à 0, ou supérieure à 1000, les résultats sont imprévisibles.  <br/> |
   
## <a name="remarks"></a>Remarques

Les valeurs de la ligne **RelEllipticalArcTo** sont équivalentes aux valeurs d'une ligne [EllipticalArcTo](ellipticalarcto-row-geometry-section.md) , multipliées par la largeur et la hauteur de la forme. par exemple: une ligne **RelEllipticalArcTo** où les **cellules X**, **Y**, **a**, **B**, **C**et **D** ont les valeurs 1, 1, 1,5, 0,5, 15 deg et 1,5 (respectivement) peuvent être remplacées par une ligne **EllipticalArcTo** avec formules `Width*1`de cellule, `Height*1'`, `Width*1.5`, `Height*0.5`, 15 deg et 1,5 (respectivement).
  

