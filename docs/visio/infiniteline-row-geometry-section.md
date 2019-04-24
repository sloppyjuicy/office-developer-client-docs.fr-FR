---
title: InfiniteLine, ligne (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3020
localization_priority: Normal
ms.assetid: 55942a42-5e88-2f6b-69f8-405ce406fcaf
description: Contient les coordonnées x et y de deux points sur une ligne infinie.
ms.openlocfilehash: b6338b6b50535379759649c791b9678de640df70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335349"
---
# <a name="infiniteline-row-geometry-section"></a>InfiniteLine Row (Geometry Section)

Contient les coordonnées *x* et *y* de deux points sur une ligne infinie. 
  
Une ligne InfiniteLine contient les cellules suivantes.
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordonnée *x* d'un point sur la ligne infinie; associée à la coordonnée *y* représentée par la cellule y.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Coordonnée *y* d'un point sur la ligne infinie; associée à la coordonnée *x* représentée par la cellule x.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Coordonnée *x* d'un point sur la ligne infinie; associée à la coordonnée *y* représentée par la cellule B.  <br/> |
|[Point](b-cell-geometry-section.md) <br/> |Coordonnée *y* d'un point sur une ligne infinie; associée à la coordonnée *x* représentée par la cellule A.  <br/> |
   
## <a name="remarks"></a>Remarques

Une section Geometry contenant une ligne Ellipse ou InfiniteLine ne doit pas contenir d'autres lignes.
  

