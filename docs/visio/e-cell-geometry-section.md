---
title: E, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251761
localization_priority: Normal
ms.assetid: bc0154b1-6930-1fe0-655c-05eab2d60230
description: Contient une formule de courbe B-spline rationnelle non uniforme (NURBS).
ms.openlocfilehash: 000c4864c6ae98bfcd9e9cfdb16ff68396f63e44
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788541"
---
# <a name="e-cell-geometry-section"></a>E, cellule (section Geometry)

Contient une formule de courbe B-spline rationnelle non uniforme (NURBS).
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule E par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Géométrie *i* . E *j* où *i* et *j* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule E par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la ligne :  <br/> |**visRowVertex** +  *j* où *j* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visNURBSData** <br/> |
   

