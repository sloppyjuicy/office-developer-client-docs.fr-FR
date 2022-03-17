---
title: EndArrowSize, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251630
ms.localizationpriority: medium
ms.assetid: e2ecf7c0-a0e9-951f-676a-8e5857bb6544
description: Détermine la taille de la pointe de flèche à la fin du trait.
ms.openlocfilehash: 26b4dc4d1e250479315ff47cd747f35701b9a09e
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63523219"
---
# <a name="endarrowsize-cell-line-format-section"></a>EndArrowSize, cellule (section Line Format)

Détermine la taille de la pointe de flèche à la fin du trait.
  
|**Valeur**|**Taille**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Très petite  <br/> |**visArrowSizeVerySmall** <br/> |
|1  <br/> |Petite  <br/> |**visArrowSizeSmall** <br/> |
|2  <br/> |Moyen  <br/> |**visArrowSizeMedium** <br/> |
|3  <br/> |Grande  <br/> |**visArrowSizeLarge** <br/> |
|4  <br/> |Très grande  <br/> |**visArrowSizeVeryLarge** <br/> |
|5  <br/> |Jumbo  <br/> |**visArrowSizeJumbo** <br/> |
|6   <br/> |Premier  <br/> |**visArrowSizeColossal** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur dans la boîte de dialogue **Trait** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Trait**, pointez sur **Flèches**, puis cliquez sur **Autres flèches**).
  
Pour obtenir une référence à la cellule EndArrowSize par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |EndArrowSize  <br/> |
   
Pour obtenir une référence à la cellule EndArrowSize à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowLine** <br/> |
|**Index de la cellule :**  <br/> |**visLineEndArrowSize** <br/> |
   

