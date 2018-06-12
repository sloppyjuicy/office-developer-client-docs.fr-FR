---
title: LockMoveX, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm640
localization_priority: Normal
ms.assetid: 48ceeeed-66ae-a81f-2aee-f0010102dfb7
description: Verrouille la position horizontale de la forme afin d'empêcher son déplacement horizontal.
ms.openlocfilehash: 981f4f417e48f70d0693e30683c4351d0e53a758
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789023"
---
# <a name="lockmovex-cell-protection-section"></a>LockMoveX, cellule (section Protection)

Verrouille la position horizontale de la forme afin d'empêcher son déplacement horizontal.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La position horizontale est verrouillée.  <br/> |
| FALSE  <br/> | La position horizontale n'est pas verrouillée.  <br/> |
   
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule LockMoveX par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockMoveX  <br/> |
   
Pour obtenir une référence à la cellule LockMoveX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockMoveX** <br/> |
   

