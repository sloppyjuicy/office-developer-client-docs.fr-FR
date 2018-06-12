---
title: Value, cellule (section User-Defined Cells)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1100
localization_priority: Normal
ms.assetid: 495b2aec-e197-75eb-9974-e7c92d26546f
description: Indique une valeur pour la cellule définie par l'utilisateur correspondante.
ms.openlocfilehash: d320c35fa8ae65dd0b21a83ad2cf23dbb3af77f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790000"
---
# <a name="value-cell-user-defined-cells-section"></a>Value, cellule (section User-Defined Cells)

Indique une valeur pour la cellule définie par l'utilisateur correspondante.
  
## <a name="remarks"></a>Note

Pour faire référence à cette valeur dans une autre cellule, indiquez le nom défini par l'utilisateur entré dans la ligne User.Row.
  
Pour obtenir une référence à la cellule Value par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Utilisateur.  *Nom* . Où la valeur utilisateur.  *Name* est le nom de ligne  <br/> |
   
Pour obtenir une référence à la cellule Value par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionUser** <br/> |
| Index de la ligne :  <br/> |**visRowUser** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visUserValue** <br/> |
   

