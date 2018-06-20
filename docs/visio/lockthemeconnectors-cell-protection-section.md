---
title: LockThemeConnectors, cellule (Section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: Empêche la cellule ConnectorsSchemeIndex dans la ligne de propriétés de thème de modification en appliquant un nouveau thème ou en sélectionnant un nouveau jeu de connecteur. N’empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet.
ms.openlocfilehash: c74bcf554f0f14de47480397a96680469826d2c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789024"
---
# <a name="lockthemeconnectors-cell-protection-section"></a>LockThemeConnectors, cellule (Section Protection)

Empêche la cellule **ConnectorsSchemeIndex** dans la ligne de **Propriétés de thème** de modification en appliquant un nouveau thème ou en sélectionnant un nouveau jeu de connecteur. N’empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |La cellule **ConnectorsSchemeIndex** ne peut pas être modifiée de sa valeur actuelle, sauf si la modification directement dans la feuille ShapeSheet.  <br/> |
|FALSE  <br/> |La cellule **ConnectorsSchemeIndex** peut être modifiée à partir de sa valeur actuelle par le biais de l’interface utilisateur.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **LockThemeConnectors** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LockThemeConnectors  <br/> |
   
Pour obtenir une référence à la cellule **LockThemeConnectors** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockThemeConnectors** <br/> |
   

