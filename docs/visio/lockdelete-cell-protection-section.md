---
title: LockDelete, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251219
localization_priority: Normal
ms.assetid: 596c62b7-8d42-1854-d709-592db09a6a84
description: Verrouille la forme afin d'empêcher sa suppression.
ms.openlocfilehash: 0819969c9ba17a52de19341b359b33ceae5b44d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359618"
---
# <a name="lockdelete-cell-protection-section"></a>LockDelete, cellule (section Protection)

Verrouille la forme afin d'empêcher sa suppression.
  
|**Value**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La forme ne peut pas être supprimée.  <br/> |
| FALSE  <br/> | La forme peut être supprimée.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LockDelete par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockDelete  <br/> |
   
Pour obtenir une référence à la cellule LockDelete à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockDelete** <br/> |
   

