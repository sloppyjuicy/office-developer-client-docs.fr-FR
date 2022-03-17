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
ms.openlocfilehash: 7bcf7c14233cea5969bf2185ae29a60060e2b18e
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63523079"
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
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |Layers.Visible[ *i*  ] where  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule Visible par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionLayer** <br/> |
|**Index de la ligne :**  <br/> |**visRowLayer** +   *i* où *i* = 0, 1, 2... |
|**Index de la cellule :**  <br/> |**visLayerVisible** <br/> |
   

