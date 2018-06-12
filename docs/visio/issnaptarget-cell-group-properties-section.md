---
title: IsSnapTarget, cellule (section Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251626
localization_priority: Normal
ms.assetid: b58131f6-a566-d9ca-bad4-4f4b66e03aaf
description: Détermine si des formes peuvent être alignées sur un groupe ou sur des formes au sein du groupe.
ms.openlocfilehash: 89536923617f80768d7c14658cb07c97595824ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788872"
---
# <a name="issnaptarget-cell-group-properties-section"></a>IsSnapTarget, cellule (section Group Properties)

Détermine si des formes peuvent être alignées sur un groupe ou sur des formes au sein du groupe.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Active l'alignement sur des formes d'un groupe.  <br/> |
|FALSE  <br/> |Active l'alignement uniquement sur le groupe.  <br/> |
   
## <a name="remarks"></a>Note

Vous pouvez également définir cette valeur en sélectionnant le groupe, en cliquant sur **comportement** sous l’onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , puis activez la case à cocher **Aligner sur les formes membres** . 
  
Pour obtenir une référence à la cellule IsSnapTarget par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |IsSnapTarget  <br/> |
   
Pour obtenir une référence à la cellule IsSnapTarget par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowGroup** <br/> |
|Index de la cellule :  <br/> |**visGroupIsSnapTarget** <br/> |
   

