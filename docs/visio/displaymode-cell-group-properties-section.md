---
title: DisplayMode, cellule (section Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251623
localization_priority: Normal
ms.assetid: e6d72529-aa03-e94b-130c-79ed04336299
description: Détermine le mode d'affichage de la forme de groupe et de ses membres.
ms.openlocfilehash: a49d7a38eac75a2845de0ca3ad22f7cbf79a63df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332710"
---
# <a name="displaymode-cell-group-properties-section"></a>DisplayMode, cellule (section Group Properties)

Détermine le mode d'affichage de la forme de groupe et de ses membres.
  
|**Valeur**|**Mode d'affichage**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Masque la forme de groupe et le texte  <br/> |**visGrpDispModeNone** <br/> |
|0,1  <br/> |Affiche la forme de groupe derrière ses membres  <br/> |**visGrpDispModeBack** <br/> |
|n°2  <br/> |Affiche la forme de groupe devant ses membres  <br/> |**visGrpDispModeFront** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur en sélectionnant le groupe, en cliquant sur **comportement** dans le groupe **création** de la forme sous l'onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , puis en sélectionnant un mode d'affichage dans la liste **données de groupe** . 
  
Pour obtenir une référence à la cellule DisplayMode par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |DisplayMode  <br/> |
   
Pour obtenir une référence à la cellule DisplayMode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowGroup** <br/> |
|Index de la cellule :  <br/> |**visGroupDisplayMode** <br/> |
   

