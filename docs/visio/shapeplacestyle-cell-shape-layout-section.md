---
title: ShapePlaceStyle, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm70007
localization_priority: Normal
ms.assetid: 29bfe8ec-ca12-8fbf-b62b-ece3710dfe2e
description: Indique comment les formes sont placées sur la page lorsque les formes sont disposées dans la boîte de dialogue Configurer la disposition (sous l'onglet création, dans le groupe disposition, cliquez sur nouvelle disposition de page, puis cliquez sur autres options de disposition). Stocke le style de disposition et les valeurs d'alignement de VisCellIndices.
ms.openlocfilehash: 381f74912b64395f33a2dc55c0bad24d36a16286
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418574"
---
# <a name="shapeplacestyle-cell-shape-layout-section"></a>ShapePlaceStyle, cellule (section Shape Layout)

Indique comment les formes sont placées sur la page lorsque les formes sont disposées dans la boîte de dialogue **configurer la disposition** (sous l'onglet **création** , dans le groupe **disposition** , cliquez sur **nouvelle disposition de page**, puis cliquez sur **autres options de disposition**). Stocke le style de disposition et les valeurs d’alignement de **VisCellIndices**. 
  
|**Constante**|**Valeur**|
|:-----|:-----|
|**visLOPlaceBottomToTop** <br/> |4  <br/> |
|**visLOPlaceCircular** <br/> |6.x  <br/> |
|**visLOPlaceCompactDownLeft** <br/> |14   <br/> |
|**visLOPlaceCompactDownRight** <br/> |7j/7  <br/> |
|**visLOPlaceCompactLeftDown** <br/> |13   <br/> |
|**visLOPlaceCompactLeftUp** <br/> |12   <br/> |
|**visLOPlaceCompactRightDown** <br/> |8bits  <br/> |
|**visLOPlaceCompactRightUp** <br/> |4,9  <br/> |
|**visLOPlaceCompactUpLeft** <br/> |11   <br/> |
|**visLOPlaceCompactUpRight** <br/> |10   <br/> |
|**visLOPlaceDefault** <br/> |0  <br/> |
|**visLOPlaceHierarchyBottomToTopCenter** <br/> |vingtaine  <br/> |
|**visLOPlaceHierarchyBottomToTopLeft** <br/> |neuf  <br/> |
|**visLOPlaceHierarchyBottomToTopRight** <br/> |21  <br/> |
|**visLOPlaceHierarchyLeftToRightBottom** <br/> |heures/24  <br/> |
|**visLOPlaceHierarchyLeftToRightMiddle** <br/> |23  <br/> |
|**visLOPlaceHierarchyLeftToRightTop** <br/> |22,5  <br/> |
|**visLOPlaceHierarchyRightToLeftBottom** <br/> |vingt  <br/> |
|**visLOPlaceHierarchyRightToLeftMiddle** <br/> |27  <br/> |
|**visLOPlaceHierarchyRightToLeftTop** <br/> |25  <br/> |
|**visLOPlaceHierarchyTopToBottomCenter** <br/> |17   <br/> |
|**visLOPlaceHierarchyTopToBottomLeft** <br/> |16   <br/> |
|**visLOPlaceHierarchyTopToBottomRight** <br/> |18   <br/> |
|**visLOPlaceLeftToRight** <br/> |n°2  <br/> |
|**visLOPlaceParentDefault** <br/> |15   <br/> |
|**visLOPlaceRadial** <br/> |3  <br/> |
|**visLOPlaceRightToLeft** <br/> |disque  <br/> |
|**visLOPlaceTopToBottom** <br/> |0,1  <br/> |
   
Pour faire référence à la cellule ShapePlaceStyle par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ShapePlaceStyle  <br/> |
   
Pour faire référence à la cellule ShapePlaceStyle par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLOPlaceStyle** <br/> |
   

