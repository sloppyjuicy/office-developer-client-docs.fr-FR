---
title: LockVtxEdit, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251224
ms.localizationpriority: medium
ms.assetid: 966cde5c-f04e-7149-3660-720ffa4f7079
description: Verrouille les sommets d’une forme afin d’empêcher leur modification.
ms.openlocfilehash: 0ac81dfabc9632bf8ae8c3d2b261b2ea0e5956c0
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63507268"
---
# <a name="lockvtxedit-cell-protection-section"></a>LockVtxEdit, cellule (section Protection)

Verrouille les sommets d’une forme afin d’empêcher leur modification.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Les sommets ne peuvent pas être modifiés. |
|FALSE  <br/> |Les sommets peuvent être modifiés. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LockVtxEdit par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |LockVtxEdit  <br/> |
   
Pour obtenir une référence à la cellule LockVtxEdit à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowLock** <br/> |
|**Index de la cellule :**  <br/> |**visLockVtxEdit** <br/> |
   

