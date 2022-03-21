---
title: ConLineJumpDirY, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251654
ms.localizationpriority: medium
ms.assetid: 93f82ae0-3442-fac1-9906-b84afef85f5c
description: Détermine la direction de la déviation de trait dans le cas d'un connecteur dynamique vertical d'une forme.
ms.openlocfilehash: c87661d8c7fa742af59814fd78fc85ea88625c11
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63632482"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a>ConLineJumpDirY, cellule (section Shape Layout)

Détermine la direction de la déviation de trait dans le cas d'un connecteur dynamique vertical d'une forme.
  
|**Valeur**|**Direction de la déviation**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Valeur par défaut de la page  <br/> |**visLOJumpDirYDefault** <br/> |
| 1  <br/> | À gauche  <br/> |**visLOJumpDirYLeft** <br/> |
| 2  <br/> | À droite  <br/> |**visLOJumpDirYRight** <br/> |
   
## <a name="remarks"></a>Remarques

Pour définir le sens vertical par défaut  de tous les sauts de connecteur sur une page, utilisez la cellule PageLineJumpDirY dans la section Mise en page. 
  
Pour obtenir une référence à la cellule ConLineJumpDirY par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | ConLineJumpDiry  <br/> |
   
Pour obtenir une référence à la cellule ConLineJumpDirY à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowShapeLayout** <br/> |
| **Index de la cellule :**  <br/> |**visSLOJumpDirY** <br/> |
   

