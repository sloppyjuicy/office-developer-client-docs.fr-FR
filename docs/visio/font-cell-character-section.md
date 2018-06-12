---
title: Font, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm390
localization_priority: Normal
ms.assetid: 935760a9-307e-90bc-c301-d04283d97427
description: Représente le numéro de la police utilisée pour mettre le texte en forme. Ce numéro dépend des polices installées sur votre système. 0 représente la police par défaut, généralement Arial.
ms.openlocfilehash: cbbf2a2400c995e0cbc217c1161fbd18f7459b28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788656"
---
# <a name="font-cell-character-section"></a>Font, cellule (section Character)

Représente le numéro de la police utilisée pour mettre le texte en forme. Ce numéro dépend des polices installées sur votre système. 0 représente la police par défaut, généralement Arial.
  
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule Font par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Char.Font [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Font par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionCharacter** <br/> |
| Index de la ligne :  <br/> |**visRowCharacter** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCharacterFont** <br/> |
   

