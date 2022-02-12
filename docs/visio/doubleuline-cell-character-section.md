---
title: DoubleULine, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm260
ms.localizationpriority: medium
ms.assetid: c18955c8-d653-c29d-d3da-9d3cd0241e17
description: Détermine si la plage de texte est soulignée ou non d'une ligne double.
ms.openlocfilehash: cfb0e374226aa0ab9f4d8d84db5778eed31468f2
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62771600"
---
# <a name="doubleuline-cell-character-section"></a>DoubleULine, cellule (section Character)

Détermine si la plage de texte est soulignée ou non d'une ligne double.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le texte est souligné en double. |
|FALSE  <br/> |Le texte n'est pas souligné en double. |
   
## <a name="remarks"></a>Remarques

La cellule DoubleULine contient des informations de mise en forme qui s'appliquent à une plage du texte de la forme si la section Character contient plusieurs lignes ou à l'ensemble du texte dans le cas contraire.
  
Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **Texte** (cliquez sur la flèche **Police** sous l’onglet **Accueil**). 
  
Pour obtenir une référence à la cellule DoubleULine par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Char.DblUnderline[ *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule DoubleULine à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionCharacter** <br/> |
|Index de la ligne :  <br/> |**visRowCharacter** +   *i* où *i* = 0, 1, 2... |
|Index de la cellule :  <br/> |**visCharacterDblUnderline** <br/> |
   

