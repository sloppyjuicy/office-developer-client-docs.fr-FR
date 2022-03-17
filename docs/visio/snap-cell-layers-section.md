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
ms.openlocfilehash: 9a115f64ccabaa33c55642003af4e6bd98634df7
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63523212"
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
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |Layers.Snap[ *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule Snap par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionLayer** <br/> |
|**Index de la ligne :**  <br/> |**visRowLayer** +   *i* où *i* = 0, 1, 2... |
|**Index de la cellule :**  <br/> |**visLayerSnap** <br/> |
   

