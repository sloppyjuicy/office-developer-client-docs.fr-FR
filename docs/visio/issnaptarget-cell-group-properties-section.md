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
ms.openlocfilehash: 2171c548a1f47bf19ee3dc3b408696364e7667b1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628030"
---
# <a name="issnaptarget-cell-group-properties-section"></a>IsSnapTarget, cellule (section Group Properties)

Détermine si des formes peuvent être alignées sur un groupe ou sur des formes au sein du groupe.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Active l'alignement sur des formes d'un groupe.  <br/> |
|FALSE  <br/> |Active l'alignement uniquement sur le groupe.  <br/> |
   
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
   

