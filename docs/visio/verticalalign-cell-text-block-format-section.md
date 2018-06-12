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
ms.openlocfilehash: cfd34f17eec597c306b69f76929877013b39015e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790014"
---
# <a name="verticalalign-cell-text-block-format-section"></a>VerticalAlign, cellule (section Text Block Format)

Détermine l'alignement vertical du texte dans le bloc de texte.
  
|**Valeur**|**Description**|**Constante d’Automation**|
|:-----|:-----|:-----|
| 0  <br/> | Haut  <br/> |**visVertTop** <br/> |
| 1  <br/> | Milieu  <br/> |**visVertMiddle** <br/> |
| 2  <br/> | Bas  <br/> |**visVertBottom** <br/> |
   
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule VerticalAlign par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | VerticalAlign  <br/> |
   
Pour obtenir une référence à la cellule VerticalAlign par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowText** <br/> |
| Index de la cellule :  <br/> |**visTxtBlkVerticalAlign** <br/> |
   

