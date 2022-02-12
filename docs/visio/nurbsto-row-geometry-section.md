---
title: NURBSTo, ligne (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251758
ms.localizationpriority: medium
ms.assetid: 7e47acfe-5ec0-3689-eb89-0168f596a739
description: Contient les coordonnées x et y, la position du deuxième au dernier nœud, la position du dernier poids, la position du premier nœud, la position de la première pondération et la formule d’une ligne B-spline rationnelle nonuniforme (NURBS).
ms.openlocfilehash: 874930eac910e6cb828a06cec4433c423fb38343
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62784760"
---
# <a name="nurbsto-row-geometry-section"></a>NURBSTo, ligne (section Geometry)

Contient les coordonnées  *x*  et  *y*  , la position du deuxième au dernier nœud, la position du dernier poids, la position du premier nœud, la position de la première pondération et la formule d’une ligne B-spline rationnelle nonuniforme (NURBS). 
  
Une ligne NURBSTo contient les cellules suivantes.
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordonnée *x*  du dernier point de contrôle d’une NURBS. |
|[Y](y-cell-geometry-section.md) <br/> |Coordonnée *y*  du dernier point de contrôle d’une NURBS. |
|[A](a-cell-geometry-section.md) <br/> |Avant-dernier nœud de la courbe NURBS. |
|[B](b-cell-geometry-section.md) <br/> |La dernière épaisseur de la courbe NURBS. |
|[C](c-cell-geometry-section.md) <br/> |Le premier nœud de la courbe NURBS. |
|[D](d-cell-geometry-section.md) <br/> |La première épaisseur de la courbe NURBS. |
|[E](e-cell-geometry-section.md) <br/> |Une formule de courbe NURBS. |
   
## <a name="remarks"></a>Remarques

La courbe NURBS est la méthode habituelle de représentation mathématique d'une courbe. Vous pouvez créer une courbe NURBS à l'aide de l'outil **Dessin à main levée**. 
  

