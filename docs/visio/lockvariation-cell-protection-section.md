---
title: LockVariation, cellule (Section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: Détermine si la variante de thème appliquée à la page ou la forme peut être modifiée en tant que valeur de type Boolean.
ms.openlocfilehash: c3c272a637f28aa4df43f6c23030d6676280138e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789041"
---
# <a name="lockvariation-cell-protection-section"></a>LockVariation, cellule (Section Protection)

Détermine si la variante de thème appliquée à la page ou la forme peut être modifiée en tant que valeur de type Boolean.
  
|||
|:-----|:-----|
|TRUE  <br/> |La variation actuelle appliquée à la page ou la forme ne peut pas être modifiée.  <br/> |
|FALSE  <br/> |La variation de la page ou la forme peut être modifiée.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **LockVariation** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockVariation  <br/> |
   
Pour obtenir une référence à la cellule **LockVariation** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockVariation** <br/> |
   

