---
title: Strikethru, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm975
localization_priority: Normal
ms.assetid: b03b4415-0b1a-eb03-2b5e-373b39a0f07a
description: Détermine si le texte est barré.
ms.openlocfilehash: 4a58123814a4782c279a36d202e1293ec222ef93
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349335"
---
# <a name="strikethru-cell-character-section"></a>Strikethru, cellule (section Character)

Détermine si le texte est barré.
  
|**Value**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le texte est barré.  <br/> |
|FALSE  <br/> |Le texte n'est pas barré.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **Texte** (sous l’onglet **Accueil**, cliquez sur la flèche **Police**). 
  
Pour obtenir une référence à la cellule Strikethru par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Char. Strikethru [ *i* ] où *i* = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Strikethru par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionCharacter** <br/> |
|Index de la ligne :  <br/> |**visRowCharacter** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visCharacterStrikethru** <br/> |
   

