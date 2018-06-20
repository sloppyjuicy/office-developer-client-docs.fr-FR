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
description: Contient les coordonnées x - et y-coordonnées du centre et de deux points sur l’ellipse.
ms.openlocfilehash: 0a2acb0efa20f67d04581f827edbfc4fb4a2d6b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788546"
---
# <a name="ellipse-row-geometry-section"></a>Ellipse, ligne (section Geometry)

Contient les coordonnées *x* - et *y* -coordonnées du centre et de deux points sur l’ellipse. 
  
Une ligne Ellipse contient les cellules suivantes.
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -coordonnées du point central.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |La valeur *y* -coordonnées du point central.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Coordonnée x d’un point sur l’ellipse ; associée à *y* -coordonnée représentée par la cellule B.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |La valeur *y* -coordonnées d’un point sur l’ellipse ; associée à la coordonnée x représentée par la cellule A.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |*X* -coordonnées d’un autre point sur l’ellipse ; associée à *y* -coordonnée représentée par la cellule D.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |La valeur *y* -coordonnées d’un autre point sur l’ellipse ; associée à *y* -coordonnée représentée par la cellule C.  <br/> |
   
## <a name="remarks"></a>Notes

Une section Geometry contenant une ligne Ellipse ou InfiniteLine ne doit pas contenir d'autres lignes.
  

