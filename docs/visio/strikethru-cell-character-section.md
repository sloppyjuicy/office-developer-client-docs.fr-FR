---
title: Strikethru, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm975
ms.localizationpriority: medium
ms.assetid: b03b4415-0b1a-eb03-2b5e-373b39a0f07a
description: Détermine si le texte est barré.
ms.openlocfilehash: ad41d5ce400d7f7ee8f1874078ad6805c4c03524
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63520692"
---
# <a name="strikethru-cell-character-section"></a>Strikethru, cellule (section Character)

Détermine si le texte est barré.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le texte est barré. |
|FALSE  <br/> |Le texte n'est pas barré. |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **Texte** (sous l’onglet **Accueil**, cliquez sur la flèche **Police**). 
  
Pour obtenir une référence à la cellule Strikethru par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |Char.Strikethru[ *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule Strikethru par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionCharacter** <br/> |
|**Index de la ligne :**  <br/> |**visRowCharacter** +   *i* où *i* = 0, 1, 2... |
|**Index de la cellule :**  <br/> |**visCharacterStrikethru** <br/> |
   

