---
title: RelCubBezTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: Contient les coordonnées x et y du point de fin d'une courbe de Bézier cubique par rapport à la largeur et la hauteur de la forme, les coordonnées x et y du point de contrôle du début de la largeur et de la hauteur de la forme relative de la courbe, ainsi que les coordonnées x et y du contro l point de la fin de la largeur et de la hauteur de la forme relative de courbe.
ms.openlocfilehash: cb886706c4c5cbb3488a95b57dcc84e0e45ee326
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430328"
---
# <a name="relcubbezto-row-geometry-section"></a>RelCubBezTo Row (Geometry Section)

Contient les coordonnées *x* et *y* du point de fin d'une courbe de Bézier cubique par rapport à la largeur et la hauteur de la forme, les coordonnées *x* et *y* du point de contrôle du début de la largeur et de la hauteur de la forme relative de la courbe, et les coordonnées *x* et *y* du point de contrôle de la fin de la largeur et de la hauteur de la forme relative de courbe. 
  
> [!NOTE]
> Une ligne **RelCubBezTo** ne peut être conservée que dans les formats de fichier. vsdx,. VSDM,. vstx,. vstm,. vssx et. VSSM. Lorsqu'un fichier est enregistré aux formats Visio 2003-2010, la ligne **RelCubBezTo** est convertie en ligne [NURBSTo](nurbsto-row-geometry-section.md) . 
  
Une ligne **RelCubBezTo** contient les cellules suivantes. 
  
|**Cellule**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordonnée *x* du sommet de fin d'une courbe de Bézier cubique par rapport à la largeur de la forme.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Coordonnée *y* du sommet de fin d'une courbe de Bézier cubique par rapport à la hauteur de la forme.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Coordonnée *x* du point de contrôle de début de la courbe par rapport à la largeur de la forme; point sur l'arc. Le point de contrôle est le mieux situé entre les sommets de début et de fin de l'arc.  <br/> |
|[Point](b-cell-geometry-section.md) <br/> |Coordonnée *y* du point de contrôle de début d'une courbe par rapport à la hauteur de la forme.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Coordonnée *x* du point de contrôle de fin de la courbe par rapport à la largeur de la forme; point sur l'arc. Le point de contrôle est le mieux situé entre le point de contrôle de début et les sommets de fin de l'arc.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Coordonnée *y* du point de contrôle de fin d'une courbe par rapport à la hauteur de la forme.  <br/> |
   

