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
ms.openlocfilehash: 89305135cdb31e5a803dd0f9d3a188586593f724
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62772781"
---
# <a name="ellipse-row-geometry-section"></a>Ellipse Row (Geometry Section)

Contient les  *coordonnées x*  et  *y*  du point central de l’ellipse et deux points sur l’ellipse. 
  
Une ligne Ellipse contient les cellules suivantes.
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordonnée *x*  du point central. |
|[Y](y-cell-geometry-section.md) <br/> |Coordonnée *y*  du point central. |
|[A](a-cell-geometry-section.md) <br/> |Coordonnée x d’un point sur l’ellipse ; associé à  *la coordonnée y*  représentée par la cellule B. |
|[B](b-cell-geometry-section.md) <br/> |Coordonnée *y*  d’un point sur l’ellipse ; associé à la coordonnée x représentée par la cellule A. |
|[C](c-cell-geometry-section.md) <br/> |Coordonnée *x*  d’un autre point sur l’ellipse ; associé à  *la coordonnée y*  représentée par la cellule D. |
|[D](d-cell-geometry-section.md) <br/> |Coordonnée *y*  d’un autre point sur l’ellipse ; associé à  *la coordonnée y*  représentée par la cellule C. |
   
## <a name="remarks"></a>Remarques

Une section Geometry contenant une ligne Ellipse ou InfiniteLine ne doit pas contenir d'autres lignes.
  

