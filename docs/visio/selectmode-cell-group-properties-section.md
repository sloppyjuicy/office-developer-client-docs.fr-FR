---
title: SelectMode, cellule (section Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm875
localization_priority: Normal
ms.assetid: 5ba68e05-f394-d7b7-390d-f0a9fdad011e
description: Détermine le mode de sélection d'une forme de groupe et de ses membres.
ms.openlocfilehash: 82f9e2806d1131a0acfd064f585c681fef0f209f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326011"
---
# <a name="selectmode-cell-group-properties-section"></a>SelectMode, cellule (section Group Properties)

Détermine le mode de sélection d'une forme de groupe et de ses membres.
  
|**Valeur**|**Mode de sélection**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Sélectionner uniquement la forme de groupe.  <br/> |**visGrpSelModeGroupOnly** <br/> |
|0,1  <br/> |Sélectionner la forme de groupe en premier.  <br/> |**visGrpSelModeGroup1st** <br/> |
|n°2  <br/> |Sélectionner les membres du groupe en premier.  <br/> |**visGrpSelModeMembers1st** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur dans la boîte de dialogue **comportement** (avec la forme groupe sélectionnée, sous l'onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , dans le groupe création de la **forme** , cliquez sur **comportement**, puis sur un mode dans la liste **sélection** sous **groupe. Comportement** ). 
  
Pour obtenir une référence à la cellule SelectMode par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |SelectMode  <br/> |
   
Pour obtenir une référence à la cellule SelectMode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowGroup** <br/> |
|Index de la cellule :  <br/> |**visGroupSelectMode** <br/> |
   

