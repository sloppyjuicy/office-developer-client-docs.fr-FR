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
ms.openlocfilehash: c89708ffa02a2c0a55e9d869299bb73848c18405
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63522687"
---
# <a name="lockmovex-cell-protection-section"></a>LockMoveX, cellule (section Protection)

Verrouille la position horizontale de la forme afin d'empêcher son déplacement horizontal.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La position horizontale est verrouillée. |
| FALSE  <br/> | La position horizontale n'est pas verrouillée. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LockMoveX par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | LockMoveX  <br/> |
   
Pour obtenir une référence à la cellule LockMoveX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowLock** <br/> |
| **Index de la cellule :**  <br/> |**visLockMoveX** <br/> |
   

