---
title: Visible, cellule (section Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1110
ms.localizationpriority: medium
ms.assetid: 02048012-a814-410b-f26e-56fcfbe106e6
description: Indique si les formes appartenant au calque sont visibles sur la page de dessin.
ms.openlocfilehash: 222950da1dce771906e7ede181377d7cc3c3fbbc
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62775244"
---
# <a name="visible-cell-layers-section"></a>Visible, cellule (section Layers)

Indique si les formes appartenant au calque sont visibles sur la page de dessin.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Les formes sont visibles. |
|FALSE  <br/> |Les formes sont masquées. |
   
## <a name="remarks"></a>Remarques

Cette cellule correspond à l’option **Visible** dans la  boîte de dialogue Propriétés des calques (sous l’onglet Accueil, dans le groupe Édition,  cliquez sur Calques **, puis** sur Propriétés des **calques**). 
  
Pour obtenir une référence à la cellule Visible par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Layers.Visible[ *i*  ] where  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule Visible par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionLayer** <br/> |
|Index de la ligne :  <br/> |**visRowLayer** +   *i* où *i* = 0, 1, 2... |
|Index de la cellule :  <br/> |**visLayerVisible** <br/> |
   

