---
title: LockThemeIndex Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: Empêche toute modification de la cellule ThemeIndex de la ligne Propriétés du thème en appliquant un nouveau thème ou en sélectionnant un nouveau modèle de connecteur. N’empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet.
ms.openlocfilehash: c0f58df4220e309017f3846f7d8060c71cb4ba9f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582567"
---
# <a name="lockthemeindex-cell-protection-section"></a>LockThemeIndex Cell (Protection Section)

Empêche toute modification de la cellule **ThemeIndex** de la ligne **Propriétés** du thème en appliquant un nouveau thème ou en sélectionnant un nouveau modèle de connecteur. N’empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |La **cellule ThemeIndex** ne peut pas être modifiée par rapport à sa valeur actuelle, sauf si elle est modifiée directement dans la feuille ShapeSheet.  <br/> |
|FALSE  <br/> |La **cellule ThemeIndex** peut être modifiée par rapport à sa valeur actuelle lorsque le thème est modifié.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **LockThemeIndex** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | LockThemeIndex  <br/> |
   
Pour obtenir une référence à la **cellule LockThemeIndex** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockThemeIndex** <br/> |
   

