---
title: RelQuadBezTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: Contient les coordonnées x et y du point de fin d'une courbe de Bézier quadratique par rapport à la largeur et à la hauteur de la forme, ainsi que les coordonnées x et y du point de contrôle de la largeur et de la hauteur de la forme relative de la courbe.
ms.openlocfilehash: f517fa006c6630a26e9162adfbb1be2139487e63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319928"
---
# <a name="relquadbezto-row-geometry-section"></a>RelQuadBezTo Row (Geometry Section)

Contient les coordonnées *x* et *y* du point de fin d'une courbe de Bézier quadratique par rapport à la largeur et à la hauteur de la forme, ainsi que les coordonnées *x* et *y* du point de contrôle de la largeur et de la hauteur de la forme relative de la courbe. 
  
> [!NOTE]
> Une ligne **RelQuadBezTo** ne peut être conservée que dans les formats de fichier. vsdx,. VSDM,. vstx,. vstm,. vssx et. VSSM. Lorsqu'un fichier est enregistré aux formats Visio 2003-2010, la ligne **RelQuadBezTo** est convertie en ligne [NURBSTo](nurbsto-row-geometry-section.md) . 
  
Une ligne **RelQuadBezTo** contient les cellules suivantes. 
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordonnée *x* du sommet de fin d'une courbe de Bézier quadratique par rapport à la largeur de la forme.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Coordonnée *y* du sommet de fin d'une courbe de Bézier quadratique par rapport à la hauteur de la forme.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Coordonnée *x* du point de contrôle de la courbe par rapport à la largeur de la forme; point sur l'arc. Le point de contrôle est le mieux situé à mi-chemin entre les sommets de début et de fin de l'arc.  <br/> |
|[Point](b-cell-geometry-section.md) <br/> |Coordonnée *y* du point de contrôle d'une courbe par rapport à la hauteur de la forme.  <br/> |
   

