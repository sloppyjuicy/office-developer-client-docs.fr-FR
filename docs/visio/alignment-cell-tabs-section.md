---
title: Alignment, cellule (section Tabs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm35
ms.localizationpriority: medium
ms.assetid: 84234177-a2df-6acc-2761-230bc5d12627
description: Détermine l'alignement des tabulations.
ms.openlocfilehash: 502074bb25a37756ce64123ddb74abc93119086a
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62776073"
---
# <a name="alignment-cell-tabs-section"></a>Alignment, cellule (section Tabs)

Détermine l'alignement des tabulations.
  
|**Valeur**|**Alignment**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Gauche  <br/> |**visTabStopLeft** <br/> |
| 1  <br/> | Centre  <br/> |**visTabStopCenter** <br/> |
| 2  <br/> | À droite  <br/> |**visTabStopRight** <br/> |
| 3  <br/> | Décimal  <br/> |**visTabStopDecimal** <br/> |
| 4  <br/> | Virgule  <br/> |**visTabStopComma** <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Alignment par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Onglets.  *ij*            où  *i et j =*  <1>, 2, 3  <br/> |
   
Pour obtenir une référence à la cellule Alignment à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionTab** <br/> |
| Index de la ligne :  <br/> |**visRowTab +** *i*            où  *i*  = 0, 1, 2... |
| Index de la cellule :  <br/> | (*j*  *3) **+ visTabAlign** <br/> |
   

