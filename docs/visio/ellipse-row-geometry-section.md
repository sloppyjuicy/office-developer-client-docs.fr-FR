---
title: Ellipse, ligne (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3010
ms.localizationpriority: medium
ms.assetid: 183fb303-4acb-a486-7b97-f11f7ae3978f
description: Contient les coordonnées x et y du point central de l’ellipse et deux points sur l’ellipse.
ms.openlocfilehash: 15b1047f790d58d65b745c052330b2441cb08a4c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619105"
---
# <a name="ellipse-row-geometry-section"></a>Ellipse Row (Geometry Section)

Contient les  *coordonnées x*  et  *y*  du point central de l’ellipse et deux points sur l’ellipse. 
  
Une ligne Ellipse contient les cellules suivantes.
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordonnée  *x*  du point central.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Coordonnée  *y*  du point central.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Coordonnée x d’un point sur l’ellipse ; associé à  *la coordonnée y*  représentée par la cellule B.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Coordonnée  *y*  d’un point sur l’ellipse ; associé à la coordonnée x représentée par la cellule A.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Coordonnée  *x*  d’un autre point sur l’ellipse ; associé à  *la coordonnée y*  représentée par la cellule D.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Coordonnée  *y*  d’un autre point sur l’ellipse ; associé à  *la coordonnée y*  représentée par la cellule C.  <br/> |
   
## <a name="remarks"></a>Remarques

Une section Geometry contenant une ligne Ellipse ou InfiniteLine ne doit pas contenir d'autres lignes.
  

