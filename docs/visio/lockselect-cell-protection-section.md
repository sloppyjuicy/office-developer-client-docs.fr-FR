---
title: LockSelect, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm660
ms.localizationpriority: medium
ms.assetid: c96b45a5-719e-8c4b-71b9-cb2224d83e21
description: Empêche la sélection d'une forme.
ms.openlocfilehash: 98a0f8151cf2b5b0c08c7a86aec87b8121a9ccb5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573949"
---
# <a name="lockselect-cell-protection-section"></a>LockSelect, cellule (section Protection)

Empêche la sélection d'une forme.
  
|**Valeur**|**Description**|
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
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockSelect** <br/> |
   

