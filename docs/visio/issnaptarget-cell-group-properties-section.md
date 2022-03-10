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
ms.openlocfilehash: f56cbf9d984a3865590c15a9d062b64762cc2c41
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63426796"
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
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |IsSnapTarget  <br/> |
   
Pour obtenir une référence à la cellule IsSnapTarget à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowGroup** <br/> |
|**Index de la cellule :**  <br/> |**visGroupIsSnapTarget** <br/> |
   

