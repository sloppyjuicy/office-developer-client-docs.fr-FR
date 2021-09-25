---
title: PageLineJumpDirY, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm770
ms.localizationpriority: medium
ms.assetid: f73cc157-b332-279b-f7cf-d5a090bc09a4
description: Détermine la direction des déviations de trait pour les connecteurs dynamiques verticaux de la page de dessin n'ayant pas de direction de déviation locale.
ms.openlocfilehash: 5265acb3b8378bf5081d440aaba4608c85cf798b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554249"
---
# <a name="pagelinejumpdiry-cell-page-layout-section"></a>PageLineJumpDirY Cell (Page Layout Section)

Détermine la direction des déviations de trait pour les connecteurs dynamiques verticaux de la page de dessin n'ayant pas de direction de déviation locale.
  
|**Valeur**|**Direction du saut de ligne**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Par défaut ; vers le haut ou paramètres de la page pour les formes  <br/> |**visLOJumpDirYDefault** <br/> |
| 1  <br/> | À gauche  <br/> |**visLOJumpDirYLeft** <br/> |
| 2  <br/> | À droite  <br/> |**visLOJumpDirYRight** <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule PageLineJumpDirY par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | PageLineJumpDiry  <br/> |
   
Pour obtenir une référence à la cellule PageLineJumpDirY à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
| Index de la cellule :  <br/> |**visPLOJumpDirY** <br/> |
   

