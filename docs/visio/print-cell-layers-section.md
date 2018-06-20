---
title: Print, cellule (section Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm825
localization_priority: Normal
ms.assetid: 9c76bf02-7269-65bb-2fd2-920243d962ef
description: Indique si les formes appartenant au calque peuvent être imprimées.
ms.openlocfilehash: cd5b2830ba8bd20cb435cdc2bca4bd55fd5a5438
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789352"
---
# <a name="print-cell-layers-section"></a>Print, cellule (section Layers)

Indique si les formes appartenant au calque peuvent être imprimées.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Les formes peuvent être imprimées.  <br/> |
|FALSE  <br/> |Les formes ne peuvent pas être imprimées.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur à l’aide de l’option **Imprimer** dans la boîte de dialogue **Propriétés des calques** (sous l’onglet **accueil** , dans le groupe **modification** , cliquez sur **calques**, puis cliquez sur **Propriétés des calques**).
  
Pour obtenir une référence à la cellule Print par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Layers.Print [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Print par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionLayer** <br/> |
|Index de la ligne :  <br/> |**visRowLayer** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visDocPreviewScope** <br/> |
   

