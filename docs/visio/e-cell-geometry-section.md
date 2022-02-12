---
title: E, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251761
ms.localizationpriority: medium
ms.assetid: bc0154b1-6930-1fe0-655c-05eab2d60230
description: Contient une formule de courbe B-spline rationnelle non uniforme (NURBS).
ms.openlocfilehash: cc9e07907a71fa44ab2c319c28b23947f8d06184
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62774307"
---
# <a name="e-cell-geometry-section"></a>E, cellule (section Geometry)

Contient une formule de courbe B-spline rationnelle non uniforme (NURBS).
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule E par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Geometry  *i*  . E  *j*            où  *i*  et  *j*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule E à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionFirstComponent** +   *i* où *i* = 0, 1, 2... |
| Index de la ligne :  <br/> |**visRowVertex** +   *j* où *j* = 0, 1, 2... |
| Index de la cellule :  <br/> |**visNURBSData** <br/> |
   

