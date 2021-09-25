---
title: ConLineJumpStyle, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251655
ms.localizationpriority: medium
ms.assetid: baa05a50-97d0-3769-635e-0ea20317d59a
description: Détermine le style de la déviation de trait pour un connecteur dynamique.
ms.openlocfilehash: b95b2b8a2c09ac8ca9a590b2d17a45083455def4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594712"
---
# <a name="conlinejumpstyle-cell-shape-layout-section"></a>ConLineJumpStyle, cellule (section Shape Layout)

Détermine le style de la déviation de trait pour un connecteur dynamique.
  
|**Valeur**|**Style de saut de ligne**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Valeur par défaut de la page  <br/> |**visLOJumpStyleDefault** <br/> |
|1  <br/> |Arc  <br/> |**visLOJumpStyleArc** <br/> |
|2  <br/> |Gap  <br/> |**visLOJumpStyleGap** <br/> |
|3  <br/> |Square  <br/> |**visLOJumpStyleSquare** <br/> |
|4   <br/> |Triangle  <br/> |**visLOJumpStyleTriangle** <br/> |
|5  <br/> |3 côtés  <br/> |**visLOJumpStyle2Point** <br/> |
|6   <br/> |4 côtés  <br/> |**visLOJumpStyle3Point** <br/> |
|7   <br/> |5 côtés  <br/> |**visLOJumpStyle4Point** <br/> |
|8   <br/> |6 côtés  <br/> |**visLOJumpStyle5Point** <br/> |
|9   <br/> |7 côtés  <br/> |**visLOJumpStyle6Point** <br/> |
   
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLOJumpStyle** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule  en sélectionnant un connecteur [](run-in-developer-mode-display-the-developer-tab.md) dynamique, en cliquant sur Comportement dans le groupe Création de forme sous l’onglet Développeur, puis sur l’onglet **Connecteur.**  
  
Pour obtenir une référence à la cellule ConLineJumpStyle par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |ConLineJumpStyle  <br/> |
   
Pour obtenir une référence à la cellule ConLineJumpStyle à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  

