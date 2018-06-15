---
title: LockVtxEdit, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251224
localization_priority: Normal
ms.assetid: 966cde5c-f04e-7149-3660-720ffa4f7079
description: Verrouille les sommets d’une forme afin d’empêcher leur modification.
ms.openlocfilehash: 3766df62bb85e1470ad0fa46274b9bbbd96b8406
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19789039"
---
# <a name="lockvtxedit-cell-protection-section"></a>LockVtxEdit, cellule (section Protection)

Verrouille les sommets d’une forme afin d’empêcher leur modification.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Les sommets ne peuvent pas être modifiés.  <br/> |
|FALSE  <br/> |Les sommets peuvent être modifiés.  <br/> |
   
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule LockVtxEdit par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |LockVtxEdit  <br/> |
   
Pour obtenir une référence à la cellule LockVtxEdit par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowLock** <br/> |
|Index de la cellule :  <br/> |**visLockVtxEdit** <br/> |
   

