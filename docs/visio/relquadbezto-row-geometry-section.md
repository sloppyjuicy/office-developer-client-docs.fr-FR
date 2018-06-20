---
title: RelQuadBezTo, ligne (Section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: Contient x - et y - coordonnées du point de terminaison d’une courbe de Bézier par rapport à la largeur de la forme et la hauteur et le x - et y-coordonnées du point de contrôle de la largeur et la hauteur de la forme relative courbe.
ms.openlocfilehash: 99796e85a857fd320598cb48993fc29bdfa4964d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789477"
---
# <a name="relquadbezto-row-geometry-section"></a>RelQuadBezTo, ligne (Section Geometry)

Contient *x* - et *y* - coordonnées du point de terminaison d’une courbe de Bézier par rapport à la largeur de la forme et la hauteur et le *x* - et *y* -coordonnées du point de contrôle de la largeur et la hauteur de la forme relative courbe. 
  
> [!NOTE]
> Une ligne **RelQuadBezTo** peut uniquement être conservée dans les formats de fichier .vsdx, .vsdm, .vstx, .vstm, .vssx et .vssm. Lorsqu’un fichier est enregistré dans les formats de Visio 2003 à 2010, la ligne **RelQuadBezTo** est convertie en une ligne [NURBSTo](nurbsto-row-geometry-section.md) . 
  
Une ligne **RelQuadBezTo** contient les cellules suivantes. 
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -coordonnées du sommet de fin d’une courbe de Bézier par rapport à la largeur de la forme.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |La valeur *y* -coordonnées du sommet de fin d’une courbe de Bézier par rapport à la hauteur de la forme.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |*X* -coordonnées du point de contrôle de la courbe par rapport à la largeur de la forme ; un point sur l’arc. Le point de contrôle se trouve mieux sur à mi-chemin entre le début et fin sommets de l’arc.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |La valeur *y* -coordonnées du point de contrôle d’une courbe par rapport à la hauteur de la forme.  <br/> |
   

