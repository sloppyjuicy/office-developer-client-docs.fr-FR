---
title: FlipY, cellule (section Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251198
ms.localizationpriority: medium
ms.assetid: 062022ff-e243-2540-becd-d9b969ce83ce
description: Indique si la forme a été retournée verticalement.
ms.openlocfilehash: ed1c3b25fce07a93e73d19c5e886bd4d797bbdc7
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62780805"
---
# <a name="flipy-cell-shape-transform-section"></a>FlipY, cellule (section Shape Transform)

Indique si la forme a été retournée verticalement.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La forme a été retournée verticalement. |
| FALSE  <br/> | La forme n'a pas été retournée verticalement. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule FlipY par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | FlipY  <br/> |
   
Pour obtenir une référence à la cellule FlipY à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowXFormOut** <br/> |
| Index de la cellule :  <br/> |**visXFormFlipY** <br/> |
   

