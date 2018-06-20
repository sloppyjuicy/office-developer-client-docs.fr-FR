---
title: Overline, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251728
localization_priority: Normal
ms.assetid: 102cce17-43ee-e313-3412-a72d6ee18fe6
description: Détermine si le texte est surmonté d'un trait.
ms.openlocfilehash: 3ceb0f5bcb6f66098938e49ea5f176921d0c9808
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789192"
---
# <a name="overline-cell-character-section"></a>Overline, cellule (section Character)

Détermine si le texte est surmonté d'un trait.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le texte est surmonté d'un trait.  <br/> |
|FALSE  <br/> |Le texte n'est pas surmonté d'un trait.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule à l’aide de la boîte de dialogue **texte** (sous l’onglet **accueil** , cliquez sur la flèche **police** ). 
  
Pour obtenir une référence à la cellule Overline par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Char.Overline [ *i* ] où *i* = < 1 >, 2. 3...  <br/> |
   
Pour obtenir une référence à la cellule Overline par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionCharacter** <br/> |
|Index de la ligne :  <br/> |**visRowCharacter** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visCharacterOverline** <br/> |
   

