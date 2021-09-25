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
ms.openlocfilehash: 50708cd670f7d048e2c0321e5752d1826cbf8091
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607751"
---
# <a name="scale-cell-character-section"></a>Scale, cellule (section Character)

Contrôle la largeur de la police. La valeur par défaut de cette cellule est 100 %.
  
## <a name="remarks"></a>Remarques

Donnez une valeur comprise entre 1 et 99 % pour réduire la largeur de la police. Donnez une valeur entre 101 et 600 % pour augmenter la largeur de la police.
  
Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **Texte** (sous l’onglet **Accueil**, cliquez sur la flèche **Police**). 
  
Pour obtenir une référence à la cellule Scale par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Char.FontScale[ *i*  ] où  *i*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Scale à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionCharacter** <br/> |
|Index de la ligne :  <br/> |**visRowCharacter**  +   *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visCharacterFontScale** <br/> |
   

