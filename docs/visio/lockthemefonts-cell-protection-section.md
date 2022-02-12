---
title: LockThemeFonts Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: Empêche la cellule FontIndex de la ligne Propriétés du thème d’être modifiée en appliquant un nouveau thème. N’empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet.
ms.openlocfilehash: 90e6b61d875760c1ae374bd263c41b519492f449
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62788870"
---
# <a name="lockthemefonts-cell-protection-section"></a>LockThemeFonts Cell (Protection Section)

Empêche la cellule **FontIndex** de la ligne **Propriétés** du thème d’être modifiée en appliquant un nouveau thème. N’empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |La **cellule FontIndex** ne peut pas être modifiée par rapport à sa valeur actuelle, sauf si elle est modifiée directement dans la feuille ShapeSheet. |
|FALSE  <br/> |La **cellule FontIndex** peut être modifiée par rapport à sa valeur actuelle lorsque le thème est modifié. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **LockThemeFonts** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | LockThemeFonts  <br/> |
   
Pour obtenir une référence à la **cellule LockThemeFonts** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockThemeFonts** <br/> |
   

