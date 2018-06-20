---
title: DocLockDuplicatePage, cellule (Section Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: Détermine si les pages du document peuvent être dupliqués, comme une valeur booléenne.
ms.openlocfilehash: 97bca23a7dc9150f66eb0c87834fca72c215448b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788493"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a>DocLockDuplicatePage, cellule (Section Document Properties)

Détermine si les pages du document peuvent être dupliqués, comme une valeur booléenne.
  
|||
|:-----|:-----|
|TRUE  <br/> |**En double** dans le menu contextuel de page et la méthode d’automation **Page.Duplicate** sont tous deux désactivés.  <br/> |
|FALSE  <br/> |La page peut être dupliquée.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **DocLockDuplicatePage** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | DocLockDuplicatePage  <br/> |
   
Pour obtenir une référence à la cellule **DocLockDuplicatePage** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowDoc** <br/> |
| Index de la cellule :  <br/> |**visDocLockDuplicatePage** <br/> |
   

