---
title: ShapePermeablePlace, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm885
ms.localizationpriority: medium
ms.assetid: b647cbb5-2769-068d-bbda-2dc983c47ac9
description: Détermine si des formes positionnables peuvent être placées sur une forme lors de la disposition des formes à l’aide de la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe Disposition, cliquez sur Nouvelle disposition de page, puis cliquez sur Autres options de disposition).
ms.openlocfilehash: 384d28f742f88e6720abe497451c77cb101a3095
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607716"
---
# <a name="shapepermeableplace-cell-shape-layout-section"></a>ShapePermeablePlace, cellule (section Shape Layout)

Détermine si des formes positionnables peuvent être placées sur une forme lors de la disposition des formes à l’aide de la boîte de dialogue **Configurer la disposition** (sous l’onglet **Création**, dans le groupe **Disposition**, cliquez sur **Nouvelle disposition de page**, puis cliquez sur **Autres options de disposition**).
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Permet de placer les formes sur une forme.  <br/> |
|FALSE  <br/> |Ne permet pas de placer les formes sur une forme.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette  cellule sous l’onglet **Placement** dans la boîte  de dialogue Comportement (avec une forme sélectionnée, sous l’onglet Développeur, dans le groupe Création de formes, cliquez sur **Comportement,** puis cliquez sur l’onglet **Placement).** [](run-in-developer-mode-display-the-developer-tab.md) 
  
Dans les versions antérieures à Visio 2000, vous pouviez définir ce comportement en faisant appel à la cellule ObjInteract de la section Miscellaneous.
  
Pour obtenir une référence à la cellule ShapePermeablePlace par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ShapePermeablePlace  <br/> |
   
Pour obtenir une référence à la cellule ShapePermeablePlace à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLOPermeablePlace** <br/> |
   

