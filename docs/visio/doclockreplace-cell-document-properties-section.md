---
title: DocLockReplace Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: Détermine si l’interface utilisateur de la forme de remplacement doit être désactivée pour ce document.
ms.openlocfilehash: e73097d88a7ea693e731b062e59832c14c55a634
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62780847"
---
# <a name="doclockreplace-cell-document-properties-section"></a>DocLockReplace Cell (Document Properties Section)

Détermine si l’interface utilisateur de la forme de remplacement doit être désactivée pour ce document. 
  
|||
|:-----|:-----|
|TRUE  <br/> |Le **bouton Remplacer la** forme est grisé dans l’interface utilisateur. |
|FALSE  <br/> |Le **bouton Remplacer la** forme est actif dans l’interface utilisateur. Les utilisateurs peuvent utiliser la fonctionnalité Remplacer la forme dans ce document. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **DocLockReplace** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | DocLocReplace  <br/> |
   
Pour obtenir une référence à la **cellule DocLocReplace** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowDoc** <br/> |
| Index de la cellule :  <br/> |**visDocLockReplace ** <br/> |
   

