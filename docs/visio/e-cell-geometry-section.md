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
ms.openlocfilehash: 6c45db2e1444256c63e72c9fcbafdbba04c97d58
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628394"
---
# <a name="e-cell-geometry-section"></a>E, cellule (section Geometry)

Contient une formule de courbe B-spline rationnelle non uniforme (NURBS).
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule E par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Geometry  *i*  . E  *j*            où  *i et*  *j*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule E à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionFirstComponent**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la ligne :  <br/> |**visRowVertex**  +   *j* où *j* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visNURBSData** <br/> |
   

