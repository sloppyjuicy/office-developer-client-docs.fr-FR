---
title: NoShow, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm735
ms.localizationpriority: medium
ms.assetid: 831075ff-2875-b598-00bb-eb8481fee57b
description: Indique si un chemin est affiché sur la page de dessin.
ms.openlocfilehash: 63c8780e572dfc5094b12c99666ea94246511d63
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62774152"
---
# <a name="noshow-cell-geometry-section"></a>NoShow, cellule (section Geometry)

Indique si un chemin est affiché sur la page de dessin.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Le trait et le remplissage du chemin représentés par cette section sont masqués. |
| FALSE  <br/> | Le trait et le remplissage du chemin sont affichés. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule NoShow par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Geometry  *i*  . NoShow où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule NoShow à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionFirstComponent** +   *i* où *i* = 0, 1, 2... |
| Index de la ligne :  <br/> |**visRowComponent** <br/> |
| Index de la cellule :  <br/> |**visCompNoShow** <br/> |
   

