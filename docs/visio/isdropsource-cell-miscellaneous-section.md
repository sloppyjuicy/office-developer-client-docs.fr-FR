---
title: IsDropSource, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm490
localization_priority: Normal
ms.assetid: 3b20e6ef-f1ac-5bb0-5ac3-4df3ae5e9bf9
description: Détermine si la forme peut être ajoutée à un groupe en la faisant glisser sur ce groupe.
ms.openlocfilehash: e8cb02a66f745530f12c7c8be56b9bdd771121b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360171"
---
# <a name="isdropsource-cell-miscellaneous-section"></a>IsDropSource, cellule (section Miscellaneous)

Détermine si la forme peut être ajoutée à un groupe en la faisant glisser sur ce groupe.
  
|**Value**|**Description**|
|:-----|:-----|
|TRUE  <br/> |La forme peut être ajoutée à un groupe par glisser-déposer sur ce groupe.  <br/> |
|FALSE  <br/> |La forme ne peut être ajoutée au groupe.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur en sélectionnant la forme, en cliquant sur **Comportement** sous l’onglet [Développeur](run-in-developer-mode-display-the-developer-tab.md), puis en cochant la case **Ajouter la forme aux groupes lors de l’insertion**. 
  
Outre l’activation de ce comportement pour la forme, vous devez également activer un groupe pour accepter d’y déposer des formes. Pour ce faire, sélectionnez le groupe, cliquez sur **Comportement** sous l’onglet [Développeur](run-in-developer-mode-display-the-developer-tab.md), puis activez la case à cocher **Accepter les formes insérées**. Cette valeur est stockée dans la cellule IsDropTarget de la section Group Properties. 
  
Pour obtenir une référence à la cellule IsDropSource par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |IsDropSource  <br/> |
   
Pour obtenir une référence à la cellule IsDropSource à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowMisc** <br/> |
|Index de la cellule :  <br/> |**visDropSource** <br/> |
   

