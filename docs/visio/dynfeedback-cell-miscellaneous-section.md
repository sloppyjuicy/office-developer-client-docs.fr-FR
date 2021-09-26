---
title: DynFeedback, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251317
ms.localizationpriority: medium
ms.assetid: 44017319-7146-3431-e476-fbb1a40341ca
description: Modifie l'aspect que prend un connecteur lorsqu'il est glissé sur la page de dessin. Lorsque le bouton de la souris est relâché, la forme du connecteur qui en résulte n'est pas affectée par ce paramètre. Ce réglage ne s'applique pas aux connecteurs repositionnables.
ms.openlocfilehash: cc4f9d66cf06150f749cef28a83d212f232d866d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619119"
---
# <a name="dynfeedback-cell-miscellaneous-section"></a>DynFeedback, cellule (section Miscellaneous)

Modifie l'aspect que prend un connecteur lorsqu'il est glissé sur la page de dessin. Lorsque le bouton de la souris est relâché, la forme du connecteur qui en résulte n'est pas affectée par ce paramètre. Ce réglage ne s'applique pas aux connecteurs repositionnables.
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Reste droit (aucune branche)  <br/> |**visDynFBDefault** <br/> |
| 1  <br/> | Affiche trois branches lors du déplacement.  <br/> |**visDynFBUCon3Leg** <br/> |
| 2  <br/> | Affiche cinq branches lors du déplacement.  <br/> |**visDynFBUCon5Leg** <br/> |
   
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
   

