---
title: PageLineJumpDirX, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251656
ms.localizationpriority: medium
ms.assetid: 77892ec7-4c6a-78a5-5af4-5b6be7709e77
description: Détermine la direction des déviations de trait pour les connecteurs dynamiques horizontaux de la page de dessin n'ayant pas de direction de déviation locale.
ms.openlocfilehash: ba5a76702a9aa6cb8e999c52edd3978259475061
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554298"
---
# <a name="pagelinejumpdirx-cell-page-layout-section"></a>PageLineJumpDirX, cellule (section Page Layout)

Détermine la direction des déviations de trait pour les connecteurs dynamiques horizontaux de la page de dessin n'ayant pas de direction de déviation locale.
  
|**Valeur**|**Direction du saut de ligne**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Par défaut ; à gauche ou paramètres de la page pour les formes  <br/> |**visLOJumpDirXDefault** <br/> |
| 1  <br/> | Up  <br/> |**visLOJumpDirXUp** <br/> |
| 2  <br/> | Down  <br/> |**visLOJumpDirXDown** <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule PageLineJumpDirX par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | PageLineJumpDirX  <br/> |
   
Pour obtenir une référence à la cellule PageLineJumpDirX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
| Index de la cellule :  <br/> |**visPLOJumpDirX** <br/> |
   

