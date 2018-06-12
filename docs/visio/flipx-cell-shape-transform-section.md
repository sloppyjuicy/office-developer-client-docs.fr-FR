---
title: FlipX, cellule (section Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251197
localization_priority: Normal
ms.assetid: 8d4f5e14-4f17-05a6-4092-5a102c9dc85f
description: Indique si la forme a été retournée horizontalement.
ms.openlocfilehash: fc014ff6c5a3650361d6afd478a5858f84fb5c47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788658"
---
# <a name="flipx-cell-shape-transform-section"></a>FlipX, cellule (section Shape Transform)

Indique si la forme a été retournée horizontalement.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La forme a été retournée horizontalement.  <br/> |
| FALSE  <br/> | La forme n'a pas été retournée horizontalement.  <br/> |
   
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule FlipX par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | FlipX  <br/> |
   
Pour obtenir une référence à la cellule FlipX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowXFormOut** <br/> |
| Index de la cellule :  <br/> |**visXFormFlipX** <br/> |
   

