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
ms.openlocfilehash: 23dc298b00463da39b9345be59cf7d4267a636a4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554802"
---
# <a name="flipx-cell-shape-transform-section"></a>FlipX, cellule (section Shape Transform)

Indique si la forme a été retournée horizontalement.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La forme a été retournée horizontalement.  <br/> |
| FALSE  <br/> | La forme n'a pas été retournée horizontalement.  <br/> |
   
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
   

