---
title: Transparency, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50135
ms.localizationpriority: medium
ms.assetid: ab835a1a-9e90-126e-279f-463882c48e93
description: Détermine le niveau de transparence d'une plage de la couleur de texte d'une forme.
ms.openlocfilehash: 2fc881807ddf907fc5cdf459a9d1d3ec5f63e531
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63626947"
---
# <a name="transparency-cell-character-section"></a>Transparency, cellule (section Character)

Détermine le niveau de transparence d'une plage de la couleur de texte d'une forme.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0 - 100  <br/> |Représente le pourcentage de transparence. La valeur par défaut est 0 % (entièrement opaque). |
   
## <a name="remarks"></a>Remarques

Les valeurs sont arrondies au pourcentage le plus proche. Une valeur de 100 % correspond à une transparence totale. Même si une forme dont le texte est entièrement transparent apparaît identique sur la page de dessin à une forme dépourvue de texte, elle interagit avec les autres objets de la page de la même façon que si elle avait une transparence de 0 %.
  
Vous pouvez également définir cette valeur à l’aide du curseur sous  l’onglet Police de la boîte de dialogue Texte  (sous l’onglet Accueil, cliquez sur la **flèche Police**). 
  
Si la section Characters contient plusieurs lignes, la cellule Transparency contient des informations de mise en forme qui sont appliquées à une sous-plage du texte d’une forme. Dans le cas contraire, elle contient des informations de mise en forme pour la totalité du texte de la forme.
  
Pour obtenir une référence à la cellule Transparency par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |Char.ColorTrans[ *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule Transparency par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionCharacter** <br/> |
|**Index de la ligne :**  <br/> |**visRowCharacter** +   *i* où *i* = 0, 1, 2... |
|**Index de la cellule :**  <br/> |**visCharacterColorTrans** <br/> |
   

