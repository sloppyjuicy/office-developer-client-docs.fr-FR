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
ms.openlocfilehash: 099f6597656d4389476818253f34e741ddd404de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432085"
---
# <a name="lockheight-cell-protection-section"></a>LockHeight, cellule (section Protection)

Verrouille la hauteur d'une forme afin qu'elle demeure intacte lorsque la forme est redimensionnée.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La hauteur est verrouillée.  <br/> |
| FALSE  <br/> | La hauteur n'est pas verrouillée.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LockHeight par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockHeight  <br/> |
   
Pour obtenir une référence à la cellule LockHeight à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockHeight** <br/> |
   

