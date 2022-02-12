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
ms.openlocfilehash: 53f330f324017f5713f979aa3aff3e4b386dba6d
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62779333"
---
# <a name="shapepermeableplace-cell-shape-layout-section"></a>ShapePermeablePlace, cellule (section Shape Layout)

Détermine si des formes positionnables peuvent être placées sur une forme lors de la disposition des formes à l’aide de la boîte de dialogue **Configurer la disposition** (sous l’onglet **Création**, dans le groupe **Disposition**, cliquez sur **Nouvelle disposition de page**, puis cliquez sur **Autres options de disposition**).
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Permet de placer les formes sur une forme. |
|FALSE  <br/> |Ne permet pas de placer les formes sur une forme. |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule sous l’onglet **Placement** dans  la boîte de dialogue Comportement (avec une forme sélectionnée, sous l’onglet Développeur,  dans le groupe Création de formes, cliquez sur **Comportement, puis** cliquez sur l’onglet [](run-in-developer-mode-display-the-developer-tab.md) **Placement**). 
  
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
   

