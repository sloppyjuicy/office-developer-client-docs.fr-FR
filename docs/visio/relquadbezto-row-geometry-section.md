---
title: RelQuadBezTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: Contient les coordonnées x et y du point de terminaison d’une courbe de Bézier quadratique par rapport à la largeur et à la hauteur de la forme et aux coordonnées x et y du point de contrôle de la largeur et de la hauteur de la forme relative de courbe.
ms.openlocfilehash: f517fa006c6630a26e9162adfbb1be2139487e63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423355"
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
   

