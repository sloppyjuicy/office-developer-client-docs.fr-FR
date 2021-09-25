---
title: LockWidth, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm675
ms.localizationpriority: medium
ms.assetid: fef022ea-38ab-2b66-60c8-b94a6b0bdfbf
description: Verrouille la largeur d'une forme afin qu'elle demeure intacte lorsque la forme est dimensionnée.
ms.openlocfilehash: 5e3b05fb7cda925c5d1c4e2942c665d55190cc7d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582560"
---
# <a name="lockwidth-cell-protection-section"></a>LockWidth, cellule (section Protection)

Verrouille la largeur d'une forme afin qu'elle demeure intacte lorsque la forme est dimensionnée.
  
|**Valeur**|**Description**|
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
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockWidth** <br/> |
   

