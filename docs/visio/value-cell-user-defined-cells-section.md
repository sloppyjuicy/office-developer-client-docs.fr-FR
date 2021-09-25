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
ms.openlocfilehash: 00a96f98682ace7c66ddba8c7aa7ac3a284a224c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559345"
---
# <a name="value-cell-user-defined-cells-section"></a>Value, cellule (section User-Defined Cells)

Indique une valeur pour la cellule définie par l'utilisateur correspondante.
  
## <a name="remarks"></a>Remarques

Pour faire référence à cette valeur dans une autre cellule, indiquez le nom défini par l'utilisateur entré dans la ligne User.Row.
  
Pour obtenir une référence à la cellule Value par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Utilisateur.  *Nom*  . Valeur où User.  *Le nom*  est le nom de la ligne  <br/> |
   
Pour obtenir une référence à la cellule Value par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionUser** <br/> |
| Index de la ligne :  <br/> |**visRowUser**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visUserValue** <br/> |
   

