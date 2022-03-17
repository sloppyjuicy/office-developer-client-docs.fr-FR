---
title: Value, cellule (section User-Defined Cells)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1100
ms.localizationpriority: medium
ms.assetid: 495b2aec-e197-75eb-9974-e7c92d26546f
description: Indique une valeur pour la cellule définie par l'utilisateur correspondante.
ms.openlocfilehash: a1c1574ed773a7ef93dd94c0962b259942c9cc95
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63521959"
---
# <a name="value-cell-user-defined-cells-section"></a>Value, cellule (section User-Defined Cells)

Indique une valeur pour la cellule définie par l'utilisateur correspondante.
  
## <a name="remarks"></a>Remarques

Pour faire référence à cette valeur dans une autre cellule, indiquez le nom défini par l'utilisateur entré dans la ligne User.Row.
  
Pour obtenir une référence à la cellule Value par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Utilisateur.  *Nom*  . Valeur où User.  *Le nom*  est le nom de la ligne  <br/> |
   
Pour obtenir une référence à la cellule Value par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionUser** <br/> |
| **Index de la ligne :**  <br/> |**visRowUser** +   *i* où *i* = 0, 1, 2... |
| **Index de la cellule :**  <br/> |**visUserValue** <br/> |
   

