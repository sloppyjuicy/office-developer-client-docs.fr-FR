---
title: LockThemeConnectors Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: Empêche la cellule ConnectorsSchemeIndex de la ligne Propriétés du thème d’être modifiée en appliquant un nouveau thème ou en sélectionnant un nouveau schéma de connecteur. N’empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet.
ms.openlocfilehash: 3e1fd7571795bb5fea7cb4d0a5f8da091b5b7783
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554396"
---
# <a name="lockthemeconnectors-cell-protection-section"></a>LockThemeConnectors Cell (Protection Section)

Empêche la cellule **ConnectorsSchemeIndex** de la ligne **Propriétés** du thème d’être modifiée en appliquant un nouveau thème ou en sélectionnant un nouveau schéma de connecteur. N’empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |La **cellule ConnectorsSchemeIndex** ne peut pas être modifiée par rapport à sa valeur actuelle, sauf si elle est modifiée directement dans la feuille ShapeSheet.  <br/> |
|FALSE  <br/> |La **cellule ConnectorsSchemeIndex** peut être modifiée à partir de sa valeur actuelle via l’interface utilisateur.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **LockThemeConnectors** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | LockThemeConnectors  <br/> |
   
Pour obtenir une référence à la **cellule LockThemeConnectors** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockThemeConnectors** <br/> |
   

