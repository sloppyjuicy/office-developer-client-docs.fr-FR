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
ms.openlocfilehash: 768a2b2adb05248049377eaee07194cdb89ed810
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328992"
---
# <a name="endarrowsize-cell-line-format-section"></a>EndArrowSize, cellule (section Line Format)

Détermine la taille de la pointe de flèche à la fin du trait.
  
|**Valeur**|**Size**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Très petite  <br/> |**visArrowSizeVerySmall** <br/> |
|0,1  <br/> |Small  <br/> |**visArrowSizeSmall** <br/> |
|n°2  <br/> |Moyenne  <br/> |**visArrowSizeMedium** <br/> |
|3  <br/> |Large  <br/> |**visArrowSizeLarge** <br/> |
|4  <br/> |Très grande  <br/> |**visArrowSizeVeryLarge** <br/> |
|disque  <br/> |Tram  <br/> |**visArrowSizeJumbo** <br/> |
|6.x  <br/> |Colossal  <br/> |**visArrowSizeColossal** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur dans la boîte de dialogue **Trait** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Trait**, pointez sur **Flèches**, puis cliquez sur **Autres flèches**).
  
Pour obtenir une référence à la cellule EndArrowSize par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |EndArrowSize  <br/> |
   
Pour obtenir une référence à la cellule EndArrowSize à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowLine** <br/> |
|Index de la cellule :  <br/> |**visLineEndArrowSize** <br/> |
   

