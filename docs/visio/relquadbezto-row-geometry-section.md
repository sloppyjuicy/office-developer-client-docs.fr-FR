---
title: RelQuadBezTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: Contient les coordonnées x et y du point de terminaison d’une courbe de Bézier quadratique par rapport à la largeur et à la hauteur de la forme et aux coordonnées x et y du point de contrôle de la largeur et de la hauteur de la forme relative de courbe.
ms.openlocfilehash: dd555b85a09a7cc01e84967b96f31a08aaa783d6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573543"
---
# <a name="relquadbezto-row-geometry-section"></a>RelQuadBezTo Row (Geometry Section)

Contient les coordonnées  *x*  et  *y*  du point de terminaison d’une courbe de Bézier quadratique par rapport à la largeur et à la hauteur de la forme et aux coordonnées  *x*  et  *y*  du point de contrôle de la largeur et de la hauteur de la forme relative de courbe. 
  
> [!NOTE]
> Une **ligne RelQuadBezTo** ne peut être persistante que dans les formats de fichier .vsdx, .vsdm, .vstx, .vstm, .vssx et .vssm. Lorsqu’un fichier est enregistré dans les formats Visio 2003-2010, la ligne **RelQuadBezTo** est convertie en ligne [NURBSTo.](nurbsto-row-geometry-section.md) 
  
Une **ligne RelQuadBezTo** contient les cellules suivantes. 
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordonnée  *x*  du sommet de fin d’une courbe de Bézier quadratique par rapport à la largeur de la forme.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Coordonnée  *y*  du sommet de fin d’une courbe de Bézier quadratique par rapport à la hauteur de la forme.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Coordonnée  *x*  du point de contrôle de la courbe par rapport à la largeur de la forme ; point sur l’arc. Le point de contrôle est mieux situé à mi-chemin entre les vertex de début et de fin de l’arc.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Coordonnée  *y*  du point de contrôle d’une courbe par rapport à la hauteur de la forme.  <br/> |
   

