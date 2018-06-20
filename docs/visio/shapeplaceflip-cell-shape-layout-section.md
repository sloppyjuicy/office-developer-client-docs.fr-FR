---
title: ShapePlaceFlip, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253247
localization_priority: Normal
ms.assetid: 40008507-d9e4-9c0e-603f-d5e6da73a94b
description: Détermine comment fait pivoter une forme positionnable, fait pivoter, ou les deux sur la page lorsque vous disposez des formes à l’aide de la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe mise en page, cliquez sur Re-mise en Page, puis cliquez sur autres Options de mise en page).
ms.openlocfilehash: 76941b9c50e6f2c68ea9abf54e81dcd18be13a70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789648"
---
# <a name="shapeplaceflip-cell-shape-layout-section"></a>ShapePlaceFlip, cellule (section Shape Layout)

Détermine comment fait pivoter une forme positionnable, fait pivoter, ou les deux sur la page lorsque vous disposez des formes à l’aide de la boîte de dialogue **Configurer la disposition** (sous l’onglet **Création** , dans le groupe **mise en page** , cliquez sur **Re-mise en Page**, puis cliquez sur **plus Options de disposition**).
  
|**Valeur**|**Description**|**Constante d’Automation**|
|:-----|:-----|:-----|
|0  <br/> |Utiliser la valeur page par défaut.  <br/> |**visLOFlipDefault** <br/> |
|1  <br/> |Retournement horizontal.  <br/> |**visLOFlipX** <br/> |
|2  <br/> |Retournement vertical.  <br/> |**visLOFlipY** <br/> |
|4  <br/> |Retourner par incréments de 90 degrés entre 0 et 270.  <br/> |**visLOFlipRotate** <br/> |
|8  <br/> |Ne pas retourner.  <br/> |**visLOFlipNone** <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de la cellule ShapePlaceFlip facilite l'orientation d'une forme positionnable vers la forme positionnable suivante à laquelle elle est liée.
  
Pour définir ce comportement pour *toutes* les formes sur la page de dessin, utilisez la cellule PlaceFlip de la section Page Layout. 
  
Pour obtenir une référence à la cellule ShapePlaceFlip par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ShapePlaceFlip  <br/> |
   
Pour obtenir une référence à la cellule ShapePlaceFlip par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLOPlaceFlip** <br/> |
   

