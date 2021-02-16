---
title: BeginArrowSize, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251629
localization_priority: Normal
ms.assetid: bfddb829-6e13-7d74-b9b9-2cb5c0937bae
description: Détermine la taille de la pointe de flèche au début du trait.
ms.openlocfilehash: 9c1288ced747c4e16090013cc043b040f1fbb59c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412281"
---
# <a name="beginarrowsize-cell-line-format-section"></a>BeginArrowSize, cellule (section Line Format)

Détermine la taille de la pointe de flèche au début du trait.
  
|**Valeur**|**Taille**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Très petite  <br/> |**visArrowSizeVerySmall** <br/> |
| 1   <br/> | Petite  <br/> |**visArrowSizeSmall** <br/> |
| 2   <br/> | Moyen  <br/> |**visArrowSizeMedium** <br/> |
| 3   <br/> | Grande  <br/> |**visArrowSizeLarge** <br/> |
| 4   <br/> | Très grande  <br/> |**visArrowSizeVeryLarge** <br/> |
| 5   <br/> | Jumbo  <br/> |**visArrowSizeJumbo** <br/> |
| 6   <br/> | Premier  <br/> |**visArrowSizeColossal** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la taille de la tête de flèche dans la boîte de dialogue **Trait**. 
  
Pour obtenir une référence à la cellule BeginArrowSize par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | BeginArrowSize  <br/> |
   
Pour obtenir une référence à la cellule BeginArrowSize à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLine** <br/> |
| Index de la cellule :  <br/> |**visLineBeginArrowSize** <br/> |
   

