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
ms.openlocfilehash: ae8af4e326a6c895b3617a4869f98eaf0db68db1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415991"
---
# <a name="conlinejumpstyle-cell-shape-layout-section"></a>ConLineJumpStyle, cellule (section Shape Layout)

Détermine le style de la déviation de trait pour un connecteur dynamique.
  
|**Valeur**|**Style de déViation de trait**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Valeur par défaut de la page  <br/> |**visLOJumpStyleDefault** <br/> |
|0,1  <br/> |Arc  <br/> |**visLOJumpStyleArc** <br/> |
|n°2  <br/> |Gap  <br/> |**visLOJumpStyleGap** <br/> |
|3  <br/> |Square  <br/> |**visLOJumpStyleSquare** <br/> |
|4  <br/> |Signalisation  <br/> |**visLOJumpStyleTriangle** <br/> |
|disque  <br/> |3 côtés  <br/> |**visLOJumpStyle2Point** <br/> |
|6.x  <br/> |4 côtés  <br/> |**visLOJumpStyle3Point** <br/> |
|7j/7  <br/> |5 côtés  <br/> |**visLOJumpStyle4Point** <br/> |
|8bits  <br/> |6 côtés  <br/> |**visLOJumpStyle5Point** <br/> |
|4,9  <br/> |7 côtés  <br/> |**visLOJumpStyle6Point** <br/> |
   
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLOJumpStyle** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule en sélectionnant un connecteur dynamique, en cliquant sur **comportement** dans le groupe **création de forme** de l'onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , puis en cliquant sur l'onglet **connecteur** . 
  
Pour obtenir une référence à la cellule ConLineJumpStyle par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |ConLineJumpStyle  <br/> |
   
Pour obtenir une référence à la cellule ConLineJumpStyle à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  

