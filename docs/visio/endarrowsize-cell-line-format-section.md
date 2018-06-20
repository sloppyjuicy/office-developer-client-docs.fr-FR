---
title: EndArrowSize, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251630
localization_priority: Normal
ms.assetid: e2ecf7c0-a0e9-951f-676a-8e5857bb6544
description: Détermine la taille de la pointe de flèche à la fin du trait.
ms.openlocfilehash: e03871c75857297634300c2eee091de2d0144903
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788577"
---
# <a name="endarrowsize-cell-line-format-section"></a>EndArrowSize, cellule (section Line Format)

Détermine la taille de la pointe de flèche à la fin du trait.
  
|**Valeur**|**Size**|**Constante d’Automation**|
|:-----|:-----|:-----|
|0  <br/> |Très petite  <br/> |**visArrowSizeVerySmall** <br/> |
|1  <br/> |Petite  <br/> |**visArrowSizeSmall** <br/> |
|2  <br/> |Moyenne  <br/> |**visArrowSizeMedium** <br/> |
|3  <br/> |Grande  <br/> |**visArrowSizeLarge** <br/> |
|4  <br/> |Très grande  <br/> |**visArrowSizeVeryLarge** <br/> |
|5  <br/> |Énorme  <br/> |**visArrowSizeJumbo** <br/> |
|6  <br/> |Colossale  <br/> |**visArrowSizeColossal** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur dans la boîte de dialogue **trait** (sous l’onglet **accueil** , dans le groupe **forme** , cliquez sur **trait**, pointez sur **flèches**, puis cliquez sur **Autres flèches**).
  
Pour obtenir une référence à la cellule EndArrowSize par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |EndArrowSize  <br/> |
   
Pour obtenir une référence à la cellule EndArrowSize par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowLine** <br/> |
|Index de la cellule :  <br/> |**visLineEndArrowSize** <br/> |
   

