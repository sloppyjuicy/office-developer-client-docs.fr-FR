---
title: LockMoveY, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm645
localization_priority: Normal
ms.assetid: 4ed8cab4-112a-e96a-f4e3-02490a6f87fa
description: Verrouille la position verticale de la forme afin d'empêcher son déplacement vertical.
ms.openlocfilehash: 24f6f477860ea3634cfdcfd92199f2de65e543db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789005"
---
# <a name="lockmovey-cell-protection-section"></a>LockMoveY, cellule (section Protection)

Verrouille la position verticale de la forme afin d'empêcher son déplacement vertical.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La position verticale est verrouillée.  <br/> |
| FALSE  <br/> | La position verticale n'est pas verrouillée.  <br/> |
   
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule LockMoveY par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockMoveY  <br/> |
   
Pour obtenir une référence à la cellule LockMoveY par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockMoveY** <br/> |
   

