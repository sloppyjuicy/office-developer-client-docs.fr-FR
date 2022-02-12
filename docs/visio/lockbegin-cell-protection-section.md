---
title: LockBegin, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm600
ms.localizationpriority: medium
ms.assetid: cce34aba-caae-51ee-992e-92a490b68ea5
description: Verrouille le point de début (BeingX, BeginY) d'une forme 1D à un emplacement donné.
ms.openlocfilehash: 5e567f6aa7cdec73c02a502003c2d63490494603
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62788884"
---
# <a name="lockbegin-cell-protection-section"></a>LockBegin, cellule (section Protection)

Verrouille le point de début (BeingX, BeginY) d'une forme 1D à un emplacement donné.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Le point de début est verrouillé. |
| FALSE  <br/> | Le point de début n'est pas verrouillé. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LockBegin par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockBegin  <br/> |
   
Pour obtenir une référence à la cellule LockBegin à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockBegin** <br/> |
   

