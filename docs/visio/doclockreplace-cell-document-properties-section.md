---
title: DocLockReplace Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: Détermine si l’interface utilisateur de la forme de remplacement doit être désactivée pour ce document.
ms.openlocfilehash: cfec9b3c51a170c549fdd0d1b0b3597c030c410c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413422"
---
# <a name="doclockreplace-cell-document-properties-section"></a>DocLockReplace Cell (Document Properties Section)

Détermine si l’interface utilisateur de la forme de remplacement doit être désactivée pour ce document. 
  
|||
|:-----|:-----|
|TRUE  <br/> |Le **bouton Remplacer la** forme est grisé dans l’interface utilisateur.  <br/> |
|FALSE  <br/> |Le **bouton Remplacer la** forme est actif dans l’interface utilisateur. Les utilisateurs peuvent utiliser la fonctionnalité Remplacer une forme dans ce document.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **DocLockReplace** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | DocLocReplace  <br/> |
   
Pour obtenir une référence à la **cellule DocLocReplace** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowDoc** <br/> |
| Index de la cellule :  <br/> |**visDocLockReplace ** <br/> |
   

