---
title: Overline, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251728
ms.localizationpriority: medium
ms.assetid: 102cce17-43ee-e313-3412-a72d6ee18fe6
description: Détermine si le texte est surmonté d'un trait.
ms.openlocfilehash: 41c3af7e85a5c4f27cd370a1ac13b9dd971110e9
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62770449"
---
# <a name="overline-cell-character-section"></a>Overline, cellule (section Character)

Détermine si le texte est surmonté d'un trait.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le texte est surmonté d'un trait. |
|FALSE  <br/> |Le texte n'est pas surmonté d'un trait. |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **Texte** (sous l’onglet **Accueil**, cliquez sur la flèche **Police**). 
  
Pour obtenir une référence à la cellule Overline par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Char.Overline[ *i*  ] où  *i*  = <1>, 2. 3... |
   
Pour obtenir une référence à la cellule Overline à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionCharacter** <br/> |
|Index de la ligne :  <br/> |**visRowCharacter** +   *i* où *i* = 0, 1, 2... |
|Index de la cellule :  <br/> |**visCharacterOverline** <br/> |
   

