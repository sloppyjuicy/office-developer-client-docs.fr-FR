---
title: Alignment, cellule (section Tabs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm35
localization_priority: Normal
ms.assetid: 84234177-a2df-6acc-2761-230bc5d12627
description: Détermine l'alignement des tabulations.
ms.openlocfilehash: 461357c9c838fb4c0e5b0159bf027dd6adce26f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425539"
---
# <a name="alignment-cell-tabs-section"></a>Alignment, cellule (section Tabs)

Détermine l'alignement des tabulations.
  
|**Valeur**|**Alignment**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Gauche  <br/> |**visTabStopLeft** <br/> |
| 0,1  <br/> | Centre  <br/> |**visTabStopCenter** <br/> |
| n°2  <br/> | À droite  <br/> |**visTabStopRight** <br/> |
| 3  <br/> | Décimal  <br/> |**visTabStopDecimal** <br/> |
| 4  <br/> | Virgule  <br/> |**visTabStopComma** <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Alignment par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Taquet.  *IJ* où *i et j =* <1>, 2, 3  <br/> |
   
Pour obtenir une référence à la cellule Alignment à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionTab** <br/> |
| Index de la ligne :  <br/> |**visRowTab +** *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> | (*j* * 3) **+ visTabAlign** <br/> |
   

