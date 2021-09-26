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
ms.openlocfilehash: 4e5e91a0a13d2e0b6f084095da813d35316f6bc8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597722"
---
# <a name="visible-cell-layers-section"></a>Visible, cellule (section Layers)

Indique si les formes appartenant au calque sont visibles sur la page de dessin.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Les formes sont visibles.  <br/> |
|FALSE  <br/> |Les formes sont masquées.  <br/> |
   
## <a name="remarks"></a>Remarques

Cette cellule correspond à l’option **Visible** dans la  boîte de  dialogue Propriétés des calques (sous l’onglet Accueil, dans le groupe Édition, cliquez sur Calques, puis sur Propriétés des **calques).**   
  
Pour obtenir une référence à la cellule Visible par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Layers.Visible[ *i*  ] où  *i*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Visible par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionLayer** <br/> |
|Index de la ligne :  <br/> |**visRowLayer**  +   *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visLayerVisible** <br/> |
   

