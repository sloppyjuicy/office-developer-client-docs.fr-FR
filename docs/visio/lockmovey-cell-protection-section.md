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
ms.openlocfilehash: e3e8b2e95d966e94f9a211dc082ace722674f2d6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627974"
---
# <a name="lockmovey-cell-protection-section"></a>LockMoveY, cellule (section Protection)

Verrouille la position verticale de la forme afin d'empêcher son déplacement vertical.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La position verticale est verrouillée.  <br/> |
| FALSE  <br/> | La position verticale n'est pas verrouillée.  <br/> |
   
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
   

