---
title: LockThemeFonts, cellule (Section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: Empêche la cellule FontIndex dans la ligne de propriétés de thème de modification en appliquant un nouveau thème. N’empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet.
ms.openlocfilehash: b90ffe4c5555df017bb0506a78351514c954ec39
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789045"
---
# <a name="lockthemefonts-cell-protection-section"></a>LockThemeFonts, cellule (Section Protection)

Empêche la cellule **FontIndex** dans la ligne de **Propriétés de thème** de modification en appliquant un nouveau thème. N’empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |La cellule **FontIndex** ne peut pas être modifiée de sa valeur actuelle, sauf si la modification directement dans la feuille ShapeSheet.  <br/> |
|FALSE  <br/> |La cellule **FontIndex** peut être modifiée à partir de sa valeur actuelle lorsque le thème est modifié.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **LockThemeFonts** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockThemeFonts  <br/> |
   
Pour obtenir une référence à la cellule **LockThemeFonts** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockThemeFonts** <br/> |
   

