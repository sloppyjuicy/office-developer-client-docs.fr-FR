---
title: LockHeight, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm635
localization_priority: Normal
ms.assetid: 218b957e-5af6-e53b-1453-a84164ae456e
description: Verrouille la hauteur d'une forme afin qu'elle demeure intacte lorsque la forme est redimensionnée.
ms.openlocfilehash: f6afe6037ff3d0810cc532bbc18bb749ee589bb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789006"
---
# <a name="lockheight-cell-protection-section"></a>LockHeight, cellule (section Protection)

Verrouille la hauteur d'une forme afin qu'elle demeure intacte lorsque la forme est redimensionnée.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La hauteur est verrouillée.  <br/> |
| FALSE  <br/> | La hauteur n'est pas verrouillée.  <br/> |
   
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule LockHeight par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockHeight  <br/> |
   
Pour obtenir une référence à la cellule LockHeight par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockHeight** <br/> |
   

