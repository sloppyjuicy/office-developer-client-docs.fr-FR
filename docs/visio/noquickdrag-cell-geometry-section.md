---
title: NoQuickDrag, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80004
localization_priority: Normal
ms.assetid: 8491f459-9de2-8e75-5532-7d3bd0986734
description: Détermine si une forme peut être sélectionnée ou déplacée lorsque l'utilisateur clique sur la zone remplie définie par la section Geometry.
ms.openlocfilehash: d60268685d93ae88abb2840f62b093db1e688c2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417720"
---
# <a name="noquickdrag-cell-geometry-section"></a>NoQuickDrag, cellule (section Geometry)

Détermine si une forme peut être sélectionnée ou déplacée lorsque l'utilisateur clique sur la zone remplie définie par la section Geometry.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule NoQuickDrag par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Géométrie *i* . NoQuickDrag, où * i *-<1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule NoQuickDrag à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionFirstComponent** +  *i* , où *i* = 0, 1, 2...  <br/> |
|Index de la ligne :  <br/> |**visRowComponent** <br/> |
|Index de la cellule :  <br/> |**visCompNoQuickDrag** <br/> |
   

