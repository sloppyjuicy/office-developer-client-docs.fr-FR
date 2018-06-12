---
title: ConLineJumpDirY, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251654
localization_priority: Normal
ms.assetid: 93f82ae0-3442-fac1-9906-b84afef85f5c
description: Détermine la direction de la déviation de trait dans le cas d'un connecteur dynamique vertical d'une forme.
ms.openlocfilehash: 2d0c0964b52c9afbccc9cb507024825434702b6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788315"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a>ConLineJumpDirY, cellule (section Shape Layout)

Détermine la direction de la déviation de trait dans le cas d'un connecteur dynamique vertical d'une forme.
  
|**Valeur**|**Direction de déviation de trait**|**Constante d’Automation**|
|:-----|:-----|:-----|
| 0  <br/> | Valeur par défaut de la page  <br/> |**visLOJumpDirYDefault** <br/> |
| 1  <br/> | Gauche  <br/> |**visLOJumpDirYLeft** <br/> |
| 2  <br/> | Droite  <br/> |**visLOJumpDirYRight** <br/> |
   
## <a name="remarks"></a>Note

Pour définir la valeur par défaut direction verticale de connecteur de *toutes les* déviations sur une page, utilisez la cellule PageLineJumpDirY de la section Page Layout. 
  
Pour obtenir une référence à la cellule ConLineJumpDirY par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | ConLineJumpDirY  <br/> |
   
Pour obtenir une référence à la cellule ConLineJumpDirY par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
| Index de la cellule :  <br/> |**visSLOJumpDirY** <br/> |
   

