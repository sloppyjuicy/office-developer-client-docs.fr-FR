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
ms.openlocfilehash: abdcc0d5285e98e5856524925a41c4f72ee7f6ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789031"
---
# <a name="lockwidth-cell-protection-section"></a>LockWidth, cellule (section Protection)

Verrouille la largeur d'une forme afin qu'elle demeure intacte lorsque la forme est dimensionnée.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La largeur est verrouillée.  <br/> |
| FALSE  <br/> | La largeur n'est pas verrouillée.  <br/> |
   
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule LockWidth par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockWidth  <br/> |
   
Pour obtenir une référence à la cellule LockWidth par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockWidth** <br/> |
   

