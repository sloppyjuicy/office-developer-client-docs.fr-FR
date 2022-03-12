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
ms.openlocfilehash: 6f00d565f87d10404f62e00275e3ef8283c7afda
ms.sourcegitcommit: 7b410a51d1e8c97e9cce8d4aa75074162b7d9485
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2022
ms.locfileid: "63448320"
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
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Onglets.  *ij*            où  *i et j =*  <1>, 2, 3  <br/> |
   
Pour obtenir une référence à la cellule Alignment à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionTab** <br/> |
| **Index de la ligne :**  <br/> |**visRowTab +** *i*            où  *i*  = 0, 1, 2... |
| **Index de la cellule :**  <br/> | (*j*  *3) **+ visTabAlign** <br/> |
   

