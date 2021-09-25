---
title: ShapePlaceFlip, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253247
ms.localizationpriority: medium
ms.assetid: 40008507-d9e4-9c0e-603f-d5e6da73a94b
description: Détermine la façon dont une forme positionnable est retournée et/ou pivote sur la page lorsque vous disposez des formes à l’aide de la boîte de dialogue Configurer la disposition (dans le groupe Disposition de l’onglet Création, cliquez sur Nouvelle disposition de page, puis cliquez sur Autres options de disposition).
ms.openlocfilehash: 4068db4cc4c1eaa96e1b0cd3a1827cbf935dfe9e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622920"
---
# <a name="shapeplaceflip-cell-shape-layout-section"></a>ShapePlaceFlip, cellule (section Shape Layout)

Détermine la façon dont une forme positionnable est retournée et/ou pivote sur la page lorsque vous disposez des formes à l’aide de la boîte de dialogue **Configurer la disposition** (dans le groupe **Disposition** de l’onglet **Création**, cliquez sur **Nouvelle disposition de page**, puis cliquez sur **Autres options de disposition**).
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Utiliser la valeur page par défaut.  <br/> |**visLOFlipDefault** <br/> |
|1  <br/> |Retournement horizontal.  <br/> |**visLOFlipX** <br/> |
|2  <br/> |Retournement vertical.  <br/> |**visLOFlipY** <br/> |
|4   <br/> |Retourner par incréments de 90 degrés entre 0 et 270.  <br/> |**visLOFlipRotate** <br/> |
|8   <br/> |Ne pas retourner.  <br/> |**visLOFlipNone** <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de la cellule ShapePlaceFlip facilite l'orientation d'une forme positionnable vers la forme positionnable suivante à laquelle elle est liée.
  
Pour définir ce comportement pour  *toutes les*  formes de la page de dessin, utilisez la cellule PlaceFlip dans la section Mise en page. 
  
Pour obtenir une référence à la cellule ShapePlaceFlip par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ShapePlaceFlip  <br/> |
   
Pour obtenir une référence à la cellule ShapePlaceFlip à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLOPlaceFlip** <br/> |
   

