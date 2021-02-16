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
description: Détermine la façon dont les formes positionnables sont retournées et/ou pivotent lorsque vous utilisez la commande Configurer la disposition (sous l’onglet Création, dans le groupe Disposition, cliquez sur Nouvelle disposition de page, puis cliquez sur Autres options de disposition).
ms.openlocfilehash: d1c31654782012b3536d35f3a12a923c2cc7a8f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434297"
---
# <a name="placeflip-cell-page-layout-section"></a>PlaceFlip, cellule (section Page Layout)

Détermine la façon dont les formes positionnables sont retournées et/ou pivotent lorsque vous utilisez la commande **Configurer la disposition** (sous l’onglet **Création**, dans le groupe **Disposition**, cliquez sur **Nouvelle disposition de page**, puis cliquez sur **Autres options de disposition**).
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
|&amp;H0  <br/> |Valeur par défaut. Pas de retournement.  <br/> |**visLOFlipDefault** <br/> |
|&amp;H1  <br/> |Retournement horizontal.  <br/> |**visLOFlipX** <br/> |
|&amp;H2  <br/> |Retournement vertical.  <br/> |**visLOFlipY** <br/> |
|&amp;H4  <br/> |Retournement par incréments de 90 degrés.  <br/> |**visLOFlipRotate** <br/> |
|&amp;H8  <br/> |Pas de retournement.  <br/> |**visLOFlipNone** <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de la cellule PlaceFlip facilite l'orientation d'une forme positionnable vers la forme positionnable suivante à laquelle elle est liée. Elle est généralement utilisée pour la mise en page de dessins qui utilisent le collage statique.
  
Pour définir ce comportement pour une forme donnée, utilisez la cellule ShapePlaceFlip de la section Shape Layout.
  
Pour obtenir une référence à la cellule PlaceFlip par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |PlaceFlip  <br/> |
   
Pour obtenir une référence à la cellule PlaceFlip à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
|Index de la cellule :  <br/> |**visPLOPlaceFlip** <br/> |
   

