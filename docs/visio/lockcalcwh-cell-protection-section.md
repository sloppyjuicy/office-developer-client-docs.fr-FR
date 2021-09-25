---
title: LockCalcWH, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm605
ms.localizationpriority: medium
ms.assetid: 6eb51e5a-03d8-3daa-b4e1-6107d540aed9
description: Verrouille un rectangle de sélection de la forme de sorte qu'elle ne puisse pas être recalculée lorsqu'un sommet est modifié ou que le type d'une ligne est changé dans la section Geometry.
ms.openlocfilehash: 4d9c6645640c2c53e086cbee384d103421945a72
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603647"
---
# <a name="lockcalcwh-cell-protection-section"></a>LockCalcWH, cellule (section Protection)

Verrouille un rectangle de sélection de la forme de sorte qu'elle ne puisse pas être recalculée lorsqu'un sommet est modifié ou que le type d'une ligne est changé dans la section Geometry.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La largeur et la hauteur ne peuvent pas être recalculées.  <br/> |
| FALSE  <br/> | La largeur et la hauteur peuvent être recalculées.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LockCalcWH par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockCalcWH  <br/> |
   
Pour obtenir une référence à la cellule LockCalcWH à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockCalcWH** <br/> |
   

