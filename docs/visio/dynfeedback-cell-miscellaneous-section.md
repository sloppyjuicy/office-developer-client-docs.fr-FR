---
title: DynFeedback, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251317
localization_priority: Normal
ms.assetid: 44017319-7146-3431-e476-fbb1a40341ca
description: Modifie l'aspect que prend un connecteur lorsqu'il est glissé sur la page de dessin. Lorsque le bouton de la souris est relâché, la forme du connecteur qui en résulte n'est pas affectée par ce paramètre. Ce réglage ne s'applique pas aux connecteurs repositionnables.
ms.openlocfilehash: 823b8db4dc6afe94a5fdac1f62aaa48d7e1b0d80
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404798"
---
# <a name="dynfeedback-cell-miscellaneous-section"></a>DynFeedback, cellule (section Miscellaneous)

Modifie l'aspect que prend un connecteur lorsqu'il est glissé sur la page de dessin. Lorsque le bouton de la souris est relâché, la forme du connecteur qui en résulte n'est pas affectée par ce paramètre. Ce réglage ne s'applique pas aux connecteurs repositionnables.
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Reste droit (aucune branche)  <br/> |**visDynFBDefault** <br/> |
| 1   <br/> | Affiche trois branches lors du déplacement.  <br/> |**visDynFBUCon3Leg** <br/> |
| 2   <br/> | Affiche cinq branches lors du déplacement.  <br/> |**visDynFBUCon5Leg** <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule DynFeedback par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | DynFeedback  <br/> |
   
Pour obtenir une référence à la cellule DynFeedback à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowMisc** <br/> |
| Index de la cellule :  <br/> |**visDynFeedback** <br/> |
   

