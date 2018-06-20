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
ms.openlocfilehash: 426b4a18bbd54887e4f60b92860a6c3846386671
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789609"
---
# <a name="selectmode-cell-group-properties-section"></a>SelectMode, cellule (section Group Properties)

Détermine le mode de sélection d'une forme de groupe et de ses membres.
  
|**Valeur**|**Mode de sélection**|**Constante d’Automation**|
|:-----|:-----|:-----|
|0  <br/> |Sélectionner uniquement la forme de groupe.  <br/> |**visGrpSelModeGroupOnly** <br/> |
|1  <br/> |Sélectionner la forme de groupe en premier.  <br/> |**visGrpSelModeGroup1st** <br/> |
|2  <br/> |Sélectionner les membres du groupe en premier.  <br/> |**visGrpSelModeMembers1st** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur dans la boîte de dialogue **comportement** (avec la forme de groupe, sous l’onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , dans le groupe **Création de la forme** , cliquez sur **comportement**, puis cliquez sur un mode dans la liste de **sélection** sous **de groupe Comportement** ). 
  
Pour obtenir une référence à la cellule SelectMode par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |SelectMode  <br/> |
   
Pour obtenir une référence à la cellule SelectMode par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowGroup** <br/> |
|Index de la cellule :  <br/> |**visGroupSelectMode** <br/> |
   

