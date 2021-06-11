---
title: DocLockDuplicatePage Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: Détermine si les pages du document peuvent être dupliquées, en tant que booléens.
ms.openlocfilehash: 3f3274c6cfadb81ef514a179279bdaed3543b654
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439659"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a>DocLockDuplicatePage Cell (Document Properties Section)

Détermine si les pages du document peuvent être dupliquées, en tant que booléens.
  
|||
|:-----|:-----|
|TRUE  <br/> |**Le doublon** dans le menu raccourci de page et la **méthode d’automatisation Page.Duplicate** sont tous deux désactivés.  <br/> |
|FALSE  <br/> |La page peut être dupliquée.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **DocLockDuplicatePage** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | DocLockDuplicatePage  <br/> |
   
Pour obtenir une référence à la **cellule DocLockDuplicatePage** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowDoc** <br/> |
| Index de la cellule :  <br/> |**visDocLockDuplicatePage** <br/> |
   

