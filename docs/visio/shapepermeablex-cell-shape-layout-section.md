---
title: ShapePermeableX, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm890
localization_priority: Normal
ms.assetid: 7e27b36c-4fd1-34e0-c168-f49eb5757b0e
description: Détermine si un connecteur peut se positionner horizontalement en traversant une forme positionnable.
ms.openlocfilehash: 21fa1683c4b1afd24992ec7a8a6daa52a8280825
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357049"
---
# <a name="shapepermeablex-cell-shape-layout-section"></a>ShapePermeableX, cellule (section Shape Layout)

Détermine si un connecteur peut se positionner horizontalement en traversant une forme positionnable.
  
|**Value**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Permet aux connecteurs de se positionner horizontalement en traversant une forme positionnable.  <br/> |
|FALSE  <br/> |Ne permet pas aux connecteurs de se positionner horizontalement en traversant une forme positionnable.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule sous l'onglet **placement** de la boîte de dialogue **comportement** (sélectionnez une forme, sous l'onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , dans le groupe création de la **forme** , cliquez sur **comportement**, puis sur l'onglet **placement** . ). 
  
Dans les versions antérieures à Visio 2000, vous pouviez définir ce comportement en faisant appel à la cellule ObjInteract de la section Miscellaneous. 
  
Pour obtenir une référence à la cellule ShapePermeableX par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ShapePermeableX  <br/> |
   
Pour obtenir une référence à la cellule ShapePermeableX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLOPermX** <br/> |
   

