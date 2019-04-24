---
title: Ellipse, ligne (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3010
localization_priority: Normal
ms.assetid: 183fb303-4acb-a486-7b97-f11f7ae3978f
description: Contient les coordonnées x et y du centre de l'ellipse et de deux points sur l'ellipse.
ms.openlocfilehash: 5121ba0c7bf97eaeaaf8a438dd40eccddada4362
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345681"
---
# <a name="ellipse-row-geometry-section"></a>Ellipse Row (Geometry Section)

Contient les coordonnées *x* et *y* du centre de l'ellipse et de deux points sur l'ellipse. 
  
Une ligne Ellipse contient les cellules suivantes.
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordonnée *x* du point central.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Coordonnée *y* du point central.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Coordonnée x d'un point sur l'ellipse; associée à la coordonnée *y* représentée par la cellule B.  <br/> |
|[Point](b-cell-geometry-section.md) <br/> |Coordonnée *y* d'un point sur l'ellipse; associée à la coordonnée x représentée par la cellule A.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Coordonnée *x* d'un autre point sur l'ellipse; associée à la coordonnée *y* représentée par la cellule D.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Coordonnée *y* d'un autre point sur l'ellipse; associée à la coordonnée *y* représentée par la cellule C.  <br/> |
   
## <a name="remarks"></a>Remarques

Une section Geometry contenant une ligne Ellipse ou InfiniteLine ne doit pas contenir d'autres lignes.
  

