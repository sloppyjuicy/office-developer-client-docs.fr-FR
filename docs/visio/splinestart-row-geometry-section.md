---
title: SplineStart, ligne (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3055
ms.localizationpriority: medium
ms.assetid: 8e327e00-0844-efa4-900b-6954d3b009bb
description: Contient les coordonnées x et y pour le deuxième point de contrôle d’une spline, son deuxième nœud, son premier nœud, le dernier nœud et le degré de la spline.
ms.openlocfilehash: fbf4880813429a3ae848b95da065299f70fc6433
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773865"
---
# <a name="splinestart-row-geometry-section"></a>SplineStart, ligne (section Geometry)

Contient  *les coordonnées x*  et  *y*  pour le deuxième point de contrôle d’une spline, son deuxième nœud, son premier nœud, le dernier nœud et le degré de la spline. 
  
Une ligne SplineStart contient les cellules suivantes.
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordonnée *x*  du deuxième point de contrôle d’une spline. |
|[Y](y-cell-geometry-section.md) <br/> |Coordonnée *y*  du deuxième point de contrôle d’une spline. |
|[A](a-cell-geometry-section.md) <br/> |Deuxième nœud de la spline. |
|[B](b-cell-geometry-section.md) <br/> |Premier nœud d'une spline. |
|[C](c-cell-geometry-section.md) <br/> |Dernier nœud d'une spline. |
|[D](d-cell-geometry-section.md) <br/> |Degré d'une spline (entier compris entre 1 et 25). |
   
## <a name="remarks"></a>Remarques

Visio affiche la définition d'une spline dans la section Geometry qui contient une ligne SplineStart, suivie d'une ou de plusieurs lignes SplineKnot. La ligne SplineStart doit être précédée d'un autre type de ligne, tel que la ligne MoveTo pour indiquer le premier point de contrôle de la spline. La ligne précédente peut être une ligne LineTo, ArcTo, NURBSTo, PolylineTo ou EllipticalArcTo si la spline suit un segment de ce type.
  

