---
title: DocLockDuplicatePage Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: Détermine si les pages du document peuvent être dupliquées, sous la forme d'une valeur booléenne.
ms.openlocfilehash: 3f3274c6cfadb81ef514a179279bdaed3543b654
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338541"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a>DocLockDuplicatePage Cell (Document Properties Section)

Détermine si les pages du document peuvent être dupliquées, sous la forme d'une valeur booléenne.
  
|||
|:-----|:-----|
|TRUE  <br/> |**** Les doublons dans le menu contextuel page et la méthode Automation **page. Duplicate** sont tous deux désactivés.  <br/> |
|FALSE  <br/> |La page peut être dupliquée.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **DocLockDuplicatePage** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez: 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | DocLockDuplicatePage  <br/> |
   
Pour obtenir une référence à la cellule **DocLockDuplicatePage** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants: 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowDoc** <br/> |
| Index de la cellule :  <br/> |**visDocLockDuplicatePage** <br/> |
   

