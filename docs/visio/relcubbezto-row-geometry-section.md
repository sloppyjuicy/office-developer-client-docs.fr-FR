---
title: RelCubBezTo, ligne (Section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: Contient le x et y - coordonnées du point de terminaison d’une courbe de Bézier cube par rapport à la largeur de la forme et height, x - et y - coordonnées du point de contrôle du début de la largeur de la courbe relative d’une forme et la hauteur et x - et y-coordonnées de le contro l point de fin de la largeur et la hauteur de la forme relative courbe.
ms.openlocfilehash: 918701c19e36753dcbf1a210dda2234d1e540d6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789429"
---
# <a name="relcubbezto-row-geometry-section"></a>RelCubBezTo, ligne (Section Geometry)

Contient *x* - et *y* - coordonnées du point de terminaison d’une courbe de Bézier cube par rapport à la largeur de la forme et height, *x* - et *y* -coordonnées du point de contrôle du début de la largeur et la hauteur de la forme relative courbe et le *x* et *y* -coordonnées du point de contrôle de la fin de la largeur et la hauteur de la forme relative courbe. 
  
> [!NOTE]
> Une ligne **RelCubBezTo** peut uniquement être conservée dans les formats de fichier .vsdx, .vsdm, .vstx, .vstm, .vssx et .vssm. Lorsqu’un fichier est enregistré dans les formats de Visio 2003 à 2010, la ligne **RelCubBezTo** est convertie en une ligne [NURBSTo](nurbsto-row-geometry-section.md) . 
  
Une ligne **RelCubBezTo** contient les cellules suivantes. 
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -coordonnées du sommet de fin d’une courbe de Bézier cube par rapport à la largeur de la forme.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |La valeur *y* -coordonnées du sommet de fin d’une courbe de Bézier cube par rapport à la hauteur de la forme.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |*X* -coordonnée de la courbe d’ouverture du point de contrôle par rapport à la largeur de la forme ; un point sur l’arc. Le point de contrôle est mieux situé entre le début et de fin des sommets de l’arc.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |La valeur *y* -coordonnées d’une courbe de début de point de contrôle par rapport à la hauteur de la forme.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |*X* -coordonnée de la courbe de fin du point de contrôle par rapport à la largeur de la forme ; un point sur l’arc. Le point de contrôle est mieux situé entre les début contrôle point et se terminant sommets de l’arc.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |La valeur *y* -point de contrôle par rapport à la hauteur de la forme de fin de la coordonnée d’une courbe.  <br/> |
   

