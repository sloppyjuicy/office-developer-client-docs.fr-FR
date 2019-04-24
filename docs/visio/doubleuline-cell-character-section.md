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
ms.openlocfilehash: 2708e7f55e1fd04d5fb902b3d382035790cbbcc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357462"
---
# <a name="doubleuline-cell-character-section"></a>DoubleULine, cellule (section Character)

Détermine si la plage de texte est soulignée ou non d'une ligne double.
  
|**Value**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le texte est souligné en double.  <br/> |
|FALSE  <br/> |Le texte n'est pas souligné en double.  <br/> |
   
## <a name="remarks"></a>Remarques

La cellule DoubleULine contient des informations de mise en forme qui s'appliquent à une plage du texte de la forme si la section Character contient plusieurs lignes ou à l'ensemble du texte dans le cas contraire.
  
Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **Texte** (cliquez sur la flèche **Police** sous l’onglet **Accueil**). 
  
Pour obtenir une référence à la cellule DoubleULine par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Char. DblUnderline [ *i* ] où *i* = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule DoubleULine à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionCharacter** <br/> |
|Index de la ligne :  <br/> |**visRowCharacter** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visCharacterDblUnderline** <br/> |
   

