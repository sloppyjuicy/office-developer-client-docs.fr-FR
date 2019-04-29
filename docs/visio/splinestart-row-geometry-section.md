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
description: Contient les coordonnées x et y du deuxième point de contrôle d'une spline, de son deuxième nœud, de son premier nœud, du dernier nœud et du degré de la spline.
ms.openlocfilehash: 2ec06619770af4e5dbcc1a763595b6e01a39052b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417475"
---
# <a name="splinestart-row-geometry-section"></a>SplineStart, ligne (section Geometry)

Contient les coordonnées *x* et *y* du deuxième point de contrôle d'une spline, de son deuxième nœud, de son premier nœud, du dernier nœud et du degré de la spline. 
  
Une ligne SplineStart contient les cellules suivantes.
  
|**Cellule**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordonnée *x* du deuxième point de contrôle d'une spline.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Coordonnée *y* du deuxième point de contrôle d'une spline.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Deuxième nœud de la spline.  <br/> |
|[Point](b-cell-geometry-section.md) <br/> |Premier nœud d'une spline.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Dernier nœud d'une spline.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Degré d'une spline (entier compris entre 1 et 25).  <br/> |
   
## <a name="remarks"></a>Remarques

Visio affiche la définition d'une spline dans la section Geometry qui contient une ligne SplineStart, suivie d'une ou de plusieurs lignes SplineKnot. La ligne SplineStart doit être précédée d'un autre type de ligne, tel que la ligne MoveTo pour indiquer le premier point de contrôle de la spline. La ligne précédente peut être une ligne LineTo, ArcTo, NURBSTo, PolylineTo ou EllipticalArcTo si la spline suit un segment de ce type.
  

