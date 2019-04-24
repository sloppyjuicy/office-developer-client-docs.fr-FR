---
title: LockThemeFonts Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: Empêche la cellule FontIndex de la ligne propriétés de thème d'être modifiée en appliquant un nouveau thème. N'empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet.
ms.openlocfilehash: b3bd21c1dcd8c8c13d843c50cb29edcc5b8c4999
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358092"
---
# <a name="lockthemefonts-cell-protection-section"></a>LockThemeFonts Cell (Protection Section)

Empêche la cellule **FontIndex** de la ligne **Propriétés de thème** d'être modifiée en appliquant un nouveau thème. N'empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet. 
  
|**Value**|**Description**|
|:-----|:-----|
|TRUE  <br/> |La cellule **FontIndex** ne peut pas être modifiée à partir de sa valeur actuelle sauf si elle a été modifiée directement dans la feuille ShapeSheet.  <br/> |
|FALSE  <br/> |La cellule **FontIndex** peut être modifiée à partir de sa valeur actuelle lorsque le thème est modifié.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **LockThemeFonts** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez: 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | LockThemeFonts  <br/> |
   
Pour obtenir une référence à la cellule **LockThemeFonts** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants: 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockThemeFonts** <br/> |
   

