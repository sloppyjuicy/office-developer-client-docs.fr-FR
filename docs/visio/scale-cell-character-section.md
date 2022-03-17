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
ms.openlocfilehash: 23b17d5290029cadedf540d5cbd103305fabaecb
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63520839"
---
# <a name="scale-cell-character-section"></a>Scale, cellule (section Character)

Contrôle la largeur de la police. La valeur par défaut de cette cellule est 100 %.
  
## <a name="remarks"></a>Remarques

Donnez une valeur comprise entre 1 et 99 % pour réduire la largeur de la police. Donnez une valeur entre 101 et 600 % pour augmenter la largeur de la police.
  
Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **Texte** (sous l’onglet **Accueil**, cliquez sur la flèche **Police**). 
  
Pour obtenir une référence à la cellule Scale par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |Char.FontScale[ *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule Scale à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionCharacter** <br/> |
|**Index de la ligne :**  <br/> |**visRowCharacter** +   *i* où *i* = 0, 1, 2... |
|**Index de la cellule :**  <br/> |**visCharacterFontScale** <br/> |
   

