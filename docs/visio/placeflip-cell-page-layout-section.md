---
title: PlaceFlip, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253251
localization_priority: Normal
ms.assetid: df014b98-cfd5-b6d3-4b8a-b0acb3b94412
description: Détermine les formes positionnables comment retourner ou faire pivoter une page lorsque vous utilisez la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe mise en page, cliquez sur Re-mise en Page, puis cliquez sur autres Options de mise en page).
ms.openlocfilehash: fb16849c7a496a4277133c68453d94d6fd2e67f8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789237"
---
# <a name="placeflip-cell-page-layout-section"></a>PlaceFlip, cellule (section Page Layout)

Détermine les formes positionnables comment retourner ou faire pivoter une page lorsque vous utilisez la boîte de dialogue **Configurer la disposition** (sous l’onglet **Création** , dans le groupe **mise en page** , cliquez sur **Re-mise en Page**, puis cliquez sur **Autres Options de mise en page**).
  
|**Valeur**|**Description**|**Constante d’Automation**|
|:-----|:-----|:-----|
|&amp;H0  <br/> |Par défaut. Pas de retournement.  <br/> |**visLOFlipDefault** <br/> |
|&amp;H1  <br/> |Retournement horizontal.  <br/> |**visLOFlipX** <br/> |
|&amp;H2  <br/> |Retournement vertical.  <br/> |**visLOFlipY** <br/> |
|&amp;H4  <br/> |Retournement par incréments de 90 degrés.  <br/> |**visLOFlipRotate** <br/> |
|&amp;H8  <br/> |Pas de retournement.  <br/> |**visLOFlipNone** <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de la cellule PlaceFlip facilite l'orientation d'une forme positionnable vers la forme positionnable suivante à laquelle elle est liée. Elle est généralement utilisée pour la mise en page de dessins qui utilisent le collage statique.
  
Pour définir ce comportement pour une forme donnée, utilisez la cellule ShapePlaceFlip de la section Shape Layout.
  
Pour obtenir une référence à la cellule PlaceFlip par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |PlaceFlip  <br/> |
   
Pour obtenir une référence à la cellule PlaceFlip par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
|Index de la cellule :  <br/> |**visPLOPlaceFlip** <br/> |
   

