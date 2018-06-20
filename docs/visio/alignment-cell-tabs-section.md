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
ms.openlocfilehash: a2178c63d0005ee8b2f0c8ebcfbc25854a5b1567
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788008"
---
# <a name="alignment-cell-tabs-section"></a>Alignment, cellule (section Tabs)

Détermine l'alignement des tabulations.
  
|**Valeur**|**Alignment**|**Constante d’Automation**|
|:-----|:-----|:-----|
| 0  <br/> | À gauche  <br/> |**visTabStopLeft** <br/> |
| 1  <br/> | Au centre  <br/> |**visTabStopCenter** <br/> |
| 2  <br/> | Droite  <br/> |**visTabStopRight** <br/> |
| 3  <br/> | Décimal  <br/> |**visTabStopDecimal** <br/> |
| 4  <br/> | Virgule  <br/> |**visTabStopComma** <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Alignment par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Onglets.  *ij* où *i et j =* < 1 >, 2, 3  <br/> |
   
Pour obtenir une référence à la cellule Alignment par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionTab** <br/> |
| Index de la ligne :  <br/> |**visRowTab +** *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> | (*j* * 3) **+ visTabAlign** <br/> |
   

