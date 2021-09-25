---
title: LockDelete, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251219
ms.localizationpriority: medium
ms.assetid: 596c62b7-8d42-1854-d709-592db09a6a84
description: Verrouille la forme afin d'empêcher sa suppression.
ms.openlocfilehash: dc746ae96dc5f8d359b1f7500b59fdbe7d7d86f8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554466"
---
# <a name="lockdelete-cell-protection-section"></a>LockDelete, cellule (section Protection)

Verrouille la forme afin d'empêcher sa suppression.
  
|**Valeur**|**Description**|
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
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockDelete** <br/> |
   

