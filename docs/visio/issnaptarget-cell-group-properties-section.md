---
title: IsSnapTarget, cellule (section Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251626
ms.localizationpriority: medium
ms.assetid: b58131f6-a566-d9ca-bad4-4f4b66e03aaf
description: Détermine si des formes peuvent être alignées sur un groupe ou sur des formes au sein du groupe.
ms.openlocfilehash: 711036626407c477db09b964d92dd801ab0ea36f
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62771341"
---
# <a name="issnaptarget-cell-group-properties-section"></a>IsSnapTarget, cellule (section Group Properties)

Détermine si des formes peuvent être alignées sur un groupe ou sur des formes au sein du groupe.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Active l'alignement sur des formes d'un groupe. |
|FALSE  <br/> |Active l'alignement uniquement sur le groupe. |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur en sélectionnant le groupe, en cliquant sur **Comportement** sous l’onglet [Développeur](run-in-developer-mode-display-the-developer-tab.md), puis en activant la case à cocher **Aligner sur les formes membres**. 
  
Pour obtenir une référence à la cellule IsSnapTarget par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |IsSnapTarget  <br/> |
   
Pour obtenir une référence à la cellule IsSnapTarget à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowGroup** <br/> |
|Index de la cellule :  <br/> |**visGroupIsSnapTarget** <br/> |
   

