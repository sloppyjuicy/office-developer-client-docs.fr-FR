---
title: IsDropTarget, cellule (section Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm495
ms.localizationpriority: medium
ms.assetid: 8140fc7b-b99c-54bb-7af3-7de6fcdae7d3
description: Détermine si le groupe accepte une forme qui y est déposée.
ms.openlocfilehash: 9e604165427e8e08768f1e8137438a1de87cc214
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598478"
---
# <a name="isdroptarget-cell-group-properties-section"></a>IsDropTarget, cellule (section Group Properties)

Détermine si le groupe accepte une forme qui y est déposée.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Il est possible d'ajouter une forme au groupe en l'y déposant.  <br/> |
|FALSE  <br/> |Il n'est pas possible d'ajouter une forme au groupe.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur en sélectionnant le groupe, en cliquant sur **Comportement** sous l’onglet [Développeur](run-in-developer-mode-display-the-developer-tab.md), puis en activant la case à cocher **Accepter les formes insérées**. 
  
Pour ajouter une forme à un groupe en l’y déposant, vous devez également activer le comportement similaire pour la forme. Sélectionnez la forme, cliquez sur **Comportement** sous l’onglet [Développeur](run-in-developer-mode-display-the-developer-tab.md), puis activez la case à cocher **Ajouter la forme aux groupes lors de l’insertion**. Cette valeur est stockée dans la cellule IsDropSource de la section Miscellaneous. 
  
Pour obtenir une référence à la cellule IsDropTarget par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |IsDropTarget  <br/> |
   
Pour obtenir une référence à la cellule IsDropTarget à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowGroup** <br/> |
|Index de la cellule :  <br/> |**visGroupIsDropTarget** <br/> |
   

