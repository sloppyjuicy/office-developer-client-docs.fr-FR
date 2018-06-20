---
title: ConLineJumpStyle, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251655
localization_priority: Normal
ms.assetid: baa05a50-97d0-3769-635e-0ea20317d59a
description: Détermine le style de la déviation de trait pour un connecteur dynamique.
ms.openlocfilehash: d3e27ddb6689fb5635674b3c4a8462fe587bce7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788340"
---
# <a name="conlinejumpstyle-cell-shape-layout-section"></a>ConLineJumpStyle, cellule (section Shape Layout)

Détermine le style de la déviation de trait pour un connecteur dynamique.
  
|**Valeur**|**Style de déviation de trait**|**Constante d’Automation**|
|:-----|:-----|:-----|
|0  <br/> |Valeur par défaut de la page  <br/> |**visLOJumpStyleDefault** <br/> |
|1  <br/> |Arc  <br/> |**visLOJumpStyleArc** <br/> |
|2  <br/> |Intervalle  <br/> |**visLOJumpStyleGap** <br/> |
|3  <br/> |Carré  <br/> |**visLOJumpStyleSquare** <br/> |
|4  <br/> |Triangle  <br/> |**visLOJumpStyleTriangle** <br/> |
|5  <br/> |3 côtés  <br/> |**visLOJumpStyle2Point** <br/> |
|6  <br/> |4 côtés  <br/> |**visLOJumpStyle3Point** <br/> |
|7  <br/> |5 côtés  <br/> |**visLOJumpStyle4Point** <br/> |
|8  <br/> |6 côtés  <br/> |**visLOJumpStyle5Point** <br/> |
|9  <br/> |7 côtés  <br/> |**visLOJumpStyle6Point** <br/> |
   
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLOJumpStyle** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule en sélectionnant un connecteur dynamique et en cliquant sur **comportement** dans le groupe **Création de la forme** sous l’onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , puis en cliquant sur l’onglet **connecteur** . 
  
Pour obtenir une référence à la cellule ConLineJumpStyle par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ConLineJumpStyle  <br/> |
   
Pour obtenir une référence à la cellule ConLineJumpStyle par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  

