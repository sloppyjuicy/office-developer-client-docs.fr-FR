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
ms.openlocfilehash: a7e511519bd64e313694313c4ce5a2a76bb2cbc3
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63376958"
---
# <a name="shapeplaceflip-cell-shape-layout-section"></a>ShapePlaceFlip, cellule (section Shape Layout)

Détermine la façon dont une forme positionnable est retournée et/ou pivote sur la page lorsque vous disposez des formes à l’aide de la boîte de dialogue **Configurer la disposition** (dans le groupe **Disposition** de l’onglet **Création**, cliquez sur **Nouvelle disposition de page**, puis cliquez sur **Autres options de disposition**).
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Utiliser la valeur page par défaut. |**visLOFlipDefault** <br/> |
|1  <br/> |Retournement horizontal. |**visLOFlipX** <br/> |
|2  <br/> |Retournement vertical. |**visLOFlipY** <br/> |
|4  <br/> |Retourner par incréments de 90 degrés entre 0 et 270. |**visLOFlipRotate** <br/> |
|8   <br/> |Ne pas retourner. |**visLOFlipNone** <br/> |

## <a name="remarks"></a>Remarques

La valeur de la cellule ShapePlaceFlip facilite l'orientation d'une forme positionnable vers la forme positionnable suivante à laquelle elle est liée.
  
Pour définir ce comportement pour *toutes* les formes de la page de dessin, utilisez la cellule PlaceFlip de la section Page Layout.
  
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
