---
title: Pos, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm805
localization_priority: Normal
ms.assetid: c02186ce-6a20-fbe7-588d-d64c3ea4dec4
description: Détermine la position du texte de la forme par rapport à la ligne de base.
ms.openlocfilehash: d5f6823d6f55493095d29054745f62b579a47893
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359814"
---
# <a name="pos-cell-character-section"></a>Pos, cellule (section Character)

Détermine la position du texte de la forme par rapport à la ligne de base.
  
|**Value**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Normal  <br/> |**visPosNormal** <br/> |
| 0,1  <br/> | Exposant  <br/> |**visPosSuper** <br/> |
| n°2  <br/> | Indice  <br/> |**visPosSub** <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Pos par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Char. POS [ *i* ] où *i* = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Pos à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionCharacter** <br/> |
| Index de la ligne :  <br/> |**visRowCharacter** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCharacterPos** <br/> |
   

