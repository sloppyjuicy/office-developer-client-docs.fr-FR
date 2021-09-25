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
ms.openlocfilehash: c4625eadf2d9729c08204eac6d6d12b9b7f69408
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573354"
---
# <a name="shapepermeabley-cell-shape-layout-section"></a>ShapePermeableY, cellule (section Shape Layout)

Détermine si un connecteur peut se positionner verticalement en traversant une forme positionnable.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Permet aux connecteurs de se positionner verticalement en traversant une forme positionnable.  <br/> |
|FALSE  <br/> |Ne permet pas aux connecteurs de se positionner verticalement en traversant une forme positionnable.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette  cellule sous l’onglet **Placement** dans la boîte  de dialogue Comportement (avec une forme sélectionnée, sous l’onglet Développeur, dans le groupe Création de formes, cliquez sur **Comportement,** puis cliquez sur l’onglet **Placement).** [](run-in-developer-mode-display-the-developer-tab.md) 
  
Dans les versions antérieures à Visio 2000, vous pouviez définir ce comportement en faisant appel à la cellule ObjInteract de la section Miscellaneous.
  
Pour obtenir une référence à la cellule ShapePermeableY par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ShapePermeableY  <br/> |
   
Pour obtenir une référence à la cellule ShapePermeableY à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLOPermY** <br/> |
   

