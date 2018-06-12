---
title: SplineStart, ligne (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3055
localization_priority: Normal
ms.assetid: 8e327e00-0844-efa4-900b-6954d3b009bb
description: Contient des x et y-coordonnées pour le deuxième point de contrôle d’une spline, du deuxième nœud, du premier nœud, du dernier nœud et du degré de la spline.
ms.openlocfilehash: 0944da12e6090fde41dc5927b5705e103d29f76d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789805"
---
# <a name="splinestart-row-geometry-section"></a>SplineStart, ligne (section Geometry)

Contient des *x* et *y* -coordonnées pour le deuxième point de contrôle d’une spline, du deuxième nœud, du premier nœud, du dernier nœud et du degré de la spline. 
  
Une ligne SplineStart contient les cellules suivantes.
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -coordonnées du deuxième point de contrôle d’une spline.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |La valeur *y* -coordonnées du deuxième point de contrôle d’une spline.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Deuxième nœud de la spline.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Premier nœud d’une spline  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Dernier nœud d’une spline  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Degré d'une spline (entier compris entre 1 et 25).  <br/> |
   
## <a name="remarks"></a>Notes

Visio affiche la définition d'une spline dans la section Geometry qui contient une ligne SplineStart, suivie d'une ou de plusieurs lignes SplineKnot. La ligne SplineStart doit être précédée d'un autre type de ligne, tel que la ligne MoveTo pour indiquer le premier point de contrôle de la spline. La ligne précédente peut être une ligne LineTo, ArcTo, NURBSTo, PolylineTo ou EllipticalArcTo si la spline suit un segment de ce type.
  

