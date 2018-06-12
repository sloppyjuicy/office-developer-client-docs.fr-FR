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
ms.openlocfilehash: 640ad93fbccf2cec26bda535c288c881aea32207
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789218"
---
# <a name="pagelinejumpdiry-cell-page-layout-section"></a>PageLineJumpDirY, cellule (section Page Layout)

Détermine la direction des déviations de trait pour les connecteurs dynamiques verticaux de la page de dessin n'ayant pas de direction de déviation locale.
  
|**Valeur**|**Direction de déviation de trait**|**Constante d’Automation**|
|:-----|:-----|:-----|
| 0  <br/> | Par défaut ; vers le haut ou paramètres de la page pour les formes  <br/> |**visLOJumpDirYDefault** <br/> |
| 1  <br/> | Gauche  <br/> |**visLOJumpDirYLeft** <br/> |
| 2  <br/> | Droite  <br/> |**visLOJumpDirYRight** <br/> |
   
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule PageLineJumpDirY par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | PageLineJumpDirY  <br/> |
   
Pour obtenir une référence à la cellule PageLineJumpDirY par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
| Index de la cellule :  <br/> |**visPLOJumpDirY** <br/> |
   

