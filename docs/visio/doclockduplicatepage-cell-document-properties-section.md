---
title: DocLockDuplicatePage Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: Détermine si les pages du document peuvent être dupliquées, en tant que booléens.
ms.openlocfilehash: 8f226bdf072554c3db73644ca54e198505332867
ms.sourcegitcommit: 7b410a51d1e8c97e9cce8d4aa75074162b7d9485
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2022
ms.locfileid: "63447605"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a>DocLockDuplicatePage Cell (Document Properties Section)

Détermine si les pages du document peuvent être dupliquées, en tant que booléens.
  
|Valeur |Description |
|:-----|:-----|
|TRUE  <br/> |**Le doublon** dans le menu raccourci de la page et la **méthode d’automatisation Page.Duplicate** sont tous deux désactivés. |
|FALSE  <br/> |La page peut être dupliquée. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **DocLockDuplicatePage** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | DocLockDuplicatePage  <br/> |
   
Pour obtenir une référence à la **cellule DocLockDuplicatePage** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowDoc** <br/> |
| **Index de la cellule :**  <br/> |**visDocLockDuplicatePage** <br/> |
   

