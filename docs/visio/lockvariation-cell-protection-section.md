---
title: LockVariation Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: Détermine si la variante de thème appliquée à la page ou à la forme peut être modifiée, en tant que valeur booléenne.
ms.openlocfilehash: 69c991e3da7a96d6c59dc825dfb78fdad3d432e7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358064"
---
# <a name="lockvariation-cell-protection-section"></a>LockVariation Cell (Protection Section)

Détermine si la variante de thème appliquée à la page ou à la forme peut être modifiée, en tant que valeur booléenne.
  
|||
|:-----|:-----|
|TRUE  <br/> |La variante actuelle appliquée à la page ou à la forme ne peut pas être modifiée.  <br/> |
|FALSE  <br/> |La variante de la page ou de la forme peut être modifiée.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **LockVariation** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez: 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | LockVariation  <br/> |
   
Pour obtenir une référence à la cellule **LockVariation** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants: 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockVariation** <br/> |
   

