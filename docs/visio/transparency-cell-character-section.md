---
title: Transparency, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50135
localization_priority: Normal
ms.assetid: ab835a1a-9e90-126e-279f-463882c48e93
description: Détermine le niveau de transparence d'une plage de la couleur de texte d'une forme.
ms.openlocfilehash: 5914a061b1bba2173b338544b05abda8780ff164
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789918"
---
# <a name="transparency-cell-character-section"></a>Transparency, cellule (section Character)

Détermine le niveau de transparence d'une plage de la couleur de texte d'une forme.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0 - 100  <br/> |Représente le pourcentage de transparence. La valeur par défaut est 0 % (entièrement opaque).  <br/> |
   
## <a name="remarks"></a>Note

Les valeurs sont arrondies au pourcentage le plus proche. Une valeur de 100 % correspond à une transparence totale. Même si une forme dont le texte est entièrement transparent apparaît identique sur la page de dessin à une forme dépourvue de texte, elle interagit avec les autres objets de la page de la même façon que si elle avait une transparence de 0 %.
  
Vous pouvez également définir cette valeur à l’aide du curseur sous l’onglet **police** de la boîte de dialogue **texte** (sous l’onglet **accueil** , cliquez sur la flèche **police** ). 
  
Si la section Characters contient plusieurs lignes, la cellule Transparency contient des informations de mise en forme qui sont appliquées à une sous-plage du texte d’une forme. Dans le cas contraire, elle contient des informations de mise en forme pour la totalité du texte de la forme.
  
Pour obtenir une référence à la cellule Transparency par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Char.ColorTrans [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Transparency par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionCharacter** <br/> |
|Index de la ligne :  <br/> |**visRowCharacter** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visCharacterColorTrans** <br/> |
   

