---
title: Font, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm390
ms.localizationpriority: medium
ms.assetid: 935760a9-307e-90bc-c301-d04283d97427
description: Représente le numéro de la police utilisée pour mettre le texte en forme. Ce numéro dépend des polices installées sur votre système. 0 représente la police par défaut, généralement Arial.
ms.openlocfilehash: 38077b5cc1c0a6538260dab4022d8e7e35c8bc6e
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62780791"
---
# <a name="font-cell-character-section"></a>Font, cellule (section Character)

Représente le numéro de la police utilisée pour mettre le texte en forme. Ce numéro dépend des polices installées sur votre système. 0 représente la police par défaut, généralement Arial.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Font par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Char.Font[  *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule Font à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionCharacter** <br/> |
| Index de la ligne :  <br/> |**visRowCharacter** +   *i* où *i* = 0, 1, 2... |
| Index de la cellule :  <br/> |**visCharacterFont** <br/> |
   

