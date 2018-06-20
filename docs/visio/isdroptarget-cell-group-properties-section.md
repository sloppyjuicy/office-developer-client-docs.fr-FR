---
title: IsDropTarget, cellule (section Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm495
localization_priority: Normal
ms.assetid: 8140fc7b-b99c-54bb-7af3-7de6fcdae7d3
description: Détermine si le groupe accepte une forme qui y est déposée.
ms.openlocfilehash: 326ead15bcdc72797853daee797d8f08d459a638
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788857"
---
# <a name="isdroptarget-cell-group-properties-section"></a>IsDropTarget, cellule (section Group Properties)

Détermine si le groupe accepte une forme qui y est déposée.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Il est possible d'ajouter une forme au groupe en l'y déposant.  <br/> |
|FALSE  <br/> |Il n'est pas possible d'ajouter une forme au groupe.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur en sélectionnant le groupe, en cliquant sur **comportement** sous l’onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , puis activez la case à cocher **accepter les formes insérées** . 
  
Pour ajouter une forme à un groupe en la faisant glisser sur le groupe, vous devez également activer le comportement de forme similaire. Vous devez sélectionner la forme et cliquez sur **comportement** sous l’onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , puis activez la case à cocher **Ajouter la forme aux groupes lors de l’insertion** . Cette valeur est stockée dans la cellule IsDropSource de la section Miscellaneous. 
  
Pour obtenir une référence à la cellule IsDropTarget par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |IsDropTarget  <br/> |
   
Pour obtenir une référence à la cellule IsDropTarget par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowGroup** <br/> |
|Index de la cellule :  <br/> |**visGroupIsDropTarget** <br/> |
   

