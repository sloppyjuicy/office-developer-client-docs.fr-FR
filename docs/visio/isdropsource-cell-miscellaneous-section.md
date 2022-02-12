---
title: IsDropSource, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm490
ms.localizationpriority: medium
ms.assetid: 3b20e6ef-f1ac-5bb0-5ac3-4df3ae5e9bf9
description: Détermine si la forme peut être ajoutée à un groupe en la faisant glisser sur ce groupe.
ms.openlocfilehash: 81f006319a9712daa07e29a21b78ea1aad4ed237
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62775688"
---
# <a name="isdropsource-cell-miscellaneous-section"></a>IsDropSource, cellule (section Miscellaneous)

Détermine si la forme peut être ajoutée à un groupe en la faisant glisser sur ce groupe.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |La forme peut être ajoutée à un groupe par glisser-déposer sur ce groupe. |
|FALSE  <br/> |La forme ne peut être ajoutée au groupe. |
   
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
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowMisc** <br/> |
|Index de la cellule :  <br/> |**visDropSource** <br/> |
   

