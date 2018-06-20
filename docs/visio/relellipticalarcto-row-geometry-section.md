---
title: RelEllipticalArcTo, ligne (Section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b7da082-5e55-411d-b109-7fb6fa8f6e8e
description: Contient des x et y - coordonnées du point de terminaison d’un arc par rapport à la largeur de la forme et height, x - et y-coordonnées des points de contrôle sur l’arc par rapport à la forme width et height, angle entre x-axe du grand axe et de rapport entre t axes principaux et secondaires de l’ellipse he.
ms.openlocfilehash: 417a2a92bc5c94f9620c7c6f1081ba81d93aa890
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789431"
---
# <a name="relellipticalarcto-row-geometry-section"></a>RelEllipticalArcTo, ligne (Section Geometry)

Contient des *x* et *y* - coordonnées du point de terminaison d’un arc par rapport à la largeur de la forme et height, *x* - et *y* -coordonnées des points de contrôle sur l’arc par rapport à la forme width et height, angle de *x*   -axe du grand axe et de rapport entre les axes principaux et secondaires de l’ellipse. 
  
> [!NOTE]
> Une ligne **RelEllipticalArcTo** peut uniquement être conservée dans les formats de fichier .vsdx, .vsdm, .vstx, .vstm, .vssx et .vssm. Lorsqu’un fichier est enregistré dans les formats de Visio 2003 à 2010, la ligne **RelEllipticalArcTo** est convertie en une ligne [EllipticalArcTo](ellipticalarcto-row-geometry-section.md) . 
  
Une ligne **RelEllipticalArcTo** contient les cellules suivantes. 
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -coordonnées du sommet de fin d’un arc par rapport à la largeur de la forme.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |La valeur *y* -coordonnées du sommet de fin d’un arc par rapport à la hauteur de la forme.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |*X* -coordonnées du point de contrôle de l’arc par rapport à la largeur de la forme ; un point sur l’arc. Le point de contrôle se trouve mieux sur à mi-chemin entre le début et fin sommets de l’arc. Sinon, l’arc peut atteindre une taille extrême afin de passer par le point de contrôle, avec des résultats imprévisibles.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |La valeur *y* -coordonnées du point de contrôle d’un arc par rapport à la largeur de la forme.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |L’angle de l’axe de principal d’un arc par rapport à *x* -axe de son parent.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Rapport entre l'axe majeur de l'arc et son axe mineur. Contrairement à la signification réelle de ces termes, l'axe « majeur » ne doit pas forcément être plus grand que l'axe « mineur ». Ce rapport peut donc être inférieur à 1. Si cette cellule a une valeur inférieure ou égale à 0, ou supérieure à 1000, les résultats sont imprévisibles.  <br/> |
   
## <a name="remarks"></a>Remarques

Valeurs de la ligne **RelEllipticalArcTo** correspondent aux valeurs dans une ligne [EllipticalArcTo](ellipticalarcto-row-geometry-section.md) , multiplié par la largeur et la hauteur de la forme. Par exemple : une **RelEllipticalArcTo** ligne où les cellules **X**, **Y**, **A**, **B**, **C**et **D** ont les valeurs 1, 1, 1,5, 0,5, 15 deg et 1,5 (respectivement) peuvent être remplacé par une ligne **EllipticalArcTo** avec les formules de cellule `Width*1`, `Height*1'`, `Width*1.5`, `Height*0.5`, 15 deg et 1,5 (respectivement).
  

