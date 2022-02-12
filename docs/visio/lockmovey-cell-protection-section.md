---
title: LockMoveY, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm645
ms.localizationpriority: medium
ms.assetid: 4ed8cab4-112a-e96a-f4e3-02490a6f87fa
description: Verrouille la position verticale de la forme afin d'empêcher son déplacement vertical.
ms.openlocfilehash: dc79ef003eacc88cd34add33add9f17e84430d83
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62778334"
---
# <a name="lockmovey-cell-protection-section"></a>LockMoveY, cellule (section Protection)

Verrouille la position verticale de la forme afin d'empêcher son déplacement vertical.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La position verticale est verrouillée. |
| FALSE  <br/> | La position verticale n'est pas verrouillée. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LockMoveY par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockMoveY  <br/> |
   
Pour obtenir une référence à la cellule LockMoveY à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockMoveY** <br/> |
   

