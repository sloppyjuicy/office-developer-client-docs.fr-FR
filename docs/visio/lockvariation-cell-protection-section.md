---
title: LockVariation Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: Détermine si la variante de thème appliquée à la page ou à la forme peut être modifiée, en tant que booléen.
ms.openlocfilehash: 348277631d2e4737e3543b21db6fcb8f8d85dde3
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62771228"
---
# <a name="lockvariation-cell-protection-section"></a>LockVariation Cell (Protection Section)

Détermine si la variante de thème appliquée à la page ou à la forme peut être modifiée, en tant que booléen.
  
|||
|:-----|:-----|
|TRUE  <br/> |La variante actuelle appliquée à la page ou à la forme ne peut pas être modifiée. |
|FALSE  <br/> |La variante de la page ou de la forme peut être modifiée. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **LockVariation** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | LockVariation  <br/> |
   
Pour obtenir une référence à la cellule **LockVariation** à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockVariation** <br/> |
   

