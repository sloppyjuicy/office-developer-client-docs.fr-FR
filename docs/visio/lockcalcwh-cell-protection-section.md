---
title: LockCalcWH, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm605
localization_priority: Normal
ms.assetid: 6eb51e5a-03d8-3daa-b4e1-6107d540aed9
description: Verrouille un rectangle de sélection de la forme de sorte qu'elle ne puisse pas être recalculée lorsqu'un sommet est modifié ou que le type d'une ligne est changé dans la section Geometry.
ms.openlocfilehash: f7f9c99eb4978e9b32968d3076b0341efe42faa6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788988"
---
# <a name="lockcalcwh-cell-protection-section"></a>LockCalcWH, cellule (section Protection)

Verrouille un rectangle de sélection de la forme de sorte qu'elle ne puisse pas être recalculée lorsqu'un sommet est modifié ou que le type d'une ligne est changé dans la section Geometry.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La largeur et la hauteur ne peuvent pas être recalculées.  <br/> |
| FALSE  <br/> | La largeur et la hauteur peuvent être recalculées.  <br/> |
   
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule LockCalcWH par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockCalcWH  <br/> |
   
Pour obtenir une référence à la cellule LockCalcWH par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockCalcWH** <br/> |
   

