---
title: Spacing, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm955
localization_priority: Normal
ms.assetid: 46feb136-01ac-1303-66ab-d772c0ec41a0
description: Définit l'espace entre les caractères. Les espaces peuvent être ajoutés ou déduits par incréments de 1/20e de point.
ms.openlocfilehash: ee714306e22cafb7f6d805851a6f977e93172377
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789798"
---
# <a name="spacing-cell-character-section"></a>Spacing, cellule (section Character)

Définit l'espace entre les caractères. Les espaces peuvent être ajoutés ou déduits par incréments de 1/20e de point.
  
## <a name="remarks"></a>Note

Vous pouvez également définir la valeur de cette cellule à l’aide de la boîte de dialogue **texte** (sous l’onglet **accueil** , cliquez sur la flèche **police** ). 
  
Pour obtenir une référence à la cellule Spacing par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Char.Letterspace [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Spacing par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionCharacter** <br/> |
|Index de la ligne :  <br/> |**visRowCharacter** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visCharacterLetterspace** <br/> |
   

