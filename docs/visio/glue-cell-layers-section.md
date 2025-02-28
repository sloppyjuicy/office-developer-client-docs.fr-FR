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
ms.openlocfilehash: 7763eae64447e8ad054065134e2ccb72277fa30b
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63426362"
---
# <a name="glue-cell-layers-section"></a>Glue, cellule (section Layers)

Détermine si les formes du calque peuvent être collées.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le collage est activé. |
|FALSE  <br/> |Le collage est désactivé. |
   
## <a name="remarks"></a>Remarques

Cette cellule correspond à  l’option **Coller** dans la  boîte de dialogue Propriétés des calques (sous l’onglet Accueil, dans le groupe Édition, cliquez sur Calques **, puis** sur Propriétés des **calques**). 
  
Pour obtenir une référence à la cellule Glue par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |Layers.Glue[  *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule Glue à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionLayer** <br/> |
|**Index de la ligne :**  <br/> |**visRowLayer** +   *i* où *i* = 0, 1, 2... |
|**Index de la cellule :**  <br/> |**visLayerGlue** <br/> |
   

