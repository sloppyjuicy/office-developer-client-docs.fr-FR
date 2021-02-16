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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435361"
---
# <a name="selectmode-cell-group-properties-section"></a>SelectMode, cellule (section Group Properties)

Détermine le mode de sélection d'une forme de groupe et de ses membres.
  
|**Valeur**|**Mode de sélection**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Sélectionner uniquement la forme de groupe.  <br/> |**visGrpSelModeGroupOnly** <br/> |
|1   <br/> |Sélectionner la forme de groupe en premier.  <br/> |**visGrpSelModeGroup1st** <br/> |
|2   <br/> |Sélectionner les membres du groupe en premier.  <br/> |**visGrpSelModeMembers1st** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir  cette valeur dans la boîte de dialogue [](run-in-developer-mode-display-the-developer-tab.md) Comportement (avec la forme de groupe sélectionnée, sous  l’onglet Développeur, dans le groupe Création de formes, cliquez sur **Comportement,** puis cliquez sur un mode dans la liste Sélection sous Comportement du  **groupe).** 
  
Pour obtenir une référence à la cellule SelectMode par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |SelectMode  <br/> |
   
Pour obtenir une référence à la cellule SelectMode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowGroup** <br/> |
|Index de la cellule :  <br/> |**visGroupSelectMode** <br/> |
   

