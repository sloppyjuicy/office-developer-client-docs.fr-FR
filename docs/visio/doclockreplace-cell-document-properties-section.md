---
title: DocLockReplace, cellule (Section Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: Détermine si la forme de remplacer l’interface utilisateur doit être désactivée pour ce document.
ms.openlocfilehash: 41552ddad4e48680960c45869ded5cf4f80d760f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788517"
---
# <a name="doclockreplace-cell-document-properties-section"></a>DocLockReplace, cellule (Section Document Properties)

Détermine si la forme de remplacer l’interface utilisateur doit être désactivée pour ce document. 
  
|||
|:-----|:-----|
|TRUE  <br/> |Le bouton **Remplacer une forme** est désactivé dans l’interface utilisateur.  <br/> |
|FALSE  <br/> |Le bouton **Remplacer une forme** est actif dans l’interface utilisateur. Les utilisateurs peuvent utiliser la fonctionnalité de remplacer la forme dans ce document.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **DocLockReplace** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | DocLocReplace  <br/> |
   
Pour obtenir une référence à la cellule **DocLocReplace** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowDoc** <br/> |
| Index de la cellule :  <br/> |** visDocLockReplace ** <br/> |
   

