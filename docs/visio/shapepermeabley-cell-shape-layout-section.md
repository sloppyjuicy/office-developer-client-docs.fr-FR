---
title: ShapePermeableY, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251666
localization_priority: Normal
ms.assetid: 90701ecf-3d34-2eac-9ee9-7965e16c0f7c
description: Détermine si un connecteur peut se positionner verticalement en traversant une forme positionnable.
ms.openlocfilehash: 4a7a389ec1d753b8582b7ff0b921a615e582b1ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789638"
---
# <a name="shapepermeabley-cell-shape-layout-section"></a>ShapePermeableY, cellule (section Shape Layout)

Détermine si un connecteur peut se positionner verticalement en traversant une forme positionnable.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Permet aux connecteurs de se positionner verticalement en traversant une forme positionnable.  <br/> |
|FALSE  <br/> |Ne permet pas aux connecteurs de se positionner verticalement en traversant une forme positionnable.  <br/> |
   
## <a name="remarks"></a>Note

Vous pouvez également définir la valeur de cette cellule dans l’onglet **Placement** dans la boîte de dialogue **comportement** (avec la forme sélectionnée, sous l’onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , dans le groupe **Création de la forme** , cliquez sur **comportement**, puis cliquez sur l’onglet **Placement** ). 
  
Dans les versions antérieures à Visio 2000, vous pouviez définir ce comportement en faisant appel à la cellule ObjInteract de la section Miscellaneous.
  
Pour obtenir une référence à la cellule ShapePermeableY par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ShapePermeableY  <br/> |
   
Pour obtenir une référence à la cellule ShapePermeableY par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLOPermY** <br/> |
   

