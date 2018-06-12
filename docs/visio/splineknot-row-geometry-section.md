---
title: SplineKnot, ligne (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3050
localization_priority: Normal
ms.assetid: 9fbae27d-4f1b-c5f7-aacb-16f359331e83
description: Contient des x et y-coordonnées du point de contrôle et du nœud d’une spline.
ms.openlocfilehash: 297889208e064870dd37ed45a17fef7cb4b333b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789803"
---
# <a name="splineknot-row-geometry-section"></a>SplineKnot, ligne (section Geometry)

Contient des *x* et *y* -coordonnées du point de contrôle et du nœud d’une spline. 
  
Une ligne SplineKnot contient les cellules suivantes.
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -coordonnées d’un point de contrôle.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |La valeur *y* -coordonnées d’un point de contrôle.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Un des nœuds de la spline (autre que le dernier ou les deux premiers).  <br/> |
   
## <a name="remarks"></a>Notes

Visio affiche la définition d'une spline dans la section Geometry qui contient une ligne SplineStart, suivie d'une ou de plusieurs lignes SplineKnot. La ligne SplineStart doit être précédée d'un autre type de ligne, tel que la ligne MoveTo pour indiquer le premier point de contrôle de la spline. La ligne précédente peut être une ligne LineTo, ArcTo, NURBSTo, PolylineTo ou EllipticalArcTo si la spline suit un segment de ce type.
  

