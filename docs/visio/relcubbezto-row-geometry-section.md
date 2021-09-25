---
title: RelCubBezTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: Contient les coordonnées x et y du point de terminaison d’une courbe de Bézier cubique par rapport à la largeur et à la hauteur de la forme, les coordonnées x et y du point de contrôle du début de la largeur et de la hauteur de la forme relative de courbe, et les coordonnées x et y du point de contrôle de la fin de la largeur et de la hauteur de la forme relative de courbe.
ms.openlocfilehash: a5a3f0e5550b4f4c003e928299a9d129a808282e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570203"
---
# <a name="relcubbezto-row-geometry-section"></a>RelCubBezTo Row (Geometry Section)

Contient les coordonnées  *x*  et  *y*  du point de terminaison d’une courbe de Bézier cubique par rapport à la largeur et à la hauteur de la forme, les coordonnées  *x*  et  *y*  du point de contrôle du début de la largeur et de la hauteur de la forme relative de courbe, et les coordonnées  *x*  et  *y*  du point de contrôle de la fin de la largeur et de la hauteur de la forme relative de courbe. 
  
> [!NOTE]
> Une **ligne RelCubBezTo** ne peut être persistante que dans les formats de fichier .vsdx, .vsdm, .vstx, .vstm, .vssx et .vssm. Lorsqu’un fichier est enregistré dans les formats Visio 2003-2010, la ligne **RelCubBezTo** est convertie en ligne [NURBSTo.](nurbsto-row-geometry-section.md) 
  
Une **ligne RelCubBezTo** contient les cellules suivantes. 
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordonnée  *x*  du sommet de fin d’une courbe de Bézier cubique par rapport à la largeur de la forme.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Coordonnée  *y*  du sommet de fin d’une courbe de Bézier cubique par rapport à la hauteur de la forme.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Coordonnée  *x*  du point de contrôle de début de la courbe par rapport à la largeur de la forme ; point sur l’arc. Le point de contrôle est mieux situé entre les vertex de début et de fin de l’arc.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Coordonnée  *y*  du point de contrôle de début d’une courbe par rapport à la hauteur de la forme.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Coordonnée  *x*  du point de contrôle de fin de la courbe par rapport à la largeur de la forme ; point sur l’arc. Le point de contrôle est mieux situé entre le point de contrôle de début et les vertex de fin de l’arc.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Coordonnée  *y*  du point de contrôle de fin d’une courbe par rapport à la hauteur de la forme.  <br/> |
   

