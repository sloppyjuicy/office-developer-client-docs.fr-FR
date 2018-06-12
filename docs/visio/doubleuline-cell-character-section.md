---
title: DoubleULine, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm260
localization_priority: Normal
ms.assetid: c18955c8-d653-c29d-d3da-9d3cd0241e17
description: Détermine si la plage de texte est soulignée ou non d'une ligne double.
ms.openlocfilehash: d0a07d8c86bd7e9ed3eb14074dda164f82c92475
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788523"
---
# <a name="doubleuline-cell-character-section"></a>DoubleULine, cellule (section Character)

Détermine si la plage de texte est soulignée ou non d'une ligne double.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le texte est souligné en double.  <br/> |
|FALSE  <br/> |Le texte n'est pas souligné en double.  <br/> |
   
## <a name="remarks"></a>Note

La cellule DoubleULine contient des informations de mise en forme qui s'appliquent à une plage du texte de la forme si la section Character contient plusieurs lignes ou à l'ensemble du texte dans le cas contraire.
  
Vous pouvez également définir la valeur de cette cellule à l’aide de la boîte de dialogue **texte** (cliquez sur la flèche **police** sous l’onglet **accueil** ). 
  
Pour obtenir une référence à la cellule DoubleULine par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Char.DblUnderline [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule DoubleULine par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionCharacter** <br/> |
|Index de la ligne :  <br/> |**visRowCharacter** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visCharacterDblUnderline** <br/> |
   

