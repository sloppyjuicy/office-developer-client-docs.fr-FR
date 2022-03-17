---
title: Spacing, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm955
ms.localizationpriority: medium
ms.assetid: 46feb136-01ac-1303-66ab-d772c0ec41a0
description: Définit l'espace entre les caractères. Les espaces peuvent être ajoutés ou déduits par incréments de 1/20e de point.
ms.openlocfilehash: bc3a191969b97e472009276a6e8f805279c2a29c
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63523191"
---
# <a name="spacing-cell-character-section"></a>Spacing, cellule (section Character)

Définit l'espace entre les caractères. Les espaces peuvent être ajoutés ou déduits par incréments de 1/20e de point.
  
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **Texte** (sous l’onglet **Accueil**, cliquez sur la flèche **Police**). 
  
Pour obtenir une référence à la cellule Spacing par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |Char.Letterspace[ *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule Spacing par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionCharacter** <br/> |
|**Index de la ligne :**  <br/> |**visRowCharacter** +   *i* où *i* = 0, 1, 2... |
|**Index de la cellule :**  <br/> |**visCharacterLetterspace** <br/> |
   

