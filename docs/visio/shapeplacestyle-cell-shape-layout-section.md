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
description: Indique comment les formes sont placées sur la page lorsqu’elles sont disposées dans la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe mise en page, cliquez sur Re-mise en Page, puis cliquez sur autres Options de mise en page). Stocke les valeurs de style et l’alignement de disposition de VisCellIndices.
ms.openlocfilehash: f160c09eae3a3135360f2b8bf6df86c78ba0968c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789650"
---
# <a name="shapeplacestyle-cell-shape-layout-section"></a>ShapePlaceStyle, cellule (section Shape Layout)

Indique comment les formes sont placées sur la page lorsqu’elles sont disposées dans la boîte de dialogue **Configurer la disposition** (sous l’onglet **Création** , dans le groupe **mise en page** , cliquez sur **Re-mise en Page**, puis cliquez sur **Autres Options de mise en page**). Stocke les valeurs de style et l’alignement de disposition de **VisCellIndices**. 
  
|**Constante**|**Valeur**|
|:-----|:-----|
|**visLOPlaceBottomToTop** <br/> |4  <br/> |
|**visLOPlaceCircular** <br/> |6  <br/> |
|**visLOPlaceCompactDownLeft** <br/> |14  <br/> |
|**visLOPlaceCompactDownRight** <br/> |7  <br/> |
|**visLOPlaceCompactLeftDown** <br/> |13  <br/> |
|**visLOPlaceCompactLeftUp** <br/> |12  <br/> |
|**visLOPlaceCompactRightDown** <br/> |8  <br/> |
|**visLOPlaceCompactRightUp** <br/> |9  <br/> |
|**visLOPlaceCompactUpLeft** <br/> |11  <br/> |
|**visLOPlaceCompactUpRight** <br/> |10  <br/> |
|**visLOPlaceDefault** <br/> |0  <br/> |
|**visLOPlaceHierarchyBottomToTopCenter** <br/> |20  <br/> |
|**visLOPlaceHierarchyBottomToTopLeft** <br/> |19  <br/> |
|**visLOPlaceHierarchyBottomToTopRight** <br/> |21  <br/> |
|**visLOPlaceHierarchyLeftToRightBottom** <br/> |24  <br/> |
|**visLOPlaceHierarchyLeftToRightMiddle** <br/> |23  <br/> |
|**visLOPlaceHierarchyLeftToRightTop** <br/> |22  <br/> |
|**visLOPlaceHierarchyRightToLeftBottom** <br/> |27  <br/> |
|**visLOPlaceHierarchyRightToLeftMiddle** <br/> |26  <br/> |
|**visLOPlaceHierarchyRightToLeftTop** <br/> |25  <br/> |
|**visLOPlaceHierarchyTopToBottomCenter** <br/> |17  <br/> |
|**visLOPlaceHierarchyTopToBottomLeft** <br/> |16  <br/> |
|**visLOPlaceHierarchyTopToBottomRight** <br/> |18  <br/> |
|**visLOPlaceLeftToRight** <br/> |2  <br/> |
|**visLOPlaceParentDefault** <br/> |15  <br/> |
|**visLOPlaceRadial** <br/> |3  <br/> |
|**visLOPlaceRightToLeft** <br/> |5  <br/> |
|**visLOPlaceTopToBottom** <br/> |1  <br/> |
   
Pour faire référence à la cellule ShapePlaceStyle par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ShapePlaceStyle  <br/> |
   
Pour faire référence à la cellule ShapePlaceStyle par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLOPlaceStyle** <br/> |
   

