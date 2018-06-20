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
ms.openlocfilehash: f2edfcb7cf9d21b2ecd97b335b07f30233903d5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788847"
---
# <a name="isdropsource-cell-miscellaneous-section"></a>IsDropSource, cellule (section Miscellaneous)

Détermine si la forme peut être ajoutée à un groupe en la faisant glisser sur ce groupe.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |La forme peut être ajoutée à un groupe par glisser-déposer sur ce groupe.  <br/> |
|FALSE  <br/> |La forme ne peut être ajoutée au groupe.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur en sélectionnant la forme, en cliquant sur **comportement** sous l’onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , puis activez la case à cocher **Ajouter la forme aux groupes lors de l’insertion** . 
  
Outre l’activation de ce comportement pour une forme, vous devez également activer un groupe d’accepter les formes qui sont déplacés dans celui-ci. Pour ce faire, sélectionnez le groupe, cliquez sur **comportement** sous l’onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , puis activez la case à cocher **accepter les formes insérées** . Cette valeur est stockée dans la cellule IsDropTarget dans la section Propriétés du groupe. 
  
Pour obtenir une référence à la cellule IsDropSource par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |IsDropSource  <br/> |
   
Pour obtenir une référence à la cellule IsDropSource par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowMisc** <br/> |
|Index de la cellule :  <br/> |**visDropSource** <br/> |
   

