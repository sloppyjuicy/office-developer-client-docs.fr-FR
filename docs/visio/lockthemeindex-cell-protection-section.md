---
title: LockThemeIndex, cellule (Section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: ThemeIndex cellule dans la ligne de propriétés de thème empêche la modification en appliquant un nouveau thème ou en sélectionnant un nouveau jeu de connecteur. N’empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet.
ms.openlocfilehash: 4bef3eb799c943ff89027e69ae8580c9c0e51243
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789027"
---
# <a name="lockthemeindex-cell-protection-section"></a>LockThemeIndex, cellule (Section Protection)

**ThemeIndex** cellule dans la ligne de **Propriétés de thème** empêche la modification en appliquant un nouveau thème ou en sélectionnant un nouveau jeu de connecteur. N’empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |La cellule **ThemeIndex** ne peut pas être modifiée de sa valeur actuelle, sauf si la modification directement dans la feuille ShapeSheet.  <br/> |
|FALSE  <br/> |La cellule **ThemeIndex** peut être modifiée à partir de sa valeur actuelle lorsque le thème est modifié.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **LockThemeIndex** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockThemeIndex  <br/> |
   
Pour obtenir une référence à la cellule **LockThemeIndex** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockThemeIndex** <br/> |
   

