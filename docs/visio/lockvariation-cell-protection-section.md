---
title: LockVariation Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: Détermine si la variante de thème appliquée à la page ou à la forme peut être modifiée, en tant que booléen.
ms.openlocfilehash: eac661fd88e53fa42999ba5e1e23af8bc113e4bf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573921"
---
# <a name="lockvariation-cell-protection-section"></a>LockVariation Cell (Protection Section)

Détermine si la variante de thème appliquée à la page ou à la forme peut être modifiée, en tant que booléen.
  
|||
|:-----|:-----|
|TRUE  <br/> |La variante actuelle appliquée à la page ou à la forme ne peut pas être modifiée.  <br/> |
|FALSE  <br/> |La variante de la page ou de la forme peut être modifiée.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **LockVariation** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | LockVariation  <br/> |
   
Pour obtenir une référence à la cellule **LockVariation** à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockVariation** <br/> |
   

