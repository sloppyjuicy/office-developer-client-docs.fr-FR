---
title: VerticalAlign, cellule (section Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1105
localization_priority: Normal
ms.assetid: ff34a23b-2881-864f-42e4-871c4fde0992
description: Détermine l'alignement vertical du texte dans le bloc de texte.
ms.openlocfilehash: 954a0cf0b80d6b675dcc016997f1923041069eac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356140"
---
# <a name="verticalalign-cell-text-block-format-section"></a>VerticalAlign, cellule (section Text Block Format)

Détermine l'alignement vertical du texte dans le bloc de texte.
  
|**Value**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Haut  <br/> |**visVertTop** <br/> |
| 0,1  <br/> | Centre  <br/> |**visVertMiddle** <br/> |
| n°2  <br/> | Inférieures  <br/> |**visVertBottom** <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule VerticalAlign par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | VerticalAlign  <br/> |
   
Pour obtenir une référence à la cellule VerticalAlign par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowText** <br/> |
| Index de la cellule :  <br/> |**visTxtBlkVerticalAlign** <br/> |
   

