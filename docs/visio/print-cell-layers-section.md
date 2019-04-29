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
ms.openlocfilehash: f9a1dca6d45b53c02ff0ed29f921c352fc947630
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435214"
---
# <a name="print-cell-layers-section"></a>Print, cellule (section Layers)

Indique si les formes appartenant au calque peuvent être imprimées.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Les formes peuvent être imprimées.  <br/> |
|FALSE  <br/> |Les formes ne peuvent pas être imprimées.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur à l’aide de l’option **Imprimer** de la boîte de dialogue **Propriétés des calques** (sous l’onglet **Accueil**, dans le groupe **Modification**, cliquez sur **Calques**, puis sur **Propriétés des calques**).
  
Pour obtenir une référence à la cellule Print par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Layers. Print [ *i* ] où *i* = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Print à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionLayer** <br/> |
|Index de la ligne :  <br/> |**visRowLayer** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visDocPreviewScope** <br/> |
   

