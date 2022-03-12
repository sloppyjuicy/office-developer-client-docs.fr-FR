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
ms.openlocfilehash: 0ebb319ae4bb0c7e5a31e9820a384ee0d5726cfe
ms.sourcegitcommit: 7b410a51d1e8c97e9cce8d4aa75074162b7d9485
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2022
ms.locfileid: "63448278"
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
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |Char.DblUnderline[ *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule DoubleULine à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionCharacter** <br/> |
|**Index de la ligne :**  <br/> |**visRowCharacter** +   *i* où *i* = 0, 1, 2... |
|**Index de la cellule :**  <br/> |**visCharacterDblUnderline** <br/> |
   

