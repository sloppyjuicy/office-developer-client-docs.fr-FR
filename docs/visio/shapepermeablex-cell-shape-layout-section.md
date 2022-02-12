---
title: ShapePermeableX, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm890
ms.localizationpriority: medium
ms.assetid: 7e27b36c-4fd1-34e0-c168-f49eb5757b0e
description: Détermine si un connecteur peut se positionner horizontalement en traversant une forme positionnable.
ms.openlocfilehash: 637b665a9ded491e66f80886e9a56bcf1c1591d8
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62779312"
---
# <a name="shapepermeablex-cell-shape-layout-section"></a>ShapePermeableX, cellule (section Shape Layout)

Détermine si un connecteur peut se positionner horizontalement en traversant une forme positionnable.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Permet aux connecteurs de se positionner horizontalement en traversant une forme positionnable. |
|FALSE  <br/> |Ne permet pas aux connecteurs de se positionner horizontalement en traversant une forme positionnable. |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule sous l’onglet **Placement** dans  la boîte de dialogue Comportement (avec une forme sélectionnée, sous l’onglet Développeur,  dans le groupe Création de formes, cliquez sur **Comportement, puis** cliquez sur l’onglet [](run-in-developer-mode-display-the-developer-tab.md) **Placement**). 
  
Dans les versions antérieures à Visio 2000, vous pouviez définir ce comportement en faisant appel à la cellule ObjInteract de la section Miscellaneous. 
  
Pour obtenir une référence à la cellule ShapePermeableX par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ShapePermeableX  <br/> |
   
Pour obtenir une référence à la cellule ShapePermeableX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLOPermX** <br/> |
   

