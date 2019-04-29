---
title: LockFormat, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm625
localization_priority: Normal
ms.assetid: e9a640f4-0af0-317c-b77b-f32c651e87b4
description: Verrouille la mise en forme d'une forme afin d'empêcher sa modification.
ms.openlocfilehash: e0d1bb8a65b8087136e57bb46ad9f5363da30030
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409677"
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
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockFormat** <br/> |
   

