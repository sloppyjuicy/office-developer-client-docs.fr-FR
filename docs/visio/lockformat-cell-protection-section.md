---
title: LockFormat, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm625
ms.localizationpriority: medium
ms.assetid: e9a640f4-0af0-317c-b77b-f32c651e87b4
description: Verrouille la mise en forme d'une forme afin d'empêcher sa modification.
ms.openlocfilehash: cbc0af1032a25a4939cbf16bb0586cf18a119cf6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603626"
---
# <a name="lockformat-cell-protection-section"></a>LockFormat, cellule (section Protection)

Verrouille la mise en forme d'une forme afin d'empêcher sa modification.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La mise en forme ne peut pas être modifiée.  <br/> |
| FALSE  <br/> | La mise en forme peut être modifiée.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LockFormat par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockFormat  <br/> |
   
Pour obtenir une référence à la cellule LockFormat à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockFormat** <br/> |
   

