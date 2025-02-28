---
title: Active, cellule (section Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm10
ms.localizationpriority: medium
ms.assetid: 4c8e366f-9e9b-30ea-a89f-57c8d7a1168e
description: Détermine si le calque est actif. Les formes sans calque pré-attribué sont affectées aux calques actifs lorsque vous les faites glisser sur la page de dessin.
ms.openlocfilehash: fa922350c540a063d9434a7e708b900e6f812b5c
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63405594"
---
# <a name="active-cell-layers-section"></a>Active, cellule (section Layers)

Détermine si le calque est actif. Les formes sans calque pré-attribué sont affectées aux calques actifs lorsque vous les faites glisser sur la page de dessin.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le calque est actif. |
|FALSE  <br/> |Le calque n'est pas actif. |
   
## <a name="remarks"></a>Remarques

La valeur de cette cellule correspond au paramètre **Actif** de la boîte de dialogue **Propriétés des calques** (dans le groupe **Modification** de l’onglet **Accueil**, cliquez sur **Calques**, puis sur **Propriétés du calque**).
  
Pour obtenir une référence à la cellule Active par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |Layers.Active[ *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule Active à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionLayer** <br/> |
|**Index de la ligne :**  <br/> |**visRowLayer** +   *i* où *i* = 0, 1, 2... |
|**Index de la cellule :**  <br/> |**visLayerActive** <br/> |
   

