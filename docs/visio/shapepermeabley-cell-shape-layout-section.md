---
title: ShapePermeableY, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251666
ms.localizationpriority: medium
ms.assetid: 90701ecf-3d34-2eac-9ee9-7965e16c0f7c
description: Détermine si un connecteur peut se positionner verticalement en traversant une forme positionnable.
ms.openlocfilehash: 1250c0569490fbb071656165c51a0ab98a52662b
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63520307"
---
# <a name="shapepermeabley-cell-shape-layout-section"></a>ShapePermeableY, cellule (section Shape Layout)

Détermine si un connecteur peut se positionner verticalement en traversant une forme positionnable.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Permet aux connecteurs de se positionner verticalement en traversant une forme positionnable. |
|FALSE  <br/> |Ne permet pas aux connecteurs de se positionner verticalement en traversant une forme positionnable. |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule sous l’onglet **Placement** dans  la boîte de dialogue Comportement (avec une forme sélectionnée, sous l’onglet Développeur,  dans le groupe Création de formes, cliquez sur **Comportement, puis** cliquez sur l’onglet [](run-in-developer-mode-display-the-developer-tab.md) **Placement**). 
  
Dans les versions antérieures à Visio 2000, vous pouviez définir ce comportement en faisant appel à la cellule ObjInteract de la section Miscellaneous.
  
Pour obtenir une référence à la cellule ShapePermeableY par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |ShapePermeableY  <br/> |
   
Pour obtenir une référence à la cellule ShapePermeableY à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowShapeLayout** <br/> |
|**Index de la cellule :**  <br/> |**visSLOPermY** <br/> |
   

