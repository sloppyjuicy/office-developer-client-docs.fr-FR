---
title: PlaceFlip, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253251
ms.localizationpriority: medium
ms.assetid: df014b98-cfd5-b6d3-4b8a-b0acb3b94412
description: Détermine la façon dont les formes positionnables sont retournées et/ou pivotent lorsque vous utilisez la commande Configurer la disposition (sous l’onglet Création, dans le groupe Disposition, cliquez sur Nouvelle disposition de page, puis cliquez sur Autres options de disposition).
ms.openlocfilehash: 2c97580b398d62203acb3d8ddef01a8e462c2c7a
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63633833"
---
# <a name="placeflip-cell-page-layout-section"></a>PlaceFlip, cellule (section Page Layout)

Détermine la façon dont les formes positionnables sont retournées et/ou pivotent lorsque vous utilisez la commande **Configurer la disposition** (sous l’onglet **Création**, dans le groupe **Disposition**, cliquez sur **Nouvelle disposition de page**, puis cliquez sur **Autres options de disposition**).
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
|&amp;H0  <br/> |Par défaut. Pas de retournement. |**visLOFlipDefault** <br/> |
|&amp;H1  <br/> |Retournement horizontal. |**visLOFlipX** <br/> |
|&amp;H2  <br/> |Retournement vertical. |**visLOFlipY** <br/> |
|&amp;H4  <br/> |Retournement par incréments de 90 degrés. |**visLOFlipRotate** <br/> |
|&amp;H8  <br/> |Pas de retournement. |**visLOFlipNone** <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de la cellule PlaceFlip facilite l'orientation d'une forme positionnable vers la forme positionnable suivante à laquelle elle est liée. Elle est généralement utilisée pour la mise en page de dessins qui utilisent le collage statique.
  
Pour définir ce comportement pour une forme donnée, utilisez la cellule ShapePlaceFlip de la section Shape Layout.
  
Pour obtenir une référence à la cellule PlaceFlip par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |PlaceFlip  <br/> |
   
Pour obtenir une référence à la cellule PlaceFlip à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowPageLayout** <br/> |
|**Index de la cellule :**  <br/> |**visPLOPlaceFlip** <br/> |
   

