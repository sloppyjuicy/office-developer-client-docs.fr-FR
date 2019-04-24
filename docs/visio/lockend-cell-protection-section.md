---
title: LockEnd, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm620
localization_priority: Normal
ms.assetid: e9742142-4d34-1ba9-480e-d1ecff4fc7cd
description: Verrouille le point de fin (EndX, EndY) d'une forme 1D à un emplacement donné.
ms.openlocfilehash: d9fe0372c44fe3b029a4d06056c8d3871c3f91e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359597"
---
# <a name="lockend-cell-protection-section"></a>LockEnd, cellule (section Protection)

Verrouille le point de fin (EndX, EndY) d'une forme 1D à un emplacement donné.
  
|**Value**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Le point de fin est verrouillé.  <br/> |
| FALSE  <br/> | Le point de fin n'est pas verrouillé.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LockEnd par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockEnd  <br/> |
   
Pour obtenir une référence à la cellule LockEnd à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockEnd** <br/> |
   

