---
title: DocLockReplace Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: Détermine si l'interface utilisateur de remplacement de la forme doit être désactivée pour ce document.
ms.openlocfilehash: cfec9b3c51a170c549fdd0d1b0b3597c030c410c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338604"
---
# <a name="doclockreplace-cell-document-properties-section"></a>DocLockReplace Cell (Document Properties Section)

Détermine si l'interface utilisateur de remplacement de la forme doit être désactivée pour ce document. 
  
|||
|:-----|:-----|
|TRUE  <br/> |Le bouton **remplacer la forme** est grisé dans l'interface utilisateur.  <br/> |
|FALSE  <br/> |Le bouton **remplacer la forme** est actif dans l'interface utilisateur. Les utilisateurs peuvent utiliser la fonctionnalité remplacer la forme dans ce document.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **DocLockReplace** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez: 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | DocLocReplace  <br/> |
   
Pour obtenir une référence à la cellule **DocLocReplace** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants: 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowDoc** <br/> |
| Index de la cellule :  <br/> |* * visDocLockReplace * * <br/> |
   

