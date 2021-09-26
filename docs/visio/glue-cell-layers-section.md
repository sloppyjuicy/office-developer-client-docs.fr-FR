---
title: Glue, cellule (section Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm415
ms.localizationpriority: medium
ms.assetid: 75f2ea45-52ac-ddfa-14ea-402933ae2449
description: Détermine si les formes du calque peuvent être collées.
ms.openlocfilehash: 64935dfd8964757f3b8590519fbb0c883200e178
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612777"
---
# <a name="glue-cell-layers-section"></a>Glue, cellule (section Layers)

Détermine si les formes du calque peuvent être collées.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le collage est activé.  <br/> |
|FALSE  <br/> |Le collage est désactivé.  <br/> |
   
## <a name="remarks"></a>Remarques

Cette cellule correspond à l’option Coller dans la  boîte de  dialogue Propriétés des calques (sous l’onglet Accueil, dans le groupe Édition, cliquez sur Calques, puis sur Propriétés des **calques).**    
  
Pour obtenir une référence à la cellule Glue par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Layers.Glue[  *i*  ] où  *i*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Glue à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionLayer** <br/> |
|Index de la ligne :  <br/> |**visRowLayer**  +   *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visLayerGlue** <br/> |
   

