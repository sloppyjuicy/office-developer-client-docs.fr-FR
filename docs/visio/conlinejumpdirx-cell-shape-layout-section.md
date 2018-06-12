---
title: ConLineJumpDirX, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm185
localization_priority: Normal
ms.assetid: f0671835-8d48-907a-eca6-43953658f800
description: Détermine la direction de la déviation du trait dans le cas d'un connecteur dynamique horizontal d'une forme.
ms.openlocfilehash: 396830d0da22c15f036f95808b3a94c33e9dc5bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788327"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a>ConLineJumpDirX, cellule (section Shape Layout)

Détermine la direction de la déviation du trait dans le cas d'un connecteur dynamique horizontal d'une forme.
  
|**Valeur**|**Direction de déviation de trait**|**Constante d’Automation**|
|:-----|:-----|:-----|
| 0  <br/> | Valeur par défaut de la page  <br/> |**visLOJumpDirXDefault** <br/> |
| 1  <br/> | Haut  <br/> |**visLOJumpDirXUp** <br/> |
| 2  <br/> | Bas  <br/> |**visLOJumpDirXDown** <br/> |
   
## <a name="remarks"></a>Note

Pour définir la valeur par défaut direction horizontale de connecteur de *toutes les* déviations sur une page, utilisez la cellule PageLineJumpDirX de la section Page Layout. 
  
Pour obtenir une référence à la cellule ConLineJumpDirX par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | ConLineJumpDirX  <br/> |
   
Pour obtenir une référence à la cellule ConLineJumpDirX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
| Index de la cellule :  <br/> |**visSLOJumpDirX** <br/> |
   

