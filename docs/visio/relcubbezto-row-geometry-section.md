---
title: RelCubBezTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: Contient les coordonnées x et y du point de terminaison d’une courbe de Bézier cubique par rapport à la largeur et à la hauteur de la forme, les coordonnées x et y du point de contrôle du début de la largeur et de la hauteur de la forme relative de courbe, et les coordonnées x et y du point de contrôle de la fin de la largeur et de la hauteur de la forme relative de courbe.
ms.openlocfilehash: c567f75327ea0be755be3d1468e466396bf6e1b7
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62180270"
---
# <a name="relcubbezto-row-geometry-section"></a>RelCubBezTo Row (Geometry Section)

Contient les coordonnées  *x*  et  *y*  du point de terminaison d’une courbe de Bézier cubique par rapport à la largeur et à la hauteur de la forme, les coordonnées  *x*  et  *y*  du point de contrôle du début de la largeur et de la hauteur de la forme relative de courbe, et les coordonnées  *x*  et  *y*  du point de contrôle de la fin de la largeur et de la hauteur de la forme relative de courbe. 
  
> [!NOTE]
> Une **ligne RelCubBezTo** ne peut être persistante que dans les formats de fichier .vsdx, .vsdm, .vstx, .vstm, .vssx et .vssm. Lorsqu’un fichier est enregistré dans les formats Visio 2003-2010, la ligne **RelCubBezTo** est convertie en ligne [NURBSTo.](nurbsto-row-geometry-section.md) 
  
Une **ligne RelCubBezTo** contient les cellules suivantes. 
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordonnée *x*  du sommet de fin d’une courbe de Bézier cubique par rapport à la largeur de la forme.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Coordonnée *y*  du sommet de fin d’une courbe de Bézier cubique par rapport à la hauteur de la forme.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Coordonnée *x*  du point de contrôle de début de la courbe par rapport à la largeur de la forme ; point sur l’arc. Le point de contrôle est mieux situé entre les vertex de début et de fin de l’arc.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Coordonnée *y*  du point de contrôle de début d’une courbe par rapport à la hauteur de la forme.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Coordonnée *x*  du point de contrôle de fin de la courbe par rapport à la largeur de la forme ; point sur l’arc. Le point de contrôle est mieux situé entre le point de contrôle de début et les vertex de fin de l’arc.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Coordonnée *y*  du point de contrôle de fin d’une courbe par rapport à la hauteur de la forme.  <br/> |
   

