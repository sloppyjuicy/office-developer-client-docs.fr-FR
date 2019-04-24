---
title: LockWidth, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm675
localization_priority: Normal
ms.assetid: fef022ea-38ab-2b66-60c8-b94a6b0bdfbf
description: Verrouille la largeur d'une forme afin qu'elle demeure intacte lorsque la forme est dimensionnée.
ms.openlocfilehash: 84c89b5f264c00d6fe5f95cb27eae74b91b88dc3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314832"
---
# <a name="lockwidth-cell-protection-section"></a>LockWidth, cellule (section Protection)

Verrouille la largeur d'une forme afin qu'elle demeure intacte lorsque la forme est dimensionnée.
  
|**Value**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La largeur est verrouillée.  <br/> |
| FALSE  <br/> | La largeur n'est pas verrouillée.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LockWidth par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockWidth  <br/> |
   
Pour obtenir une référence à la cellule LockWidth à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockWidth** <br/> |
   

