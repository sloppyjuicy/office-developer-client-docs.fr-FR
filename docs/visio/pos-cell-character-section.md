---
title: Pos, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm805
ms.localizationpriority: medium
ms.assetid: c02186ce-6a20-fbe7-588d-d64c3ea4dec4
description: Détermine la position du texte de la forme par rapport à la ligne de base.
ms.openlocfilehash: 1c27c302b6f8a2b51ded275ca3e2719311d98f83
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62788814"
---
# <a name="pos-cell-character-section"></a>Pos, cellule (section Character)

Détermine la position du texte de la forme par rapport à la ligne de base.
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Normal  <br/> |**visPosNormal** <br/> |
| 1  <br/> | Exposant  <br/> |**visPosSuper** <br/> |
| 2  <br/> | Indice  <br/> |**visPosSub** <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Pos par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Char.Pos[  *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule Pos à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionCharacter** <br/> |
| Index de la ligne :  <br/> |**visRowCharacter** +   *i* où *i* = 0, 1, 2... |
| Index de la cellule :  <br/> |**visCharacterPos** <br/> |
   

