---
title: SplineKnot, ligne (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3050
ms.localizationpriority: medium
ms.assetid: 9fbae27d-4f1b-c5f7-aacb-16f359331e83
description: Contient les coordonnées x et y du point de contrôle d’une spline et du nœud d’une spline.
ms.openlocfilehash: 8364962a4a9889b4f992e5eae9916b8935602d11
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62772507"
---
# <a name="splineknot-row-geometry-section"></a>SplineKnot, ligne (section Geometry)

Contient  *les coordonnées*  *x et y*  du point de contrôle d’une spline et du nœud d’une spline. 
  
Une ligne SplineKnot contient les cellules suivantes.
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordonnée *x*  d’un point de contrôle. |
|[Y](y-cell-geometry-section.md) <br/> |Coordonnée *y*  d’un point de contrôle. |
|[A](a-cell-geometry-section.md) <br/> |Un des nœuds de la spline (autre que le dernier ou les deux premiers). |
   
## <a name="remarks"></a>Remarques

Visio affiche la définition d'une spline dans la section Geometry qui contient une ligne SplineStart, suivie d'une ou de plusieurs lignes SplineKnot. La ligne SplineStart doit être précédée d'un autre type de ligne, tel que la ligne MoveTo pour indiquer le premier point de contrôle de la spline. La ligne précédente peut être une ligne LineTo, ArcTo, NURBSTo, PolylineTo ou EllipticalArcTo si la spline suit un segment de ce type.
  

