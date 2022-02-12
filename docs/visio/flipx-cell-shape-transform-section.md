---
title: FlipX, cellule (section Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251197
ms.localizationpriority: medium
ms.assetid: 8d4f5e14-4f17-05a6-4092-5a102c9dc85f
description: Indique si la forme a été retournée horizontalement.
ms.openlocfilehash: ce96a2b86d6e54138b68bba3a02009bab94f0036
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62787302"
---
# <a name="flipx-cell-shape-transform-section"></a>FlipX, cellule (section Shape Transform)

Indique si la forme a été retournée horizontalement.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La forme a été retournée horizontalement. |
| FALSE  <br/> | La forme n'a pas été retournée horizontalement. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule FlipX par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | FlipX  <br/> |
   
Pour obtenir une référence à la cellule FlipX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowXFormOut** <br/> |
| Index de la cellule :  <br/> |**visXFormFlipX** <br/> |
   

