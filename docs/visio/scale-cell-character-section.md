---
title: Scale, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm870
localization_priority: Normal
ms.assetid: d6fe2574-b719-f38e-b1f1-592a812f1682
description: Contrôle la largeur de la police. La valeur par défaut de cette cellule est 100 %.
ms.openlocfilehash: fedbc0aec23320d03ca358f34babda56eaab31e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789594"
---
# <a name="scale-cell-character-section"></a>Scale, cellule (section Character)

Contrôle la largeur de la police. La valeur par défaut de cette cellule est 100 %.
  
## <a name="remarks"></a>Note

Donnez une valeur comprise entre 1 et 99 % pour réduire la largeur de la police. Donnez une valeur entre 101 et 600 % pour augmenter la largeur de la police.
  
Vous pouvez également définir la valeur de cette cellule à l’aide de la boîte de dialogue **texte** (sous l’onglet **accueil** , cliquez sur la flèche **police** ). 
  
Pour obtenir une référence à la cellule Scale par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Char.FontScale [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Scale par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionCharacter** <br/> |
|Index de la ligne :  <br/> |**visRowCharacter** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visCharacterFontScale** <br/> |
   

