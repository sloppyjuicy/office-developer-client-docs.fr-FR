---
title: LockThemeIndex Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: Empêche toute modification de la cellule ThemeIndex dans la ligne Propriétés du thème en appliquant un nouveau thème ou en sélectionnant un nouveau modèle de connecteur. N’empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet.
ms.openlocfilehash: 94e84a3ff0d2178a3151dc45cd6998083844196e
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62775530"
---
# <a name="lockthemeindex-cell-protection-section"></a>LockThemeIndex Cell (Protection Section)

Empêche toute **modification de la cellule ThemeIndex** dans la ligne **Propriétés** du thème en appliquant un nouveau thème ou en sélectionnant un nouveau modèle de connecteur. N’empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |La **cellule ThemeIndex** ne peut pas être modifiée par rapport à sa valeur actuelle, sauf si elle est modifiée directement dans la feuille ShapeSheet. |
|FALSE  <br/> |La **cellule ThemeIndex** peut être modifiée par rapport à sa valeur actuelle lorsque le thème est modifié. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **LockThemeIndex** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | LockThemeIndex  <br/> |
   
Pour obtenir une référence à la **cellule LockThemeIndex** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockThemeIndex** <br/> |
   

