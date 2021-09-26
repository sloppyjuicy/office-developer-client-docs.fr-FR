---
title: NoQuickDrag, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80004
ms.localizationpriority: medium
ms.assetid: 8491f459-9de2-8e75-5532-7d3bd0986734
description: Détermine si une forme peut être sélectionnée ou glissée lorsque l’utilisateur clique sur la zone remplie définie par la section Geometry.
ms.openlocfilehash: 052080f2334eb776e8a50d608724a6faa445d2ab
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627869"
---
# <a name="noquickdrag-cell-geometry-section"></a>NoQuickDrag, cellule (section Geometry)

Détermine si une forme peut être sélectionnée ou glissée lorsque l’utilisateur clique sur la zone remplie définie par la section Geometry.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule NoQuickDrag par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Geometry  *i*  . NoQuickDrag, où * i * - <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule NoQuickDrag à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionFirstComponent**  +   *i* , où *i* = 0, 1, 2...  <br/> |
|Index de la ligne :  <br/> |**visRowComponent** <br/> |
|Index de la cellule :  <br/> |**visCompNoQuickDrag** <br/> |
   

