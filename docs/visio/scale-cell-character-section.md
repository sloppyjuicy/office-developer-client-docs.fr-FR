---
title: Scale, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm870
ms.localizationpriority: medium
ms.assetid: d6fe2574-b719-f38e-b1f1-592a812f1682
description: Contrôle la largeur de la police. La valeur par défaut de cette cellule est 100 %.
ms.openlocfilehash: 97610813956517a3960e4be297efe0da8f3a50ba
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62781925"
---
# <a name="scale-cell-character-section"></a>Scale, cellule (section Character)

Contrôle la largeur de la police. La valeur par défaut de cette cellule est 100 %.
  
## <a name="remarks"></a>Remarques

Donnez une valeur comprise entre 1 et 99 % pour réduire la largeur de la police. Donnez une valeur entre 101 et 600 % pour augmenter la largeur de la police.
  
Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **Texte** (sous l’onglet **Accueil**, cliquez sur la flèche **Police**). 
  
Pour obtenir une référence à la cellule Scale par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Char.FontScale[ *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule Scale à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionCharacter** <br/> |
|Index de la ligne :  <br/> |**visRowCharacter** +   *i* où *i* = 0, 1, 2... |
|Index de la cellule :  <br/> |**visCharacterFontScale** <br/> |
   

