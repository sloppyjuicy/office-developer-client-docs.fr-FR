---
title: ShapePermeablePlace, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm885
localization_priority: Normal
ms.assetid: b647cbb5-2769-068d-bbda-2dc983c47ac9
description: Détermine si des formes positionnables peuvent être placées sur une forme lors de la disposition des formes à l’aide de la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe Disposition, cliquez sur Nouvelle disposition de page, puis cliquez sur Autres options de disposition).
ms.openlocfilehash: ceecfa25c66c3ba261865d0131a3f55ef444d5e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357056"
---
# <a name="shapepermeableplace-cell-shape-layout-section"></a>ShapePermeablePlace, cellule (section Shape Layout)

Détermine si des formes positionnables peuvent être placées sur une forme lors de la disposition des formes à l’aide de la boîte de dialogue **Configurer la disposition** (sous l’onglet **Création**, dans le groupe **Disposition**, cliquez sur **Nouvelle disposition de page**, puis cliquez sur **Autres options de disposition**).
  
|**Value**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Permet de placer les formes sur une forme.  <br/> |
|FALSE  <br/> |Ne permet pas de placer les formes sur une forme.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule sous l'onglet **placement** de la boîte de dialogue **comportement** (sélectionnez une forme, sous l'onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , dans le groupe création de la **forme** , cliquez sur **comportement**, puis sur l'onglet **placement** . ). 
  
Dans les versions antérieures à Visio 2000, vous pouviez définir ce comportement en faisant appel à la cellule ObjInteract de la section Miscellaneous.
  
Pour obtenir une référence à la cellule ShapePermeablePlace par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ShapePermeablePlace  <br/> |
   
Pour obtenir une référence à la cellule ShapePermeablePlace à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLOPermeablePlace** <br/> |
   

