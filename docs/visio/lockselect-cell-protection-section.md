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
ms.openlocfilehash: 082e993f7773640f59022c46458563d491197908
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19789026"
---
# <a name="lockselect-cell-protection-section"></a>LockSelect, cellule (section Protection)

Empêche la sélection d'une forme.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La forme ne peut pas être sélectionnée.  <br/> |
| FALSE  <br/> | La forme peut être sélectionnée.  <br/> |
   
## <a name="remarks"></a>Note

Dans l’ordre pour que l’effet de LockSelect, la case **formes** doit être sélectionnée dans la boîte de dialogue **Protéger le Document** . 
  
Pour obtenir une référence à la cellule LockSelect par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockSelect  <br/> |
   
Pour obtenir une référence à la cellule LockSelect par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockSelect** <br/> |
   

