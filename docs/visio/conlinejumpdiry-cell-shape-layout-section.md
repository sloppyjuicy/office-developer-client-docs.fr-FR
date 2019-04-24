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
ms.openlocfilehash: f86c77da62042d1bc2c0274564efa9fdb0887971
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342741"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a>ConLineJumpDirY, cellule (section Shape Layout)

Détermine la direction de la déviation de trait dans le cas d'un connecteur dynamique vertical d'une forme.
  
|**Valeur**|**Direction de la déviation**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Valeur par défaut de la page  <br/> |**visLOJumpDirYDefault** <br/> |
| 0,1  <br/> | À gauche  <br/> |**visLOJumpDirYLeft** <br/> |
| n°2  <br/> | À droite  <br/> |**visLOJumpDirYRight** <br/> |
   
## <a name="remarks"></a>Remarques

Pour définir la direction verticale par défaut de *toutes les* déviations de connecteur d'une page, utilisez la cellule PageLineJumpDirY de la section Page Layout. 
  
Pour obtenir une référence à la cellule ConLineJumpDirY par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | ConLineJumpDirY  <br/> |
   
Pour obtenir une référence à la cellule ConLineJumpDirY à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
| Index de la cellule :  <br/> |**visSLOJumpDirY** <br/> |
   

