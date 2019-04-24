---
title: PageLineJumpDirY, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm770
localization_priority: Normal
ms.assetid: f73cc157-b332-279b-f7cf-d5a090bc09a4
description: Détermine la direction des déviations de trait pour les connecteurs dynamiques verticaux de la page de dessin n'ayant pas de direction de déviation locale.
ms.openlocfilehash: 21ad1d95fd83780f31778dbc8bb70f9bdb4b922d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329896"
---
# <a name="pagelinejumpdiry-cell-page-layout-section"></a>PageLineJumpDirY Cell (Page Layout Section)

Détermine la direction des déviations de trait pour les connecteurs dynamiques verticaux de la page de dessin n'ayant pas de direction de déviation locale.
  
|**Valeur**|**Direction de la déviation de trait**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Par défaut ; vers le haut ou paramètres de la page pour les formes  <br/> |**visLOJumpDirYDefault** <br/> |
| 0,1  <br/> | À gauche  <br/> |**visLOJumpDirYLeft** <br/> |
| n°2  <br/> | À droite  <br/> |**visLOJumpDirYRight** <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule PageLineJumpDirY par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | PageLineJumpDirY  <br/> |
   
Pour obtenir une référence à la cellule PageLineJumpDirY à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
| Index de la cellule :  <br/> |**visPLOJumpDirY** <br/> |
   

