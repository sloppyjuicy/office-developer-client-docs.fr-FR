---
title: Glue, cellule (section Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm415
localization_priority: Normal
ms.assetid: 75f2ea45-52ac-ddfa-14ea-402933ae2449
description: Détermine si les formes du calque peuvent être collées.
ms.openlocfilehash: 81a54bebaa8ca68a8fbc8853c69f88efb34bbdb2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788717"
---
# <a name="glue-cell-layers-section"></a>Glue, cellule (section Layers)

Détermine si les formes du calque peuvent être collées.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le collage est activé.  <br/> |
|FALSE  <br/> |Le collage est désactivé.  <br/> |
   
## <a name="remarks"></a>Remarques

Cette cellule correspond à l’option **Collage** dans la boîte de dialogue **Propriétés des calques** (sous l’onglet **accueil** , dans le groupe **modification** , cliquez sur **calques**, puis cliquez sur **Propriétés des calques** ). 
  
Pour obtenir une référence à la cellule Glue par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Layers.Glue [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Glue par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionLayer** <br/> |
|Index de la ligne :  <br/> |**visRowLayer** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visLayerGlue** <br/> |
   

