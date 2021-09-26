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
ms.openlocfilehash: ca90a85a327f9f51380957bcdd3fd5c3ff4a6d36
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612469"
---
# <a name="lockvtxedit-cell-protection-section"></a>LockVtxEdit, cellule (section Protection)

Verrouille les sommets d’une forme afin d’empêcher leur modification.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Les sommets ne peuvent pas être modifiés.  <br/> |
|FALSE  <br/> |Les sommets peuvent être modifiés.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LockVtxEdit par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |LockVtxEdit  <br/> |
   
Pour obtenir une référence à la cellule LockVtxEdit à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowLock** <br/> |
|Index de la cellule :  <br/> |**visLockVtxEdit** <br/> |
   

