---
title: LockThemeFonts Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: Empêche la cellule FontIndex de la ligne Propriétés du thème d’être modifiée en appliquant un nouveau thème. N’empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet.
ms.openlocfilehash: b3bd21c1dcd8c8c13d843c50cb29edcc5b8c4999
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421227"
---
# <a name="lockthemefonts-cell-protection-section"></a>LockThemeFonts Cell (Protection Section)

Empêche la cellule **FontIndex** de la ligne **Propriétés** du thème d’être modifiée en appliquant un nouveau thème. N’empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |La **cellule FontIndex** ne peut pas être modifiée par rapport à sa valeur actuelle, sauf si elle est modifiée directement dans la feuille ShapeSheet.  <br/> |
|FALSE  <br/> |La **cellule FontIndex** peut être modifiée par rapport à sa valeur actuelle lorsque le thème est modifié.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **LockThemeFonts** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | LockThemeFonts  <br/> |
   
Pour obtenir une référence à la **cellule LockThemeFonts** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockThemeFonts** <br/> |
   

