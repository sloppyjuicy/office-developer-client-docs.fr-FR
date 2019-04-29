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
ms.openlocfilehash: 55886a7e96bd2c08966cb85f5edad6a7174e30cd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408515"
---
# <a name="glue-cell-layers-section"></a>Glue, cellule (section Layers)

Détermine si les formes du calque peuvent être collées.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le collage est activé.  <br/> |
|FALSE  <br/> |Le collage est désactivé.  <br/> |
   
## <a name="remarks"></a>Remarques

Cette cellule correspond à l' **option collage** dans la boîte de dialogue **Propriétés** des calques (sous l'onglet **Accueil** , dans le groupe **modification** , cliquez sur calques, puis sur **Propriétés des calques** ). **** 
  
Pour obtenir une référence à la cellule Glue par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Layers. Glue [ *i* ] où *i* = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Glue à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionLayer** <br/> |
|Index de la ligne :  <br/> |**visRowLayer** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visLayerGlue** <br/> |
   

