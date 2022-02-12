---
title: Print, cellule (section Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm825
ms.localizationpriority: medium
ms.assetid: 9c76bf02-7269-65bb-2fd2-920243d962ef
description: Indique si les formes appartenant au calque peuvent être imprimées.
ms.openlocfilehash: f7393d3c1353b187aeafffec21b9f49a9c83bc59
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62777067"
---
# <a name="print-cell-layers-section"></a>Print, cellule (section Layers)

Indique si les formes appartenant au calque peuvent être imprimées.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Les formes peuvent être imprimées. |
|FALSE  <br/> |Les formes ne peuvent pas être imprimées. |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur à l’aide de l’option **Imprimer** de la boîte de dialogue **Propriétés des calques** (sous l’onglet **Accueil**, dans le groupe **Modification**, cliquez sur **Calques**, puis sur **Propriétés des calques**).
  
Pour obtenir une référence à la cellule Print par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Layers.Print[ *i*  ] where  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule Print à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionLayer** <br/> |
|Index de la ligne :  <br/> |**visRowLayer** +   *i* où *i* = 0, 1, 2... |
|Index de la cellule :  <br/> |**visDocPreviewScope** <br/> |
   

