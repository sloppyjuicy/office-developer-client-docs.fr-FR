---
title: RelQuadBezTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: Contient les coordonnées x et y du point de terminaison d’une courbe de Bézier quadratique par rapport à la largeur et à la hauteur de la forme et aux coordonnées x et y du point de contrôle de la largeur et de la hauteur de la forme relative de courbe.
ms.openlocfilehash: 6806ce86fa98f076d919325090d50337f9db8b92
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62180179"
---
# <a name="relquadbezto-row-geometry-section"></a>RelQuadBezTo Row (Geometry Section)

Contient les coordonnées  *x*  et  *y*  du point de terminaison d’une courbe de Bézier quadratique par rapport à la largeur et à la hauteur de la forme et aux coordonnées  *x*  et  *y*  du point de contrôle de la largeur et de la hauteur de la forme relative de courbe. 
  
> [!NOTE]
> Une **ligne RelQuadBezTo** ne peut être persistante que dans les formats de fichier .vsdx, .vsdm, .vstx, .vstm, .vssx et .vssm. Lorsqu’un fichier est enregistré dans les formats Visio 2003-2010, la ligne **RelQuadBezTo** est convertie en ligne [NURBSTo.](nurbsto-row-geometry-section.md) 
  
Une **ligne RelQuadBezTo** contient les cellules suivantes. 
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordonnée *x*  du sommet de fin d’une courbe de Bézier quadratique par rapport à la largeur de la forme.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Coordonnée *y*  du sommet de fin d’une courbe de Bézier quadratique par rapport à la hauteur de la forme.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Coordonnée *x*  du point de contrôle de la courbe par rapport à la largeur de la forme ; point sur l’arc. Le point de contrôle est mieux situé à mi-chemin entre les vertex de début et de fin de l’arc.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Coordonnée *y*  du point de contrôle d’une courbe par rapport à la hauteur de la forme.  <br/> |
   

