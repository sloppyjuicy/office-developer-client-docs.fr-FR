---
title: LockSelect, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm660
localization_priority: Normal
ms.assetid: c96b45a5-719e-8c4b-71b9-cb2224d83e21
description: Empêche la sélection d'une forme.
ms.openlocfilehash: c9f762f390dbea1e4ff2bd5bcf9566b8c67df11f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360668"
---
# <a name="lockselect-cell-protection-section"></a>LockSelect, cellule (section Protection)

Empêche la sélection d'une forme.
  
|**Value**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La forme ne peut pas être sélectionnée.  <br/> |
| FALSE  <br/> | La forme peut être sélectionnée.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour que l'effet de LockSelect s'applique, la case **Formes** doit être activée dans la boîte de dialogue **Protéger le document**. 
  
Pour obtenir une référence à la cellule LockSelect par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockSelect  <br/> |
   
Pour obtenir une référence à la cellule LockSelect à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockSelect** <br/> |
   

