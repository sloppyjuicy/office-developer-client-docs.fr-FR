---
title: NoLine, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm715
ms.localizationpriority: medium
ms.assetid: f9624af2-c087-3dde-9140-339c438b3652
description: Détermine si un trait est tracé autour du contour du chemin.
ms.openlocfilehash: 6631d30da00f63f89314d362f981d888256d36f9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573872"
---
# <a name="noline-cell-geometry-section"></a>NoLine, cellule (section Geometry)

Détermine si un trait est tracé autour du contour du chemin.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Aucun trait n'est tracé autour du contour du chemin correspondant à la limite d'une région qu'il est possible de remplir.  <br/> |
| FALSE  <br/> | Un trait est tracé autour du contour du chemin.  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque vous décidez d'utiliser le blanc comme couleur de trait, le trait existe même s'il n'est pas visible sur un arrière-plan blanc. Lorsque vous définissez la valeur de cette cellule comme TRUE, aucun trait n'est tracé.
  
Pour obtenir une référence à la cellule NoLine par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Geometry  *i*  . NoLine où  *i*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule NoLine à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionFirstComponent**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la ligne :  <br/> |**visRowComponent** <br/> |
| Index de la cellule :  <br/> |**visCompNoLine** <br/> |
   

