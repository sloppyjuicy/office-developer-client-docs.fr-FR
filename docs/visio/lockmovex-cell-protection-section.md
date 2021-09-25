---
title: LockMoveX, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm640
ms.localizationpriority: medium
ms.assetid: 48ceeeed-66ae-a81f-2aee-f0010102dfb7
description: Verrouille la position horizontale de la forme afin d'empêcher son déplacement horizontal.
ms.openlocfilehash: d42e146028854085ffc9a312ef99018ccd27ad3a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603619"
---
# <a name="lockmovex-cell-protection-section"></a>LockMoveX, cellule (section Protection)

Verrouille la position horizontale de la forme afin d'empêcher son déplacement horizontal.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La position horizontale est verrouillée.  <br/> |
| FALSE  <br/> | La position horizontale n'est pas verrouillée.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LockMoveX par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockMoveX  <br/> |
   
Pour obtenir une référence à la cellule LockMoveX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockMoveX** <br/> |
   

