---
title: Snap, cellule (section Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251355
ms.localizationpriority: medium
ms.assetid: c1b24e45-6f08-686b-b53d-e85fb9087a50
description: Détermine si d'autres formes peuvent être alignées sur les formes attribuées au calque. Les formes associées au calque peuvent être alignées sur d'autres formes, mais les autres formes ne peuvent pas être alignées sur elles.
ms.openlocfilehash: 7bef592411efd89905b44a917bccd9b050ced531
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62776927"
---
# <a name="snap-cell-layers-section"></a>Snap, cellule (section Layers)

Détermine si d'autres formes peuvent être alignées sur les formes attribuées au calque. Les formes associées au calque peuvent être alignées sur d'autres formes, mais les autres formes ne peuvent pas être alignées sur elles.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Les autres formes peuvent s'aligner sur les formes du calque. |
|FALSE  <br/> |Les autres formes ne peuvent pas s'aligner sur les formes du calque. |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule à l’aide de l’option **Alignement** dans la boîte de dialogue **Propriétés des calques** (sous l’onglet **Accueil**, dans le groupe **Modification**, cliquez sur **Calques**, puis sur **Propriétés des calques**).
  
Pour obtenir une référence à la cellule Snap par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Layers.Snap[ *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule Snap par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionLayer** <br/> |
|Index de la ligne :  <br/> |**visRowLayer** +   *i* où *i* = 0, 1, 2... |
|Index de la cellule :  <br/> |**visLayerSnap** <br/> |
   

